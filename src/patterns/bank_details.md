---
title: "Bank details"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
description: "Follow this pattern whenever you need to ask for bank details."
---
Help users provide bank details.

## When to use this pattern
Follow this pattern if you need users to provide their bank details so you can use them for financial transactions.

Only ask for bank details securely within your service. For example, do not ask users to send their bank details by email.

Consider if you can re-use bank details from data we already have (for example from an API call with the Department of Social Insurance Services).   

## How it works

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Bank account details</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="bank-in">IBAN</label>
            <span id="bank-hint" class="govcy-hint">You can ask your bank or check your bank statement</span>
            <input id="bank-in" type="text" aria-describedby="bank-hint" class="govcy-text-input govcy-text-input-char_35">
        </div>
        <div class="govcy-form-control">
            <button type="submit" class="govcy-btn-primary">Continue</button>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Bank account details</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="bank-in">IBAN</label>
            <span id="bank-hint" class="govcy-hint">You can ask your bank or check your bank statement</span>
            <input id="bank-in" type="text" aria-describedby="bank-hint" class="govcy-text-input govcy-text-input-char_35">
        </div>
        <div class="govcy-form-control">
            <button type="submit" class="govcy-btn-primary">Continue</button>
        </div>
    </fieldset>
</form>
```

When asking users for their bank details, you must make it clear why you’re asking.

Include extra fields if your payment service provider needs additional information.

### Choose how to get paid
Not everyone has a bank account or wants to share their account details online.

Consider if you can let users choose to get paid by an alternative method.

Adapt this question depending on what payment options your users need and what your service can support.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>How do you want to be paid?</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosBankGroup" id="bank-option1">
                <label class="govcy-label" for="bank-option1">Cypriot bank</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosBankGroup" id="bank-option2">
                <label class="govcy-label" for="bank-option2">Non Cypriot bank</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosBankGroup" id="bank-option3">
                <label class="govcy-label" for="bank-option3">Cheque</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosBankGroup" id="bank-option4" aria-describedby="bank-option4-hint">
                <label class="govcy-label" for="bank-option4">None of the above</label>
                <span id="bank-option4-hint" class="govcy-hint">We'll contact you to arrange payment</span>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>How do you want to be paid?</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosBankGroup" id="bank-option1">
                <label class="govcy-label" for="bank-option1">Cypriot bank</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosBankGroup" id="bank-option2">
                <label class="govcy-label" for="bank-option2">Non Cypriot bank</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosBankGroup" id="bank-option3">
                <label class="govcy-label" for="bank-option3">Cheque</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="radiosBankGroup" id="bank-option4" aria-describedby="bank-option4-hint">
                <label class="govcy-label" for="bank-option4">None of the above</label>
                <span id="bank-option4-hint" class="govcy-hint">We'll contact you to arrange payment</span>
            </div>
        </div>
    </fieldset>
</form>
```
### International bank account details
If you expect your users will have a non-CY bank account, you’ll need to:
- use different fields to sort code and account number - usually BIC code (also known as ‘SWIFT code’)
- do research on other fields you may need to add for the countries your service supports
- only show the fields for the country your user selects

If you expect your users to have a non-CY bank account, give them an option to select this.

Only show the fields that relate to that country.

Most countries need the BIC, sometimes known as the SWIFT code.

### Error messages
Make sure to follow the instructions for [error messages](../../components/error_message) and [error summary](../../components/error_summary) when validating user input and to use the [text input error variant style](../../components/text_input/#error-messages).

