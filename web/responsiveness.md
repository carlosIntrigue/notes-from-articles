# Responsive Web Design Basics

oct-10-2019

## Intro

- number of mobile devices is increasing astronomically but the web isn't optimized for them.
- There is a wide vairety of resolutions across all smart devices.
- Responsive web design was originally defined by Ethan Marcotte
- The layout should change based on the capabilities of the device.

## Set the viewport

- Pages optimized for a variety of devices must include a meta view port tag in the head.
- The meta viewport tag controls the width and scaling of the browser.
- Use `width=device-width` to match the screen with device independent pixels. This scales text properly when zoomed in.
- `initial-scale=1` establishes a 1:1 relationship between css pixels and devie independent pixels. This resizes the page when device orientation changes.

## Size content to the viewport

- Since large fixed size elements do not render well on smaller screens avoid using fixed sizes
- Don't style as a function of the viewport
- Style for resolutions using css media queries

## Applying Media queries

- Media queries should be used to apply styles based on specific devices.
- There are three ways to add media queries.

```

<link rel="stylesheet" href="print.css" media="print">

@media print {
  /* print style sheets go here */
}

@import url(print.css) print; // Least preferred way
```

- Media queries are not mutually exclusive and they are applied with precedence rules in CSS.

## Apply media queries based on viewport size

- Media queries enable us to create a responsive experince based on device screen.

```
@media (query) {
  /* CSS Rules used when query matches */
}
```

- There are several different items we can query on.
- The ones used the most often are `min-qidth, max-width, min-height, max-height`

```

    @media (min-width: 500px) and (max-width: 600px) {
        h1 {
        color: fuchsia;
        }

        .desc:after {
        content:" In fact, it's between 500px and 600px wide.";
        }
    }


```

## How to choose breakpoints

- Choose them based on content not on device classes, let the content adjust to its container.
- Design for smallest first then scale up.
- keep lines of text about 70-80 characters

## View media query breakpoints in Chrome DevTools

- Devtoolscan be used to inspect different device sizes
