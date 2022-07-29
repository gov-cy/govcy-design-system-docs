---
"title" : "Details"
date: 2022-02-01 00:01:01Z
---
Make it easier for the users to scan the page, by letting them reveal more detailed information only if they need it.

## When to use this component
Use the details component to make a page easier to scan when it contains information that only some users will need.

## When not to use this component
Do not use the details component to hide information that the majority of your users will need.

## How it works
The details component is a short link that shows more detailed help text when a user clicks on it. 

Make the link text short and descriptive so users can quickly work out if they need to click on it.

You can use the HTML below to create a select component.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<details class="govcy-details">
    <summary class="govcy-details__summary">
        <span class="govcy-details__summary-text">How to control cookies</span>
    </summary>
    <p class="govcy-details__text">
        You can delete all cookies that are already on your computer and you can set most browsers to prevent them from being placed. If you do this, however, you may have to manually adjust some preferences every time you visit a site and some services and functionalities may not work.
    </p>
</details>
</div>

*Sample HTML Code*

```html
<details class="govcy-details">
    <summary class="govcy-details__summary">
        <span class="govcy-details__summary-text">How to control cookies</span>
    </summary>
    <p class="govcy-details__text">
        You can delete all cookies that are already on your computer and you can set most browsers to prevent them from being placed. If you do this, however, you may have to manually adjust some preferences every time you visit a site and some services and functionalities may not work.
    </p>
</details>
```
