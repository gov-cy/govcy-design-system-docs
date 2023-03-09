---
"title" : "Fieldset"
date: 2022-02-01 00:01:01Z
---
Use the fieldset component to group related form inputs.

## When to use this component
Use the fieldset component when you need to show a relationship between multiple form inputs. For example, you may need to group a set of text inputs into a single fieldset when asking for an address.

## How it works

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Contact Address</legend>
        <div class="govcy-form-control">
            <label class="govcy-label" for="address">Address / Number</label>
            <input id="address" type="text" class="govcy-text-input" >
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label" for="village">Town / Village</label>
            <input id="village" type="text" class="govcy-text-input" >
        </div>
        <div class="govcy-form-control">    
            <label class="govcy-label" for="district">District</label>
            <input id="district" type="text" class="govcy-text-input" >
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label" for="postcode">Postal code</label>
            <input id="postcode" type="text" class="govcy-text-input" >
        </div>
    </fieldset>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <fieldset class="govcy-fieldset">
        <legend class="govcy-legend">Contact Address</legend>
        <div class="govcy-form-control">
            <label class="govcy-label" for="address">Address / Number</label>
            <input id="address" type="text" class="govcy-text-input" >
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label" for="village">Town / Village</label>
            <input id="village" type="text" class="govcy-text-input" >
        </div>
        <div class="govcy-form-control">    
            <label class="govcy-label" for="district">District</label>
            <input id="district" type="text" class="govcy-text-input" >
        </div>
        <div class="govcy-form-control">
            <label class="govcy-label" for="postcode">Postal code</label>
            <input id="postcode" type="text" class="govcy-text-input" >
        </div>
    </fieldset>
</form>
```

The first element inside a fieldset must be a `<legend>` which describes the group of inputs. This could be a question, such as ‘What is your current address?’ or a statement like ‘Personal details’.

If you’re asking just [one question per page](../../patterns/question_pages/#start-by-asking-one-question-per-page) as recommended, you can set the contents of the `<legend>` as the page heading. This is good practice as it means that users of screen readers will only hear the contents once.

Read more about [how to set legends as headings](../../patterns/labels_and_legend_headings).

On [question pages](../../patterns/question_pages) containing a group of inputs, including the question as the legend helps users of screen readers to understand that the inputs are all related to that question.

