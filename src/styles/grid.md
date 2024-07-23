---
title: "Grid system"
date: 2022-02-01 00:00:03Z
description: "Use the grid system to lay out the content on your service’s pages."
--- 

Use the grid system to lay out the content on your service’s pages. For more information on how to lay out content in the `main` section, see the [layout page](../layout).

## Breakpoints
A breakpoint is the screen size threshold determined by specific layout requirements.

Each screen size range determines the number of columns, and recommended gutters for each display size.

|Screen size|Body|Margin|Gutter|
|---|---|---|---|
|**XS** (0-576px)|Scaling|16px|8px|
|**S** (577-767px)|Scaling|32px|16px|
|**M** (768-991px)|720px|Scaling|24px|
|**L** (992-1199px)|960px|Scaling|24px|
|**XL** (1200-1439px)|1100px|Scaling|24px|
|**XXL** (1440+)|1200px|Scaling|24px|

{.govcy-table}

Using our [developers assets](../../getting-started/developer-assets) and the coded examples, the layout adjusts to suit the screen size and orientation for a given breakpoint range automatically.

The default maximum width is `1200px` and changes accordingly to the active breakpoint.

At `XS` device, margin has a baseline value of `16px`. The body remains responsive to increases in size. Upon reaching the next larger breakpoint, S device at `577px` wide, the margin increases to `32px`.

When the width of the body reaches `M` devices and above `768+`, the margin becomes flexible and the body region can maintain a maximum width stated while margins again scale horizontally.

## The grid system
The system uses 12 columns to lay out the content in the desktop viewport. The content in the columns is laid out vertically on viewports smaller than the defined responsive breakpoint.

The grid system uses a series of containers, rows, and columns to layout and align content.

## The grid system with gov.cy CSS
Using our [developers assets](../../getting-started/developer-assets) and the instructions below, the grid adjusts automatically.  

Use `container` classes to contain, pad, and sometimes center the content within them. While containers can be nested, most layouts do not require a nested container.

The design system comes with two different container classes:

- `.govcy-container`, which sets to max-width at each responsive breakpoint
- `.govcy-container-fluid`, which is width: 100% at all breakpoints

Use `govcy-row` class to distinguish rows.

Use `govcy-col-*` classes to distinguish columns. Replace the asterisk (\*) on the naming classes convention with a number from 1 to 12 to define how many column widths the element should have.

*Example*
<div class="govcy-container govcy-p-4 govcy-bg-info govcy-mb-4">
    <div class="row govcy-mb-2">
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-11 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-2 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-10 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-3 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-9 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-4 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-8 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-5 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-7 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-6 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-6 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-7 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-5 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-8 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-4 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-9 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-3 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-10 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-2 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-11 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-12 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-6 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-6 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-4 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-4 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-4 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-3 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-3 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-3 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-3 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-2 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-2 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-2 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-2 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-2 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-2 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
    <div class="row govcy-mb-2">
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
        <div class="govcy-col-1 govcy-bg-light govcy-br-primary govcy-br-1">col</div>
    </div>
</div>

*HTML code*
```html
<div class="govcy-container">
    <div class="govcy-row">
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-11">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-2">col</div>
        <div class="govcy-col-10">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-3">col</div>
        <div class="govcy-col-9">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-4">col</div>
        <div class="govcy-col-8">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-5">col</div>
        <div class="govcy-col-7">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-6">col</div>
        <div class="govcy-col-6">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-7">col</div>
        <div class="govcy-col-5">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-8">col</div>
        <div class="govcy-col-4">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-9">col</div>
        <div class="govcy-col-3">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-10">col</div>
        <div class="govcy-col-2">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-11">col</div>
        <div class="govcy-col-1">col</div>
    </div>
   
    <div class="govcy-row ">
        <div class="govcy-col-12">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-6">col</div>
        <div class="govcy-col-6">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-4">col</div>
        <div class="govcy-col-4">col</div>
        <div class="govcy-col-4">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-3">col</div>
        <div class="govcy-col-3">col</div>
        <div class="govcy-col-3">col</div>
        <div class="govcy-col-3">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-2">col</div>
        <div class="govcy-col-2">col</div>
        <div class="govcy-col-2">col</div>
        <div class="govcy-col-2">col</div>
        <div class="govcy-col-2">col</div>
        <div class="govcy-col-2">col</div>
    </div>
    <div class="govcy-row ">
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
        <div class="govcy-col-1">col</div>
    </div>
 </div>
```

