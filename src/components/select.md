---
"title" : "Select"
date: 2022-02-01 00:01:01Z
description: "Use the select component when users can only select one option from a long list."
---
The select component allows users to choose an option from a long list.

## When to use this component
The select component should only be used as a last resort in public-facing services because research shows that some users find selects very difficult to use. Only use the select component if you are allowing the user to select a single option from a long list.

## When not to use this component
If you are presenting the user with fewer options, prefer to use the [radio](../radio) component.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

Before using the select component, try to present fewer options to the users. You can achieve that by asking users multiple questions. Asking questions means you’re less likely to need to use the select component, and can consider using a different solution, such as [radios](../radio).

If you use the component when loading data that was previously stored (for example loading the postal address country already stored in your profile), you should make the stored option pre-selected by default.

If you use the component for questions, you should not pre-select any of the options in case it influences users’ answers.

### Single question page
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="sort2">Sort by</label></h1>
        <select class="govcy-select" id="sort2" name="sort2">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="sort2">Sort by</label></h1>
        <select class="govcy-select" id="sort2" name="sort2">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
```
### More than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<label>` as the page heading.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="sort1">Sort by</label>
        <select class="govcy-select" id="sort1" name="sort1">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="sort1">Sort by</label>
        <select class="govcy-select" id="sort1" name="sort1">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
```
### Hint text
A hint can help users understand the options, but it is not always necessary.  Do not include a hint for straightforward selections.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="sort3">Sort by</label>
        <span id="sort3-hint" class="govcy-hint">Will sort results accordingly</span>
        <select class="govcy-select" id="sort3" name="sort3" aria-describedby="sort3-hint">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="sort3">Sort by</label>
        <span id="sort3-hint" class="govcy-hint">Will sort results accordingly</span>
        <select class="govcy-select" id="sort3" name="sort3" aria-describedby="sort3-hint">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
```

### Order of elements inside the component
Place the elements inside the component in the following order.
1. Label
2. Hint
3. Error message
4. Select

### Error messages
Make sure to follow the instructions for [error messages](../error_message) and [error summary](../error_summary) when validating user input. Error messages should be styled like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="sort-err">Sort by</label></h1>
        <span id="sort-err-hint" class="govcy-hint">Will sort results accordingly</span>
        <p id="sort-err-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Please select valid options
        </p>
        <select class="govcy-select govcy-select-error" id="sort-err" name="sort-err" aria-describedby="sort-err-hint sort-err-error">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="sort-err">Sort by</label></h1>
        <span id="sort-err-hint" class="govcy-hint">Will sort results accordingly</span>
        <p id="sort-err-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Please select valid options
        </p>
        <select class="govcy-select govcy-select-error" id="sort-err" name="sort-err" aria-describedby="sort-err-hint sort-err-error">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
```
Here is example with the component used in a more than one question page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="sort-err1">Sort by</label>
        <span id="sort-err-hint1" class="govcy-hint">Will sort results accordingly</span>
        <p id="sort-err-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Please select valid options
        </p>
        <select class="govcy-select govcy-select-error" id="sort-err1" name="sort-err1" aria-describedby="sort-err-hint1 sort-err-error1">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="sort-err1">Sort by</label>
        <span id="sort-err-hint1" class="govcy-hint">Will sort results accordingly</span>
        <p id="sort-err-error1" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Please select valid options
        </p>
        <select class="govcy-select govcy-select-error" id="sort-err1" name="sort-err1" aria-describedby="sort-err-hint1 sort-err-error1">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
```

## Accessibility
Make sure:
- you associate the `label` element with the select it relate to, using the `for` attribute
- when using a hints, add  `aria-describedby` on the `select` element, with the id of the hint element. 
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `text` element, with the id of the error message. 
- not to disable copy and paste