---
title: "Labels and legends headings"
date: 2022-02-01 00:01:02Z
tags: "how_to"
---
Whenever you design a form, you should start by splitting it across multiple pages with each page containing just one thing, for example:
- one piece of information you’re telling a user
- one decision they have to make
- one question they have to answer

This helps users focus and understand what’s being asked of them.

When you’re asking just one question on a page, you can make the question the page’s heading. Your page heading will then most likely be the same as the `<label>` or `<legend>` for the input.

For example, on a page that only asks users for their postcode, the question ‘What is your postcode’ would be both the page heading and the most logical `<label>` for your text input.

## Labels as page headings
To set the contents of a label as the page heading, you need to put the `<label>` tag inside the `<h1>` tag.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <h1><label class="govcy-label" for="in1">Label</label></h1>
        <span class="govcy-hint">Hint</span>
        <input type="text" class="govcy-text-input" id="in1">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <h1><label class="govcy-label" for="in1">Label</label></h1>
        <span class="govcy-hint">Hint</span>
        <input type="text" class="govcy-text-input" id="in1">
    </div>
</form>
```

## Legends as page headings

To set the contents of a legend as the page heading, you need to put the `<legend>` tag outside the `<h1>` tag.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Do you agree?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Yes
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">No
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Do you agree?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Yes
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">No
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
```