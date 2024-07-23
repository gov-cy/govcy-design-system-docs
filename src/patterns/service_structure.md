---
title: "Structuring a service"
date: 2022-02-01 00:01:02Z
tags: "how_to"
description: "This pattern explains how to structure an online service. "
---
This pattern explains how to structure an online service. 

Before you start, review the design system’s [principles](../../getting-started/principles/) to design user-focused services. 

Through your design you will need to make sure:
- users will be able to complete the service from start to finish
- the amount of steps and information needed by the users is reduced to the minimum
- there are no dead ends
- complex internal structures of the government organization are hidden from the users
- decisions by the service, such as approval or rejection, are made clear to the users
- the service is consistent with other gov.cy services and works in a familiar way
- everyone can use and understand the service
- users and their information are treated with care and respect

Design services that focus on achieving users' goals and work independently and in isolation from other services. Do not design them as part of bulky systems that required extensive user training, and instead create clear, easy-to-use services, that allow users to complete specific tasks without needing to navigate through or depend on other services.

All gov.cy services must follow the [basic structure](#basic-structure). In this document we also describe variations of the basic structure, in which the "Gather information" step is handled differently depending on the need. 

## Basic structure
All gov.cy services must follow the basic structure.

### How it works

A service should:

1. Start with an informative start page
2. If needed, ask the users to sign-in
3. Gather information from the users
4. Let the users check their answers before submitting
5. Show the users a confirmation of successful completion page.

You may structure the “Gather information” step differently, in order to handle the complexity and specific needs of each service.

![An example flow of a standard service](../../img/v3_example_flow_of_a_standard_service.png){style="aspect-ratio: auto;"}

### Start page
Before starting the service, users should be presented with a page describing all the information they will need from the start, such as:
- what the service does.
- who it is for.
- what is needed to use the service.
- other ways to apply.
- how they can get help.

![Illustration of a start page](../../img/illustration_start_page.png){style="aspect-ratio: auto;"}

Keep in mind that research has shown that users avoid reading long text, so keep your information minimal, to the point and avoid using legal jargon.

This page usually resides on the GOV.CY portal. 

### Sign in

If the service requires users to sign in, choose to use the [Ariadni CY-Login (opens in new tab)](https://dsf.dmrid.gov.cy/2022/06/08/ariadni-cy-login-specifications/){rel="noreferrer noopener" target="_blank"} whenever possible to do so.

### One thing at a time

Prefer to split the [questions](../question_pages) across multiple pages with each page containing just one thing, for example:
- one piece of information you’re telling a user
- one decision they must make
- one question they must answer

![Illustration of splitting questions to ask one thing at a time](../../img/one-thing-at-a-time.png){style="aspect-ratio: auto;"}

User research will tell you when you can merge pages together. For example, if you’re designing an internal service for government users who need to repeat and switch between tasks quickly.

Keeping one thing on a page helps users to:
- understand what you’re asking them to do
- focus on the specific question and its answer
- reduce the stress of filling out humongous forms
- find their way through an unfamiliar process
- use the service on a mobile device
- recover easily from errors

It may also help to:
- save users’ answers automatically as they go
- capture analytics and statistics about each question
- handle branching questions and [loops](../multiple_things)
- apply conditional logic and guide users to complete the service in a more relaxed manner
- direct the users to a specific question where they can change their answer (see [check answers pattern](../check_answers)).

#### Reusing entered information
If the same type of information is needed more than once, make it easier to reuse previously entered answers through one of these methods:
- pre-populating the relevant fields
- showing carried-forward responses as an option for the user to select

### Check your answers page
Use the [check answers pattern](../check_answers) to let users check their answers before submitting information to a service.

Make sure to use the [success button](../../components/button/#success-button) to indicate that the user is about to completed the service.

![Illustration a check your answers page](../../img/v3_illustration_check_answers.png){style="aspect-ratio: auto;"}

### Confirmation page
After the users have submitted their application, present a [confirmation page](../confirmation-pages/) with a panel to inform them that they have successfully completed the transaction. This reassures the users their application has been filed and provides useful information on what will happen next.

![Illustration a confirmation page](../../img/illustration_confirmation_page.png){style="aspect-ratio: auto;"}

Research has shown that users feel more at ease when:
- they are presented with a reference number for their application
- they receive a notification either by email or by SMS
- they can save or print the confirmation.

<hr class="govcy-line">

## Variant 1 - Linear structure
This structure is designed to provide a linear flow for simple services, guiding users step-by-step from start to completion.

### When to use this structure
Use this structure when:

- The service can be simplified to a linear flow.
- The questions or information required from the user are straightforward and can be collected in a sequence.
- The service can be completed in a short amount of time.

### How it works

The linear structure of a service should:

1. Start with an informative start page.
2. If needed, ask the users to sign-in.
3. Gather information from the users, one question at a time.
4. Let the users check their answers before submitting.
5. Show the users a confirmation of successful completion page.

![An example flow of a linear service](../../img/v3_illustration_linear_structure.png){style="aspect-ratio: auto;"}

<hr class="govcy-line">

## Variant 2 - Break the service into sections
There may be cases where you need to implement complicated services, involving multiple tasks that users may need to complete over several sessions. In such cases you may consider gathering information from the users, by breaking the service into tasks. 

### When to use this structure 
Use this structure when:
- The service is inherently complex and involves multiple sections or tasks.
- Users need to manage and understand the progress of various sections and tasks.
- It is predicted that users may need to revisit the service more than once to complete it.

### How it works
Breaking the service into sections, uses the same structure and principles as the [basic service structure](#basic-structure). You only need to replace the "Gather information" step with the following:  

1. Let the users decide on which task or section to work on using a [task list page](../task-list-page/).
2. Gather information from the users, one section at a time.
3. Repeat this process until all tasks or sections are completed.

![Illustration of breaking the service into tasks](../../img/v3_illustration_breaking_the_service_into_tasks.png){style="aspect-ratio: auto;"}

Let users complete the different sections in an asynchronous manner. Also consider saving the users' responses and progress, and then to continue where they left off when they return.

After gathering information from the users you should still:
- Let the users [check their answers](#check-your-answers-page) from all sections before submitting.
- Show the users a [confirmation of successful completion page](#confirmation-page).

### Task list 
Use the [task list page](../task-list-page/) pattern to help users understand the tasks involved in completing a service. Each task on the task list should represent a different section to be completed by the user.

After completing all the tasks and the user clicks the 'Continue' button, navigate the user to the [check your answers](../check_answers/) page. Make sure to validate if the user has completed all the sections, or if a special condition does not allow the users to complete the service and show appropriate [error summary on the task list page](../task-list-page/#showing-errors) accordingly. 

Always allow users to go back into a task to change their answer. If a user decides to go back to a previous task, make sure information they have already entered is pre-populated.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h1>Service name</h1>
<section>
    <p class="govcy-fs-5 govcy-fw-700">Application incomplete</p>
    <p>You’ve completed 1 of 5 sections.</p>
</section>
<table class="govcy-table">
    <tbody>
        <tr>
            <td><a href="#">Company information <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
        <tr>
            <td><a href="#">Your contact details <span class="govcy-visually-hidden"> with status IN PROGRESS </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-cyan">IN PROGRESS</span></td>
        </tr>
        <tr>
            <td><a href="#">List convictions <span class="govcy-visually-hidden"> with status NOT STARTED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">NOT STARTED</span></td>
        </tr>
        <tr>
            <td><a href="#">Provide financial evidence <span class="govcy-visually-hidden"> with status CANNOT START YET </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">CANNOT START YET</span></td>
        </tr>
        <tr>
            <td><a href="#">Give medical information <span class="govcy-visually-hidden"> with status CANNOT START YET </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">CANNOT START YET</span></td>
        </tr>
    </tbody>
</table>
<button type="button" class="govcy-btn-primary">Continue</button>
</div>

*HTML code*
```html
<h1>Service name</h1>
<section>
    <p class="govcy-fs-5 govcy-fw-700">Application incomplete</p>
    <p>You’ve completed 1 of 5 sections.</p>
</section>
<table class="govcy-table">
    <tbody>
        <tr>
            <td><a href="#">Company information <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
        <tr>
            <td><a href="#">Your contact details <span class="govcy-visually-hidden"> with status IN PROGRESS </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-cyan">IN PROGRESS</span></td>
        </tr>
        <tr>
            <td><a href="#">List convictions <span class="govcy-visually-hidden"> with status NOT STARTED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">NOT STARTED</span></td>
        </tr>
        <tr>
            <td><a href="#">Provide financial evidence <span class="govcy-visually-hidden"> with status CANNOT START YET </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">CANNOT START YET</span></td>
        </tr>
        <tr>
            <td><a href="#">Give medical information <span class="govcy-visually-hidden"> with status CANNOT START YET </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">CANNOT START YET</span></td>
        </tr>
    </tbody>
</table>
<button type="button" class="govcy-btn-primary">Continue</button>
```

### Sections
Each section represents a task the user needs to take, in order to complete a service. Break the service into independent sections of smaller and related questions. 

Within each section, follow the [one thing at a time](#one-thing-at-a-time) principle and allow the users to answer questions one page at a time. This will also enable your service to apply conditional logic if needed. 

If the section consists of more than one question, present the user with a [summary list](../../components/summary_list/) before returning to the task list page. Make sure the button of the summary list for each section, is not the [success button](../../components/button/#success-button), as this button should only be used once in your service - when the users are ready for their final submission.

![Illustration of a section with a summary list](../../img/v3_illustration_secction_summary_list.png){style="aspect-ratio: auto;"}

If the service allows users to enter multiple answers of the same type, you may implement [the multiple things pattern](../multiple_things/) for a section.

After completing all the questions of the section, return the user to the task list page. 

#### Section statuses 
When a user visits the service for the first time, a section may have either a 'Not started' or a 'Cannot start yet' status.

When the user starts answering questions for a section, mark the status of that section as 'In progress'.

After answering all the section's questions, mark the status section as 'Completed' and return the user to the task list page. 

If the user starts answering questions on a section, but leaves without answering all of them, make sure that the status of the section is marked as 'In progress'. 

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Note that a user may return to a section at any time and change an answer. In such cases your service should be smart enough to decide whether the user has completed the section and the status is 'Completed', or there are pending questions and the status is 'In Progress'. 
		</p>
    </div>
</div>

#### Optional sections
Depending on the service, a section may be optional for some users. In such a case you may begin your section with a [radio question](../../components/radio/) and depending on the users' answer, decide if you wish to ask more questions related to that section. 

For example you may ask 'Have you donated blood before?'. 
- If the user answers 'Yes', mark the status as 'In progress' and present questions related to previous blood donations. 
- If the user answers 'No', you should mark the section as 'Completed' and return the user to the task list page.  

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Have you donated blood before?</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="blooddonation" id="blooddonation-yes">
                <label class="govcy-label" for="blooddonation-yes">Yes, I’ve donated blood before</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="blooddonation" id="blooddonation-no">
                <label class="govcy-label" for="blooddonation-no">No, I never donated blood before</label>
            </div>
        </div>
    </fieldset>
    <button type="submit" class="govcy-btn-primary">Continue</button>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Have you donated blood before?</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="blooddonation" id="blooddonation-yes">
                <label class="govcy-label" for="blooddonation-yes">Yes, I’ve donated blood before</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="blooddonation" id="blooddonation-no">
                <label class="govcy-label" for="blooddonation-no">No, I never donated blood before</label>
            </div>
        </div>
    </fieldset>
    <button type="submit" class="govcy-btn-primary">Continue</button>
</form>
```

#### Allow users to decide if the section is completed
Your service should be in a position to understand if a user has completed a section and mark it accordingly.

There are cases however, where it’s better to let the user decide when a task is completed.

This can be helpful when a section involves:
- some questions that are optional
- writing a long answer (such as in a textarea)
- looking up information, such as details about previous jobs
- answers that need to be checked carefully with someone else

Do this by asking a [radio question](../../components/radio/) at the end of the section — either as the last question (if the task is a single page) or on the [summary list](../../components/summary_list/) page (if the section has one).

Ask ‘Have you completed this section?’ with the radio options ‘Yes, I’ve completed this section’ or ‘No, I’ll come back to it later’.
- If the user selects ‘No’ mark the section as ‘Not started’ or ‘In progress’.
- If the user selects ‘Yes’ mark the section as ‘Completed’.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Have you completed this section?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="completed2" id="option2-yes">
                <label class="govcy-label" for="option2-yes">Yes, I’ve completed this section</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="completed2" id="option2-no">
                <label class="govcy-label" for="option2-no">No, I’ll come back to it later</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Have you completed this section?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="completed2" id="option2-yes">
                <label class="govcy-label" for="option2-yes">Yes, I’ve completed this section</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="completed2" id="option2-no">
                <label class="govcy-label" for="option2-no">No, I’ll come back to it later</label>
            </div>
        </div>
    </fieldset>
</form>
```

### Check your answers page change links
The 'Change' links on the [check your answers page](../check_answers/#let-users-go-back-and-change-their-answers), should lead to either the beginning of the related section, or its summary list page, depending on the implementation of each service. 

Make sure to test your approach with the users.

### Validate and guide the users throughout

Complex services are difficult for users, so do your best to make it easy for them. Ask them easy to understand questions and follow the [one thing at a time](#one-thing-at-a-time) principle. Do not overload your pages with instructions, instead simplify the questions asked and use validations to guide them throughout the process. 

Depending on the service, you may want to validate on the following levels:

1. Question pages. Validate the users' input on each page. Follow the instructions for [error messages](../../components/error_message) and [error summary](../../components/error_summary) when needed. 
2. Sections' summary list pages. Validate the users' answers for the specific section as a whole. Check if the user has answered all the necessary questions, or if there are business rule violations for the specific section, and show an [error summary](../../components/error_summary) when needed.  
3. The task list. Validate the users' answers for all the sections of the task list as a whole. Validate if users have completed all the sections, or if a special condition does not allow them to complete the service. Show appropriate [error summary on the task list page](../task-list-page/#showing-errors) when needed.

Remember that validations are run when the users distinctly indicate that they are done with the specific page, for example when clicking the “continue” button.

It is also important not to block users from using other sections of the service when there is an error, so consider when it is appropriate to use the [allow users to continue error summary variant](../../components/error_summary/#allow-users-to-continue).

In order to guide users, the [error messages content](../../components/error_message/#errors-content) should be short, easy to understand and specific.

Remember to always validate the users' data before submitting on the [check your answers page](../check_answers/#showing-errors).

<hr class="govcy-line">

## Variant 3 - Asynchronous basic structure
The asynchronous basic structure uses the same structure and principles as the [basic service structure](#basic-structure), but also takes advantage of the [task list page](../task-list-page/) described in the [break the service into sections variant](#variant-2---break-the-service-into-sections) to let users decide on which question to work on. 

### When to use this structure 
Use this structure when:

- The service involves multiple questions or pieces of information that cannot be easily reduced or simplified.
- The flexibility to answer questions in any order will help the users to complete the service.
- It is predicted that users may need to revisit the service more than once to complete it.

### How it works

In this structure, the service should:

1. Start with an informative start page
2. If needed, ask the users to sign-in
3. Present a [Task List page](../task-list-page/) where users can select which question to answer
4. Gather information from the users, one question at a time
5. Let the users check their answers before submitting
6. Show the users a confirmation of successful completion page.

![An example flow of a asynchronous service](../../img/v3_illustration_async_structure.png){style="aspect-ratio: auto;"}

Let users answer different questions in an asynchronous manner through the [task list page](../task-list-page/). Also consider saving the users' responses and progress, and then to continue where they left off when they return. 

User research will show you what to do when users click on the `Continue` button of each question. You may allow users to continue answering questions in a linear manner, or return to the task list page to allow users to continue using the service in an asynchronously.

Remember to follow the [one thing at a time](#one-thing-at-a-time) principle and allow the users to answer questions one page at a time. This will also enable your service to apply conditional logic if needed. 

After gathering information from the users you should still:
- Let the users [check their answers](#check-your-answers-page) before submitting.
- Show the users a [confirmation of successful completion page](#confirmation-page).

Follow the same instructions concerning the [task list](#task-list) and [statuses](#section-statuses) as in the break the service into tasks and sections structure.

## Contribute
If you have used or researched this pattern, please let us have your feedback, so we can make it better for everyone. Send us an email at <a href="mailto:dsf@dits.dmrid.gov.cy" target="_blank">dsf@dits.dmrid.gov.cy</a> to get in touch. 

