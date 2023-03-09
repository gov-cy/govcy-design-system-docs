---
"title" : "Text Input"
date: 2022-02-01 00:01:01Z
---
## When to use this component
Use the text input component when you need to let users enter text that’s no longer than a single line, such as their name or phone number.

## When not to use this component
Do not use the text input component if you need to let users enter longer answers that might span multiple lines. In this case, you should use a [textarea](../text_input/#textarea) instead.

## How it works

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in1">Label</label>
        <span class="govcy-hint">Hint</span>
        <input type="text" class="govcy-text-input" id="in1">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in1">Label</label>
        <span class="govcy-hint">Hint</span>
        <input type="text" class="govcy-text-input" id="in1">
    </div>
</form>
```
**Important**: All text inputs must have visible labels; placeholder text is not an acceptable replacement for a label as it vanishes when users start typing.
Labels should be aligned above the text input they refer to. They should be short, direct and written in sentence case. Do not use colons at the end of labels.

If you are asking just [one question per page](../../patterns/question_pages/#start-by-asking-one-question-per-page) as recommended, you can set the contents of the `<label>` as the page heading. 

Read more about why and [how to set legends as headings](../../patterns/labels_and_legend_headings).

If you’re asking more than one question on the page, do not set the contents of the `<legent>` as the page heading. Read more about asking [multiple questions on question pages](../../patterns/question_pages/#asking-multiple-questions-on-a-page).

Use [hint text](../../patterns/hint_text) for help that’s relevant to the majority of users, like how their information will be used, or where to find it.

### Show errors 
Error messages should follow the guidance in [error message](../error_message) and have specific error messages for specific error states.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="in2">Label</label>
        <p class="govcy-input-error-msg" id="error1"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
        <input type="text" class="govcy-text-input govcy-text-input-error" id="in2" aria-describedby="error1">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="in2">Label</label>
        <p class="govcy-input-error-msg" id="error1"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
        <input type="text" class="govcy-text-input govcy-text-input-error" id="in2" aria-describedby="error1">
    </div>
</form>
```

### Use appropriately-sized text inputs

Help users understand what they should enter by making text inputs the right size for the content they’re intended for.

By default, the width of text inputs is fluid and will fit the full width of the container they are placed into.

If you want to make the input smaller, you can either use a fixed width input, or use the width override classes to create a smaller, fluid width input.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in3">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_20" placeholder="20 Characters" maxlength="20" id="in3">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in4">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_10" placeholder="10 Characters" maxlength="10" id="in4">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in5">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_5" placeholder="5 Chars" maxlength="5" id="in5">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in6">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_4" placeholder="4 Chars" maxlength="4" id="in6">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in7">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_3" placeholder="3" maxlength="3" id="in7">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in8">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_2" placeholder="2" maxlength="2" id="in8">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in3">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_20" placeholder="20 Characters" maxlength="20" id="in3">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in4">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_10" placeholder="10 Characters" maxlength="10" id="in4">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in5">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_5" placeholder="5 Chars" maxlength="5" id="in5">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in6">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_4" placeholder="4 Chars" maxlength="4" id="in6">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in7">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_3" placeholder="3" maxlength="3" id="in7">
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in8">Label</label>
        <input type="text" class="govcy-text-input govcy-text-input-char_2" placeholder="2" maxlength="2" id="in8">
    </div>
</form>
```

### Textarea

Use the textarea component when you need to let users enter an amount of text that’s longer than a single line. 

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in9">Can you provide more detail?</label>
        <span class="govcy-hint">Do not include personal or financial information, like credit card details.</span>
        <textarea class="govcy-text-area" rows="5" id="in9"></textarea>
        <span class="govcy-hint">You may enter up to 300 characters.</span>
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in9">Can you provide more detail?</label>
        <span class="govcy-hint">Do not include personal or financial information, like credit card details.</span>
        <textarea class="govcy-text-area" rows="5" id="in9"></textarea>
        <span class="govcy-hint">You may enter up to 300 characters.</span>
    </div>
</form>
```

### Do not disable copy and paste
Users will often need to copy and paste information into a text input or a textarea, so do not stop them from doing this.

### How and when to spellcheck a user’s input

If you are asking users for information which is not appropriate to spellcheck, like a reference number, name, email address or Social Insurance number, disable the spellcheck.

To do this set the `spellcheck` attribute to `false` as shown in this example.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in10">Social Insurance</label>
        <input type="text" class="govcy-text-input" spellcheck="false" id="in10">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in10">Social Insurance</label>
        <input type="text" class="govcy-text-input" spellcheck="false" id="in10">
    </div>
</form>
```

### Mobile and Finger-friendly numeric inputs 

For mobile and figner friendly numeric inputs, use the `inputmode` and `pattern` attributes. Do not use `<input type="number">` as there is a risk of users accidentally incrementing a number when they’re trying to do something else - for example, scroll up or down the page.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in11">Credit Card number</label>
        <input type="text" class="govcy-text-input" spellcheck="false" pattern="[0-9]*" inputmode="numeric" id="in11">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in11">Credit Card number</label>
        <input type="text" class="govcy-text-input" spellcheck="false" pattern="[0-9]*" inputmode="numeric" id="in11">
    </div>
</form>
```

An other example of using `inputmode` and `pattern` attributes can be found on the [date input](../date_input) component.

This suggestion is not applicable to the [telephone number](../../patterns/telephone) pattern.

### Turn off HTML5 validation
Do not use HTML5 validation because the visual style, placement and content of HTML5 error messages cannot be made consistent with the GOV.CY Design System

To turn off HTML5 validation, add `novalidate` to your form tags.

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
```

Do not add `required` to your input fields.

### Use the autocomplete attribute
Use the `autocomplete` attribute on text inputs to help users complete forms more quickly. This lets you specify an input’s purpose so browsers can autofill the information on a user’s behalf if they’ve entered it previously.

For example, to enable autofill on a postcode field, set the autocomplete attribute to `postal-code`. 

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in12">Postcode</label>
        <input type="text" class="govcy-text-input"spellcheck="false" autocomplete="postal-code" id="in12">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in12">Postcode</label>
        <input type="text" class="govcy-text-input"spellcheck="false" autocomplete="postal-code" id="in12">
    </div>
</form>
```