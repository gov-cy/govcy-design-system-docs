---
"title" : "Radio"
date: 2022-02-01 00:01:01Z
---
Use the radios component when users can only select one option from a list.

## When to use this component
Use the radios component when users can only select one option from a list.

## When not to use this component
Do not use the radios component if users might need to select more than one option. In this case, you should use the [checkbox](../checkbox) component instead.

## How it works

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Option 1
                <input class="govcy-radio-input" type="radio" checked="checked" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Option 2
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Option 3
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
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
            <label class="govcy-radio">Option 1
                <input class="govcy-radio-input" type="radio" checked="checked" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Option 2
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Option 3
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
```

Always position radios to the left of their labels. This makes them easier to find, especially for users of screen magnifiers.

Unlike with checkboxes, users can only select one option from a list of radios. Do not assume that users will know how many options they can select based on the visual difference between radios and checkboxes alone.

If needed, add a hint explaining this, for example, ‘Select one option’.

Prefer not to pre-select radio options as this makes it more likely that users will not realise they’ve missed a question or submit the wrong answer. 

Include ‘None of the above’ or ‘I do not know’ if they are valid options. This helps the users as there is no option to deselect an option once it has been selected. 

Group radios together in a `<fieldset>` with a `<legend>` that describes them, as shown in the examples on this page. This is usually a question, like ‘Where do you live?’.

### Asking one question on the page
If you are asking just [one question per page](../../patterns/question_pages/#start-by-asking-one-question-per-page) as recommended, you can set the contents of the `<legend>` as the page heading. 

Read more about why and [how to set legends as headings](../../patterns/labels_and_legend_headings).

Example of how radio component looks like when asking one question on the page:
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Where do you live?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Nicosia
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Limassol
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Larnaca
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Paphos
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Famagousta
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Kyrenia
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Where do you live?</h1></legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Nicosia
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Limassol
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Larnaca
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Paphos
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Famagousta
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Kyrenia
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
```

### Asking more than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<legend>` as the page heading. Read more about asking [multiple questions on question pages](../../patterns/question_pages/#asking-multiple-questions-on-a-page).
Example of how radio component looks like when asking more than one question on the page:
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Where do you live?</legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Nicosia
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Limassol
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Larnaca
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Paphos
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Famagousta
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Kyrenia
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Where do you live?</legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Nicosia
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Limassol
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Larnaca
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Paphos
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Famagousta
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">Kyrenia
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
```

### Inline radios
In some cases, you can choose to display radios ‘inline’ beside one another (horizontally).

Only use inline radios when:
- the question only has two options
- both options are short

Remember that on small screens such as mobile devices, the radios will still be ‘stacked’ on top of one another (vertically).

Example or inline radios:
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Do you wish to continue?</h1></legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error1"><span class="govcy-visually-hidden-error">Error: </span>Mandatory field</p>
            <label class="govcy-radio govcy-d-sm-inline-block">Yes
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error1">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio govcy-d-sm-inline-block">No
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error1">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Do you wish to continue?</h1></legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error1"><span class="govcy-visually-hidden-error">Error: </span>Mandatory field</p>
            <label class="govcy-radio govcy-d-sm-inline-block">Yes
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error1">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio govcy-d-sm-inline-block">No
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error1">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
</form>
```

### Radio items with hints
You can add hints to radio items to provide additional information about the options. Hints can appear below the `<legend>` or the `<label>`.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Select your certificate</h1></legend>
        <span class="govcy-hint govcy-mt-2">Different options will appear depending on your option.</span>
        <div class="govcy-form-control">
            <label class="govcy-radio">Vaccination
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
                <span class="govcy-hint govcy-mt-2">You have been vaccinated and this has been entered in the relevant database of the Ministry of Health.</span>
            </label>
            <label class="govcy-radio">Recovery
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
                <span class="govcy-hint govcy-mt-2">You have been diagnosed with COVID-19, and the test result has been declared and entered in the relevant database of the Ministry of Health.</span>
            </label>
            <label class="govcy-radio">Laboratory testing
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
                <span class="govcy-hint govcy-mt-2">You have been tested during the last 7 days for COVID-19 after undergoing a laboratory antigen rapid test or molecular methodology (RT-PCR) test and received a negative result which has been entered by the laboratory in the relevant database of the Ministry of Health.</span>
            </label>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Select your certificate</h1></legend>
        <span class="govcy-hint govcy-mt-2">Different options will appear depending on your option.</span>
        <div class="govcy-form-control">
            <label class="govcy-radio">Vaccination
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
                <span class="govcy-hint govcy-mt-2">You have been vaccinated and this has been entered in the relevant database of the Ministry of Health.</span>
            </label>
            <label class="govcy-radio">Recovery
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
                <span class="govcy-hint govcy-mt-2">You have been diagnosed with COVID-19, and the test result has been declared and entered in the relevant database of the Ministry of Health.</span>
            </label>
            <label class="govcy-radio">Laboratory testing
                <input class="govcy-radio-input" type="radio" name="radio">
                <span class="govcy-radio-checked"></span>
                <span class="govcy-hint govcy-mt-2">You have been tested during the last 7 days for COVID-19 after undergoing a laboratory antigen rapid test or molecular methodology (RT-PCR) test and received a negative result which has been entered by the laboratory in the relevant database of the Ministry of Health.</span>
            </label>
        </div>
    </fieldset>
</form>
```

### Conditional radios (revealing a question)
You can ask the user a related question when they select a particular radio option, so they only see the question when it’s relevant to them. Do use conditional radios to show or hide anything that is not a question.

This might make two related questions easier to answer by grouping them on the same page. For example, you could reveal an email input when the user selects the ‘Contact me by email option.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What email should we use</legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Use existing email address
                <input class="govcy-radio-input" name="collapseGroup" type="radio" data-bs-toggle="collapse" data-bs-target=".email.show" checked="">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">No, use different email address
                <input class="govcy-radio-input collapsed" name="collapseGroup" type="radio" data-bs-toggle="collapse" data-bs-target=".email:not(.show)" aria-expanded="false">
                <span class="govcy-radio-checked"></span>
            </label>
            <div class="email govcy-pl-3 govcy-ml-1 collapse" style="">
                <div class="govcy-form-control govcy-form-control-hint">
                    <label class="govcy-label" for="">Email Address</label>
                    <span class="govcy-hint">We'll only use this for applicatin</span>
                    <input type="text" class="govcy-text-input" placeholder="email address">
                </div>
            </div>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What email should we use</legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Use existing email address
                <input class="govcy-radio-input" name="collapseGroup" type="radio" data-bs-toggle="collapse" data-bs-target=".email.show" checked="">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">No, use different email address
                <input class="govcy-radio-input collapsed" name="collapseGroup" type="radio" data-bs-toggle="collapse" data-bs-target=".email:not(.show)" aria-expanded="false">
                <span class="govcy-radio-checked"></span>
            </label>
            <div class="email govcy-pl-3 govcy-ml-1 collapse" style="">
                <div class="govcy-form-control govcy-form-control-hint">
                    <label class="govcy-label" for="">Email Address</label>
                    <span class="govcy-hint">We'll only use this for applicatin</span>
                    <input type="text" class="govcy-text-input" placeholder="email address">
                </div>
            </div>
        </div>
    </fieldset>
</form>
```

When using conditional radios, keep it simple. If the related question is complicated or has more than one part, show it on the next page in the process instead. Conditional radios should not be used with inline radios.

### Show errors
Error messages should follow the guidance in error message and have specific error messages for specific error states.

Display an error message if none of the radios are selected.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Do you wish to continue</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error2"><span class="govcy-visually-hidden-error">Error: </span>Select how you would like to proceed</p>
            <label class="govcy-radio">Yes
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error2">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">No
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error2">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Do you wish to continue</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error3"><span class="govcy-visually-hidden-error">Error: </span>Select how you would like to proceed</p>
            <label class="govcy-radio govcy-d-sm-inline-block">Yes
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error3">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio govcy-d-sm-inline-block">No
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error3">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What email should we use</legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Use existing home address
                <input class="govcy-radio-input" name="collapseGroup" type="radio" data-bs-toggle="collapse" data-bs-target=".address.show" checked="">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">No, use different home address
                <input class="govcy-radio-input" name="collapseGroup" type="radio" data-bs-toggle="collapse" data-bs-target=".address:not(.show)">
                <span class="govcy-radio-checked"></span>
            </label>
            <div class="collapse address govcy-pl-3 govcy-ml-1">
                <div class="govcy-form-control govcy-form-control-error">
                    <label class="govcy-label" for="">Home address</label>
                    <p class="govcy-input-error-msg" id="error4"><span class="govcy-visually-hidden-error">Error: </span>Please type valid home address</p>
                    <textarea type="textarea" class="govcy-text-area" placeholder="home address"  aria-describedby="error4"></textarea>
                </div>
            </div>
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Do you wish to continue</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error2"><span class="govcy-visually-hidden-error">Error: </span>Select how you would like to proceed</p>
            <label class="govcy-radio">Yes
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error2">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">No
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error2">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Do you wish to continue</legend>
        <div class="govcy-form-control govcy-form-control-error">
            <p class="govcy-input-error-msg" id="error3"><span class="govcy-visually-hidden-error">Error: </span>Select how you would like to proceed</p>
            <label class="govcy-radio govcy-d-sm-inline-block">Yes
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error3">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio govcy-d-sm-inline-block">No
                <input class="govcy-radio-input" type="radio" name="radio" aria-describedby="error3">
                <span class="govcy-radio-checked"></span>
            </label>
        </div>
    </fieldset>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What email should we use</legend>
        <div class="govcy-form-control">
            <label class="govcy-radio">Use existing home address
                <input class="govcy-radio-input" name="collapseGroup" type="radio" data-bs-toggle="collapse" data-bs-target=".address.show" checked="">
                <span class="govcy-radio-checked"></span>
            </label>
            <label class="govcy-radio">No, use different home address
                <input class="govcy-radio-input" name="collapseGroup" type="radio" data-bs-toggle="collapse" data-bs-target=".address:not(.show)">
                <span class="govcy-radio-checked"></span>
            </label>
            <div class="collapse address govcy-pl-3 govcy-ml-1">
                <div class="govcy-form-control govcy-form-control-error">
                    <label class="govcy-label" for="">Home address</label>
                    <p class="govcy-input-error-msg" id="error4"><span class="govcy-visually-hidden-error">Error: </span>Please type valid home address</p>
                    <textarea type="textarea" class="govcy-text-area" placeholder="home address"  aria-describedby="error4"></textarea>
                </div>
            </div>
        </div>
    </fieldset>
</form>
```

### Ordering Items
The order of the items increases the bias in your service, so use caution on how you order them. To reduce bias, it is recommended to order radio options alphabetically by default. 

In some cases, it can be helpful to order them in a different logical order, for instance from most-to-least common options.
