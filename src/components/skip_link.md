---
"title" : "Skip Link"
date: 2022-02-01 00:01:01Z
---
Some people use the `tab` key on their keyboard to navigate through the links and form elements on a web page. Use the skip link component to help keyboard-only users skip to the main content of a page.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
    <a href="#mainContainer" style="background-color: #ffdd00;color: #272525 !important;outline: none;border-bottom: 0 !important;display: block;overflow: hidden;padding: 5px; text-decoration: underline !important;">Skip to main content</a>
</div>

*Sample HTML Code*

```html
<a href="#mainContainer" class="govcy-skip-link">Skip to main content</a>
```
## When to use this component
All GOV.CY pages must include a skip link. 

## How it works
You should place the skip link immediately after the opening `<body>` tag. However, if you’re using a component that must be read before the user can skip to the main content (such as a cookie banner) , place the skip link immediately after the component.

The skip link component is visually hidden until a keyboard press activates it. The link should give the users the option to bypass the top-level navigation links and jump to the main content (`mainContainer`) of the page.

Use the link text "Skip to main content" for English and "Μετάβαση στο κύριο περιεχόμενο" for Greek.
