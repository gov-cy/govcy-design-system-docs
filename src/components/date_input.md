---
"title" : "Date input"
date: 2022-02-01 00:01:01Z
---

Use the date input component to help users enter a memorable date or one they can easily look up.

## When to use this component
Use the date input component when you’re asking users for a date they’ll already know, or can look up without using a calendar.

## When not to use this component
Do not use the date input component if users are unlikely to know the exact date of the event you’re asking about.

## How it works
The date input component consists of 3 fields to let users enter a day, month and year.

The 3 date fields are grouped together with a `<legend>` that describes them, as shown in the examples on this page. This is usually a question, like ‘What is your date of birth?’.

If you’re asking one question per page, you can set the contents of the `<legend>` as the page heading. This is good practice as it means that users of screen readers will only hear the contents once.

Make sure that any example dates you use in [hint text](../../patterns/hint_text) are valid for the question being asked. As a best practice you should allow both single-digit and double-digit values for day and month (for example `01` or `1`). 

Never automatically tab users between the fields of the date input because this can be confusing and may clash with normal keyboard controls.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
    <div class="govcy-container">
        <form action="" class="govcy-form" novalidate>
            <fieldset class="govcy-fieldset">
                <div class="govcy-form-control">
                    <legend class="govcy-legend govcy-mb-1">Date of birth</legend>
                    <span class="govcy-hint govcy-mb-3">For example, 13 8 2007</span>
                    <div class="govcy-d-flex">
                        <div class="govcy-d-block">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_1">Day</label>
                            <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" id="day_1" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                        </div>
                        <div class="govcy-d-block govcy-ml-2">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_1">Month</label>
                            <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" id="month_1" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                        </div>
                        <div class="govcy-d-block govcy-ml-2">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_1">Year</label>
                            <input class="govcy-text-input govcy-text-input-char_6 govcy-p-3" id="year_1" placeholder="" maxlength="4" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                        </div>
                    </div>
                </div>
            </fieldset>
        </form>
    </div>
</div>
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
    <div class="govcy-container">
        <form action="" class="govcy-form" novalidate>
            <fieldset class="govcy-fieldset">
                <div class="govcy-form-control">
                    <legend class="govcy-legend govcy-mb-1">Ημερομηνία γεννήσεως</legend>
                    <span class="govcy-hint govcy-mb-3">Για παράδειγμα, 13 8 2007</span>
                    <div class="govcy-d-flex">
                        <div class="govcy-d-block">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_2">Μέρα       </label>
                            <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" id="day_2" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                        </div>
                        <div class="govcy-d-block govcy-ml-2">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_2">Μήνας</label>
                            <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" id="month_2" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                        </div>
                        <div class="govcy-d-block govcy-ml-2">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_2">Χρόνος</label>
                            <input class="govcy-text-input govcy-text-input-char_6 govcy-p-3" id="year_2" placeholder="" maxlength="4" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                        </div>
                    </div>
                </div>
            </fieldset>
        </form>
    </div>
</div>  

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <div class="govcy-form-control">
            <legend class="govcy-legend govcy-mb-1">Date of birth</legend>
            <span class="govcy-hint govcy-mb-3">For example, 13 8 2007</span>
            <div class="govcy-d-flex">
                <div class="govcy-d-block">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_1">Day</label>
                    <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" id="day_1" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                </div>
                <div class="govcy-d-block govcy-ml-2">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_1">Month</label>
                    <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" id="month_1" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                </div>
                <div class="govcy-d-block govcy-ml-2">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_1">Year</label>
                    <input class="govcy-text-input govcy-text-input-char_6 govcy-p-3" id="year_1" placeholder="" maxlength="4" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                </div>
            </div>
        </div>
    </fieldset>
</form>
```

*Example with error message*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-container">
    <form action="" class="govcy-form" novalidate>
        <fieldset class="govcy-fieldset">
            <div class="govcy-form-control govcy-form-control-error">
                <legend class="govcy-legend govcy-mb-1">Date of birth</legend>
                <span class="govcy-visually-hidden-error">Error: </span>
                <p id="date_error_1" class="govcy-input-error-msg govcy-mb-3">There is an error</p>
                <div class="govcy-d-flex">
                    <div class="govcy-d-block">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_3">Day</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2" id="day_3" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" aria-describedby="date_error_1">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_3">Month</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2"  id="month_3" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" aria-describedby="date_error_1">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_3">Year</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_6 govcy-p-3" id="year_3" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" aria-describedby="date_error_1">
                    </div>
                </div>
            </div>
        </fieldset>
    </form>
</div>
</div>

*Sample HTML Code*

```html
<div class="govcy-container">
    <form action="" class="govcy-form" novalidate>
        <fieldset class="govcy-fieldset">
            <div class="govcy-form-control govcy-form-control-error">
                <legend class="govcy-legend govcy-mb-1">Date of birth</legend>
                <span class="govcy-visually-hidden-error">Error: </span>
                <p id="date_error_1" class="govcy-input-error-msg govcy-mb-3">There is an error</p>
                <div class="govcy-d-flex">
                    <div class="govcy-d-block">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_2">Day</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2" id="day_2" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" aria-describedby="date_error_1">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_2">Month</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2"  id="month_2" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" aria-describedby="date_error_1">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_2">Year</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_6 govcy-p-3" id="year_2" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" aria-describedby="date_error_1">
                    </div>
                </div>
            </div>
        </fieldset>
    </form>
</div>
```