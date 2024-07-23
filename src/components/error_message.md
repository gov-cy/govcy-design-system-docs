---
"title" : "Error Message"
date: 2022-02-01 00:01:01Z
description: "Use this component to show an error message next to the field and in the error summary when there is a validation error."
---
Show an error message when there is a validation error. In the error message explain what went wrong and how to fix it.

## When to use this component
Show an error message next to the field and in the [error summary](../error_summary/) when there is a validation error.

## When not to use this component
Do not use error messages to tell a user that they are not eligible or do not have permission to do something or to tell them about a lack of capacity or other problem the user cannot fix - because the problem is with the service rather than with the information the user has provided.

Instead, take the user to a page that explains the problem (for example, telling them why they’re not eligible) and provides useful information about what to do next.

There are separate patterns for:

- [‘there is a problem with the service’ pages](../../patterns/there-is-a-problem/)
- [‘page not found’ pages](../../patterns/page-not-found-pages/)
- [‘service unavailable’ pages](../../patterns/service-unavailable-pages/)

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

Always summarize all errors at the top of the page, by using the [error summary](../error_summary/).

When showing the errors, use [linking to an element on the same page](../../styles/typography/#linking-to-an-element-on-the-same-page) to move keyboard focus to the error summary heading. Read more about this on the [error summary](../error_summary/#how-it-works) page. 

For each error:

- put the message in red after the question text and hint text
- use a red border to visually connect the message and the question it belongs to
- if the error relates to a specific field within the question, give it a red border and refer to that field in the error message - for example: “you must enter a year”

To help screen reader users, the error message component includes a hidden ‘Error:’ before the error message. These users will hear, for example, `<span class="govcy-visually-hidden-error"> Error: </span> The date your passport was issued must be in the past`. Also add  `aria-describedby` on the element, with the id of the error message. 

More details on how to style error messages for each component type, can be found on the components' individual documentation page.

### When to check for errors

Run the validations for each page or question after the users distinctly indicate that their inputs are ready to be submitted, for example when clicking the “continue” button. This gives the user the opportunity to review their answer, or get out of the input’s focus and not get flooded with red error messages which can be overwhelming.

### Examples

See below some examples of error messages.

*Examples*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="in-error">Label</label></h1>
        <p id="in-error-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input id="in-error" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in-error-error">
    </div>
</div>

<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="in-error1">Label</label>
        <p id="in-error-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input id="in-error1" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in-error-error1">
    </div>
</div>

<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="input-err1">What is your job description?</label>
        <p id="job-description-input-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Enter a valid Job description
        </p>
        <textarea id="input-err1" class="govcy-text-area govcy-text-area-error" aria-describedby="job-description-input-error1" rows="5"></textarea>
    </div>
</div>

<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="sort-err1">Sort by</label>
        <span id="sort-err-hint1" class="govcy-hint">Will sort results accordingly</span>
        <p id="sort-err-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Please select valid options
        </p>
        <select class="govcy-select govcy-select-error" id="sort-err1" name="sort-err1" aria-describedby="sort-err-hint1 sort-err-error1">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</div>

<div class="govcy-form">
    <fieldset class="govcy-fieldset" aria-describedby="option6-error">
        <legend class="govcy-legend">Do you wish to continue?</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="option6-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option6" id="option6-yes">
                <label class="govcy-label" for="option6-yes">Yes</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option6" id="option6-no">
                <label class="govcy-label" for="option6-no">No</label>
            </div>
        </div>
    </fieldset>
</div>

<div class="govcy-form">
    <fieldset class="govcy-fieldset" aria-describedby="option7-error">
        <legend class="govcy-legend">Do you wish to continue?</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="option7-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-radio govcy-d-sm-inline-block">
                <input class="govcy-radio-input" type="radio" name="option7" id="option7-yes">
                <label class="govcy-label" for="option7-yes">Yes</label>
            </div>
            <div class="govcy-radio govcy-d-sm-inline-block">
                <input class="govcy-radio-input" type="radio" name="option7" id="option7-no">
                <label class="govcy-label" for="option7-no">No</label>
            </div>
        </div>
    </fieldset>
</div>

<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-simple-error-email" name="collapseGroupsimple-error" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-simple-error-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroupsimple-error" type="radio" id="option6-simple-error-emailDif" value="emailDif" data-aria-controls="email-simple-error-different" checked/>
                <label class="govcy-label" for="option6-simple-error-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-error govcy-pl-4 govcy-ml-5 govcy-radio__conditional" id="email-simple-error-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple-error-1">Perosnal Email Address</label>
                    <span id="in4-simple-error-hint-1" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4-simple-error-1" type="text" class="govcy-text-input" aria-describedby="in4-simple-error-hint-1" value="test@email.com"/>
                </div>
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple-error">Work Email Address</label>
                    <span id="in4-simple-error-hint" class="govcy-hint">We'll only use this for applying</span>
                    <p id="in4-simple-error-error-msg" class="govcy-input-error-msg">
                        <span class="govcy-visually-hidden-error">Error:</span>
                        Enter email address
                    </p>
                    <input id="in4-simple-error" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in4-simple-error-hint in4-simple-error-error-msg"/>
                </div>
            </div>
        </div>
    </fieldset>
</div>

<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="file5">Upload a file</label>
        <span id="file5-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <p id="file5-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input class="govcy-file-upload" type="file" id="file5" name="file5" aria-describedby="file5-hint file5-error">
    </div>
</div>

<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="appointment-err-date1">Appointment Date</label>
        <span id="appointment-err-date-hint1" class="govcy-hint">For example, 13/8/2007</span>
        <p id="appointment-err-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Appointment Date must include a year
        </p>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input govcy-text-input-error" 
                id="appointment-err-date1"
                name="appointment-err-date1"
                aria-describedby="appointment-err-date-hint1 appointment-err-error1"/>
        </div>
    </div>
</div>

<div class="govcy-form">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date-err1-hint date-err1-error">
        <legend class="govcy-legend">Date of birth</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <span class="govcy-hint" id="date-err1-hint">For example, 12 11 2007</span>
            <p id="date-err1-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_err1">Day</label>
                    <input id="day_err1" class="govcy-text-input govcy-text-input-char_3 govcy-text-input-error" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-day">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_err1">Month</label>
                    <select id="month_err1" class="govcy-select govcy-select-error" autocomplete="bday-month">
                        <option value="" selected=""></option>
                        <option value="1">1 - January</option>
                        <option value="2">2 - February</option>
                        <option value="3">3 - March</option>
                        <option value="4">4 - April</option>
                        <option value="5">5 - May</option>
                        <option value="6">6 - June</option>
                        <option value="7">7 - July</option>
                        <option value="8">8 - August</option>
                        <option value="9">9 - September</option>
                        <option value="10">10 - October</option>
                        <option value="11">11 - November</option>
                        <option value="12">12 - December</option>
                    </select>
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_err1">Year</label>
                    <input id="year_err1" class="govcy-text-input govcy-text-input-char_6 govcy-text-input-error" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-year">
                </div>
            </div>
        </div>
    </fieldset>
</div>

<div class="govcy-form">
    <fieldset class="govcy-fieldset" aria-describedby="check-er-input-error1">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="check-er-input-error1" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check-er-checkbox-group1" type="checkbox" id="check-er-option10">
                <label class="govcy-label" for="check-er-option10">Option 1</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check-er-checkbox-group1" type="checkbox" id="check-er-option11">
                <label class="govcy-label" for="check-er-option11">Option 2</label>
            </div>
        </div>
    </fieldset>
</div>

<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="input3">Enter a job description</label>
        <p id="job-description-input-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Job description must be 150 characters or less
        </p>
        <textarea id="input3" class="govcy-text-area govcy-text-area-error" aria-describedby="govcy-hint-hint3 job-description-input-error" rows="5">A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format. A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format. A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format.
        </textarea>
        <div  id="govcy-hint-hint3" class="govcy-character-count" data-maxwords="150">
            <div class="govcy-character-remaining-counter">You have <span></span> words remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> words more</div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="in-error">Label</label></h1>
        <p id="in-error-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input id="in-error" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in-error-error">
    </div>
</form>

<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="in-error1">Label</label>
        <p id="in-error-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input id="in-error1" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in-error-error1">
    </div>
</form>

<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="input-err1">What is your job description?</label>
        <p id="job-description-input-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Enter a valid Job description
        </p>
        <textarea id="input-err1" class="govcy-text-area govcy-text-area-error" aria-describedby="job-description-input-error1" rows="5"></textarea>
    </div>
</form>

<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="sort-err1">Sort by</label>
        <span id="sort-err-hint1" class="govcy-hint">Will sort results accordingly</span>
        <p id="sort-err-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Please select valid options
        </p>
        <select class="govcy-select govcy-select-error" id="sort-err1" name="sort-err1" aria-describedby="sort-err-hint1 sort-err-error1">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>

<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="option6-error">
        <legend class="govcy-legend">Do you wish to continue?</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="option6-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option6" id="option6-yes">
                <label class="govcy-label" for="option6-yes">Yes</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option6" id="option6-no">
                <label class="govcy-label" for="option6-no">No</label>
            </div>
        </div>
    </fieldset>
</form>

<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="option7-error">
        <legend class="govcy-legend">Do you wish to continue?</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="option7-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-radio govcy-d-sm-inline-block">
                <input class="govcy-radio-input" type="radio" name="option7" id="option7-yes">
                <label class="govcy-label" for="option7-yes">Yes</label>
            </div>
            <div class="govcy-radio govcy-d-sm-inline-block">
                <input class="govcy-radio-input" type="radio" name="option7" id="option7-no">
                <label class="govcy-label" for="option7-no">No</label>
            </div>
        </div>
    </fieldset>
</form>

<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-simple-error-email" name="collapseGroupsimple-error" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-simple-error-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroupsimple-error" type="radio" id="option6-simple-error-emailDif" value="emailDif" data-aria-controls="email-simple-error-different" checked/>
                <label class="govcy-label" for="option6-simple-error-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-error govcy-pl-4 govcy-ml-5 govcy-radio__conditional" id="email-simple-error-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple-error-1">Perosnal Email Address</label>
                    <span id="in4-simple-error-hint-1" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4-simple-error-1" type="text" class="govcy-text-input" aria-describedby="in4-simple-error-hint-1" value="test@email.com"/>
                </div>
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple-error">Work Email Address</label>
                    <span id="in4-simple-error-hint" class="govcy-hint">We'll only use this for applying</span>
                    <p id="in4-simple-error-error-msg" class="govcy-input-error-msg">
                        <span class="govcy-visually-hidden-error">Error:</span>
                        Enter email address
                    </p>
                    <input id="in4-simple-error" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in4-simple-error-hint in4-simple-error-error-msg"/>
                </div>
            </div>
        </div>
    </fieldset>
</form>

<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="file5">Upload a file</label>
        <span id="file5-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <p id="file5-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input class="govcy-file-upload" type="file" id="file5" name="file5" aria-describedby="file5-hint file5-error">
    </div>
</form>

<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="appointment-err-date1">Appointment Date</label>
        <span id="appointment-err-date-hint1" class="govcy-hint">For example, 13/8/2007</span>
        <p id="appointment-err-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Appointment Date must include a year
        </p>
        <div class="govcy-date-picker">
            <input type="text" class="govcy-text-input govcy-text-input-error" 
                id="appointment-err-date1"
                name="appointment-err-date1"
                aria-describedby="appointment-err-date-hint1 appointment-err-error1"/>
        </div>
    </div>
</form>

<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date-err1-hint date-err1-error">
        <legend class="govcy-legend">Date of birth</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <span class="govcy-hint" id="date-err1-hint">For example, 12 11 2007</span>
            <p id="date-err1-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_err1">Day</label>
                    <input id="day_err1" class="govcy-text-input govcy-text-input-char_3 govcy-text-input-error" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-day">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_err1">Month</label>
                    <select id="month_err1" class="govcy-select govcy-select-error" autocomplete="bday-month">
                        <option value="" selected=""></option>
                        <option value="1">1 - January</option>
                        <option value="2">2 - February</option>
                        <option value="3">3 - March</option>
                        <option value="4">4 - April</option>
                        <option value="5">5 - May</option>
                        <option value="6">6 - June</option>
                        <option value="7">7 - July</option>
                        <option value="8">8 - August</option>
                        <option value="9">9 - September</option>
                        <option value="10">10 - October</option>
                        <option value="11">11 - November</option>
                        <option value="12">12 - December</option>
                    </select>
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_err1">Year</label>
                    <input id="year_err1" class="govcy-text-input govcy-text-input-char_6 govcy-text-input-error" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-year">
                </div>
            </div>
        </div>
    </fieldset>
</form>

<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" aria-describedby="check-er-input-error1">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="check-er-input-error1" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check-er-checkbox-group1" type="checkbox" id="check-er-option10">
                <label class="govcy-label" for="check-er-option10">Option 1</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check-er-checkbox-group1" type="checkbox" id="check-er-option11">
                <label class="govcy-label" for="check-er-option11">Option 2</label>
            </div>
        </div>
    </fieldset>
</form>

<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
    <label class="govcy-label govcy-label-primary" for="input3">Enter a job description</label>
        <p id="job-description-input-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Job description must be 150 characters or less
        </p>
        <textarea id="input3" class="govcy-text-area govcy-text-area-error" aria-describedby="govcy-hint-hint3 job-description-input-error" rows="5">A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format. A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format. A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format.
        </textarea>
        <div  id="govcy-hint-hint3" class="govcy-character-count" data-maxwords="150">
            <div class="govcy-character-remaining-counter">You have <span></span> words remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> words more</div>
        </div>
    </div>
</form>
```
### Allow users to continue
There may be cases where you would allow users to continue with the service, even if there are errors on a specific section. This may be helpful in cases where users do not have all the information needed to complete the service at the time, but they can still complete other parts of the service.

In such a case you should still use the error summary and error messages components, but use the [allow users to continue error summary variant](../error_summary/#allow-users-to-continue).

## Errors content
### Be clear and concise
Describe what has happened and tell them how to fix it. The message must be in plain English, use positive language and get to the point.

Do not use:

- technical jargon like ‘form post error’, ‘unspecified error’ and ‘error 0x0000000643’
- words like ‘forbidden’, ‘illegal’, ‘you forgot’ and ‘prohibited’
- ‘please’ because it implies a choice
- ‘sorry’ because it does not help fix the problem
- ‘valid’ and ‘invalid’ because they do not add anything to the message
- humourous, informal language like ‘oops’

Do not give an example in the error message if there is an example on the screen. For example, if you are asking for a Date and include ‘13/8/2007’ as hint text, do not include an example in the error message.

Above all, aim for clarity.

Read the message out loud to see if it sounds like something you would say.
### Be consistent
Use the same message next to the field and in the error summary so they:

- look, sound and mean the same
- make sense out of context
- reduce the cognitive effort needed to understand what has happened

Use the question or form label in the error to provide context. For example, ‘Enter how many hours you work a week’ for ‘How many hours do you work a week?’
### Be specific
General errors are not helpful to everyone. They do not make sense out of context. Avoid messages like:

- ‘An error occurred’
- ‘Answer the question’
- ‘Select an option’
- ‘Fill in the field’
- ‘This field is required’

Different errors need different messages. For example, text fields may be:

- empty
- too long
- too short
- using characters that are not allowed
- in the wrong format

An error for a specific situation is more helpful. It will tell someone what has happened and how to fix it.
### Use instructions and descriptions
Some errors work better as instructions and some work better as descriptions. For example:

- ‘Enter your first name’ is clearer, more direct and natural than ‘First name must have an entry’
- ‘Enter a first name that is 35 characters or less’ is wordier, less direct and natural than ‘First name must be 35 characters or less’
- ‘Enter a date after 31 August 2017 for when you started the course’ is wordier, less direct and natural than ‘Date you started the course must be after 31 August 2017’

Use both instructions and descriptions, but use them consistently.  
For example, use an instruction for empty fields like ‘Enter your name’, but a description like ‘Name must be 35 characters or less’ for entries that are too long.
### Error texts language
The error messages should correspond to the language the user is viewing the website. If English is toggled, display errors in English, if Greek is toggled display the error messages in Greek.

For this reason the error messages should manually be inserted in both languages.

### Component text
Use the following patterns for error messages depending on the scenario:

#### Checkboxes

| Scenario                                                                | English                                                                                                                                                                                                  | Greek                                                                                                                                                                                                      |
| ----------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **If nothing is selected and the question has options in it**           | `Select if [whatever it is]`<br><br>Example: `Select if you are a Cypriot or a citizen of a different country`.                                                                                          | `Επιλέξτε αν [ό,τι κι αν είναι]`<br><br>Example: `Επιλέξτε αν είστε Κύπριος ή πολίτης διαφορετικής χώρας`                                                                                                  |
| **If nothing is selected and the question does not have options in it** | `Select [whatever it is]`<br><br>Example: `Select your nationality or nationalities`                                                                                                                     | `Επιλέξτε [ό, τι κι αν είναι]`<br><br>Example: `Επιλέξτε την εθνικότητα ή τις εθνικότητες σας`                                                                                                             |
| **If users check both a ‘none’ checkbox and another checkbox**          | `Select [option label text] or select “[none of the above label text]”`<br><br>Example: `Select countries you will be travelling to, or select “No, I will not be travelling to any of these countries”` | `Επιλέξτε [ετικέτα επιλογής] ή επιλέξτε ‘[καμία από τις παραπάνω ετικέτες]’`<br><br>Example: `Επιλέξτε τις χώρες στις οποίες θα ταξιδέψετε ή επιλέξτε “Όχι, δεν θα ταξιδεύω σε καμία από αυτές τις χώρες”` |

{.govcy-table}

#### Text input or textarea

| Scenario | English | Greek |
| ---- | ---- | ---- |
| **If the input is empty** | `Enter [whatever it is]`<br><br>Example: `Enter your first name`. | `Εισαγάγετε [ό,τι κι αν είναι]`<br><br>Example: `Εισαγάγετε το όνομά σας` |
| **If the input is too long** | `[whatever it is] must be [number] characters or less`<br><br>Example: `Address line 1 must be 35 characters or less` | `[ό,τι κι αν είναι] πρέπει να είναι [αριθμός] χαρακτήρες ή λιγότεροι`<br><br>Example: `Η γραμμή διεύθυνσης 1 πρέπει να αποτελείται από 35 χαρακτήρες ή λιγότερους` |
| **If the input is too short** | `[whatever it is] must be [number] characters or more`<br><br>Example: `Full name must be 2 characters or more` | `[ό,τι κι αν είναι] πρέπει να είναι [αριθμός] χαρακτήρες ή περισσότεροι`<br><br>Example: `Το πλήρες όνομα πρέπει να αποτελείται από 2 χαρακτήρες ή περισσότερους` |
| **If the input has both a minimum and maximum length** | `[whatever it is] must be between [number] and [number] characters`<br><br>Example: `Last name must be between 2 and 35 characters` | `[ό,τι κι αν είναι] πρέπει να είναι μεταξύ [number] και [number] χαρακτήρες`<br><br>Example: `Το επώνυμο πρέπει να είναι από 2 έως 35 χαρακτήρες` |
| **If the input uses characters that are not allowed and you know what the characters are** | `[whatever it is] must not include [characters]`<br><br>Example: `Town or city must not include è and €` | `[ό,τι κι αν είναι] δεν πρέπει να περιλαμβάνει [χαρακτήρες]`<br><br>Example: `Η πόλη ή το χωριό δεν πρέπει να περιλαμβάνει è και €` |
| **If the input uses characters that are not allowed and you do not know what the characters are**<br><br>Note: Support all the characters the user might need to enter, including numbers and symbols. | `[whatever it is] must only include [list of allowed characters]`<br><br>Example: `Full name must only include letters a to z, and special characters such as hyphens, spaces and apostrophes` | `[ό,τι κι αν είναι] πρέπει να περιλαμβάνει μόνο [λίστα από χαρακτήρες που επιτρέπονται]`<br><br>Example: `Το πλήρες όνομα πρέπει να περιλαμβάνει μόνο γράμματα από α έως ω και ειδικούς χαρακτήρες όπως παύλες, κενά και αποστρόφους` |

{.govcy-table}

#### Numeric text input

| Scenario                                                                                                                                                                                   | English                                                                                                                                               | Greek                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **If the input is not a number**<br><br>Note: If the input requires a decimal, use a decimal in the example. If the input allows both whole numbers and decimals, use both in the example. | `[whatever it is] must be a number [optional example]`<br><br>Example: `Hours worked a week must be a number, like 30`                                | `[ό,τι κι αν είναι] πρέπει να είναι αριθμός [προαιρετικό παράδειγμα]`<br><br>Example: `Οι ώρες εργασίας την εβδομάδα πρέπει να είναι ένας αριθμός, όπως 30`                         |
| **If the input is not a whole number**                                                                                                                                                     | `[whatever it is] must be a whole number [optional example]`<br><br>Example: `Hours worked a week must be a whole number, like 30`                    | `[ό,τι κι αν είναι] πρέπει να είναι ακέραιος αριθμός [προαιρετικό παράδειγμα]`<br><br>Example: `Οι ώρες εργασίας την εβδομάδα πρέπει να είναι ακέραιος αριθμός, όπως 30`            |
| **If the number is too low**                                                                                                                                                               | `[whatever it is] must be [lowest] or more`<br><br>Example: `Hours worked a week must be 16 or more`                                                  | `[ό,τι κι αν είναι] πρέπει να είναι [το λιγότερο] ή περισσότερο`<br><br>Example: `Οι ώρες εργασίας την εβδομάδα πρέπει να είναι 16 ή περισσότερες`                                  |
| **If the number is too high**                                                                                                                                                              | `[whatever it is] must be [highest] or fewer`<br><br>Example: `Hours worked a week must be 99 or fewer`                                               | `[ό,τι κι αν είναι] πρέπει να είναι [το υψηλότερο] ή λιγότερο`<br><br>Example: `Οι ώρες εργασίας την εβδομάδα πρέπει να είναι 99 ή λιγότερες`                                       |
| **If the input must be between 2 numbers**                                                                                                                                                 | `[whatever it is] must be between [lowest] and [highest]`<br><br>Example: `Hours worked a week must be between 16 and 99`                             | `[ό,τι κι αν είναι] πρέπει να είναι μεταξύ [χαμηλότερο] και [υψηλότερο]`<br><br>Example: `Οι ώρες εργασίας την εβδομάδα πρέπει να είναι μεταξύ 16 και 99`                           |
| **If the input is an amount of money that needs decimals**                                                                                                                                 | `[whatever it is] must include cents, like [xxx,xx] or [yyy,yy]`<br><br>Example: `How much you earn a week must include pence, like 123,45 or 156,00` | `[ό,τι κι αν είναι] πρέπει να περιλαμβάνει λεπτά, όπως [xxx,xx] ή [yyy,yy]`<br><br>Example: `Το ποσό που κερδίζετε την εβδομάδα πρέπει να περιλαμβάνει λεπτά, όπως 123,45 ή 156,00` |
| **If the input is an amount of money that must not have decimals**                                                                                                                         | `[whatever it is] must not include cents, like [xxx] or [yyy]`<br><br>Example: `How much you earn a week must not include cents, like 123 or 156`     | `[ό,τι κι αν είναι] δεν πρέπει να περιλαμβάνει λεπτά, όπως [xxx] ή [yyy]`<br><br>Example: `Το ποσό που κερδίζετε την εβδομάδα δεν πρέπει να περιλαμβάνει λεπτά, όπως 123 ή 156`     |

{.govcy-table}

#### Email address

| Scenario | English | Greek |
| ---- | ---- | ---- |
| **If the email address is not in the correct format and there is no example** | `Enter an email address in the correct format, like name@example.com` | `Εισαγάγετε μια διεύθυνση ηλεκτρονικού ταχυδρομείου στη σωστή μορφή, όπως name@example.com` |
| **If the email address is not in the correct format and there is an example** | `Enter an email address in the correct format` | `Εισαγάγετε μια διεύθυνση ηλεκτρονικού ταχυδρομείου στη σωστή μορφή` |

{.govcy-table}

#### Bank details

| Scenario | English | Greek |
| ---- | ---- | ---- |
| **If the IBAN is empty** | `Enter an IBAN` | `Εισαγάγετε ένα IBAN` |
| **If the IBAN entered has an error** | `Enter a valid IBAN` | `Εισάγετε έγκυρο IBAN` |

{.govcy-table}

#### Radios

| Scenario | English | Greek |
| ---- | ---- | ---- |
| **If it’s a ‘yes’ or ‘no’ question** | `Select yes if [whatever it is is true]`<br><br>Example: `Select yes if Sarah normally lives with you` | `Επιλέξτε ναι εάν [ό,τι και αν είναι αληθές]`<br><br>Example: `Επιλέξτε ναι εάν η Σάρα ζει μαζί σας` |
| **If there are two options which are not ‘yes’ and ‘no’** | `Select if [whatever it is]`<br><br>Example: `Select if you are employed or self-employed` | `Επιλέξτε εάν [ό,τι κι αν είναι]`<br><br>Example: `Επιλέξτε εάν είστε μισθωτός ή αυτοτελώς εργαζομενος` |
| **If there are more than two options** | `Select [whatever it is]`<br><br>Example: `Select the day of the week you pay your rent` | `Επιλέξτε [ό,τι κι αν είναι]`<br><br>Example: `Επιλέξτε την ημέρα της εβδομάδας που πληρώνετε το ενοίκιο σας` |

{.govcy-table}

#### File upload

| Scenario | English | Greek |
| ---- | ---- | ---- |
| **If no file has been selected** | `Select a [whatever they need to select]`<br><br>Example: `Select a document` | `Επιλέξτε ένα [ό,τι θέλουν να επιλέξουν]`<br><br>Example: `Επιλέξτε ένα έγγραφο` |
| **If the file is the wrong file type** | `The selected file must be a [list of file types]`<br><br>Example: `The selected file must be a CSV or ODS’` or `The selected file must be a JPG, BMP, PNG, TIF or PDF` | `Το επιλεγμένο αρχείο πρέπει να είναι μια [λίστα τύπων αρχείων]`<br><br>Example: `Το επιλεγμένο αρχείο πρέπει να είναι CSV ή ODS` or `Το επιλεγμένο αρχείο πρέπει να είναι JPG, BMP, PNG, TIF ή PDF` |
| **If the file is too big** | `The selected file must be smaller than [largest file size]`<br><br>Example: `The selected file must be smaller than 2MB` | `Το επιλεγμένο αρχείο πρέπει να είναι μικρότερο από το [μεγαλύτερο μέγεθος αρχείου]`<br><br>Example: `Το επιλεγμένο αρχείο πρέπει να είναι μικρότερο από 2MB` |
| **If the file is empty** | `The selected file is empty` | `Το επιλεγμένο αρχείο είναι κενό` |
| **If there was a problem and the file was not uploaded** | `The selected file could not be uploaded – try again` | `Δεν ήταν δυνατή η μεταφόρτωση του επιλεγμένου αρχείου - δοκιμάστε ξανά` |
| **If there is a limit on how many files the user can select** | `You can only select up to [highest number] files at the same time`<br><br>Example: `You can only select up to 10 files at the same time` | `Μπορείτε να επιλέξετε μόνο έως [με τον υψηλότερο αριθμό] αρχεία ταυτόχρονα`<br><br>Example: `Μπορείτε να επιλέξετε μόνο έως 10 αρχεία ταυτόχρονα` |
| **If the file is not in a template that must be used or the template has been changed** | `The selected file must use the template` | `Το επιλεγμένο αρχείο πρέπει να χρησιμοποιεί το πρότυπο` |

{.govcy-table}

#### Date input

| Scenario | English | Greek |
| ---- | ---- | ---- |
| **If nothing is entered**<br><br>Note: Highlight the date input as a whole. | `Enter [whatever it is]`<br><br>Example: `Enter your date of birth` | `Εισάγετε [ό, τι κι αν είναι]`<br><br>Example: `Εισάγετε την ημερομηνία γέννησής σας` |
| **If the date is incomplete**<br><br>Note: Highlight the day, month or year field where the information is missing or incomplete. If more than one field is missing information, highlight the fields the user needs to fill in. | `[whatever it is] must include a [whatever is missing]`<br><br>Example: `Date of birth must include a month` or `Date of birth must include a day and month` or `Year must include 4 numbers` | `[ό,τι κι αν είναι] πρέπει να περιλαμβάνει [ό,τι λείπει]`<br><br>Example: `Η ημερομηνία γέννησης πρέπει να περιλαμβάνει ένα μήνα` or ` ημερομηνία γέννησης πρέπει να περιλαμβάνει μια ημέρα και μήνα` or `Το έτος πρέπει να είναι 4 ψηφία` |
| **If the date entered cannot be correct**<br><br>For example, ‘13’ in the month field cannot be correct.<br><br>Highlight the day, month or year field with the incorrect information. Or highlight the date as a whole if there’s incorrect information in more than one field, or it’s not clear which field is incorrect. | `[Whatever it is] must be a real date`<br><br>Example: `Date of birth must be a real date` | `[Ό,τι κι αν είναι] πρέπει να είναι μια πραγματική ημερομηνία`<br><br>Example: `Η ημερομηνία γέννησης πρέπει να είναι πραγματική ημερομηνία` |
| **If the date is in the future when it needs to be in the past**<br><br>Highlight the date input as a whole. | `[whatever it is] must be in the past`<br><br>Example: `Date of birth must be in the past` | `[ό,τι κι αν είναι] πρέπει να είναι στο παρελθόν`<br><br>Example: `Η ημερομηνία γέννησης πρέπει να είναι στο παρελθόν` |
| **If the date is in the future when it needs to be today or in the past**<br><br>Highlight the date input as a whole. | `[whatever it is] must be today or in the past`<br><br>Example: `Date of birth must be today or in the past` | `[ό,τι κι αν είναι] πρέπει να είναι σήμερα ή στο παρελθόν`<br><br>Example: `Η ημερομηνία γέννησης πρέπει να είναι σήμερα ή στο παρελθόν` |
| **If the date is in the past when it needs to be in the future**<br><br>Highlight the date input as a whole. | `[whatever it is] must be in the future`<br><br>Example: `The date your course ends must be in the future` | `[ό,τι κι αν είναι] πρέπει να είναι στο μέλλον`<br><br>`Η ημερομηνία λήξης του μαθήματος πρέπει να είναι στο μέλλον` |
| **If the date is in the past when it needs to be today or in the future**<br><br>Highlight the date input as a whole. | `[whatever it is] must be today or in the future`<br><br>Example: `The date your course ends must be today or in the future` | `[ό,τι κι αν είναι] πρέπει να είναι σήμερα ή στο μέλλον`<br><br>Example: `Η ημερομηνία λήξης του μαθήματος πρέπει να είναι σήμερα ή στο μέλλον` |
| **If the date must be the same as or after another date**<br><br>Highlight the date input as a whole. | `[whatever it is] must be the same as or after [date and optional description]`<br><br>Example: `The date your course ends must be the same as or after 1 September 2017 when you started the course` | `[ό,τι κι αν είναι] πρέπει να είναι ίδιο ή μετά από [ημερομηνία και προαιρετική περιγραφή]`<br><br>Example: `Η ημερομηνία λήξης του μαθήματος πρέπει να είναι η ίδια ή μετά την 1η Σεπτεμβρίου 2017 όταν ξεκινήσατε το μάθημα` |
| **If the date must be after another date**<br><br>Highlight the date input as a whole. | `[whatever it is] must be after [date and optional description]`<br><br>Example: `The day your course ends must be after 1 September 2017` | `[ό,τι κι αν είναι] πρέπει να είναι μετά την [ημερομηνία και προαιρετική περιγραφή]`<br><br>Example: `Η ημέρα που τελειώνει το μάθημά σας πρέπει να είναι μετά την 1η Σεπτεμβρίου 2017` |
| **If the date must be the same as or before another date**<br><br>Highlight the date input as a whole. | `[whatever it is] must be the same as or before [date and optional description]`<br><br>Example: `The date of Gordon’s last exam must be the same as or before 31 August 2017 when they left school` | `[όποιο και αν είναι] πρέπει να είναι το ίδιο ή πριν από [ημερομηνία και προαιρετική περιγραφή]`<br><br>Example: `Η ημερομηνία της τελευταίας εξέτασης του Gordon πρέπει να είναι η ίδια ή πριν από τις 31 Αυγούστου 2017 όταν έφυγε από το σχολείο` |
| **If the date must be before another date**<br><br>Highlight the date input as a whole. | `[whatever it is] must be before [date and optional description]`<br><br>Example: `The date of Gordon’s last exam must be the same as or before 31 August 2017` | `[ό,τι κι αν είναι] πρέπει να είναι πριν από [ημερομηνία και προαιρετική περιγραφή]`<br><br>Example: `Η ημερομηνία της τελευταίας εξέτασης του Gordon πρέπει να είναι πριν από τις 31 Αυγούστου 2017`  |
| **If the date must be between two dates**<br><br>Highlight the date input as a whole. | `[whatever it is] must be between [date] and [date and optional description]`<br><br>Example: `The date your contract started must be between 1 September 2017 and 30 September 2017 when you were self-employed` | `[όποια και αν είναι] πρέπει να είναι μεταξύ [ημερομηνία] και [ημερομηνία και προαιρετική περιγραφή]`<br><br>Example: `Η ημερομηνία έναρξης της σύμβασής σας πρέπει να είναι μεταξύ 1ης Σεπτεμβρίου 2017 και 30 Σεπτεμβρίου 2017 όταν ήσασταν αυτοαπασχολούμενος` |

{.govcy-table}

#### Select

| Scenario | English | Greek |
| ---- | ---- | ---- |
| **If nothing is selected** | `Select [whatever it is]`<br><br>Example: `Select a location` | `Επιλέξτε [ό, τι κι αν είναι]`<br><br>Example: `Επιλέξτε την τοποθεσία` |

{.govcy-table}

## Accessibility
Make sure:
- you use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `input` element, with the id of the error message. 
- not to clear any form fields when adding error messages
- you follow the instructions for [errors content](#errors-content)
