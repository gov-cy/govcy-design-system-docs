---
title: "Social Insurance Numbers"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
description: "Follow this pattern whenever you need to ask for social insurance numbers."
---
Help users provide social insurance numbers. 

## When to use this pattern
Follow this pattern whenever you need to ask for social insurance numbers.

Only ask for social insurance numbers securely within your service. For example, do not ask users to send their social insurance numbers by email.

Consider if you can re-use social insurance numbers from data we already have (for example from an API call with the Department of Social Insurance Services).  

## How it works
Use a single [whole number numeric input pattern](../numeric_inputs/#whole-numbers). 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="sin-in">What is your social insurance number?</label></h1>
        <input id="sin-in" type="text" class="govcy-text-input govcy-text-input-char_10" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="sin-in">What is your social insurance number?</label></h1>
        <input id="sin-in" type="text" class="govcy-text-input govcy-text-input-char_10" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
    </div>
</form>
```
When asking users for their social insurance number, you must make it clear why you’re asking.

Help users to enter a valid Social insurance number by:
- checking they have entered the correct format. The social insurance number can be only numbers. Use the [error messages](../../components/error_message) and [error summary](../../components/error_summary) components to display any validation messages
- allowing users to paste the email address
- setting the `type="text"`, ` pattern="[0-9]*"` and `inputmode="numeric"` so that devices display the correct keyboard
- setting the `spellcheck` attribute to `false` so that browsers do not spellcheck the email address
- use the 10 characters fix width text input variant.

### Pattern text
Write the label in full and never use abbreviations such as ‘SINO’ or ‘SI Number’.

Use the following text:
- In English: `Social insurance number`
- In Greek: `Αριθμός κοινωνικών ασφαλίσεων`

### Error messages
Make sure to follow the instructions for [error messages](../../components/error_message) and [error summary](../../components/error_summary) when validating user input and to use the [text input error variant style](../../components/text_input/#error-messages).

