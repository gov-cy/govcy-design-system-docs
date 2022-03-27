---
title: "Layout"
date: 2022-02-01 00:00:05Z
---

Layouts section concerns content that resides inside the `<main>` element of the [page template](../page_templates). 

## Two-thirds layout
This layout uses one column and takes up the two thirds of the `<main>`. 

To be used when there is no need for a side menu and when components do not require the use of the full width of the page. 

For most types of page, we recommend using this layout as it stops lines of text getting so long that the page becomes difficult to read on desktop devices. This would usually mean no more than 60 characters per line.

*Example*

<div class="govcy-container">
    <div class="row">
        <article class="govcy-col-8" style="background-color:aqua;">Article <br><br> </article>
    </div>
</div>

*Sample HTML Code*

```html
<div class="govcy-container">
    <div class="row">
        <article class="govcy-col-8"></article>
    </div>
</div>
```

## Max-width layout
This layout uses one column and takes up the full size of the `<main>`. To be used when there is no need for a side menu and when components require the use of the full width of the page. 

*Example*

<div class="govcy-container">
    <div class="row">
        <article class="govcy-col-12" style="background-color:aqua;">Article <br><br> </article>
    </div>
</div>


*Sample HTML Code*

```html
<div class="govcy-container">
    <div class="row">                        
        <article class="govcy-col-12"></article>
    </div>
</div>
```

## One-third + Two-thirds layout
Use this page layout for services that need a side menu. 

The `<aside>` container must appear on the left of the `<article>` container on Desktop screens and last on mobile screens. It’s width must take ⅓ of the `service` section. 

The `<article>` container must appear on the right of the `<aside>` container on Desktop screens and first on mobile screens.It’s width must take ⅔ of the `service` section. 

*Example* 

<div class="govcy-container">
    <div class="row">
        <article class="govcy-col-8 govcy-order-last" style="background-color:aqua;">Article <br><br></article>
        <aside class="govcy-col-4 govcy-order-first" style="background-color:yellowgreen;">aside</aside>
    </div>
</div>


*Sample HTML Code*

```html
<div class="govcy-container">
    <div class="row">
        <article class="govcy-col-8 govcy-order-last"></article>
        <aside class="govcy-col-4 govcy-order-first"></aside>
    </div>
</div>
```

Take a look at this <a target='_blank' rel="noreferrer noopener" href='../../samples/layouts/'>demo page with layouts</a> as the would appear inside the `<main>` section.