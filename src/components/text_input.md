---
"title" : "Text Input"
date: 2022-02-01 00:01:01Z
description: "Use the text input component when you need to let users enter text that’s no longer than a single line."
---
## When to use this component
Use the text input component when you need to let users enter text that’s no longer than a single line, such as their name or phone number.

## When not to use this component
Do not use the text input component if you need to let users enter longer answers that might span multiple lines. In this case, you should use a [text area](../../components/textarea/) instead.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

All text inputs must have visible labels and the text input.

Labels should be aligned above the text input they refer to. They should be short, direct and written in sentence case. Do not use colons at the end of labels.

### Do not use placeholder text
Do not use placeholder text in place of a label, or for hints or examples, as:

- it vanishes when the user starts typing, which can cause problems for users with memory conditions or when reviewing answers
- not all screen readers read it out
- its browser default styles often do not meet [minimum contrast requirements (opens in new tab)](https://www.w3.org/TR/WCAG22/#contrast-minimum){rel="noreferrer noopener" target="_blank"}

### Single question page
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="in2">Label</label></h1>
        <input id="in2" type="text" class="govcy-text-input">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="in2">Label</label></h1>
        <input id="in2" type="text" class="govcy-text-input">
    </div>
</form>
```
### More than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<label>` as the page heading. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-label-primary">
        <label class="govcy-label govcy-label-primary" for="in1">Label</label>
        <input id="in1" type="text" class="govcy-text-input">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-label-primary">
        <label class="govcy-label govcy-label-primary" for="in1">Label</label>
        <input id="in1" type="text" class="govcy-text-input">
    </div>
</form>
```
### Text input patterns 
The design system has patterns with text input variations for specific purposes. Use these patterns when asking users for:  

-  [Addresses](../../patterns/addresses/)
-  [Bank details](../../patterns/bank_details/) 
-  [Currency amounts](../../patterns/currency-amount/)
-  [Date input](../date_input/)
-  [Date picker](../date_picker)
-  [Email address](../../patterns/email/)
-  [Names](../../patterns/names/)
-  [Numeric inputs](../../patterns/numeric_inputs/)
-  [Social Insurance Numbers](../../patterns/social_insurance_number/)
-  [Telephone](../../patterns/telephone/)

### Hint text
Use hint text for help that’s relevant to the majority of users, like how their information will be used, or where to find it.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="in3">Label</label></h1>
        <span id="in3-hint" class="govcy-hint">Hint</span>
        <input id="in3" type="text" class="govcy-text-input" aria-describedby="in3-hint">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="in3">Label</label></h1>
        <span id="in3-hint" class="govcy-hint">Hint</span>
        <input id="in3" type="text" class="govcy-text-input" aria-describedby="in3-hint">
    </div>
</form>
```
Remember to adjust the `aria-describedby` attribute to include the hint message's `id`.

### Fixed width text inputs
Help users understand what they should enter by making text inputs the right size for the content they’re intended for.

By default, the width of text inputs is fluid and will fit the full width of the container they are placed into.

If you want to make the input smaller, you can either use a fixed width input, or use the width override classes to create a smaller, fluid width input.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-50">50 Characters</label>
        <input id="in-size-50" type="text" class="govcy-text-input govcy-text-input-char_50" maxlength="50">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-35">35 Characters</label>
        <input id="in-size-35" type="text" class="govcy-text-input govcy-text-input-char_35" maxlength="35">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-20">20 Characters</label>
        <input id="in-size-20" type="text" class="govcy-text-input govcy-text-input-char_20" maxlength="20">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-10">10 Characters</label>
        <input id="in-size-10" type="text" class="govcy-text-input govcy-text-input-char_10" maxlength="10">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-9">9 Characters</label>
        <input id="in-size-9" type="text" class="govcy-text-input govcy-text-input-char_9" maxlength="9">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-8">8 Characters</label>
        <input id="in-size-8" type="text" class="govcy-text-input govcy-text-input-char_8" maxlength="8">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-7">7 Characters</label>
        <input id="in-size-7" type="text" class="govcy-text-input govcy-text-input-char_7" maxlength="7">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-6">6 Characters</label>
        <input id="in-size-6" type="text" class="govcy-text-input govcy-text-input-char_6" maxlength="6">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-5">5 Characters</label>
        <input id="in-size-5" type="text" class="govcy-text-input govcy-text-input-char_5" maxlength="5">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-4">4 Characters</label>
        <input id="in-size-4" type="text" class="govcy-text-input govcy-text-input-char_4" maxlength="4">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-3">3 Characters</label>
        <input id="in-size-3" type="text" class="govcy-text-input govcy-text-input-char_3" maxlength="3">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-2">2 Characters</label>
        <input id="in-size-2" type="text" class="govcy-text-input govcy-text-input-char_2" maxlength="2">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-50">50 Characters</label>
        <input id="in-size-50" type="text" class="govcy-text-input govcy-text-input-char_50" maxlength="50">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-35">35 Characters</label>
        <input id="in-size-35" type="text" class="govcy-text-input govcy-text-input-char_35" maxlength="35">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-20">20 Characters</label>
        <input id="in-size-20" type="text" class="govcy-text-input govcy-text-input-char_20" maxlength="20">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-10">10 Characters</label>
        <input id="in-size-10" type="text" class="govcy-text-input govcy-text-input-char_10" maxlength="10">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-9">9 Characters</label>
        <input id="in-size-9" type="text" class="govcy-text-input govcy-text-input-char_9" maxlength="9">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-8">8 Characters</label>
        <input id="in-size-8" type="text" class="govcy-text-input govcy-text-input-char_8" maxlength="8">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-7">7 Characters</label>
        <input id="in-size-7" type="text" class="govcy-text-input govcy-text-input-char_7" maxlength="7">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-6">6 Characters</label>
        <input id="in-size-6" type="text" class="govcy-text-input govcy-text-input-char_6" maxlength="6">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-5">5 Characters</label>
        <input id="in-size-5" type="text" class="govcy-text-input govcy-text-input-char_5" maxlength="5">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-4">4 Characters</label>
        <input id="in-size-4" type="text" class="govcy-text-input govcy-text-input-char_4" maxlength="4">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-3">3 Characters</label>
        <input id="in-size-3" type="text" class="govcy-text-input govcy-text-input-char_3" maxlength="3">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-size-2">2 Characters</label>
        <input id="in-size-2" type="text" class="govcy-text-input govcy-text-input-char_2" maxlength="2">
    </div>
</form>
```

### Turn off HTML5 validation
Do not use HTML5 validation because the visual style, placement and content of HTML5 error messages cannot be made consistent with the gov.cy Unified Design System

To turn off HTML5 validation, add `novalidate` to your form tags.

```html
<form action="" class="govcy-form" novalidate>
```

Do not add `required` to your input fields.

### Use the autocomplete attribute
Use the `autocomplete` attribute on text inputs to help users complete forms more quickly. This lets you specify an input’s purpose so browsers can autofill the information on a user’s behalf if they’ve entered it previously.

For example, to enable autofill on a postcode field, set the `autocomplete` attribute to `postal-code`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in4">Postcode</label>
        <input type="text" class="govcy-text-input"spellcheck="false" autocomplete="postal-code" id="in4">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in4">Postcode</label>
        <input type="text" class="govcy-text-input"spellcheck="false" autocomplete="postal-code" id="in4">
    </div>
</form>
```

See more specific examples in the [text input patterns](#text-input-patterns).

### Do not disable copy and paste
Users often need to copy and paste information into a text input, so do not stop them from doing this. 

### Avoid restricting the length of a user’s input
Using the `maxlength` attribute means there is no feedback to users that their text input is truncated. This is especially true where the text has been copied and pasted from elsewhere. This can cause users to accidentally provide incorrect or incomplete information.

A restrictive maximum length can stop users from formatting information in their usual way. For example, putting spaces in a postcode or commas in a large number.

Some assistive technologies do not tell users if an input has a `maxlength` set or if the user has passed the limit. Voice control software may insert additional spaces into the input.

If you must enforce a maximum length for technical reasons, you may inform the user of the limit in the hint, but allow them to provide more information than the limit. Only return an error if the value is longer than allowed after normalisation. For longer values, consider using the [character count component](../character_count/) instead.

### Spellcheck a user’s input
Sometimes, browsers will spellcheck the information a user puts into a text input. If a user enters something which is recognised as a spelling error, sighted users will see a red line under the word.

If you are asking users for information which is not appropriate to spellcheck, like a reference number, name, email address or National Insurance number, disable the spellcheck.

To do this set the `spellcheck` attribute to `false`.

Browsers do not consistently spellcheck user’s input by default. If you are asking a question where spellcheck would be useful, set the `spellcheck` attribute to `true`.

### Order of elements inside the component
Place the elements inside the component in the following order.
1. Label
2. Hint
3. Error message
4. Input

### Error messages
Make sure to follow the instructions for [error messages](../error_message) and [error summary](../error_summary) when validating user input. Error messages should be styled like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="in-error">Label</label></h1>
        <span id="in-error-hint" class="govcy-hint">Hint</span>
        <p id="in-error-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input id="in-error" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in-error-hint in-error-error">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="in-error">Label</label></h1>
        <span id="in-error-hint" class="govcy-hint">Hint</span>
        <p id="in-error-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input id="in-error" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in-error-hint in-error-error">
    </div>
</form>
```

Here is example with a text input used in a more than one question page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="in-error1">Label</label>
        <p id="in-error-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input id="in-error1" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in-error-error1">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="in-error1">Label</label>
        <p id="in-error-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input id="in-error1" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in-error-error1">
    </div>
</form>
```
Remember to adjust the `aria-describedby` attribute to include the error message's `id` and add  `<span class="govcy-visually-hidden-error">Error:</span>` in the error message.
## Accessibility
Make sure:
- if there is a relevant [input purpose (opens in new tab)](https://www.w3.org/TR/WCAG21/#input-purposes){rel="noreferrer noopener" target="_blank"}, you’ll need to use the `autocomplete` attribute to meet [WCAG 2.1 Level AA (opens in new tab)](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html){rel="noreferrer noopener" target="_blank"}
- you associate the `label` elements with the input they relate to, using the `for` attribute
- when using a hints, add `aria-describedby` on the `input` element, with the id of the hint element 
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `input` element, with the id of the error message 
- not to disable copy and paste
- not to restrict maximum length with the `maxlength` attribute exactly to the allowed limit of the input 