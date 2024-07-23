---
title: "Confirm an email address"
date: 2022-02-01 00:01:02Z
tags: "help_users"
description: "Check that a user has access to a specific email account using an email confirmation loop."
---
Check that a user has access to a specific email account using an email confirmation loop.

## When to use this pattern
Only use email confirmation loops if:

- critical functionality in the service is only available via email, for example, a password reset
- accidentally using the wrong email address would give someone else access to sensitive information about the user

Remember that confirmed emails do not prove a person’s identity, just that they have access to that email address at the time they confirmed.

## How it works
Email confirmation loops can be disruptive because they force users to switch from your service to their email account and back again.

Common problems with email confirmation include:

- confusing users about the journey outside the service
- assuming users have an email account and access to it
- sending emails to spam folders so users do not see them, for example, because it goes to their spam folder
- taking too long to send the confirmation email

You must design your service to reduce these issues for users.

If you use email confirmation loops you must consider:

- any expiry conditions you set on the email link
- letting users resend their email
- whether to use a blocking or non-blocking loop
- the design of the ‘activate your account’ page

Use the following flow to confirm the email address.

1. Ask the user to enter their email address.
2. Send confirmation code via email
3. Ask the user to enter the confirmation code.

### 1. Ask the user to enter their email.
Use the [email pattern](../email/) to ask the user for their mobile number:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="email-in">What is your email address?</label></h1>
        <span id="email-hint" class="govcy-hint">We’ll only use this email address for this application</span>
        <input id="email-in" type="email" class="govcy-text-input" aria-describedby="email-hint" autocomplete="email" spellcheck="false">
    </div>
    <button id="btnMobileSubmit" type="button" class="govcy-btn-primary">Continue</button>
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
    <button id="btnMobileSubmit" type="button" class="govcy-btn-primary">Continue</button>
</form>
```
### 2. Send confirmation code via SMS
Send an email with the a confirmation code. 

Make sure you write the name of the service on the subject. Apart from the confirmation page, mention when the code expires. For example:

```markdown
Ο κωδικός ασφαλείας σας είναι:

1234

Εισαγάγετε τον κωδικό αυτό στη σελίδα ‘Ελέγξετε το email σας’, για να επιβεβαιώσετε ότι έχετε πρόσβαση στο email σας. Ο κωδικός λήγει σε 15 λεπτά. 

Μην απαντήσετε σε αυτό το μήνυμα.

============

Your security code is:

1234

Enter the security code in the “Check your email” page, to confirm that you have been able to access your email. The code expires in 15 minutes. 

Do not reply to this email.
```

You can use our guide on [how to create an HTML email](../../guides/create_an_html_email/) to create emails that are consistent with the styles of gov.cy.

### 3. Ask the use to enter the confirmation code.
Use the [whole number numeric input pattern](../numeric_inputs/#whole-numbers) to ask the user for the confirmation code. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h1>Check your email</h1>
<p>
    We’ve emailed a security code to <strong>me@example.com</strong> so that we know that you can access your email.
</p>
<div class="govcy-form">
   <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="email-otp">Enter the security code</label>
            <input type="text" class="govcy-text-input govcy-text-input-char_4 " id="email-otp" name="email-otp" value="" maxlength="4" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
    </div>
    <button class="govcy-btn-primary">Continue</button>
</div>
<p>If you have not received the security code after a few minutes: </p>
<ul>
    <li>check the email address above is correct</li>
    <li>look in the folder where your unwanted, ‘spam’ or ‘junk’ email goes </li>
</ul>
<p>You can <a href="#">enter the email address again or try a different email address</a>.</p>
</div>

*HTML code*
```html
<h1>Check your email</h1>
<p>
    We’ve emailed a security code to <strong>me@example.com</strong> so that we know that you can access your email.
</p>
<form class="govcy-form" action="" novalidate>
   <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="email-otp">Enter the security code</label>
            <input type="text" class="govcy-text-input govcy-text-input-char_4 " id="email-otp" name="email-otp" value="" maxlength="4" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
    </div>
    <button class="govcy-btn-primary">Continue</button>
</form>
<p>If you have not received the security code after a few minutes: </p>
<ul>
    <li>check the email address above is correct</li>
    <li>look in the folder where your unwanted, ‘spam’ or ‘junk’ email goes </li>
</ul>
<p>You can <a href="#">enter the email address again or try a different email address</a>.</p>
```

### Expiry conditions and policy
You must set an expiry date on the email you send so that the link cannot be used after a certain period of time.  
You should also set the link to expire when:

- it’s been used once
- it’s superseded by a new link
- the user has changed the email address on their account

If a user attempts to use an expired link or a link that’s already been used then you should explain that it’s expired, and why.

In order to prevent abuse:

- allow the users to send a confirmation emails at most 5 times per session
- allow the users to have 3 attempts for each confirmation code that is sent.

### Let users resend the email
You should let users resend the email confirmation link in case they entered the wrong email address previously or the email did not arrive.

### Blocking or non-blocking loops
There are 2 versions of the email confirmation loop: blocking and non-blocking.

In a blocking loop, the user cannot use the service until they have confirmed their email address.

In the non-blocking version, they can continue to use the service, but will be reminded regularly that they need to confirm their email. Some functionality may not be available until they’ve done this.

Blocking loops have a simpler flow, but if a user cannot complete the loop then they’re unable to use the service at all. It’s important that you send the emails instantly if you use blocking loops.

Non-blocking loops need more careful design because you cannot guarantee that all users will confirm their email. This could stop people from accessing your service.

You can also use a combination of both, by starting users on a non-blocking loop initially and then change to a blocking loop.