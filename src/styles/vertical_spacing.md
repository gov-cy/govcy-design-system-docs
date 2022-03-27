---
title: "Vertical Spacing"
date: 2022-02-01 00:00:04Z
--- 

Use the design system to lay out the content on your service’s pages vertically in a uniform and consisted manner.

## Component margin
The system uses margin bottom attribute on each component to manage vertical spacing and distinguishes [typography](../typography) ( i.e. `<p>,<ul>,<ol> `), [headings ](../typography/#headings) (i.e. `<h1>,<h2>,<h3>,<h4>,<h5>,<h6>`) from the [rest of the components](../../components). 

The following margin bottom values must be applied:

| Component Type     | margin-bottom value |
| ------------------ | ------------------- |
| typography         | 16px                |
| headings             | 24px                |
| rest of components | 24px                |

{.govcy-table}

## Vertical spacing with GOVCY CSS

The grid system automatically adjusts vertical spacing when using the[ govcy css](../../getting_started/#css-and-javascript) for typography, headings and components that include the `govcy-form-control` class.

If you like to implement the same vertical spacing as decribed above, you can use the [margin utility classes](../../css_utilities/#margin%2C-padding) as follows

| Utility Class     | margin-bottom value |
| ------------------ | ------------------- |
| govcy-mb-3   | 16px                |
| govcy-mb-4   | 24px                |

{.govcy-table}