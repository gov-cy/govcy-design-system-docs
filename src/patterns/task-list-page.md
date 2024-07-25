---
title: "Task list page"
date: 2022-02-01 00:01:02Z
tags: "pages"
description: "Use this page to help users understand the tasks involved in a completing a service and when they’ve completed them."
---
Task list pages help users understand the tasks involved in a completing a service and when they’ve completed them. The task list gives users more control over how they complete long, complex services.

## When to use this pattern
Use a task list page for complicated services, involving multiple tasks that users may need to complete over a number of sessions. 

Task list are most effective on service that their tasks can be completed in an asynchronous manner.

Only use the task list if there’s evidence that users:
- do not want to, or cannot, complete all the tasks in one sitting
- need to be able to choose the order they complete the tasks in

Read the [structuring a service](../service_structure/) for more information on how to use the task list within a service.

## When not to use this pattern
Try to simplify the transaction or the service before you use a task list page. If you’re able to reduce the number of tasks or steps involved, you might not need one.

The task list should not be used as a way of showing users their answers. For this, you should use a [summary list](../../components/summary_list/) instead.

## How it works
Use a task list in the page's [main section](../../getting-started/page-template/#sections). Note that all code examples in this page shows only the `Main` section.

You should show a task list page:
- at the start of the transaction
- at the start of each returning session

If it needs to be completed over multiple sessions, consider saving the users' progress, and then to continue where they left off when they return. 

If you use a task list page in your service, you’ll need to:
- group related actions or questions into tasks
- show the status of the tasks

If there are lots of tasks to complete, you might also need to group them further into steps.

The task lists consists of rows with the name of the task as a link and a [tag](../../components/tag/) describing the status of the task.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h1>Service name</h1>
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

Add `<span class="govcy-visually-hidden"> with status [whatever status] </span>` to let screen reader users know the status of each task link.  

Users should be able to complete tasks in whatever order they like.

The status alongside the task indicates whether they can start it. Users can select a task to start completing it. Once they have completed it and returned to the task list, the status for that task will have changed to ‘Completed’.

Users can only move on from the task list when all tasks are shown as ‘Completed’.

Always allow users to go back into a task to change their answer. If a user decides to go back to a previous task, make sure information they have already entered is pre-populated.

### Group related actions into tasks
Group related activities and questions into tasks, for example, ‘Provide financial evidence’ and ‘Give medical information’. This will help users understand and plan what they need to do.

Where possible, task names should:

- describe what the task or activity involved
- start with verbs, for example, ‘check’, ‘declare’, ‘report’

Read the [structuring a service - break the service into sections structure](../service_structure/#variant-2---break-the-service-into-sections) for more information on tasks and sections.

### Showing the progress 
You can show the progress of the service as shown in the example below.

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

### Tasks that cannot start yet
There may be cases where tasks need to be completed in a specific order. In such a case, mark the tasks that cannot start yet with the `CANNOT START YET` status, and make sure to order the tasks in a logical order. User research will help you to decide whether or not to have the task displayed as a link. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
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
            <td>Give medical information</td>
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
            <td>Give medical information</td>
            <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">CANNOT START YET</span></td>
        </tr>
    </tbody>
</table>
<button type="button" class="govcy-btn-primary">Continue</button>
```


### Showing errors
If the user tries to continue without completing all tasks, display the [error summary](../../components/error_summary/) and link the errors with the task link.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2 data-toc-exclude role="alert">There is a problem</h2>
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

*HTML code*
```html
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
```

There may be cases where the users have completed all the tasks but still cannot continue due to a business rule. 

In the scenario shown in the example below, the users were asked to declare their 2013 impairment on either deposits or securities, or both. In order to submit the application, the users must declare impairment on at least one category. The user in this example has completed all the sections, but declared that there was no impairment either deposits or securities.  

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2 data-toc-exclude role="alert">There is a problem</h2>
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

*HTML code*
```html
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
```

### Group tasks into steps
If your transaction involves lots of tasks, make it manageable by splitting it up into steps that represent stages in the process.

For example, you could group all tasks which help users find out if your service is right for them in a step called ‘Check before you start’.

Where possible, allow users to complete tasks in any order. This will help them plan their time and complete sections as and when they can.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h1>Service name</h1>
<section>
    <p class="govcy-fs-5 govcy-fw-700">Application incomplete</p>
    <p>You’ve completed 3 of 8 sections.</p>
</section>
<section>
    <h2 data-toc-exclude>1. Check before you start</h2>
    <table class="govcy-table">
        <tbody>
            <tr>
                <td><a href="#">Check eligibility <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
            </tr>
            <tr>
                <td><a href="#">Read declaration <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
            </tr>
        </tbody>
    </table>
</section>
<section>
    <h2 data-toc-exclude>2. Complete application</h2>
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
                <td><a href="#">Provide financial evidence <span class="govcy-visually-hidden"> with status NOT STARTED </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">NOT STARTED</span></td>
            </tr>
            <tr>
                <td><a href="#">Give medical information <span class="govcy-visually-hidden"> with status NOT STARTED </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">NOT STARTED</span></td>
            </tr>
        </tbody>
    </table>
</section>
<section>
    <h2 data-toc-exclude>3. Apply</h2>
    <table class="govcy-table">
        <tbody>
            <tr>
                <td><a href="#">Submit and pay <span class="govcy-visually-hidden"> with status CANNOT START YET </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">CANNOT START YET</span></td>
            </tr>
        </tbody>
    </table>
</section>
<button type="button" class="govcy-btn-primary">Continue</button>
</div>

*HTML code*
```html
<h1>Service name</h1>
<section>
    <p class="govcy-fs-5 govcy-fw-700">Application incomplete</p>
    <p>You’ve completed 3 of 8 sections.</p>
</section>
<section>
    <h2>1. Check before you start</h2>
    <table class="govcy-table">
        <tbody>
            <tr>
                <td><a href="#">Check eligibility <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
            </tr>
            <tr>
                <td><a href="#">Read declaration <span class="govcy-visually-hidden"> with status COMPLETED </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag">COMPLETED</span></td>
            </tr>
        </tbody>
    </table>
</section>
<section>
    <h2>2. Complete application</h2>
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
                <td><a href="#">Provide financial evidence <span class="govcy-visually-hidden"> with status NOT STARTED </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">NOT STARTED</span></td>
            </tr>
            <tr>
                <td><a href="#">Give medical information <span class="govcy-visually-hidden"> with status NOT STARTED </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">NOT STARTED</span></td>
            </tr>
        </tbody>
    </table>
</section>
<section>
    <h2>3. Apply</h2>
    <table class="govcy-table">
        <tbody>
            <tr>
                <td><a href="#">Submit and pay <span class="govcy-visually-hidden"> with status CANNOT START YET </span></a></td>
                <td class="govcy-text-end"><span class="govcy-tag govcy-tag-gray">CANNOT START YET</span></td>
            </tr>
        </tbody>
    </table>
</section>
<button type="button" class="govcy-btn-primary">Continue</button>
```
### Errors in tasks
If the users encounter a validation error while completing a task, consider using the [allow users to continue error summary variant](../../components/error_summary/#allow-users-to-continue), with a link to the task list page. This will allow users to continue with other tasks, even if they cannot complete the specific task at that moment. 

### Marking tasks as completed
Your service should be in a position to understand if a user has completed a task and mark it accordingly.

There are cases however, where it’s better to let the user decide when a task is completed.

Read the [structuring a service - break the service into sections structure](../service_structure/#variant-2---break-the-service-into-sections) for more information on allowing users to decide if the section is completed.

### Status text and style
Use the following statuses:
<div class="govcy-table-responsive">

| Tag HTML | English text | Greek text |
| ---- | ---- | ---- |
| `<span class="govcy-tag govcy-tag-gray">NOT STARTED</span>` <br><br> *Example* <br> <span class="govcy-tag govcy-tag-gray">NOT STARTED</span> | NOT STARTED | ΔΕΝ ΞΕΚΙΝΗΣΕ |
| `<span class="govcy-tag govcy-tag-gray">CANNOT START YET</span>` <br><br> *Example* <br> <span class="govcy-tag govcy-tag-gray">CANNOT START YET</span> | CANNOT START YET | ΔΕΝ ΜΠΟΡΕΙ ΝΑ ΞΕΚΙΝΗΣΕΙ AKOMA |
| `<span class="govcy-tag govcy-tag-cyan">IN PROGRESS</span>` <br><br> *Example* <br> <span class="govcy-tag govcy-tag-cyan">IN PROGRESS</span> | IN PROGESS | ΣΕ ΕΞΕΛΙΞΗ  |
| `<span class="govcy-tag">COMPLETED</span>` <br><br> *Example* <br> <span class="govcy-tag">COMPLETED</span> | COMPLETED | ΟΛΟΚΛΗΡΩΘΗΚΕ |

{.govcy-table}
</div>

Although we recommend using consistent wording across task lists, you can change it if research shows that different text is more suitable to your service or users.

If you are creating your own statuses, use adjectives rather than verbs. Use sentence case, and keep it short, so that it can be easily read and understood.

Do not use the red background colour for any status text except errors.

## Accessibility
Make sure:
- you add `<span class="govcy-visually-hidden"> with status [whatever status] </span>` to let screen reader users know the status of each task
- [you don't use colour alone to convey information (opens in new tab)](https://www.w3.org/WAI/WCAG21/Understanding/use-of-color.html){rel="noreferrer noopener" target="_blank"} 
- background and text colour of the status tags must comply with the [contrast ratio of 4.5:1 (opens in new tab)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html){rel="noreferrer noopener" target="_blank"}
- if you use the same tag in more than one place, make sure you keep the colour consistent