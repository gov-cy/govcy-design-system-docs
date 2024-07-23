---
title: "Date picker"
date: 2022-02-01 00:01:01Z
description: "Use the date picker component when you’re asking users for a date that is in the near future or recent past"
---

The date picker component consists of an input box where users can type their date, accompanied with a calendar button giving users different ways to pick a date.

## When to use this component
Use the date picker component when you’re asking users for a date that is in the near future or recent past.

This component works best for picking dates that users will most likely have to look up, for example when scheduling something. Knowing the day of the week helps users choose a specific date.

## When not to use this component
Do not use the date picker component for dates that are not near future or recent past. Research has shown that the date picker is more helpful for dates within the current or adjacent months. 

The further the desired date is from today, the more difficult it is for users to use the date picker. Never use the date picker for birth dates. Use the [date input](../date_input) instead.

If users are likely to know the exact date of the event, it is best to use the [date input](../date_input). 

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). The component uses JavaScript. To use it with the gov.cy [developer assets](../../getting-started/developer-assets/), make sure to include the main JavaScript file in your page. 

You must also include the desired language pack which is located in the developer assets under `js/locales` as follows:

```html
<script src="/js/locales/govcy.datepicker.en.js"></script>
```

Adjust the `src` attribute accordingly, depending on the location of the language files. 

For Greek include the  `govcy.datepicker.el.js` file.
For English include the  `govcy.datepicker.en.js` file.

### Single question page
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="appointment1-date">Appointment Date</label></h1>
        <span id="appointment1-date-hint" class="govcy-hint">For example, 13/8/2007</span>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input" 
                id="appointment1-date"
                name="appointment1-date"
                aria-describedby="appointment1-date-hint"/>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="appointment1-date">Appointment Date</label></h1>
        <span id="appointment1-date-hint" class="govcy-hint">For example, 13/8/2007</span>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input" 
                id="appointment1-date"
                name="appointment1-date"
                aria-describedby="appointment1-date-hint"/>
        </div>
    </div>
</form>
```
### More than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<label>` as the page heading. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form" >
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="appointment2-date">Appointment Date</label>
        <span id="appointment2-date-hint" class="govcy-hint">For example, 13/8/2007</span>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input" 
                id="appointment2-date"
                name="appointment2-date"
                aria-describedby="appointment2-date-hint"/>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="appointment2-date">Appointment Date</label>
        <span id="appointment2-date-hint" class="govcy-hint">For example, 13/8/2007</span>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input" 
                id="appointment2-date"
                name="appointment2-date"
                aria-describedby="appointment2-date-hint"/>
        </div>
    </div>
</form>
```

### Order of elements inside the component
Place the elements inside the component in the following order.
1. Label
2. Hint
3. Error message
4. Input

### Error messages
Make sure to follow the instructions for [error messages](../error_message) and [error summary](../error_summary) when validating user input.

When validating the date, allow both single-digit and double-digit values for day and month (for example `01` or `1`).

Error messages should be styled like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="appointment-err-date">Appointment Date</label></h1>
        <span id="appointment-err-date-hint" class="govcy-hint">For example, 13/8/2007</span>
        <p id="appointment-err-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Appointment Date must include a year
        </p>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input govcy-text-input-error" 
                id="appointment-err-date"
                name="appointment-err-date"
                aria-describedby="appointment-err-date-hint appointment-err-error"/>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="appointment-err-date">Appointment Date</label></h1>
        <span id="appointment-err-date-hint" class="govcy-hint">For example, 13/8/2007</span>
        <p id="appointment-err-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Appointment Date must include a year
        </p>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input govcy-text-input-error" 
                id="appointment-err-date"
                name="appointment-err-date"
                aria-describedby="appointment-err-date-hint appointment-err-error"/>
        </div>
    </div>
</form>
```
Here is example with the component used in a more than one question page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="appointment-err-date1">Appointment Date</label>
        <span id="appointment-err-date-hint1" class="govcy-hint">For example, 13/8/2007</span>
        <p id="appointment-err-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Appointment Date must include a year
        </p>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input govcy-text-input-error" 
                id="appointment-err-date1"
                name="appointment-err-date1"
                aria-describedby="appointment-err-date-hint1 appointment-err-error1"/>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="appointment-err-date1">Appointment Date</label>
        <span id="appointment-err-date-hint1" class="govcy-hint">For example, 13/8/2007</span>
        <p id="appointment-err-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Appointment Date must include a year
        </p>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input govcy-text-input-error" 
                id="appointment-err-date1"
                name="appointment-err-date1"
                aria-describedby="appointment-err-date-hint1 appointment-err-error1"/>
        </div>
    </div>
</form>
```
### Component text
Use the following text:

| Text | English | Greek |
| ---- | ---- | ---- |
| **Hint text** | For example, 13/8/2007 | Για παράδειγμα, 13/8/2007 |

{.govcy-table}

## Accessibility
Using the component with screen reader technology might prove difficult, so always allow users to enter the date using the text box directly.

Make sure:
- you associate the `label` elements with the input they relate to, using the `for` attribute
- you display a hint with an example date and add `aria-describedby` on the `input` element, with the id of the hint element
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `text` element, with the id of the error message 
- not to disable copy and paste

## Contribute
If you have used or researched this pattern, please let us know what you found so we can make it better for everyone. Send us an email at [dsf@dits.dmrid.gov.cy](mailto:dsf@dits.dmrid.gov.cy) to get in touch.

We are particularly interested in:
- research on screen readers