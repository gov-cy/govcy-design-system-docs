---
"title" : "Date input"
date: 2022-02-01 00:01:01Z
description: "Let users enter a memorable date or one they can easily look up."
---

Use the date input component to help users enter a memorable date or one they can easily look up.

## When to use this component
Use the date input component when you’re asking users for a date they’ll already know, or can look up without using a calendar.

## When not to use this component
Do not use the date input component if users are unlikely to know the exact date of the event you’re asking about.

If you are asking for a date that is in the near future or recent past, for example when scheduling an appointment, you can use the [date picker](../date_picker) component.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

The date input component consists of three grouped fields that invite users to enter a day, a month, and a year. This is the easiest way for users to enter dates they know well.

The 3 date fields are grouped together with a `<legend>` that describes them, as shown in the examples on this page. This is usually a question, like ‘What is your date of birth?’.

Make sure that any example dates you use in hint text are valid for the question being asked. As a best practice you should allow both single-digit and double-digit values for day and month (for example `01` or `1`).

Never automatically tab users between the fields of the date input because this can be confusing and may clash with normal keyboard controls.

### Single question page
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date1-hint">
        <legend class="govcy-legend"><h1>Date input</h1></legend>
        <div class="govcy-form-control">
            <span class="govcy-hint" id="date1-hint">For example, 12 11 2007</span>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_1">Day</label>
                    <input id="day_1" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_1">Month</label>
                    <select id="month_1" class="govcy-select">
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
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_1">Year</label>
                    <input id="year_1" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date1-hint">
        <legend class="govcy-legend"><h1>Date input</h1></legend>
        <div class="govcy-form-control">
            <span class="govcy-hint" id="date1-hint">For example, 12 11 2007</span>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_1">Day</label>
                    <input id="day_1" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_1">Month</label>
                    <select id="month_1" class="govcy-select">
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
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_1">Year</label>
                    <input id="year_1" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
            </div>
        </div>
    </fieldset>
</form>
```

### More than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<legend>` as the page heading. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date2-hint">
        <legend class="govcy-legend">Date input</legend>
        <div class="govcy-form-control">
            <span class="govcy-hint" id="date2-hint">For example, 12 11 2007</span>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_2">Day</label>
                    <input id="day_2" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_2">Month</label>
                    <select id="month_2" class="govcy-select">
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
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_2">Year</label>
                    <input id="year_2" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date2-hint">
        <legend class="govcy-legend">Date input</legend>
        <div class="govcy-form-control">
            <span class="govcy-hint" id="date2-hint">For example, 12 11 2007</span>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_2">Day</label>
                    <input id="day_2" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_2">Month</label>
                    <select id="month_2" class="govcy-select">
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
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_2">Year</label>
                    <input id="year_2" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric">
                </div>
            </div>
        </div>
    </fieldset>
</form>
```

### Autocomplete for a date of birth
Use the `autocomplete` attribute on the date input component when you’re asking for a date of birth. This lets browsers autofill the information on a user’s behalf if they’ve entered it previously.

To do this, set the `autocomplete` attribute on the 3 fields to `bday-day`, `bday-month` and `bday-year`. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date3-hint">
        <legend class="govcy-legend">Date of birth</legend>
        <div class="govcy-form-control">
            <span class="govcy-hint" id="date3-hint">For example, 12 11 2007</span>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_3">Day</label>
                    <input id="day_3" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-day">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_3">Month</label>
                    <select id="month_3" class="govcy-select" autocomplete="bday-month">
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
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_3">Year</label>
                    <input id="year_3" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-year">
                </div>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date3-hint">
        <legend class="govcy-legend">Date of birth</legend>
        <div class="govcy-form-control">
            <span class="govcy-hint" id="date3-hint">For example, 12 11 2007</span>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_3">Day</label>
                    <input id="day_3" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-day">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_3">Month</label>
                    <select id="month_3" class="govcy-select" autocomplete="bday-month">
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
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_3">Year</label>
                    <input id="year_3" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-year">
                </div>
            </div>
        </div>
    </fieldset>
</form>
```
### Component text
Use the following text:

| Text | English | Greek |
| ---- | ---- | ---- |
| **Day label** | Day | Μέρα |
| **Month label** | Month | Μήνας |
| **Year label** | Year | Χρόνος |
| **Date of birth legend** | Date of birth | Ημερομηνία γεννήσεως |
| **Hint text** | For example, 13 8 2007 | Για παράδειγμα, 13 8 2007 |
| **Months** | January<br> February<br> March<br> April<br> May<br> June<br> July<br> August<br> September<br> October<br> November<br> December | Ιανουάριος<br> Φεβρουάριος<br> Μάρτιος<br> Απρίλιος<br> Μάϊος<br> Ιούνιος<br> Ιούλιος<br> Αύγουστος<br> Σεπτέμβριος<br> Οκτώβριος<br> Νοέμβριος<br> Δεκέμβριος |


{.govcy-table}

### Order of elements inside the component
Place the elements inside the component in the following order.

1. Fieldset
    1. Legend
    1. Form control
        1. Hint
        2. Error message
        3. Inputs

### Error messages
Make sure to follow the instructions for [error messages](../error_message) and [error summary](../error_summary) when validating user input.

If you’re highlighting the whole date, style all the fields like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
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
</div>

*HTML code*
```html
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
```

If you’re highlighting part of the date - either the day, month or year - only style the fields that have an error. The error message must say which field has an error, like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date-err2-hint date-err2-error">
        <legend class="govcy-legend">Date of birth</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <span class="govcy-hint" id="date-err2-hint">For example, 12 11 2007</span>
            <p id="date-err2-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Date of birth must include a month and a year
            </p>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_err2">Day</label>
                    <input id="day_err2" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-day">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_err2">Month</label>
                    <select id="month_err2" class="govcy-select govcy-select-error" autocomplete="bday-month">
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
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" role="group" aria-describedby="date-err2-hint date-err2-error">
        <legend class="govcy-legend">Date of birth</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <span class="govcy-hint" id="date-err2-hint">For example, 12 11 2007</span>
            <p id="date-err2-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Date of birth must include a month and a year
            </p>
            <div class="govcy-d-flex govcy-flex-wrap">
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_err2">Day</label>
                    <input id="day_err2" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric" autocomplete="bday-day">
                </div>
                <div class="govcy-d-block govcy-mr-3">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_err2">Month</label>
                    <select id="month_err2" class="govcy-select govcy-select-error" autocomplete="bday-month">
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
## Accessibility
Make sure:
- you use the `autocomplete` attribute for birth dates
- you add a `legend` for your `fieldset`
- you associate the `label` elements with the input they relate to, using the `for` attribute
- when using a hints, add  `aria-describedby` on the `fieldset` element, with the id of the hint element 
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `fieldset` element, with the id of the error message. 
- you do not disable copy and paste