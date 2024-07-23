---
"title" : "Error Summary"
date: 2022-02-01 00:01:01Z
description: "Use this component at the top of a page to summarise any errors a user has made."
---
Use this component at the top of a page to summarise any errors a user has made.

When there is a validation error, you must show both an error summary and an error message next to each field that contains an error.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p class="govcy-mb-0">
        <a href="#">Enter your full name</a>
        <a href="#">Social insurance number should be 16 digit long</a>
    </p>
</div>
</div>

*HTML code*
```html
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p class="govcy-mb-0">
        <a href="#">Enter your full name</a>
        <a href="#">Social insurance number should be 16 digit long</a>
    </p>
</div>
```

## When to use this component
Always show an error summary when there is a validation error or other violation that the user can fix, even if there’s only one.

## When not to use this component
Do not use error messages to tell a user that they are not eligible or do not have permission to do something or to tell them about a lack of capacity or other problem the user cannot fix - because the problem is with the service rather than with the information the user has provided.

Instead, take the user to a page that explains the problem (for example, telling them why they’re not eligible) and provides useful information about what to do next.

There are separate patterns for:

- [‘there is a problem with the service’ pages](../../patterns/there-is-a-problem/)
- [‘page not found’ pages](../../patterns/page-not-found-pages/)
- [‘service unavailable’ pages](../../patterns/service-unavailable-pages/)

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

When showing the error summary, use [linking to an element on the same page](../../styles/typography/#linking-to-an-element-on-the-same-page) to move keyboard focus to the error summary heading. This will draw the attention to the users that there is an a problem. Sighted users will be navigated to the error summary area on the page, and screen readers will read out that there is a problem. 

Here are some sample pages showing the error summary when the user clicks the ‘continue’ button. 
- [Server side rendering example (opens in new tab)](../../samples/template-heading-input/){rel="noreferrer noopener" target="_blank"}. This example redirects the user to a different page that shows the error, this was done for demonstration purposes, in a real implementation, the errors should appear in the same page.
- [Single page application example (opens in new tab)](../../samples/template-heading-input-js/){rel="noreferrer noopener" target="_blank"}.

You must also:

- include the heading ‘There is a problem’ in English and ‘Υπάρχει πρόβλημα’ in Greek
- if there is a validation error on a field, use use [linking to an element on the same page](../../styles/typography/#linking-to-an-element-on-the-same-page) to link each error to the fields that have validation errors
    - make sure the error messages in the error summary are worded the same as those which appear next to the fields with errors
- if there is a business rule, link each error to the ‘change’ link or relevant page where the user can correct the violation. 

### When to check for errors

Check for errors on each page or question, after the users distinctly indicate that they have finished with the current page, for example when clicking the “continue” button. This gives the user the opportunity to review their answer, or get out of the input’s focus and not get flooded with red error messages which can be overwhelming.

### Where to put the error summary

Put the error summary at the top of the [main](../../getting-started/page-template/#sections) (`<main>`) container, right above the `<h1>`. If your page includes breadcrumbs or a back link, place it below these.

### Linking from the error summary to each answer
You must link the errors in the error summary to the answer they relate to.

For questions that require a user to answer using a single field, like a file upload, select, textarea, text input or character count, link to the field.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p>
        <a href="#in3">Enter your full name</a>
    </p>
</div>
<div class="govcy-row">
    <div action="" class="govcy-form" novalidate="">
        <div class="govcy-form-control govcy-form-control-error">
            <h1><label class="govcy-label govcy-label-primary" for="in3">Fullname</label></h1>
            <p id="in3-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Enter your full name
            </p>
            <input id="in3" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in3-error">
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p>
        <a href="#in3">Enter your full name</a>
    </p>
</div>
<div class="govcy-row">
    <form action="" class="govcy-form" novalidate="">
        <div class="govcy-form-control govcy-form-control-error">
            <h1><label class="govcy-label govcy-label-primary" for="in3">Fullname</label></h1>
            <p id="in3-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Enter your full name
            </p>
            <input id="in3" type="text" class="govcy-text-input govcy-text-input-error" aria-describedby="in3-error">
        </div>
    </form>
</div>
```
When a user has to enter their answer into multiple fields, such as the day, month and year fields in the date input component, link to the first field that contains an error.

If you do not know which field contains an error, link to the first field.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p>
        <a href="#year_err2">Date of birth must include a year</a>
    </p>
</div>
<div action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date-err2-hint date-err2-error">
        <legend class="govcy-legend"><h1>What is your date of birth?</h1></legend>
        <div class="govcy-form-control govcy-form-control-error">
            <span class="govcy-hint" id="date-err2-hint">For example, 12 11 2007</span>
            <p id="date-err2-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Date of birth must include a year
            </p>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_err2">Day</label>
                    <input id="day_err2" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-day">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_err2">Month</label>
                    <select id="month_err2" class="govcy-select" autocomplete="bday-month">
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
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_err2">Year</label>
                    <input id="year_err2" class="govcy-text-input govcy-text-input-char_6 govcy-text-input-error" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-year">
                </div>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p>
        <a href="#year_err2">Date of birth must include a year</a>
    </p>
</div>
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date-err2-hint date-err2-error">
        <legend class="govcy-legend"><h1>What is your date of birth?</h1></legend>
        <div class="govcy-form-control govcy-form-control-error">
            <span class="govcy-hint" id="date-err2-hint">For example, 12 11 2007</span>
            <p id="date-err2-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Date of birth must include a year
            </p>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_err2">Day</label>
                    <input id="day_err2" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-day">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_err2">Month</label>
                    <select id="month_err2" class="govcy-select" autocomplete="bday-month">
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
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_err2">Year</label>
                    <input id="year_err2" class="govcy-text-input govcy-text-input-char_6 govcy-text-input-error" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-year">
                </div>
            </div>
        </div>
    </fieldset>
</form>
```
For questions that require a user to select one or more options from a list using radios or checkboxes, link to the first radio or checkbox.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p>
        <a href="#check4-nationality">Select if you are Cypriot, from other European country, or citizen from another country</a>
    </p>
</div>
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="check4-fildset-hint check-er-input-error">
        <legend class="govcy-legend"><h1>What is your nationality?</h1></legend>
        <div class="govcy-form-control govcy-form-control-error">
	        <span class="govcy-hint" id="check4-fildset-hint">If you have dual nationality, select all options that are relevant to you. </span>
            <p id="check-er-input-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Select if you are Cypriot, from other European country, or citizen from another country
            </p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check4-checkbox-group" type="checkbox" id="check4-nationality">
                <label class="govcy-label" for="check4-nationality">Cypriot</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check4-checkbox-group" type="checkbox" id="check4-otherEurope">
                <label class="govcy-label" for="check4-otherEurope">Other European Union country</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check4-checkbox-group" type="checkbox" id="check4-anotherCountry" aria-describedby="check4-anotherCountry-hint">
                <label class="govcy-label" for="check4-anotherCountry">Citizen of another country</label>
                <span class="govcy-hint" id="check4-anotherCountry-hint">Check this if you do not have nationality from a country</span>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p>
        <a href="#check4-nationality">Select if you are Cypriot, from other European country, or citizen from another country</a>
    </p>
</div>
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="check4-fildset-hint check-er-input-error">
        <legend class="govcy-legend"><h1>What is your nationality?</h1></legend>
        <div class="govcy-form-control govcy-form-control-error">
	        <span class="govcy-hint" id="check4-fildset-hint">If you have dual nationality, select all options that are relevant to you. </span>
            <p id="check-er-input-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Select if you are Cypriot, from other European country, or citizen from another country
            </p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check4-checkbox-group" type="checkbox" id="check4-nationality">
                <label class="govcy-label" for="check4-nationality">Cypriot</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check4-checkbox-group" type="checkbox" id="check4-otherEurope">
                <label class="govcy-label" for="check4-otherEurope">Other European Union country</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check4-checkbox-group" type="checkbox" id="check4-anotherCountry" aria-describedby="check4-anotherCountry-hint">
                <label class="govcy-label" for="check4-anotherCountry">Citizen of another country</label>
                <span class="govcy-hint" id="check4-anotherCountry-hint">Check this if you do not have nationality from a country</span>
            </div>
        </div>
    </fieldset>
</form>
```

### Showing summary without error messages
There may be cases where you would show an error summary without showing error messages, for example on a [task list](../../patterns/task-list-page/#showing-errors) or a [check your answers](../../patterns/check_answers/#showing-errors) page. This might be helpful in cases where a business rule is violated, but an action by the user can correct the violation.

In such a case, the link for each error in the error summary, should link to the relevant page where the user can correct the violation.

*Example*
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p class="govcy-mb-0">
        <a href="#contact-details">Complete the section on your contact details</a>
        <a href="#medical-information">Complete the section on medical information</a>
    </p>
</div>

*HTML code*
```html
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p class="govcy-mb-0">
        <a href="#contact-details">Complete the section on your contact details</a>
        <a href="#medical-information">Complete the section on medical information</a>
    </p>
</div>
```

### Allow users to continue
There may be cases where you would allow users to continue with the service, even if there are errors on a specific section. This may be helpful in cases where users do not have all the information needed to complete the service at the time, but they can still complete other parts of the service.

In such a case you should still use the error summary and error messages components, but also provide them in the error summary with:
- a paragraph explaining that they can continue but will need to complete the section before final submission
- a link that would allow them to continue with other parts of the service 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p>
        <a href="#">Enter your full name</a>
        <a href="#">Social insurance number should be 16 digit long</a>
    </p>
    <p>You can continue with other sections of your application, but you will have to complete the missing information before you can submit.</p>
    <a href="#">Back to home page</a>
</div>
</div>

*HTML code*
```html
<div class="govcy-alert-error govcy-br-5 govcy-br-danger govcy-p-3">
    <h2>There is a problem</h2>
    <p>
        <a href="#">Enter your full name</a>
        <a href="#">Social insurance number should be 16 digit long</a>
    </p>
    <p>You can continue with other sections of your application, but you will have to complete the missing information before you can submit.</p>
    <a href="#">Back to home page</a>
</div>
```
### Component text
Use the following text in the heading:

- **English**: ‘There is a problem’ 
- **Greek**: ‘Υπάρχει πρόβλημα’

## Accessibility
Make sure:
- you link the error summary to where the user can correct the error
- you use the [error message component](../error_message) on validation errors
- when showing the error summary, to use [linking to an element on the same page](../../styles/typography/#linking-to-an-element-on-the-same-page) to move keyboard focus to the error summary heading.