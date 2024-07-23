---
"title" : "Fieldset"
date: 2022-02-01 00:01:01Z
description: "Use the fieldset component to group related form inputs."
---
Use the fieldset component to group related form inputs.

## When to use this component
Use the fieldset component when you need to show a relationship between multiple form inputs. For example, you may need to group a set of text inputs into a single fieldset when asking for an address.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form" novalidate action="">
    <fieldset class="govcy-fieldset" aria-describedby="address-hint1">
        <legend class="govcy-legend"><h1>What is your address?</h1></legend>
        <span class="govcy-hint" id="address-hint1">The address will only be used for correspondence</span>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyManualAddressLine1">Address line 1</label>
               <input id="cyManualAddressLine1" name="cyManualAddressLine1" type="text" class="govcy-text-input" autocomplete="address-line1"> 
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyManualAddressLine2">Address line 2 (optional)</label>
                <input id="cyManualAddressLine2" name="cyManualAddressLine2" type="text" class="govcy-text-input" autocomplete="address-line2">  
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyManualTownOrCity">Town or city</label>
                <input id="cyManualTownOrCity" name="cyManualTownOrCity" type="text" class="govcy-text-input" autocomplete="address-level2">
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyManualPostalCode">Postcode</label>
            <input id="cyManualPostalCode" name="cyManualPostalCode" type="text" class="govcy-text-input govcy-text-input-char_20 " autocomplete="postal-code">
        </div>
    </fieldset>
</div>
</div>

*HTML code*
```html
<form class="govcy-form" novalidate action="">
    <fieldset class="govcy-fieldset" aria-describedby="address-hint1">
        <legend class="govcy-legend"><h1>What is your address?</h1></legend>
        <span class="govcy-hint" id="address-hint1">The address will only be used for correspondence</span>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyManualAddressLine1">Address line 1</label>
               <input id="cyManualAddressLine1" name="cyManualAddressLine1" type="text" class="govcy-text-input" autocomplete="address-line1"> 
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyManualAddressLine2">Address line 2 (optional)</label>
                <input id="cyManualAddressLine2" name="cyManualAddressLine2" type="text" class="govcy-text-input" autocomplete="address-line2">  
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyManualTownOrCity">Town or city</label>
                <input id="cyManualTownOrCity" name="cyManualTownOrCity" type="text" class="govcy-text-input" autocomplete="address-level2">
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label govcy-label-primary" for="cyManualPostalCode">Postcode</label>
            <input id="cyManualPostalCode" name="cyManualPostalCode" type="text" class="govcy-text-input govcy-text-input-char_20 " autocomplete="postal-code">
        </div>
    </fieldset>
</form>
```

The first element inside a fieldset must be a `<legend>` which describes the group of inputs. This is usually a question, such as ‘What is your current address?’ or a statement like ‘Personal details’.

If you’re asking just [one question per page](../../patterns/service_structure/#one-thing-at-a-time) as recommended, you can set the contents of the `<legend>` as the page heading. This is good practice as it means that users of screen readers will only hear the contents once.

Read more about [single questions pages legends as headings](../../patterns/labels_and_legend_headings/#legends-as-page-headings).

On [question pages](../../patterns/question_pages/) containing a group of inputs, including the question as the legend helps users of screen readers to understand that the inputs are all related to that question.

Include general help text in the legend if it would help the user fill in the form, and you cannot write it as hint text. However, try to keep it as short as possible.

## Accessibility
Make sure:
- you add a `legend` for your `fieldset`
- you associate the `label` elements with the input they relate to, using the `for` attribute
- when using a hints, add  `aria-describedby` on the `fieldset` element, with the id of the hint element 
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `input` and `fieldset` elements, with the id of the error message. 
- you do not disable copy and paste
