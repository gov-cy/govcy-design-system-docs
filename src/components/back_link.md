---
title: "Back Link"
date: 2022-02-01 00:01:01Z
---

Use the back link component to help users go back to the previous page in a multi-page transaction.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-container">
        <span class="bi bi-chevron-left"></span>
        <a href="#" class="govcy-back-link">Back</a>
        <br>
        <span class="bi bi-chevron-left"></span>
        <a href="#" class="govcy-back-link">Πίσω</a>
   </div> 
</div>  

*Sample HTML Code*

```html
<div class="govcy-float-start">
	<span class="bi bi-chevron-left"></span>
	<a class="govcy-back-link" href="/">Back</a>
</div>   
```

Although browsers have a back button, some sites break when you use it - so many users avoid it, instead of losing their progress in a service. Also, not all users are aware of the back button.

## When to use this component
Always include the back link component on [question pages](../../patterns/question_pages).

## When not to use this component
Never use the back link component together with [breadcrumbs](../breadcrumbs). If necessary, you should do research with your users to learn which they find more helpful in your service.

## How it works
Always place back links at the top of a page, in the [Before Main](../../styles/page_templates) (`<section id="before-main">`) element. Placing them here means that the ‘Skip to main content’ link allows the user to skip all navigation links, including the back link.

If the user is logged in, the back link must be on the same line as the [User’s name and sign out](../user_name_and_sign_out) component. Use the `govcy-float-start` to achieve this as shown on the code example above.

Make sure the link takes users to the previous page they were on, in the state they last saw it. Where possible, ensure it works even when JavaScript is not available.

If this is not possible, you should hide the back link when JavaScript is not available.
