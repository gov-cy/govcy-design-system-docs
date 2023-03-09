---
"title" : "Checkbox"
date: 2022-02-01 00:01:01Z
---
Let users select one or more options by using the checkboxes component.

## When to use this component
Use the checkboxes component when you need to help users:
- select multiple options from a list
- toggle a single option on or off

## When not to use this component
Do not use the checkboxes component if users can only choose one option from a selection. In this case, use the [radio](../radio) component.

## How it works

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control">
            <label class="govcy-checkbox">Option 1
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Option 2
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Option 3
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control">
            <label class="govcy-checkbox">Option 1
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Option 2
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Option 3
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
</form>
```

Always position checkboxes to the left of their labels. This makes them easier to find, especially for users of screen magnifiers.

Unlike with radios, users can select multiple options from a list of checkboxes. Do not assume that users will know how many options they can select based on the visual difference between radios and checkboxes alone.

If needed, add a [hint](../../patterns/hint_text) explaining this, for example, ‘Select all that apply’.

Prefer not to pre-select checkbox options as this makes it more likely that users will not realise they’ve missed a question or submit the wrong answer. 

Group radios together in a `<fieldset>` with a `<legend>` that describes them, as shown in the examples on this page. This is usually a question, like ‘What is your nationality?’.

### Asking one question on the page
If you are asking just [one question per page](../../patterns/question_pages/#start-by-asking-one-question-per-page) as recommended, you can set the contents of the `<legend>` as the page heading. 

Read more about why and [how to set legends as headings](../../patterns/labels_and_legend_headings).

Example of how checkbox component looks like when asking one question on the page:
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your nationality?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-checkbox">Cypriot
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Other European Union country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Citizen of another country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your nationality?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-checkbox">Cypriot
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Other European Union country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Citizen of another country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
</form>
```

### Asking more than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<legend>` as the page heading. Read more about asking [multiple questions on question pages](../../patterns/question_pages/#asking-multiple-questions-on-a-page).
Example of how checkbox component looks like when asking more than one question on the page:
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What is your nationality?</legend>
        <div class="govcy-form-control">
            <label class="govcy-checkbox">Cypriot
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Other European Union country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Citizen of another country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What is your nationality?</legend>
        <div class="govcy-form-control">
            <label class="govcy-checkbox">Cypriot
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Other European Union country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Citizen of another country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
</form>
```

### Checkbox items with hints
You can add [hints](../../patterns/hint_text) to checkbox items to provide additional information about the options. Hints can appear below the `<legend>` or the `<label>`.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your nationality?</h1></legend>
        <span class="govcy-hint">If you have dual nationality, select all options that are relevant to you. </span>
        <div class="govcy-form-control">
            <label class="govcy-checkbox">Cypriot
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Other European Union country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Citizen of another country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
                <span class="govcy-hint govcy-mt-2">Check this if you do not have nationality from a country </span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your nationality?</h1></legend>
        <span class="govcy-hint">If you have dual nationality, select all options that are relevant to you. </span>
        <div class="govcy-form-control">
            <label class="govcy-checkbox">Cypriot
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Other European Union country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Citizen of another country
                <input class="govcy-checkbox-input" type="checkbox">
                <span class="govcy-tickbox"></span>
                <span class="govcy-hint govcy-mt-2">Check this if you do not have nationality from a country </span>
            </label>
        </div>
    </fieldset>
</form>
```

### Show errors

Error messages should follow the guidance in [error message](../error_message) and have specific error messages for specific error states.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error1"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
            <label class="govcy-checkbox">Option 1
                <input class="govcy-checkbox-input" type="checkbox" aria-describedby="error1">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Option 2
                <input class="govcy-checkbox-input" type="checkbox" aria-describedby="error1">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error1"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
            <label class="govcy-checkbox">Option 1
                <input class="govcy-checkbox-input" type="checkbox" aria-describedby="error1">
                <span class="govcy-tickbox"></span>
            </label>
            <label class="govcy-checkbox">Option 2
                <input class="govcy-checkbox-input" type="checkbox" aria-describedby="error1">
                <span class="govcy-tickbox"></span>
            </label>
        </div>
    </fieldset>
</form>
```

### Ordering Items
The order of the items increases the bias in your service, so use caution on how you order them. To reduce bias, it is recommended to order checkbox options alphabetically by default. 

In some cases, it can be helpful to order them in a different logical order, for instance from most-to-least common options.
