# CSS.2.3: Box Model

![](../../.gitbook/assets/box-model.png)

The CSS Box model describes how much room a given element on the page takes up.

Refer back to these sections of the CSS exercises that talk about setting element dimensions:

[https://www.freecodecamp.org/learn/responsive-web-design/basic-css/adjust-the-padding-of-an-element](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/adjust-the-padding-of-an-element)\
[https://www.freecodecamp.org/learn/responsive-web-design/basic-css/adjust-the-margin-of-an-element](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/adjust-the-margin-of-an-element)\
[https://www.freecodecamp.org/learn/responsive-web-design/basic-css/add-a-negative-margin-to-an-element](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/add-a-negative-margin-to-an-element)\
[https://www.freecodecamp.org/learn/responsive-web-design/basic-css/add-different-padding-to-each-side-of-an-element](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/add-different-padding-to-each-side-of-an-element)\
[https://www.freecodecamp.org/learn/responsive-web-design/basic-css/add-different-margins-to-each-side-of-an-element](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/add-different-margins-to-each-side-of-an-element)\
[https://www.freecodecamp.org/learn/responsive-web-design/basic-css/use-clockwise-notation-to-specify-the-padding-of-an-element](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/use-clockwise-notation-to-specify-the-padding-of-an-element)\
[https://www.freecodecamp.org/learn/responsive-web-design/basic-css/use-clockwise-notation-to-specify-the-margin-of-an-element](https://www.freecodecamp.org/learn/responsive-web-design/basic-css/use-clockwise-notation-to-specify-the-margin-of-an-element)

Now we'll describe more features of the box model. We need to know more about how elements take up space on the page so that we can lay them out properly.

{% hint style="warning" %}
Generally speaking, box (element) sizing in CSS is affected by many different interplaying factors, depending on which styles are set. We will detail many of these styles and factors in the other sections.

The following page describes some common box properties, but in general a layout should avoid relying on multiple layout boxes being an exact pixel size, because multiple interacting boxes can be complicated to manage with CSS.

A good default is to allow, as much as is possible, for the CSS rendering engine to lay out the boxes in a "natural" way.
{% endhint %}

### Base Box Size

Without any CSS a box (element) will be the size of it's contents. If the box is `display` `block`, it's width will expand to the parent (containing) container, then it will expand downward.

### Width & Height

There are several common ways to set the dimensions of a box:

#### Pixel

For elements that are display block, you can manually set the size of an element:

```css
p {
  width: 100px;
  height: 100px;
}
```

#### Percent

We can set the width of a box using relative measurements:

```css
p {
  width: 50%;
  height: 100px;
}
```

#### Viewport

We can set the size of a box using viewport units.

```css
p {
  width: 100vw;
  height: 100vh;
}
```

See more on viewport units here: [https://css-tricks.com/fun-viewport-units/](https://css-tricks.com/fun-viewport-units/)

### LImitations of Width & Height

You cannot set width & height on inline elements.

You cannot set percentage height, unless the parent container has a fixed size.

Without [flexbox](../css.3-flexbox/), writing CSS that vertically centers boxes is difficult / not recommended.

### Seeing and Manipulating the Box

For every element that Chrome puts on the screen, we can see a helpful graphic that describes how much size the box takes up.

If you select an element in the elements tab and scroll to the bottom of the CSS pane you'll see the box model section.

![](../../.gitbook/assets/dev-t-b-model.png)

With this tool you can highlight each part of the box. The size of the box reported in the tool should match the CSS styles applied (although other factors besides directly set CSS values may affect the size of the box).

![](../../.gitbook/assets/dev-t-b-model-2.png)

Here you can see that the hovered section in the dev tools box model diagram is **highlighted in the same green** **color** on screen. Also note the size of the padding, 50px, matches the style applied in the pane above.

### Box Size Calculations

Note that the box model tools calculate the final size of the box in pixels. If we give a relative measurement in CSS like percent, the box diagram gives us the measurement in pixels.

![](../../.gitbook/assets/dev-t-b-model-3.png)

### Consistent Sizing

One flaw of the default behavior of the box model is that the size of a box doesn't include it's padding. Consider the following example:

```css
p {
  width: 200px;
  padding: 50px;
}
```

This CSS produces a box 300px wide (padding adds 50px to EACH side), not 200px wide.

#### Box Sizing

With the box-sizing style we can set the dimension to include padding. This code sets the correct size calculation for every single element in the document. We'll use this code for every HTML page we style.

```css
*,
*:before,
*:after {
  box-sizing: border-box;
}
```

See more about box sizing here: [https://css-tricks.com/box-sizing/](https://css-tricks.com/box-sizing/)

## Further Reading

Video on box sizing: [https://www.youtube.com/watch?v=dLGr1Qb2nKc](https://www.youtube.com/watch?v=dLGr1Qb2nKc)
