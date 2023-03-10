---
"title" : "Error Message"
date: 2022-02-01 00:01:01Z
---
Show an error message when there is a validation error. In the error message explain what went wrong and how to fix it.

## When to use this component
Show an error message next to the field and in the [error summary](../error_summary) when there is a validation error.

## When not to use this component
Do not use error messages to tell a user that they are not eligible or do not have permission to do something. Or to tell them about a lack of capacity or other problem the user cannot fix - because the problem is with the service rather than with the information the user has provided.

Instead, take the user to a page that explains the problem (for example, telling them why they’re not eligible) and provides useful information about what to do next.

## How it works

Run the validations for each page/question after the users distinctly indicate that their inputs are ready to be submitted, for example when clicking the "continue" button. This gives the user the opportunity to review their answer, or get out of the input's focus and not get flooded with red error messages which can be overwhelming. 

For each error:
- put the message in red after the question text and hint text
- use a red border to visually connect the message and the question it belongs to
- if the error relates to a specific field within the question, give it a red border and refer to that field in the error message - for example: “you must enter a year”

To help screen reader users, the error message component includes a hidden ‘Error:’ before the error message. These users will hear, for example, `<span class="govcy-visually-hidden-error"> Error: </span> The date your passport was issued must be in the past`.

Use `aria-describedby="error_message_id"` to help announce the error message on screen readers.

Summarize all errors at the top of the page the user is on using an [error summary](../error_summary).

*Examples*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="in1">Label</label>
        <p class="govcy-input-error-msg" id="error1"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
        <input type="text" id="in1" class="govcy-text-input govcy-text-input-error" aria-describedby="error1">
    </div>
    <fieldset class="govcy-fieldset">
        <div class="govcy-form-control govcy-form-control-error">
            <legend class="govcy-legend govcy-mb-1">Date of birth</legend>
            <p class="govcy-input-error-msg govcy-mb-3" id="error2"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
            <div class="govcy-d-flex">
                <div class="govcy-d-block">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day">Day</label>
                    <input type="text" class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2" id="day" maxlength="2" aria-describedby="error2">
                </div>
                <div class="govcy-d-block govcy-ml-2">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month">Month</label>
                    <input type="text" class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2" id="month" maxlength="2" aria-describedby="error2">
                </div>
                <div class="govcy-d-block govcy-ml-2">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year">Year</label>
                    <input type="text" class="govcy-text-input govcy-text-input-error govcy-text-input-char_6 govcy-p-3" id="year" maxlength="4" aria-describedby="error2">
                </div>
            </div>
        </div>
    </fieldset>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error3"><span class="govcy-visually-hidden-error">Error: </span>There is an error</span>
            <label class="govcy-checkbox">Option 1
                <input class="govcy-checkbox-input" type="checkbox" aria-describedby="error3">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Option 2
                <input class="govcy-checkbox-input" type="checkbox" aria-describedby="error3">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error4"><span class="govcy-visually-hidden-error">Error: </span>Mandatory field</p>
            <label class="govcy-radio">Option 1
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error4">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Option 2
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error4">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Option 3
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error4">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
    <div class="govcy-form-control govcy-form-control-error govcy-pb-1">
        <label class="govcy-label govcy-mb-1" for="in2">Upload a file</label>
        <p class="govcy-input-error-msg govcy-mb-3" id="error5"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
        <input class="govcy-file-upload" type="file" id="in2" name="in2" aria-describedby="error5">
    </div>
</form>
</div>
