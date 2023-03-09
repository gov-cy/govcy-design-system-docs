---
"title" : "Select"
date: 2022-02-01 00:01:01Z
---
The select component allows users to choose an option from a long list.

## When to use this component
The select component should only be used as a last resort in public-facing services because research shows that some users find selects very difficult to use. Only use the select component if you are allowing the user to select a single option from a long list. 

## When not to use this component
If you are presenting the user with fewer options, prefer to use the [radios](../radio) component.

## How it works
Before using the select component, try to present fewer options to the users. You can achieve that by asking users multiple questions. Asking questions means you’re less likely to need to use the select component, and can consider using a different solution, such as [radios](../radio).

If you use the component when loading data that was previously stored (for example loading the postal address country already stored in your profile), you should make the stored option pre-selected by default.

If you use the component for questions, you should not pre-select any of the options in case it influences users’ answers.

You can use the HTML below to create a select component.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label" for="sort">Label</label>
        <span class="govcy-hint">Hint</span>
        <select class="govcy-select" id="sort" name="sort" required>
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label" for="input">Label</label>
        <span class="govcy-hint">Hint</span>
        <select class="govcy-select" id="sort" name="sort" required>
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
```

### Show errors
Error messages should follow the guidance in error message and have specific error messages for specific error states.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="sort1">Label</label>
        <p id="select-option-input-error" class="govcy-input-error-msg">
        <span class="govcy-visually-hidden-error">Error:</span>Please select valid options
        </p>
        <select class="govcy-select govcy-select-error" id="sort1" name="sort1" required aria-describedby="select-option-input-error">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" novalidate class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="sort1">Label</label>
        <p id="select-option-input-error" class="govcy-input-error-msg">
        <span class="govcy-visually-hidden-error">Error:</span>Please select valid options
        </p>
        <select class="govcy-select govcy-select-error" id="sort1" name="sort1" required aria-describedby="select-option-input-error">
            <option value="" selected>None</option>
            <option value="published">Recently published</option>
            <option value="updated">Recently updated</option>
            <option value="views">Most views</option>
            <option value="comments">Most comments</option>
        </select>
    </div>
</form>
```