---
title: "Confirmation pages"
date: 2022-02-01 00:01:02Z
tags: "pages"
description: "Use this page to let users know they’ve completed a transaction."
---
Use this page to let users know they’ve completed a transaction.

## When to use this pattern
You should use a confirmation page at the end of a transaction.

## How it works
Confirmation pages reassure users that they have completed a transaction and helps them understand what to expect next.

Your confirmation page must include:

- a reference number, if there is one
- details of what happens next and when
- contact details for the service
- links to information or services that users are likely to need next
- a link to a feedback page
- a way for users to save a record of the transaction, for example, as a PDF

Note that the code example below shows only the `Main` section. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<!--main-->
 <div class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <div class="govcy-alert-completed-notification">
                <div class="govcy-alert-completed-notification-body govcy-bg-success">
                    <h1>Application Complete</h1>
                    <p>Your Reference Number</p>
                    <p class="fw-bold">DSF2204111303108618</p>
                </div>   
            </div>
            <p>We have sent you a confirmation email</p>
            <p><a href="#">Help us improve this service</a></p>
            <h2>What happens next</h2>
            <p>We’ve sent your application to Registers office.</p>
            <p>They will contact you either to confirm your registration, or to ask for more information.</p>
        </article>
    </div>
</div>
</div>

*HTML code*
```html
 <!--main-->
 <main class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <div class="govcy-alert-completed-notification">
                <div class="govcy-alert-completed-notification-body govcy-bg-success">
                    <h1>Application Complete</h1>
                    <p>Your Reference Number</p>
                    <p class="fw-bold">DSF2204111303108618</p>
                </div>   
            </div>
            <p>We have sent you a confirmation email</p>
            <p><a href="#">Help us improve this service</a></p>
            <h2>What happens next</h2>
            <p>We’ve sent your application to Registers office.</p>
            <p>They will contact you either to confirm your registration, or to ask for more information.</p>
        </article>
    </div>
</main>
```

### Help users who bookmark the page
Some users will bookmark the confirmation page as a form of receipt. You should allow them to return to the page, whenever possible.

If you cannot, make sure your service responds in a helpful way when users return using a bookmarked link. For example, if people use your service to make an application you could provide links to information on:

- tracking an application
- starting a new application
- what to do or who to contact if they have a problem with their application
