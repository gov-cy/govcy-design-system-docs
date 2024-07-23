---
"title" : "Checkbox"
date: 2022-02-01 00:01:01Z
description: "Let users select one or more options by using the checkboxes component."
---
Let users select one or more options by using the checkboxes component.

## When to use this component
Use the checkboxes component when you need to help users:

- select multiple options from a list
- toggle a single option on or off

## When not to use this component
Do not use the checkboxes component if users can only choose one option from a selection. In this case, use the [radio](../radio) component.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option1">
                <label class="govcy-label" for="check1-option1">Option 1</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option2">
                <label class="govcy-label" for="check1-option2">Option 2</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option3">
                <label class="govcy-label" for="check1-option3">Option 3</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option1">
                <label class="govcy-label" for="check1-option1">Option 1</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option2">
                <label class="govcy-label" for="check1-option2">Option 2</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check1-checkbox-group" type="checkbox" id="check1-option3">
                <label class="govcy-label" for="check1-option3">Option 3</label>
            </div>
        </div>
    </fieldset>
</form>
```

Always position checkboxes to the left of their labels. This makes them easier to find, especially for users of screen magnifiers.

Unlike with radios, users can select multiple options from a list of checkboxes. Do not assume that users will know how many options they can select based on the visual difference between radios and checkboxes alone.

If needed, add a hint explaining this, for example, 'Select all that apply'.

Prefer not to pre-select checkbox options as this makes it more likely that users will not realise they’ve missed a question or submit the wrong answer.

Group radios together in a `<fieldset>` with a `<legend>` that describes them, as shown in the examples on this page. This is usually a question, like ‘What is your nationality?’.

### Single question page
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly. 

Example of how the component looks like when asking one question on the page:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your nationality?</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check2-checkbox-group" type="checkbox" id="check2-nationality">
                <label class="govcy-label" for="check2-nationality">Cypriot</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check2-checkbox-group" type="checkbox" id="check2-otherEurope">
                <label class="govcy-label" for="check2-otherEurope">Other European Union country</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check2-checkbox-group" type="checkbox" id="check2-anotherCountry">
                <label class="govcy-label" for="check2-anotherCountry">Citizen of another country</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>What is your nationality?</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check2-checkbox-group" type="checkbox" id="check2-nationality">
                <label class="govcy-label" for="check2-nationality">Cypriot</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check2-checkbox-group" type="checkbox" id="check2-otherEurope">
                <label class="govcy-label" for="check2-otherEurope">Other European Union country</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check2-checkbox-group" type="checkbox" id="check2-anotherCountry">
                <label class="govcy-label" for="check2-anotherCountry">Citizen of another country</label>
            </div>
        </div>
    </fieldset>
</form>
```

### Asking more than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<legend>` as the page heading.

Example of how the component looks like when asking more than one question on the page:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What is your nationality?</legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check3-checkbox-group" type="checkbox" id="check3-nationality">
                <label class="govcy-label" for="check3-nationality">Cypriot</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check3-checkbox-group" type="checkbox" id="check3-otherEurope">
                <label class="govcy-label" for="check3-otherEurope">Other European Union country</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check3-checkbox-group" type="checkbox" id="check3-anotherCountry">
                <label class="govcy-label" for="check3-anotherCountry">Citizen of another country</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What is your nationality?</legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check3-checkbox-group" type="checkbox" id="check3-nationality">
                <label class="govcy-label" for="check3-nationality">Cypriot</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check3-checkbox-group" type="checkbox" id="check3-otherEurope">
                <label class="govcy-label" for="check3-otherEurope">Other European Union country</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check3-checkbox-group" type="checkbox" id="check3-anotherCountry">
                <label class="govcy-label" for="check3-anotherCountry">Citizen of another country</label>
            </div>
        </div>
    </fieldset>
</form>
```
### Checkbox items with hints
You can add hints to checkbox items to provide additional information about the options. Hints can appear below the `<legend>` or the `<label>`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="check4-fildset-hint">
        <legend class="govcy-legend">What is your nationality?</legend>
        <div class="govcy-form-control">
	        <span class="govcy-hint" id="check4-fildset-hint">If you have dual nationality, select all options that are relevant to you. </span>
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
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="check4-fildset-hint">
        <legend class="govcy-legend">What is your nationality?</legend>
        <div class="govcy-form-control">
	        <span class="govcy-hint" id="check4-fildset-hint">If you have dual nationality, select all options that are relevant to you. </span>
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

### Add an option for ‘none’
When ‘none’ would be a valid answer, give users the option to check a box to say none of the other options apply to them – without this option, users would have to leave all of the boxes unchecked. Giving users this option also makes sure they do not skip the question by accident.

Show the ‘none’ option last. Separate it from the other options using a divider. The text is usually the word ‘or’. Use `<span class="govcy-visually-hidden">Or, </span>` to make sure the separator word is read by screen readers. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Did you travel to any of these destinations last year?</legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check5-checkbox-group" type="checkbox" id="check5-otherEurope">
                <label class="govcy-label" for="check5-otherEurope">European Union</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check5-checkbox-group" type="checkbox" id="check5-other">
                <label class="govcy-label" for="check5-other">Other destination</label>
            </div>
            <p class="govcy-ml-3 govcy-mb-3">Or</p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check5-checkbox-group" type="checkbox" id="check5-no">
                <label class="govcy-label" for="check5-no"><span class="govcy-visually-hidden">Or, </span>I did not travel last year</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Did you travel to any of these destinations last year?</legend>
        <div class="govcy-form-control">
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check5-checkbox-group" type="checkbox" id="check5-otherEurope">
                <label class="govcy-label" for="check5-otherEurope">European Union</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check5-checkbox-group" type="checkbox" id="check5-other">
                <label class="govcy-label" for="check5-other">Other destination</label>
            </div>
            <p class="govcy-ml-3 govcy-mb-3">Or</p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check5-checkbox-group" type="checkbox" id="check5-no">
                <label class="govcy-label" for="check5-no"><span class="govcy-visually-hidden">Or, </span>I did not travel last year</label>
            </div>
        </div>
    </fieldset>
</form>
```

If a user selects both the ‘none’ and another checkbox, display an error message when the page is validated.


*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="check-er-15-input-error">
        <legend class="govcy-legend">Did you travel to any of these destinations last year?</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="check-er-15-input-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Select a destination, or select ‘I did not travel last year’
            </p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check51-checkbox-group" type="checkbox" id="check51-otherEurope" checked>
                <label class="govcy-label" for="check51-otherEurope">European Union</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check51-checkbox-group" type="checkbox" id="check51-other">
                <label class="govcy-label" for="check51-other">Other destination</label>
            </div>
            <p class="govcy-ml-3 govcy-mb-3">Or</p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check51-checkbox-group" type="checkbox" id="check51-no" checked>
                <label class="govcy-label" for="check51-no"><span class="govcy-visually-hidden">Or, </span>I did not travel last year</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="check-er-15-input-error">
        <legend class="govcy-legend">Did you travel to any of these destinations last year?</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="check-er-15-input-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>Select a destination, or select ‘I did not travel last year’
            </p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check51-checkbox-group" type="checkbox" id="check51-otherEurope" checked>
                <label class="govcy-label" for="check51-otherEurope">European Union</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check51-checkbox-group" type="checkbox" id="check51-other">
                <label class="govcy-label" for="check51-other">Other destination</label>
            </div>
            <p class="govcy-ml-3 govcy-mb-3">Or</p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check51-checkbox-group" type="checkbox" id="check51-no" checked>
                <label class="govcy-label" for="check51-no"><span class="govcy-visually-hidden">Or, </span>I did not travel last year</label>
            </div>
        </div>
    </fieldset>
</form>
```

### Order of elements inside the component
Place the elements inside the component in the following order.

1. Fieldset
    1. Legend
    1. Form control
        1. Hint
        2. Error message
        3. Inputs

### Error messages
Make sure to follow the instructions for [error messages](../error_message) and [error summary](../error_summary) when validating user input. Error messages should be styled like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" aria-describedby="check-er-input-error">
		<legend class="govcy-legend"><h1>Legend</h1></legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="check-er-input-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check-er-checkbox-group" type="checkbox" id="check-er-option7">
                <label class="govcy-label" for="check-er-option7">Option 1</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check-er-checkbox-group" type="checkbox" id="check-er-option8">
                <label class="govcy-label" for="check-er-option8">Option 2</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset" aria-describedby="check-er-input-error">
		<legend class="govcy-legend"><h1>Legend</h1></legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p id="check-er-input-error" class="govcy-input-error-msg">
                <span class="govcy-visually-hidden-error">Error:</span>There is an error
            </p>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check-er-checkbox-group" type="checkbox" id="check-er-option7">
                <label class="govcy-label" for="check-er-option7">Option 1</label>
            </div>
            <div class="govcy-checkbox">
                <input class="govcy-checkbox-input" name="check-er-checkbox-group" type="checkbox" id="check-er-option8">
                <label class="govcy-label" for="check-er-option8">Option 2</label>
            </div>
        </div>
    </fieldset>
</form>
```

Here is example with the component used in a more than one question page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
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
</div>

*HTML code*
```html
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
```

Remember to adjust the `aria-describedby` attribute to include the error message's `id` and add  `<span class="govcy-visually-hidden-error">Error:</span>` in the error message.
## Ordering Items
The order of the items increases the bias in your service, so use caution on how you order them. To reduce bias, it is recommended to order checkbox options alphabetically by default.

In some cases, it can be helpful to order them in a different logical order, for instance from most-to-least common options.

## Accessibility
Make sure:
- you associate the `label` elements with the checkbox input they relate to, using the `for` attribute
- you add a `legend` for your `fieldset`
- when using a hints, add  `aria-describedby` on the `fieldset` or `input` element, with the id of the hint element 
- when using the 'or' separator, use `<span class="govcy-visually-hidden">Or, </span>` in the input label to make sure the separator word is read by screen readers 
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `fieldset` element, with the id of the error message
