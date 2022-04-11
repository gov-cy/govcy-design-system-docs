---
title: "User’s name and sign out"
date: 2022-02-01 00:01:01Z
---
Use this component to help the user’s identify which account they are signed in withand provide them with a link to sign out of their account.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-container">
    <div class="govcy-text-end"> User’s Name | 
        <a href="#" class="govcy-sign-out">Sign Out</a>
    </div>
</div>  
</div>  

*Sample HTML Code*

```html
<div class="govcy-text-end"> User’s Name | 
    <a href="#" class="govcy-sign-out">Sign Out</a>
</div>     
```

The `User’s name` in this component should contain the name (not the username) of the signed in CY Login profile account.

## When to use this component
Always include this component when the user is signed in with an CY Login account.

## When not to use this component
Never use the component when the user is not signed in. 

## How it works

Always place the user’s name and sign out component at the top of a page, in the [Before Main](../../styles/page_templates) (`<section id="before-main">`) element. The component should be the second component to appear after the header (the [back link](../back_link) is first) and should be aligned to the left of the page as shown in the example below. You can use the `govcy-text-end` class to align the component on the left.

Make sure to implement the sign out mechanism according to CY Login’s standards when the user clicks the `sign out` link.