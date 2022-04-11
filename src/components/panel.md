---
"title" : "Panel"
date: 2022-02-01 00:01:01Z
searchKeys: "success panel"
---

The panel component is a visible container used on confirmation or results pages to highlight important content.

## When to use this component
Use the panel component to display important information when a transaction has been completed.

In most cases, the panel component is used on confirmation pages, to tell the user they have successfully completed the transaction.

## When not to use this component
Never use the panel component to highlight important information within body content.

## How it works

You can use the HTML below to create a file component.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
    <div class="row govcy-px-2">
        <div class="govcy-alert-completed-notification govcy-px-0">
            <div class="govcy-alert-completed-notification-body govcy-bg-success">
                <h1>Your application has been sent</h1>
                <p class="govcy-mb-0">Your Reference Number DSF2204111303108618</p>
            </div>   
        </div>
    </div>
</div>

*Sample HTML Code*

```html
<div class="row govcy-px-2">
    <div class="govcy-alert-completed-notification govcy-px-0">
        <div class="govcy-alert-completed-notification-body govcy-bg-success">
            <h1>Your application has been sent</h1>
            <p class="govcy-mb-0">Your Reference Number DSF2204111303108618</p>
        </div>   
    </div>
</div>
```