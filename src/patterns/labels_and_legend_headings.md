---
title: "Labels and legends"
date: 2022-02-01 00:01:02Z
tags: "how_to"
description: "How to use labels and legends for single and multiple questions on a page."
---

Depending if your page contains a single or multiple question, you will have to adjust your `<label>` or `<legend>` accordingly.

## Single question page 
 Whenever you design a form, you should start by splitting it across multiple pages with each page containing just one thing, for example:
- one piece of information you’re telling a user
- one decision they have to make
- one question they have to answer

This helps users focus and understand what’s being asked of them.

When you’re asking just one question on a page, you can make the question the page’s heading. Your page heading will then most likely be the same as the `<label>` or `<legend>` for the input.

For example, on a page that only asks users for their postcode, the question ‘What is your postcode’ would be both the page heading and the most logical `<label>` for your text input.

### Labels as page headings
To set the contents of a label as the page heading, put the `<label>` tag inside the `<h1>` tag.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
	    <h1><label class="govcy-label govcy-label-primary" for="input">Label</label></h1>
        <input id="input" type="text" class="govcy-text-input">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
	    <h1><label class="govcy-label govcy-label-primary" for="input">Label</label></h1>
        <input id="input" type="text" class="govcy-text-input">
    </div>
</form>
```
This is relevant to all components that include labels such as [character count](../../components/character_count/), all variants of [text input](../../components/text_input/), [textarea](../../components/textarea/), [select](../../components/select/), [date picker](../../components/date_picker/), and [file upload](../../components/file/).

### Legends as page headings
To set the contents of a legend as the page heading, you need to put the `<legend>` tag outside the `<h1>` tag.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Legend</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" checked="checked" name="radiosGroup" id="option1">
                <label class="govcy-label" for="option1">Option 1</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosGroup" id="option2">
                <label class="govcy-label" for="option2">Option 2</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosGroup" id="option3">
                <label class="govcy-label" for="option3">Option 3</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Legend</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" checked="checked" name="radiosGroup" id="option1">
                <label class="govcy-label" for="option1">Option 1</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosGroup" id="option2">
                <label class="govcy-label" for="option2">Option 2</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosGroup" id="option3">
                <label class="govcy-label" for="option3">Option 3</label>
            </div>
        </div>
    </fieldset>
</form>
```
This is relevant to all components that include legends such as [fieldset](../../components/fieldset/),  [radios](../../components/radio/), and [checkboxes](../../components/checkbox/).
## Multiple question
If your question contains more than one question make sure you have a valid header level 1 (`<h1>`) that is not associated with a `<label>` or `<legend>`. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h1>Check your phone</h1>
<div class="govcy-form">
   <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="Otp">Enter the security code</label>
            <input type="text" class="govcy-text-input govcy-text-input-char_4 " id="Otp" name="Otp" value="" autocomplete="one-time-code" maxlength="4" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-tel1">Last 4 digits of your mobile telephone number</label>
        <span class="govcy-hint" id="tel-hint1">We’ll only use this for validation</span>
        <input class="govcy-text-input govcy-text-input-char_20" id="in-tel1" name="in-tel1" type="tel" spellcheck="false" aria-describedby="tel-hint1" autocomplete="tel">
    </div>
    <button class="govcy-btn-primary">Continue</button>
</div>
</div>

*HTML code*
```html
<h1>Check your phone</h1>
<form class="govcy-form" action="" novalidate>
   <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="Otp">Enter the security code</label>
            <input type="text" class="govcy-text-input govcy-text-input-char_4 " id="Otp" name="Otp" value="" autocomplete="one-time-code" maxlength="4" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
    </div>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in-tel1">Last 4 digits of your mobile telephone number</label>
        <span class="govcy-hint" id="tel-hint1">We’ll only use this for validation</span>
        <input class="govcy-text-input govcy-text-input-char_20" id="in-tel1" name="in-tel1" type="tel" spellcheck="false" aria-describedby="tel-hint1" autocomplete="tel">
    </div>
    <button class="govcy-btn-primary">Continue</button>
</form>

```
### Labels in multiple question pages
To set the contents of a label in multiple question pages, make sure the  `<label>` tag is not inside an `<h1>` tag.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in1">Label</label>
        <input id="in1" type="text" class="govcy-text-input">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in1">Label</label>
        <input id="in1" type="text" class="govcy-text-input">
    </div>
</form>
```
This is relevant to all components that include labels such as [character count](../../components/character_count/), all variants of [text input](../../components/text_input/), [textarea](../../components/textarea/), [select](../../components/select/), [date picker](../../components/date_picker/), and [file upload](../../components/file/).

### Legends as page headings
To set the contents of a legend in multiple question pages, make sure the `<legend>` tag is not part of  an `<h1>` tag.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option1">
                <label class="govcy-label" for="check1-option1">Option 1</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option2">
                <label class="govcy-label" for="check1-option2">Option 2</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option3">
                <label class="govcy-label" for="check1-option3">Option 3</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option1">
                <label class="govcy-label" for="check1-option1">Option 1</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option2">
                <label class="govcy-label" for="check1-option2">Option 2</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option3">
                <label class="govcy-label" for="check1-option3">Option 3</label>
            </div>
        </div>
    </fieldset>
</form>
```
This is relevant to all components that include legends such as [fieldset](../../components/fieldset/),  [radios](../../components/radio/), and [checkboxes](../../components/checkbox/).