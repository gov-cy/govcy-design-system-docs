---
title: "Warning text"
date: 2022-02-01 00:01:01Z
description: "Use the warning text component when you need to warn users about something important."
---

## When to use this component
Use the warning text component when you need to warn users about something important, such as legal consequences of an action, or lack of action, that they might take

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-warning-text">
    <span class="govcy-warning-text-icon" aria-hidden="true">!</span>
    <span class="govcy-warning-text-message">
        <span class="govcy-visually-hidden">Warning:</span>
        You can be fined up to €500 if you do not register.</span>
</div>
</div>

*HTML code*
```html
<div class="govcy-warning-text">
    <span class="govcy-warning-text-icon" aria-hidden="true">!</span>
    <span class="govcy-warning-text-message">
        <span class="govcy-visually-hidden">Warning:</span>
        You can be fined up to €500 if you do not register.</span>
</div>
```
### Component text
Use the following text:
- **English**: "Warning"
- **Greek**: "Προσοχή"

## Accessibility
Make sure:
- to use `aria-hidden="true"` on the warning icon
- to use the `<span class="govcy-visually-hidden">Warning:</span>` on the warning text 