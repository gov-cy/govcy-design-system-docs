---
title: "Email"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
---
Follow this pattern whenever you need to ask for an email address.

## How it works

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in1">Email address</label>
        <span class="govcy-hint" id="email-hint">We’ll only use this for this application</span>
        <input class="govcy-text-input" id="in1" name="in1" type="email" spellcheck="false" aria-describedby="email-hint" autocomplete="email">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in1">Email address</label>
        <span class="govcy-hint" id="email-hint">We’ll only use this for this application</span>
        <input class="govcy-text-input" id="in1" name="in1" type="email" spellcheck="false" aria-describedby="email-hint" autocomplete="email">
    </div>
</form>
```

When asking users for their email address, you must make it clear why you’re asking.

You may also need to check that users have access to the email account they give you.

Make sure the field can accommodate up to 256 characters, which is the longest an email address can be.

Help users to enter a valid email address by:
- checking they have entered the correct format
- allowing users to paste the email address
- setting the `type` attribute to `email` so that devices display the correct keyboard
- setting the `spellcheck` attribute to `false` so that browsers do not spellcheck the email address
- setting the `autocomplete` attribute to `email`. This lets browsers autofill the email address on a user’s behalf if they’ve entered it previously.

### When to ask for repeat or loop 
Only ask users to repeat their email address if your user research shows it to be effective.

If email is an essential part of your service - for example to send a password reset - you can confirm whether the user has access to the email address they give you using an email confirmation loop. However, these are disruptive and should be avoided as far as possible.

### Show errors
Error messages should follow the guidance in [error message](../../components/error_message) as shown in the example below.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="in2">Email address</label>
        <p class="govcy-input-error-msg" id="error2"><span class="govcy-visually-hidden-error">Error: </span>Enter an email address in the correct format, like name@example.com</p>
        <input class="govcy-text-input govcy-text-input-error" id="in2" name="in2" type="email" spellcheck="false" aria-describedby="email-hint" autocomplete="email" aria-describedby="error2">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="in2">Email address</label>
        <p class="govcy-input-error-msg" id="error2"><span class="govcy-visually-hidden-error">Error: </span>Enter an email address in the correct format, like name@example.com</p>
        <input class="govcy-text-input govcy-text-input-error" id="in2" name="in2" type="email" spellcheck="false" aria-describedby="email-hint" autocomplete="email" aria-describedby="error2">
    </div>
</form>
```