---
title: "Inset text"
date: 2022-02-01 00:01:01Z
description: "Use the inset text component to differentiate a block of text from the content that surrounds it."
---

## When to use this component
Use the inset text component to differentiate a block of text from the content that surrounds it, for example:

- quotes
- examples
- additional information about the page

## When not to use this component
Some users do not notice inset text if it’s used on complex pages or near to other visually prominent elements. For this reason, avoid using inset text as a way of highlighting very important information that users need to see.

If you need to draw attention to very important content, like legal information, use the [warning text](../warning_text/) component instead.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

Use inset text very sparingly - it’s less effective if it’s overused.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<blockquote class="govcy-inset-text">
    <p>It can take up to 8 weeks to register a lasting power of attorney if there are no mistakes in the application.</p>
</blockquote>
</div>

*HTML code*
```html
<blockquote class="govcy-inset-text">
    <p>It can take up to 8 weeks to register a lasting power of attorney if there are no mistakes in the application.</p>
</blockquote>
```
