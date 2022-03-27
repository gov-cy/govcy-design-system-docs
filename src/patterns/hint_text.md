---
title: "Hint Text"
date: 2022-02-01 00:01:02Z
tags: "help_users"
---
Use hint text for help that’s relevant to the majority of users, like how their information will be used, or where to find it. 

## How it works

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

You can use hint text after `<legends>` or `<labels>`.

Do not include links within hint text. While screen readers will read out the link text when describing the field, they will not tell users that the text is a link.
