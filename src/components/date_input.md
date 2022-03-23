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

The 3 date fields are grouped together with a `<label>` that describes them, as shown in the examples on this page. This is usually a question, like ‘What is your date of birth?’.

If you’re asking one question per page, you can set the contents of the `<label>` as the page heading. This is good practice as it means that users of screen readers will only hear the contents once.

Make sure that any example dates you use in [hint text](../../patterns/hint_text) are valid for the question being asked.

Never automatically tab users between the fields of the date input because this can be confusing and may clash with normal keyboard controls.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
    <div class="govcy-container">
        <form action="" class="govcy-form" novalidate>
            <fieldset class="govcy-fieldset">
                <div class="govcy-form-control">
                    <label class="govcy-label govcy-mb-1" for="">Date of birth</label>
                    <span class="govcy-hint govcy-mb-3">For emample, 12 11 2007</span>
                    <div class="govcy-d-flex">
                        <div class="govcy-d-block">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Day</label>
                            <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                        </div>
                        <div class="govcy-d-block govcy-ml-2">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Month</label>
                            <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                        </div>
                        <div class="govcy-d-block govcy-ml-2">
                            <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Year</label>
                            <input class="govcy-text-input govcy-text-input-char_6 govcy-p-3" placeholder="" maxlength="4" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
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
            <div class="govcy-form-control">
                <label class="govcy-label govcy-mb-1" for="">Date of birth</label>
                <span class="govcy-hint govcy-mb-3">For emample, 12 11 2007</span>
                <div class="govcy-d-flex">
                    <div class="govcy-d-block">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Day</label>
                        <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Month</label>
                        <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Year</label>
                        <input class="govcy-text-input govcy-text-input-char_6 govcy-p-3" placeholder="" maxlength="4" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                    </div>
                </div>
            </div>
        </fieldset>
    </form>
</div>
```

*Example with error message*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-container">
    <form action="" class="govcy-form" novalidate>
        <fieldset class="govcy-fieldset">
            <div class="govcy-form-control govcy-form-control-error">
                <label class="govcy-label govcy-mb-1" for="">Date of birth</label>
                <span class="govcy-visually-hidden-error">Error: </span>
                <span class="govcy-input-error-msg govcy-mb-3">There is an error</span>
                <div class="govcy-d-flex">
                    <div class="govcy-d-block">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Day</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Month</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Year</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_6 govcy-p-3" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
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
                <label class="govcy-label govcy-mb-1" for="">Date of birth</label>
                <span class="govcy-visually-hidden-error">Error: </span>
                <span class="govcy-input-error-msg govcy-mb-3">There is an error</span>
                <div class="govcy-d-flex">
                    <div class="govcy-d-block">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Day</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Month</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_3 govcy-p-2" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                    </div>
                    <div class="govcy-d-block govcy-ml-2">
                        <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="">Year</label>
                        <input class="govcy-text-input govcy-text-input-error govcy-text-input-char_6 govcy-p-3" placeholder="" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric">
                    </div>
                </div>
            </div>
        </fieldset>
    </form>
</div>
```