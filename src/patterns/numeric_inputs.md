---
title: "Numeric inputs"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
description: "Follow this pattern whenever you need to ask for numeric inputs."
---
Help users provide numeric inputs. 

## When to use this pattern
Follow this pattern whenever you need to ask for numeric inputs.

## How it works
The pattern uses the [text input component](../../components/text_input/). 

Do not limit or validate the users' input as they type. Run validations as described in the [error message component](../../components/error_message/). 

### Whole numbers
If you only allow whole numbers, use the `inputmode` and `pattern` attributes. 

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Do not use <code>&lt;input type="number"&gt;</code> as there is a risk of users accidentally incrementing a number when they’re trying to do something else - for example, scroll up or down the page. Make sure to set <code>spellcheck="false"</code>.
		</p>
    </div>
</div>

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in1">Credit Card number</label>
        <input id="in1" type="text" class="govcy-text-input govcy-text-input-char_20" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="in1">Credit Card number</label>
        <input id="in1" type="text" class="govcy-text-input govcy-text-input-char_20" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
    </div>
</form>
```

This will bring up the numeric keyboard on mobile devices and make it much easier for the users to enter their input. 

### Decimal numbers
If you allow decimal numbers, use `type=”text”`. Do not set the `inputmode` attribute to `decimal` as it causes some devices to bring up a keypad without a key for the decimal separator. Make sure to set `spellcheck="false"`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form"> 
    <div class="govcy-form-control"> 
        <label class="govcy-label govcy-label-primary" for="in2">Enter your income (€)</label>  
        <input type="text" spellcheck="false" class="govcy-text-input govcy-text-input-char_20" id="in2">  
    </div> 
</div> 
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate> 
    <div class="govcy-form-control"> 
        <label class="govcy-label govcy-label-primary" for="in2">Enter your income (€)</label>  
        <input type="text" spellcheck="false" class="govcy-text-input govcy-text-input-char_20" id="in2">  
    </div> 
</form> 
```

### Error messages
Make sure to follow the instructions for [error messages](../../components/error_message) and [error summary](../../components/error_summary) when validating user input and to use the [text input error variant style](../../components/text_input/#error-messages).