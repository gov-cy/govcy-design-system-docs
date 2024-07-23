---
title: "Email"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
description: "Follow this pattern whenever you need to ask for an email address."
---
## When to use this pattern
Only ask for people’s email if you need that information to deliver a service and you cannot get the information from data we already have (for example from an API call with the Civil Registry and Migration Department). 

## How it works

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="email-in">What is your email address?</label></h1>
        <span id="email-hint" class="govcy-hint">We’ll only use this email address for this application</span>
        <input id="email-in" type="email" class="govcy-text-input" aria-describedby="email-hint" autocomplete="email" spellcheck="false">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="email-in">What is your email address?</label></h1>
        <span id="email-hint" class="govcy-hint">We’ll only use this email address for this application</span>
        <input id="email-in" type="email" class="govcy-text-input" aria-describedby="email-hint" autocomplete="email" spellcheck="false">
    </div>
</form>
```

When asking users for their email address, you must make it clear why you’re asking.

You may also need to check that users have access to the email account they give you.

Make sure the field can accommodate up to 256 characters, which is the longest an email address can be.

Help users to enter a valid email address by:
- checking they have entered the correct format. Use the [error messages](../../components/error_message) and [error summary](../../components/error_summary) components to display any validation messages
- allowing users to paste the email address
- setting the `type` attribute to `email` so that devices display the correct keyboard
- setting the `spellcheck` attribute to `false` so that browsers do not spellcheck the email address
- setting the `autocomplete` attribute to `email`. This lets browsers autofill the email address on a user’s behalf if they’ve entered it previously
- accommodate up to 254 characters, which is the longest an email address can be.

### Tell users why you want the email address
Make it clear what the email address will be used for so that:

- users feel confident that you’re not going to abuse it
- users with multiple email addresses can choose which one enter

If the email address field is part of a sign-in box, you do not need to say ‘Your email is required to sign you in’.

### When to ask for repeat or loop
Only ask users to repeat their email address if your user research shows it to be effective.

If email is an essential part of your service - for example to send a password reset - you can confirm whether the user has access to the email address they give you using an [email confirmation loop](../confirm_email_address/). 

However, this is disruptive and should be avoided as far as possible.

### Error messages
Make sure to follow the instructions for [error messages](../../components/error_message) and [error summary](../../components/error_summary) when validating user input and to use the [text input error variant style](../../components/text_input/#error-messages). 