---
"title" : "Radio"
date: 2022-02-01 00:01:01Z
description: "Use the radios component when users can only select one option from a list."
---

## When to use this component
Use the radios component when users can only select one option from a list.

## When not to use this component
Do not use the radios component if users might need to select more than one option. In this case, you should use the [checkbox](../checkbox/) component instead.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Legend</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="simple" id="option-1">
                <label class="govcy-label" for="option-1">Option 1</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="simple" id="option-2">
                <label class="govcy-label" for="option-2">Option 2</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="simple" id="option-3">
                <label class="govcy-label" for="option-3">Option 3</label>
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
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="simple" id="option-1">
                <label class="govcy-label" for="option-1">Option 1</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="simple" id="option-2">
                <label class="govcy-label" for="option-2">Option 2</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="simple" id="option-3">
                <label class="govcy-label" for="option-3">Option 3</label>
            </div>
        </div>
    </fieldset>
</form>
```

Always position radios to the left of their labels. This makes them easier to find, especially for users of screen magnifiers.

Unlike with checkboxes, users can only select one option from a list of radios. Do not assume that users will know how many options they can select based on the visual difference between radios and checkboxes alone.

If needed, add a hint explaining this, for example, ‘Select one option’.

Do not pre-select radio options as this makes it more likely that users will not realise they’ve missed a question or submit the wrong answer.

Include ‘None of the above’ or ‘I do not know’ if they are valid options. This helps the users as there is no option to deselect an option once it has been selected.

Group radios together in a `<fieldset>` with a `<legend>` that describes them, as shown in the examples on this page. This is usually a question, like ‘Where do you live?’.

### Single question page
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly. 

Example of how the component looks like when asking one question on the page:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Where do you live?</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-nic">
                <label class="govcy-label" for="option1-nic">Nicosia</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-lim">
                <label class="govcy-label" for="option1-lim">Limassol</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-lar">
                <label class="govcy-label" for="option1-lar">Larnaca</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-pap">
                <label class="govcy-label" for="option1-pap">Paphos</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-fam">
                <label class="govcy-label" for="option1-fam">Famagousta</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-kyr">
                <label class="govcy-label" for="option1-kyr">Kyrenia</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend"><h1>Where do you live?</h1></legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-nic">
                <label class="govcy-label" for="option1-nic">Nicosia</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-lim">
                <label class="govcy-label" for="option1-lim">Limassol</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-lar">
                <label class="govcy-label" for="option1-lar">Larnaca</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-pap">
                <label class="govcy-label" for="option1-pap">Paphos</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-fam">
                <label class="govcy-label" for="option1-fam">Famagousta</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option1" id="option1-kyr">
                <label class="govcy-label" for="option1-kyr">Kyrenia</label>
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
        <legend class="govcy-legend">Where do you live?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-nic">
                <label class="govcy-label" for="option2-nic">Nicosia</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-lim">
                <label class="govcy-label" for="option2-lim">Limassol</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-lar">
                <label class="govcy-label" for="option2-lar">Larnaca</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-pap">
                <label class="govcy-label" for="option2-pap">Paphos</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-fam">
                <label class="govcy-label" for="option2-fam">Famagousta</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-kyr">
                <label class="govcy-label" for="option2-kyr">Kyrenia</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Where do you live?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-nic">
                <label class="govcy-label" for="option2-nic">Nicosia</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-lim">
                <label class="govcy-label" for="option2-lim">Limassol</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-lar">
                <label class="govcy-label" for="option2-lar">Larnaca</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-pap">
                <label class="govcy-label" for="option2-pap">Paphos</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-fam">
                <label class="govcy-label" for="option2-fam">Famagousta</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option2" id="option2-kyr">
                <label class="govcy-label" for="option2-kyr">Kyrenia</label>
            </div>
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

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Do you wish to continue?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio govcy-d-sm-inline-block">
                <input class="govcy-radio-input" type="radio" name="option3" id="option3-yes">
                <label class="govcy-label" for="option3-yes">Yes</label>
            </div>
            <div class="govcy-radio govcy-d-sm-inline-block">
                <input class="govcy-radio-input" type="radio" name="option3" id="option3-no">
                <label class="govcy-label" for="option3-no">No</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Do you wish to continue?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio govcy-d-sm-inline-block">
                <input class="govcy-radio-input" type="radio" name="option3" id="option3-yes">
                <label class="govcy-label" for="option3-yes">Yes</label>
            </div>
            <div class="govcy-radio govcy-d-sm-inline-block">
                <input class="govcy-radio-input" type="radio" name="option3" id="option3-no">
                <label class="govcy-label" for="option3-no">No</label>
            </div>
        </div>
    </fieldset>
</form>
```
### Radio items with hints
You can add hints to radio items to provide additional information about the options. Hints can appear below the `<legend>` or the `<label>`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="option4-fildset-hint">
        <legend class="govcy-legend"><h1>Select your certificate</h1></legend>
        <div class="govcy-form-control">
	        <span class="govcy-hint" id="option4-fildset-hint">Different options will appear depending on your option.</span>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option4" id="option4-1" aria-describedby="option4-1-hint">
                <label class="govcy-label" for="option4-1">Vaccination</label>
                <span id="option4-1-hint" class="govcy-hint">You have been vaccinated and this has been entered in the relevant database of the Ministry of Health.</span>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option4" id="option4-2" aria-describedby="option4-2-hint">
                <label class="govcy-label" for="option4-2">Recovery</label>
                <span id="option4-2-hint" class="govcy-hint">You have been diagnosed with COVID-19, and the test result has been declared and entered in the relevant database of the Ministry of Health.</span>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option4" id="option4-3" aria-describedby="option4-3-hint">
                <label class="govcy-label" for="option4-3">Laboratory testing</label>
                <span id="option4-3-hint" class="govcy-hint">You have been tested during the last 7 days for COVID-19 after undergoing a laboratory antigen rapid test or molecular methodology (RT-PCR) test and received a negative result which has been entered by the laboratory in the relevant database of the Ministry of Health.</span>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset" aria-describedby="option4-fildset-hint">
        <legend class="govcy-legend"><h1>Select your certificate</h1></legend>
        <div class="govcy-form-control">
	        <span class="govcy-hint" id="option4-fildset-hint">Different options will appear depending on your option.</span>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option4" id="option4-1" aria-describedby="option4-1-hint">
                <label class="govcy-label" for="option4-1">Vaccination</label>
                <span id="option4-1-hint" class="govcy-hint">You have been vaccinated and this has been entered in the relevant database of the Ministry of Health.</span>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option4" id="option4-2" aria-describedby="option4-2-hint">
                <label class="govcy-label" for="option4-2">Recovery</label>
                <span id="option4-2-hint" class="govcy-hint">You have been diagnosed with COVID-19, and the test result has been declared and entered in the relevant database of the Ministry of Health.</span>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option4" id="option4-3" aria-describedby="option4-3-hint">
                <label class="govcy-label" for="option4-3">Laboratory testing</label>
                <span id="option4-3-hint" class="govcy-hint">You have been tested during the last 7 days for COVID-19 after undergoing a laboratory antigen rapid test or molecular methodology (RT-PCR) test and received a negative result which has been entered by the laboratory in the relevant database of the Ministry of Health.</span>
            </div>
        </div>
    </fieldset>
</form>
```
### Add an option for ‘none’
When ‘none’ would be a valid answer, give users the option to check a radio to say none of the other options apply to them – without this option, users would have to leave all of the radios unchecked. Giving users this option also makes sure they do not skip the question by accident.

Show the ‘none’ option last. Separate it from the other options using a divider. The text is usually the word ‘or’. Use `<span class="govcy-visually-hidden">Or, </span>` to make sure the separator word is read by screen readers.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Where do you live?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option9" id="option9-cy">
                <label class="govcy-label" for="option9-cy">Cyprus</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option9" id="option9-eu">
                <label class="govcy-label" for="option9-eu">Other European Union country</label>
            </div>
            <p class="govcy-ml-3 govcy-mb-3">Or</p>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option9" id="option9-noneu">
                <label class="govcy-label" for="option9-noneu"><span class="govcy-visually-hidden">Or, </span>Not in the European Union</label>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Where do you live?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option9" id="option9-cy">
                <label class="govcy-label" for="option9-cy">Cyprus</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option9" id="option9-eu">
                <label class="govcy-label" for="option9-eu">Other European Union country</label>
            </div>
            <p class="govcy-ml-3 govcy-mb-3">Or</p>
            <div class="govcy-radio">
                <input class="govcy-radio-input" type="radio" name="option9" id="option9-noneu">
                <label class="govcy-label" for="option9-noneu"><span class="govcy-visually-hidden">Or, </span>Not in the European Union</label>
            </div>
        </div>
    </fieldset>
</form>
```
### Conditional radios (revealing a question)
You can ask the user a related question when they select a particular radio option, so they only see the question when it’s relevant to them. 

This might make two related questions easier to answer by grouping them on the same page. For example, you could reveal an email input when the user selects the ‘Contact me by email option‘.

Do use conditional radios to show or hide anything that is not a question.

Do not conditionally reveal questions to inline radios, such as ‘yes’ and ‘no’ options placed next to each other.

Never use more than one group of conditional radios on the same page.

To implement a conditional radio and connect it with a collapsing area, use the `data-aria-controls` attribute, as shown in the examples below.

*Simple example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-simple-email" name="collapseGroupSimple" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-simple-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroupSimple" type="radio" id="option6-simple-emailDif" value="emailDif" data-aria-controls="email-simple-different"/>
                <label class="govcy-label" for="option6-simple-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional govcy-radio__conditional--hidden" id="email-simple-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple">Email Address</label>
                    <span id="in4-simple-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4-simple" type="text" class="govcy-text-input" aria-describedby="in4-simple-hint"/>
                </div>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-simple-email" name="collapseGroupSimple" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-simple-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroupSimple" type="radio" id="option6-simple-emailDif" value="emailDif" data-aria-controls="email-simple-different"/>
                <label class="govcy-label" for="option6-simple-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional govcy-radio__conditional--hidden" id="email-simple-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple">Email Address</label>
                    <span id="in4-simple-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4-simple" type="text" class="govcy-text-input" aria-describedby="in4-simple-hint"/>
                </div>
            </div>
        </div>
    </fieldset>
</form>
```
When revisiting the same page, the checked radio button should be preselected and the conditional content collapsed.

To start with preselected radio and collapse content:
- set the radio as `checked`
- remove the class `govcy-radio__conditional--hidden` from the relative content

*Example with content collapsed*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-simple-collapsed-email" name="collapseGroupsimple-collapsed" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-simple-collapsed-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroupsimple-collapsed" type="radio" id="option6-simple-collapsed-emailDif" value="emailDif" data-aria-controls="email-simple-collapsed-different" checked/>
                <label class="govcy-label" for="option6-simple-collapsed-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional" id="email-simple-collapsed-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple-collapsed">Email Address</label>
                    <span id="in4-simple-collapsed-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4-simple-collapsed" type="text" class="govcy-text-input" aria-describedby="in4-simple-collapsed-hint" value="test@email.com"/>
                </div>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-simple-collapsed-email" name="collapseGroupsimple-collapsed" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-simple-collapsed-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroupsimple-collapsed" type="radio" id="option6-simple-collapsed-emailDif" value="emailDif" data-aria-controls="email-simple-collapsed-different" checked/>
                <label class="govcy-label" for="option6-simple-collapsed-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional" id="email-simple-collapsed-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4-simple-collapsed">Email Address</label>
                    <span id="in4-simple-collapsed-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4-simple-collapsed" type="text" class="govcy-text-input" aria-describedby="in4-simple-collapsed-hint" value="test@email.com"/>
                </div>
            </div>
        </div>
    </fieldset>
</form>
```

You can add multiple radio buttons in the same conditional group or add multiple inputs within the conditional radio's content.

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			<strong>Keep it simple</strong>. When we tested complicated questions that were conditionally revealed, particularly questions with more that one part, users did get confused. When we broke the questions in different pages, it was easier for the users to answer.<br>
            If the related question is complicated or has more than one part, show it on the next page in the process instead.
		</p>
    </div>
</div>

*Complex example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-email" name="collapseGroup" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroup" type="radio" id="option6-emailDif" value="emailDif" data-aria-controls="email-different"/>
                <label class="govcy-label" for="option6-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional govcy-radio__conditional--hidden" id="email-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4">Personal Email Address</label>
                    <span id="in4-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4" type="text" class="govcy-text-input" aria-describedby="in4-hint"/>
                </div>
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in5">Work Email Address</label>
                    <span id="in5-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in5" type="text" class="govcy-text-input" aria-describedby="in5-hint"/>
                </div>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroup" type="radio" id="option6a-addressDif" value="emailDif" data-aria-controls="address-different"/>
                <label class="govcy-label" for="option6a-addressDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different home address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional govcy-radio__conditional--hidden" id="address-different">
                <div class="govcy-form-control"> 
                    <label class="govcy-label" for="in4a">Home Address</label>
                    <span id="in4a-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4a" type="text" class="govcy-text-input" aria-describedby="in4a-hint"/>
                </div>
            </div>
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">What contact details should we use?</legend>
        <div class="govcy-form-control">
            <div class="govcy-radio">
                <input class="govcy-radio-input" id="option6-email" name="collapseGroup" type="radio" value="existingContactDetails" />
                <label class="govcy-label" for="option6-email">Use existing contact details</label>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroup" type="radio" id="option6-emailDif" value="emailDif" data-aria-controls="email-different"/>
                <label class="govcy-label" for="option6-emailDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different email address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional govcy-radio__conditional--hidden" id="email-different">
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in4">Personal Email Address</label>
                    <span id="in4-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4" type="text" class="govcy-text-input" aria-describedby="in4-hint"/>
                </div>
                <div class="govcy-form-control">
                    <label class="govcy-label" for="in5">Work Email Address</label>
                    <span id="in5-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in5" type="text" class="govcy-text-input" aria-describedby="in5-hint"/>
                </div>
            </div>
            <div class="govcy-radio">
                <input class="govcy-radio-input" name="collapseGroup" type="radio" id="option6a-addressDif" value="emailDif" data-aria-controls="address-different"/>
                <label class="govcy-label" for="option6a-addressDif">
                    <span class="govcy-visually-hidden">This option expands and has more questions,</span>
                    Use different home address
                </label>
            </div>
            <div class="govcy-form-control govcy-form-control-hint govcy-pl-4 govcy-ml-5 govcy-radio__conditional govcy-radio__conditional--hidden" id="address-different">
                <div class="govcy-form-control"> 
                    <label class="govcy-label" for="in4a">Home Address</label>
                    <span id="in4a-hint" class="govcy-hint">We'll only use this for applying</span>
                    <input id="in4a" type="text" class="govcy-text-input" aria-describedby="in4a-hint"/>
                </div>
            </div>
        </div>
    </fieldset>
</form>
```

#### Conditional radios accessibility issue
Users are not always notified when a conditionally revealed question is shown or hidden. To help screen readers inform users that more questions will are revealed use `<span class="govcy-visually-hidden">This option expands and has more questions,</span>` in the option's `label`. 

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
</div>

*HTML code*
```html
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
```
Remember to adjust the `aria-describedby` attribute to include the error message's `id` and add  `<span class="govcy-visually-hidden-error">Error:</span>` in the error message.

## Ordering Items
The order of the items increases the bias in your service, so use caution on how you order them. To reduce bias, it is recommended to order radio options alphabetically by default.

In some cases, it can be helpful to order them in a different logical order, for instance from most-to-least common options.

## Accessibility
Make sure:
- you associate the `label` elements with the checkbox input they relate to, using the `for` attribute
- you add a `legend` for your `fieldset`
- when using a hints, add  `aria-describedby` on the `fieldset` or `input` element, with the id of the hint element 
- when using the 'or' separator, use `<span class="govcy-visually-hidden">Or, </span>` in the input label to make sure the separator word is read by screen readers. 
- when using conditional radios,  use `<span class="govcy-visually-hidden">This option expands and has more questions,</span>` in the conditional option's `label`
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `fieldset` element, with the id of the error message. 


