---
title: "How to handle errors and problems in a service"
date: 2022-02-01 00:01:03Z
description: "Use this guide to choose the right pattern or component when something stops users from continuing."
image: v3_custom_design_element.png
twoThirds: true
---


In this guide we will be looking at when and how to choose the right pattern or component when something stops users from continuing through a service.

Different teams may use the word “error” in different ways. For example, developers may think of errors as code exceptions, while designers may think of validation errors. Users do not usually make this distinction. They need to know what happened, whether they can do something about it, and what to do next.

The Unified Design System provides different components and patterns for different situations. This guide helps you choose the right one.

--------

## When to check for problems

The core principle is: 

<blockquote class="govcy-inset-text">
    <p>Check when the user asks the service to move them forward, not while they are still working</p>
</blockquote>

Check for problems at the point where the user clearly indicates that they are ready to continue, submit, or complete a task.

Do not show validation errors while the user is still entering information, moving between fields, or reviewing what they typed. This can be overwhelming and may make the service harder to use.

For example, check for problems when the user:

- clicks **Continue** on a question page
- clicks **Save and continue** on a task list or hub page
- clicks **Submit** on the check your answers page

### Validation errors

Run validation after the user clicks **Continue** or another action that means they are ready to move on.

### Eligibility checks during the journey

Run eligibility checks when the service has enough information to know whether the user can continue.

This may be:

- after the user signs in
- after the user answers a question that affects eligibility
- before showing the check your answers page
- before accepting the final submission

### Checks on task lists, hub pages and grouped pages

Some pages do not ask a single question, but still need to check whether the user has completed enough information to continue.

For example, a task list, hub page, or “add another” page may need to check that the user has:

- completed all required tasks
- added at least one item
- added no more than the maximum number of items
- completed all required details for each item

Run these checks when the user selects **Continue**, **Save and continue**, or another action that means they are ready to move on.

--------

## What to show the users

The UDS has several components and patterns to help users fix problems.

### Start with what the user can do next

Before choosing a component or pattern, ask:

<blockquote class="govcy-inset-text">
    <p>Can the user do something in the service to fix the problem?</p>
</blockquote>

If the user can fix the problem, keep them in the service and show them where to fix it.

If the user cannot fix the problem in the service, show a page that explains what happened and what they can do next.

### When the user's answers are missing, incomplete, or invalid

Use the [error summary](../../components/error_summary/) when the user needs to correct something before they can continue.

Use the [error message](../../components/error_message/) as well when the problem is connected to a specific input.

For example, use an error summary and error message when:

- a required field is empty
- a date is in the wrong format
- a number is outside the allowed range
- a file is too large
- the user selected “Other” but did not enter more details
- the user cannot continue because a business rule has been violated and they can fix it by changing an answer
- when a task has not been completed

In these cases, the user’s answer is missing, incomplete, or invalid. 

Here are some examples:

**Example of validation error on a question page**

<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2 role="alert">There is a problem</h2>
    <p class="govcy-mb-0">
        <a href="#in-tel">Enter a valid telephone number</a>
    </p>
</div>
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="in-tel">What is your telephone number?</label></h1>
        <p id="in-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Enter a valid telephone number
        </p>
        <input class="govcy-text-input govcy-text-input-char_20 govcy-text-input-error" id="in-tel" name="in-tel" type="tel" spellcheck="false" aria-describedby="in-error" autocomplete="tel">
    </div>
    <button type="button" class="govcy-btn-primary">Continue</button>
</form>
</div>

**Example of a Task List page with errors not all tasks completed**

<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2 role="alert">There is a problem</h2>
    <p class="govcy-mb-0">
        <a href="#contact-details">Complete the section on your contact details</a>
        <a href="#medical-information">Complete the section on medical information</a>
    </p>
</div>
<h1>Service name</h1>
<section>
    <p class="govcy-fs-5 govcy-fw-700">Application incomplete</p>
    <p>You’ve completed 3 of 5 sections.</p>
</section>
<table class="govcy-table">
    <tbody>
        <tr>
            <td><a id="company-information" href="#">Company information <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
        <tr>
            <td><a id="contact-details" href="#">Your contact details <span class="govcy-visually-hidden"> with status IN PROGRESS </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-cyan">IN PROGRESS</span></td>
        </tr>
        <tr>
            <td><a id="convictions" href="#">List convictions <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
        <tr>
            <td><a id="financial-evidence" href="#">Provide financial evidence <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
        <tr>
            <td><a id="medical-information" href="#">Give medical information <span class="govcy-visually-hidden"> with status CANNOT START YET </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">CANNOT START YET</span></td>
        </tr>
    </tbody>
</table>
<button type="button" class="govcy-btn-primary">Continue</button>
</div>

**Example of a Task List page with business error**

<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2 role="alert">There is a problem</h2>
    <p class="govcy-mb-0">
        <a href="#deposits">Declare an impairment on either deposits or securities</a>
    </p>
</div>
<h1>Service name</h1>
<section>
    <p class="govcy-fs-5 govcy-fw-700">Application complete</p>
    <p>You’ve completed 4 of 4 sections.</p>
</section>
<table class="govcy-table">
    <tbody>
        <tr>
            <td><a id="deposits" href="#">Deposits impairment<span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
        <tr>
            <td><a id="impairment" href="#">Securities impairment<span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
        <tr>
            <td><a id="compensations" href="#">List compensations you claimed <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
        <tr>
            <td><a id="consent" href="#">Provide consent for access to bank details <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
            <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
        </tr>
    </tbody>
</table>
<button type="button" class="govcy-btn-primary">Continue</button>
</div>

#### How to show the error summary

<img src="{{ '/img/UDS_error_summary_js.gif' | url }}" alt="Visual representation of how to show the error summary using linking to an element on the same page" class="govcy-img-ar-auto" style="height: 400px;">

Simply display the error summary on the page is not enough. You also need to:
- move the keyboard focus to the error summary heading using a hashed link (for example `#error-summary-heading`). This will draw the attention to the users that there is an a problem. Sighted users will be navigated to the error summary area on the page, and screen readers will read out that there is a problem
- include the attribute `role="alert"` on the error summary heading (`<h2>`)
- include the heading ‘There is a problem’ in English and ‘Υπάρχει πρόβλημα’ in Greek
- if there is a validation error on a field, use use [linking to an element on the same page](../../styles/typography/#linking-to-an-element-on-the-same-page) to link each error to the fields that have validation errors
    - make sure the error messages in the error summary are worded the same as those which appear next to the fields with errors
- if there is a business rule, link each error to the ‘change’ link or relevant page where the user can correct the violation.  

For more guidance on how to show the error summary, see the [error summary component - how it works](../../components/error_summary/#how-it-works).

### When the user is not eligible

Use a [Cannot use the service page](../../patterns/cannot-use-the-service/) when the user cannot use or continue with the service because they do not meet the eligibility rules.

For example, use this pattern when:

- the user is not registered in a required register
- the user does not have the required role or authorisation
- the user’s profile type cannot use the service
- an eligibility check shows that the user cannot use the service

**Example**:

<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Your citizenship is not Cypriot

To use this service, you need to be a Cypriot citizen.

If you think that there is a mistake in our records, please visit your nearest [District Administration Office](https://www.gov.cy/moi/en/documents/application-submission-offices/){rel="noreferrer noopener" target="_blank"}.

</div>

#### When a user becomes ineligible during the journey

Sometimes the user gives a valid answer that makes them ineligible.

For example, a service may only be for people who live in Cyprus. If the user answers that they live outside Cyprus, the answer is valid, but the service is not for them.

In the normal question flow, use a [Cannot use the service page](../../patterns/cannot-use-the-service/).

Include a link to change the answer if the user may have made a mistake.

**Example**:

<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# You do not live in Cyprus 

To use this service, you need to be living in Cyprus. 

[Change your answer](#)

</div>

### When the user is on the check your answers page

If the problem is found on the [check your answers page](../../patterns/check_answers/) and the user can fix it by changing an answer, use an [error summary](../../patterns/check_answers/#showing-errors).

This can happen because web services are asynchronous. Ideally, users should not reach the check your answers page with answers that make them ineligible, but it can happen.

The error summary should link to the answer the user needs to change.

Use a [cannot use the service page](../../patterns/cannot-use-the-service/) from the check your answers page only when the user cannot fix the problem by changing an answer.

**Example of validation error on the check your answers page**:

<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
    <div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
        <h2 role="alert">There is a problem</h2>
        <p>
            <a href="#contact-details">Complete the section on your contact details</a>
            <a href="#medical-information">Complete the section on medical information</a>
        </p>
    </div>
    <h1>Check your answers before submitting your application</h1>
    <dl class="govcy-summary-list">
        <div class="govcy-summary-list-row">
            <dt class="govcy-summary-list-key">
                Name
            </dt>
            <dd class="govcy-summary-list-value">
                Andreas Andreou
            </dd>
            <dd class="govcy-summary-list-actions">
                <a href="#">Change<span class="govcy-visually-hidden"> name</span></a>
            </dd>
        </div>
        <div class="govcy-summary-list-row">
            <dt class="govcy-summary-list-key">
                Date of birth
            </dt>
            <dd class="govcy-summary-list-value">
                10 March 1990
            </dd>
            <dd class="govcy-summary-list-actions">
                <a href="#">Change<span class="govcy-visually-hidden"> date of birth</span></a>
            </dd>
        </div>
        <div class="govcy-summary-list-row">
            <dt class="govcy-summary-list-key">
                Address
            </dt>
            <dd class="govcy-summary-list-value">
                50 Enton Street<br>Nicosia<br>2066
            </dd>
            <dd class="govcy-summary-list-actions">
                <a href="#">Change<span class="govcy-visually-hidden"> address</span></a>
            </dd>
        </div>
        <div class="govcy-summary-list-row">
            <dt class="govcy-summary-list-key">
                Contact details
            </dt>
            <dd class="govcy-summary-list-value">
                <a id="contact-details" href="#">Enter contact details</a>
            </dd>
        </div>
        <div class="govcy-summary-list-row">
            <dt class="govcy-summary-list-key">
                Medical information
            </dt>
            <dd class="govcy-summary-list-value">
                <a id="medical-information" href="#">Enter your medical information</a>
            </dd>
        </div>
    </dl>
    <button type="button" class="govcy-btn-success">Submit</button>
</div>

### When the service gets an unexpected response

Sometimes a service depends on an API or another system to continue the journey.

If the API or system returns an unexpected response, times out, or cannot be reached, do not show an error summary unless the user can fix the problem by changing something in the service.

Use a [there is a problem with the service page](../../patterns/there-is-a-problem/) when the problem is unexpected and the user cannot fix it. This pattern is for unexpected service problems and should be used instead of showing technical messages like 500, bad request, or API error. 

For example, use a there is a problem with the service page when:

- an API does not respond
- an API returns an unexpected format
- an API returns an error that is not mapped to a user-facing eligibility or business rule
- the service cannot save, load, upload, download, or submit because of a system problem
- the service cannot confirm whether the user is eligible

Do not use an error summary for these problems, because there is no answer or action in the page that the user can correct. Error summaries are for validation errors or other violations that the user can fix. 

If the API response represents a known business rule, show the relevant pattern instead. For example:

- if the response means the user is not eligible, use a [cannot use the service page](../../patterns/cannot-use-the-service/)
- if the service is deliberately unavailable, use a [service unavailable page](../../patterns/service-unavailable-pages/)
- if the user needs to change an answer on the check your answers page, use an [error summary](../../components/error_summary/)

### Choose the right pattern or component

Here is a summary of the patterns and components that can be used to handle errors and problems.

|Situation|Use|
|---|---|
|The user left a required field empty|[Error summary](../../components/error_summary/) and [error message](../../components/error_message/)|
|The user entered an answer in the wrong format|[Error summary](../../components/error_summary/) and [error message](../../components/error_message/)|
|The user gave a valid answer that stops the normal journey|[Cannot use the service pages](../../patterns/cannot-use-the-service/)|
|The user can fix an issue from the check your answers page|[Error summary](../../components/error_summary/)|
|The user left a task unfinished on a task list|[Error summary](../../components/error_summary/)|
|The user cannot fix an eligibility issue|[Cannot use the service pages](../../patterns/cannot-use-the-service/)|
|The page or URL does not exist|[Page not found pages](../../patterns/page-not-found-pages/)|
|The service is intentionally unavailable|[Service unavailable pages](../../patterns/service-unavailable-pages/)|
|There is an unexpected technical problem|[There is a problem with the service pages](../../patterns/there-is-a-problem/)|
|An API or system returns an unexpected response that the user cannot fix|[There is a problem with the service pages](../../patterns/there-is-a-problem/)|

{.govcy-table}


### Do not use

Do not use:

- `error messages` for eligibility failures
- `error summaries` for planned service downtime
- `cannot use the service pages` for technical problems
- `page not found pages` for users who are not eligible
- `service unavailable pages` for validation errors
- vague headings like “Error”, “Access denied” or “Something went wrong” when a clearer explanation is possible

## Accessibility

Make sure users can understand what happened and what they can do next.

When using `error messages` and `error summaries`, follow the accessibility guidelines for [error messages](../../components/error_message/#accessibility) and [error summary](../../components/error_summary/#accessibility).

When using a page pattern:

- use a clear `H1`
- explain the problem in plain language
- include a next step when there is one
- include contact information when users may need help