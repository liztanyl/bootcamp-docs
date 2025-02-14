# 7.7: Designing Component Hierarchy

## Introduction

One of the most difficult, confusing aspects of building a React app is deciding what components are responsible for what, and where the data gets stored. We'll look at some of the principles of React app design through examples.

Note that some React best practices are what is left out, i.e., state is not created unnecessarily, data is only controlled top-down, components functionally calculate values and states where possible, etc.

## E-Commerce App Example

1. Our example is a full-stack e-commerce app. The app begins empty.
2. When the user clicks a button, the app requests a list of all available items from the server.
3. When the user clicks on any item in the list a detail view appears.
4. When the user clicks the Add to Cart button, the cart is displayed with all the items. In the cart the total for all items is calculated.
5. See the full repo here: [https://github.com/rocketacademy/react-ecom-bootcamp](https://github.com/rocketacademy/react-ecom-bootcamp)

![](../../.gitbook/assets/shopping.jpg)

## "App-Level" \(or "Parent-Level"\) Data vs "Component-Level" Data

### App-Level Data

Because the data about what items are in the list is needed throughout the app, we put the items array at the "app level", in the `App` component. This is the same for all the other data we need throughout the app, such as which item is currently selected, and the array of items in the cart.

```javascript
const [items, setItems] = useState([]);
const [cart, setCart] = useState([]);
const [selectedItemIndex, setSelectedItem] = useState();
```

[https://github.com/rocketacademy/react-ecom-bootcamp/blob/main/src/App.jsx\#L9-L11](https://github.com/rocketacademy/react-ecom-bootcamp/blob/main/src/App.jsx#L9-L11)

### Component-Level Data

There are a few pieces of data that are not needed at the app level, such as the GST calculated on all the items in the cart and the quantity selected in the detail view.

```javascript
const subTotal = items.reduce(
  (acc, item) => Number(acc) + Number(item.price),
  0
);

const gst = subTotal * 0.07;

const total = subTotal + gst;
```

[https://github.com/rocketacademy/react-ecom-bootcamp/blob/main/src/components/Cart.jsx\#L7-L14](https://github.com/rocketacademy/react-ecom-bootcamp/blob/main/src/components/Cart.jsx#L7-L14)

## Data Flows

### Modifying Data in Parent Components via Prop Functions 

Similar to [Module 7.6: Passing Data Between Sibling Components](../7.6-passing-data-between-sibling-components.md), when a child component needs to manipulate data at the app level we pass a "prop function" down into the child component, which sends the parent necessary data via the prop function when the user performs an action.

For example, when the user clicks to add an item to cart, we send that item's index to `App` via a prop function to add that item to the `cart` array stored in app state. We format the data \(to add quantity\) in the prop function before modifying `cart`.

### Examples

The following examples demonstrate the same concepts as in [Module 7.6: Passing Data Between Sibling Components](../7.6-passing-data-between-sibling-components.md).

1. Adding an item to the cart from the `itemDetail`: [https://github.com/rocketacademy/react-ecom-bootcamp/blob/main/src/components/ItemDetail.jsx\#L14-L16](https://github.com/rocketacademy/react-ecom-bootcamp/blob/main/src/components/ItemDetail.jsx#L14-L16)
2. Adding the `item` into the `cart` array: [https://github.com/rocketacademy/react-ecom-bootcamp/blob/main/src/App.jsx\#L13-L15](https://github.com/rocketacademy/react-ecom-bootcamp/blob/main/src/App.jsx#L13-L15)
3. The setting of the `cart` array sets off the rendering of the `Cart` component and items in the cart. 

