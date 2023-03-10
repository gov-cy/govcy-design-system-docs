---
title: "Breadcrumbs"
date: 2022-02-01 00:01:01Z
---
The breadcrumbs component helps users to understand where they are within a website’s structure and move between levels.

## When to use this component
Use the breadcrumbs component when you need to help users understand and move between the multiple levels of a website.

## When not to use this component
Never use the breadcrumbs component together with the [back link](../back_link). 

You should do research with your users to learn if breadcrumbs are helpful in your service. Do not use the breadcrumbs component on websites with a flat structure, or to show progress through a linear journey or transaction.

If you’re using other navigational elements on the page, such as a sidebar, consider whether your users need the additional support of breadcrumbs.

## How it works
Always place breadcrumbs at the top of a page, in the [Before Main](../../styles/page_templates) (`<section id="before-main">`) element. Placing them here means that the ‘Skip to main content’ link allows the user to skip all navigation links, including breadcrumbs.

If the user is logged in, breadcrumbs must be on the same line as the [User’s name and sign out](../user_name_and_sign_out) component. Use the `govcy-float-start` to achieve this as shown on the code example above.

The breadcrumb should start with your ‘home’ page and end with the parent section of the current page.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-container">
        <a href="#" class="govcy-back-link">Home</a>
        <span class="bi bi-chevron-right"></span>
        <a href="#" class="govcy-back-link">Overview</a>
        <span class="bi bi-chevron-right"></span>
        <span>Home</span>
   </div> 
</div>  

*Sample HTML Code*

```html
<div class="govcy-float-start">
	<a href="#" class="govcy-back-link">Home</a>
    <span class="bi bi-chevron-right"></span>
    <a href="#" class="govcy-back-link">Overview</a>
    <span class="bi bi-chevron-right"></span>
    <span>Home</span>
</div>    
```