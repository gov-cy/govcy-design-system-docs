---
title: "Breadcrumbs"
date: 2022-02-01 00:01:01Z
description: "The breadcrumbs component helps users to understand where they are within a website’s structure and move between levels."
---
The breadcrumbs component helps users to understand where they are within a website’s structure and move between levels.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<nav>
    <ol class="govcy-breadcrumb">
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Home</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Passports, travel and living abroad</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Travel abroad</a></li>
    </ol>
</nav>
</div>

*HTML code*
```html
<nav>
    <ol class="govcy-breadcrumb">
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Home</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Passports, travel and living abroad</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Travel abroad</a></li>
    </ol>
</nav>
```

## When to use this component
Use the breadcrumbs component when you need to help users understand and move between the multiple levels of a website.

## When not to use this component
Breadcrumbs work best on websites with clear hierarchical structure. Avoid using breadcrumbs on services.  

Do not use the breadcrumbs component on websites with a flat structure, or to show progress through a linear journey or transaction.

If you’re using other navigational elements on the page, such as a sidebar, consider whether your users need the additional support of breadcrumbs.

Never use the [back link](../back_link) component together with breadcrumbs. If necessary, you should do research with your users to learn which they find more helpful in your service.

## How it works
Always place back links at the top of a page, in the [Before main](../../getting-started/page-template/#sections) section. Placing them here means that the ‘Skip to main content’ link allows the user to skip all navigation links, including the back link.

The breadcrumb should start with your ‘home’ page and end with the parent section of the current page.

## Collapsing breadcrumbs on mobile devices
If you have long breadcrumbs you can configure the component to only show the first and last items on mobile devices.

To do this, add a `govcy-breadcrumbs-collapse-on-mobile` class to the outer `<div>` element of the component HTML.

Scroll the section to a mobile viewport to view the collapse.  

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<nav>
    <ol class="govcy-breadcrumb govcy-breadcrumbs-collapse-on-mobile">
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Home</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Enviroment</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Rural</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Land management</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Economic growth in rural areas</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Documents</a></li>
    </ol>
</nav>
</div>

*HTML code*
```html
<nav>
    <ol class="govcy-breadcrumb govcy-breadcrumbs-collapse-on-mobile">
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Home</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Enviroment</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Rural</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Land management</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Economic growth in rural areas</a></li>
        <li class="govcy-breadcrumb-item"><a href="#" class="govcy-breadcrumb-link">Documents</a></li>
    </ol>
</nav>
```

## Accessibility
Make sure: 
- no other interactive elements are too close to the breadcrumbs. This is to make sure users can easily interact with the breadcrumbs 
- you use the `<nav>` element to allow assistive technology to present the breadcrumbs in context as a navigational element on the page
- you use ordered lists `<ol>` and list items `<li>` to allow assistive technology to enumerate the items in the breadcrumbs