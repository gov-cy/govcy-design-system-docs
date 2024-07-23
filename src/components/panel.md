---
"title" : "Panel"
date: 2022-02-01 00:01:01Z
searchKeys: "success panel"
description: "Use the panel component to display important information when a transaction has been completed."
---

The panel component is a visible container used on confirmation or results pages to highlight important content.

## When to use this component
Use the panel component to display important information when a transaction has been completed. 

In most cases, the panel component is used on [confirmation pages](../../patterns/confirmation-pages/), to tell the user they have successfully completed the transaction.

## When not to use this component
Never use the panel component to highlight important information within body content.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

You can use the HTML below to create a file component.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-completed-notification">
    <div class="govcy-alert-completed-notification-body govcy-bg-success">
        <h1>Your application has been sent</h1>
        <p>Your Reference Number</p>
        <p class="govcy-fw-bold">DSF2204111303108618</p>
    </div>   
</div>
</div>

*HTML code*
```html
<div class="govcy-alert-completed-notification">
    <div class="govcy-alert-completed-notification-body govcy-bg-success">
        <h1>Your application has been sent</h1>
        <p>Your Reference Number</p>
        <p class="govcy-fw-bold">DSF2204111303108618</p>
    </div>   
</div>
```
### Component text

Keep your panel text brief, as it’s only meant for a high-level explanation of what has happened. For example, ‘Application complete’.

Aim to use short words and phrases to make sure highlighted information is easy to read at different screen sizes. For example, shorter amounts of information is less likely to wrap around the panel, which can happen when using the zoom function on mobiles.

If you need to give detailed information, or more context, use the description text under the heading text.