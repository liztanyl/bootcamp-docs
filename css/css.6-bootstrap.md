# CSS.6: Bootstrap

## Introduction

[Bootstrap](https://getbootstrap.com) is an open-source CSS library created at Twitter and [open-sourced in 2011](https://en.wikipedia.org/wiki/Bootstrap\_\(front-end\_framework\)). It provides a set of styles for a 12-column grid, and CSS and JS for common UI elements, such as carousels and alert boxes.

## Why use Bootstrap

There are three parts to Bootstrap:

1. CSS and DOM manipulation library "components" that creates things like [carousels](https://getbootstrap.com/docs/5.0/components/carousel/) and [modals](https://getbootstrap.com/docs/5.0/components/modal/). You must use the bootstrap Javascript for these features.
2. A common UI look and feel with things like [navbars](https://getbootstrap.com/docs/5.0/components/navbar/), [tabs](https://getbootstrap.com/docs/5.0/components/navs-tabs/) and [alerts](https://getbootstrap.com/docs/5.0/components/alerts/). These come with their own color schemes and things like rounded corners and button hover animations.
3. This section mostly covers the most complex CSS part of Bootstrap- the [Responsive Grid](https://getbootstrap.com/docs/5.0/layout/grid/).

{% hint style="danger" %}
When using Bootstrap, **do not** name custom CSS classes the same as Bootstrap CSS classes to prevent conflicts.

Do not add any box model or layout styles to an element that already has a Bootstrap layout class on it, such as margin.
{% endhint %}

## Responsive Grid

Bootstrap CSS allows a developer to write HTML classes and create mobile-first responsive layouts easily.

{% embed url="https://www.youtube.com/watch?v=qmPmwdshCMw" %}

## Equal 2-column Layout

[https://getbootstrap.com/docs/5.0/layout/grid/#equal-width](https://getbootstrap.com/docs/5.0/layout/grid/#equal-width)

{% embed url="https://codepen.io/awongh-sandwich/pen/poPWJOg" %}

## Responsive Columns

{% hint style="warning" %}
Resize the window to see the columns resize themselves!
{% endhint %}

[https://getbootstrap.com/docs/5.0/layout/grid/#all-breakpoints](https://getbootstrap.com/docs/5.0/layout/grid/#all-breakpoints)

{% embed url="https://codepen.io/awongh-sandwich/pen/KKmXpYz" %}

## Bootstrap Starter Code

From here: [https://getbootstrap.com/docs/5.0/getting-started/introduction/#starter-template](https://getbootstrap.com/docs/5.0/getting-started/introduction/#starter-template)

```markup
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- Optional JavaScript; -->
    <!-- Will need JS is using any components: https://getbootstrap.com/docs/5.0/components -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>
  </body>
</html>
```

## Responsive Breakpoint Cheatsheet

Bootstrap grid has built-in mobile first responsive media query breakpoints. When setting media queries to match up with the bootstrap breakpoints here are the pixel widths:

|                       |                          |                     |                     |                     |                      |                       |
| --------------------- | ------------------------ | ------------------- | ------------------- | ------------------- | -------------------- | --------------------- |
| size                  | <p>xs<br>&#x3C;576px</p> | <p>sm<br>≥576px</p> | <p>md<br>≥768px</p> | <p>lg<br>≥992px</p> | <p>xl<br>≥1200px</p> | <p>xxl<br>≥1400px</p> |
| Container `max-width` | None (auto)              | 540px               | 720px               | 960px               | 1140px               | 1320px                |
| Class prefix          | `.col-`                  | `.col-sm-`          | `.col-md-`          | `.col-lg-`          | `.col-xl-`           | `.col-xxl-`           |

[https://getbootstrap.com/docs/5.0/layout/grid/#grid-options](https://getbootstrap.com/docs/5.0/layout/grid/#grid-options)

## Exercise

[Codepen fork the responsive column Codepen from above](https://codepen.io/awongh-sandwich/pen/KKmXpYz) and change the grid measurements of the columns to see them change width, e.g, `col-6` to `col-2`.

Inspect the CSS of the columns to see how the column widths are being set.

## Further Reading For Bootstrap Day 1:

{% embed url="https://getbootstrap.com/docs/5.0/getting-started/introduction" %}

## Bootstrap Day 2

### Required Reading

{% embed url="https://getbootstrap.com/docs/5.0/layout/breakpoints" %}

{% embed url="https://getbootstrap.com/docs/5.0/layout/containers" %}

{% embed url="https://getbootstrap.com/docs/5.0/forms/overview" %}
Read all the sub-categories in Forms
{% endembed %}

{% embed url="https://getbootstrap.com/docs/5.0/components/card" %}

{% embed url="https://getbootstrap.com/docs/5.0/components/dropdowns" %}

{% embed url="https://getbootstrap.com/docs/5.0/components/navbar" %}

{% embed url="https://getbootstrap.com/docs/5.0/utilities/flex" %}

{% embed url="https://getbootstrap.com/docs/5.0/components/navs-tabs" %}

