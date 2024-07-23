---
title: "Textarea"
date: 2022-02-01 00:01:01Z
description: "Use the text area component when you need to let users enter an amount of text that’s longer than a single line."
---

## When to use this component
Use the text area component when you need to let users enter an amount of text that’s longer than a single line.

## When not to use this component
Users can find open-ended questions difficult to answer. It might be better to break up one complex question into a series of simple ones, for example where users can select from options using [radios](../radio).

### If you need to ask an open question
Do not use the text area component if you need to let users enter shorter answers no longer than a single line, such as a phone number or name. In this case, you should use the [text input](../text_input) component.

## How it works
The text area component should only exist in the [main section](../../getting-started/page-template/#sections). 

You must label text areas. Placeholder text is not a suitable substitute for a label, as it disappears when users click inside the text area.

Labels must be aligned above the text area they refer to. They should be short, direct and written in sentence case. Do not use colons at the end of labels.

You can use hint text whenever necessary for help that’s relevant to the majority of users.

### Single question page 
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="input1">Can you provide more detail?</label></h1>
        <textarea id="input1" class="govcy-text-area" rows="5"></textarea>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="input1">Can you provide more detail?</label></h1>
        <textarea id="input1" class="govcy-text-area" rows="5"></textarea>
    </div>
</form>
```
### More than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<label>` as the page heading. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input2">Can you provide more detail?</label>
        <textarea id="input2" class="govcy-text-area" rows="5"></textarea>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input2">Can you provide more detail?</label>
        <textarea id="input2" class="govcy-text-area" rows="5"></textarea>
    </div>
</form>
```
### Hint text
Use hint text for help that’s relevant to the majority of users, like how their information will be used, or where to find it.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input3">Can you provide more detail?</label>
        <span class="govcy-hint" id="govcy-hint3">Do not include personal or financial information like your National Insurance number or credit card details.</span>
        <textarea id="input3" class="govcy-text-area" rows="5" aria-describedby="govcy-hint3"></textarea>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input3">Can you provide more detail?</label>
        <span class="govcy-hint" id="govcy-hint3">Do not include personal or financial information like your National Insurance number or credit card details.</span>
        <textarea id="input3" class="govcy-text-area" rows="5" aria-describedby="govcy-hint3"></textarea>
    </div>
</form>
```
Remember to adjust the `aria-describedby` attribute to include the hint message's `id`.

### Use appropriately-sized textareas
Make the height of a textarea proportional to the amount of text you expect users to enter. You can set the height of a textarea by by specifying the `rows` attribute.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input4">Can you provide more detail?</label>
        <span class="govcy-hint" id="govcy-hint4">Do not include personal or financial information like your National Insurance number or credit card details.</span>
        <textarea id="input4" class="govcy-text-area" rows="10" aria-describedby="govcy-hint4"></textarea>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input4">Can you provide more detail?</label>
        <span class="govcy-hint" id="govcy-hint4">Do not include personal or financial information like your National Insurance number or credit card details.</span>
        <textarea id="input4" class="govcy-text-area" rows="10" aria-describedby="govcy-hint4"></textarea>
    </div>
</form>
```
### Do not disable copy and paste
Users often need to copy and paste information into a text input, so do not stop them from doing this.

### Avoid restricting the length of a user’s input
Using the `maxlength` attribute means there is no feedback to users that their text input is truncated. This is especially true where the text has been copied and pasted from elsewhere. This can cause users to accidentally provide incorrect or incomplete information.

A restrictive maximum length can stop users from formatting information in their usual way. For example, putting spaces in a postcode or commas in a large number.

Some assistive technologies do not tell users if an input has a `maxlength` set or if the user has passed the limit. Voice control software may insert additional spaces into the input.

If you must enforce a maximum length for technical reasons, inform the user of the limit in the hint, but allow them to provide more information. Only return an error if the value is longer than allowed after normalisation. For longer values, consider using the [character count component](../character_count) instead.

### Order of elements inside the component
Place the elements inside the component in the following order.
1. Label
2. Hint
3. Error message
4. Textarea

### Error messages
Make sure to follow the instructions for [error messages](../error_message) and [error summary](../error_summary) when validating user input. Error messages should be styled like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="input-err">What is your job description?</label></h1>
        <p id="job-description-input-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Enter a valid Job description
        </p>
        <textarea id="input-err" class="govcy-text-area govcy-text-area-error" aria-describedby="job-description-input-error" rows="5"></textarea>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="input-err">What is your job description?</label></h1>
        <p id="job-description-input-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Enter a valid Job description
        </p>
        <textarea id="input-err" class="govcy-text-area govcy-text-area-error" aria-describedby="job-description-input-error" rows="5"></textarea>
    </div>
</form>
```
Here is example with a text area used in a more than one question page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="input-err1">What is your job description?</label>
        <p id="job-description-input-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Enter a valid Job description
        </p>
        <textarea id="input-err1" class="govcy-text-area govcy-text-area-error" aria-describedby="job-description-input-error1" rows="5"></textarea>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="input-err1">What is your job description?</label>
        <p id="job-description-input-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Enter a valid Job description
        </p>
        <textarea id="input-err1" class="govcy-text-area govcy-text-area-error" aria-describedby="job-description-input-error1" rows="5"></textarea>
    </div>
</form>
```
Remember to adjust the `aria-describedby` attribute to include the error message's `id` and add  `<span class="govcy-visually-hidden-error">Error:</span>` in the error message.

## Accessibility
Make sure:
- if there is a relevant [input purpose (opens in new tab)](https://www.w3.org/TR/WCAG21/#input-purposes){rel="noreferrer noopener" target="_blank"}, you’ll need to use the `autocomplete` attribute to meet [WCAG 2.1 Level AA (opens in new tab)](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html){rel="noreferrer noopener" target="_blank"}
- you associate the `label` elements with the textarea they relate to, using the `for` attribute
- when using a hints, add `aria-describedby` on the `textarea` element, with the id of the hint element 
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `textarea` element, with the id of the error message 
- not to disable copy and paste
- not to restrict maximum length with the `maxlength` attribute exactly to the allowed limit of the textarea 