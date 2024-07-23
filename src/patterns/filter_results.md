---
title: "Filter results"
date: 2022-02-01 00:01:02Z
tags: "help_users"
description: "Help users filter results."
---
Filter results patterns is an optional search method with improved accuracy and more filtering options.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form govcy-search-form">
    <div class="govcy-row">
        <div class="govcy-col-md-4">    
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="tm">Trademark Number</label>
                <span id="hint-tm" class="govcy-hint">999999</span>
                <input id="tm" type="text" class="govcy-text-input" aria-describedby="hint-tm">
            </div>
        </div>
        <div class="govcy-col-md-4">    
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="name">Name</label>
                <span id="hint-name" class="govcy-hint">Enter name</span>
                <input id="name" type="text" class="govcy-text-input" aria-describedby="hint-name">
            </div>
        </div>
        <div class="govcy-col-md-4">
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="pid">Person Id</label>
                <span id="hint-pid" class="govcy-hint">999999</span>
                <input id="pid" type="text" class="govcy-text-input" aria-describedby="hint-pid">
            </div>
        </div>
    </div>
    <div class="govcy-row">
        <div class="govcy-col-md-4">    
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="class">Class</label>
                <span id="hint-class" class="govcy-hint">Hint</span>
                <select class="govcy-select w-100" id="class" name="" aria-describedby="hint-class">
                    <option value="" selected="">None</option>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                    <option value="D">D</option>
                </select>
            </div>
        </div>
        <div class="govcy-col-md-4">    
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="type">Type</label>
                <span id="hint-type" class="govcy-hint">Hint</span>
                <select class="govcy-select w-100" id="type" name="" aria-describedby="hint-type">
                    <option value="" selected="">None</option>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                    <option value="D">D</option>
                </select>
            </div>
        </div>
        <div class="govcy-col-md-4">
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="kind">Kind</label>
                <span id="hint-kind" class="govcy-hint">Hint</span>
                <select class="govcy-select w-100" id="kind" name="" aria-describedby="hint-kind">
                    <option value="" selected="">None</option>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                    <option value="D">D</option>
                </select>
            </div>
        </div>
    </div>
    <div class="govcy-row">
        <div class="govcy-col-12">
            <button type="button" class="govcy-btn-primary">Search</button>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form govcy-search-form" novalidate="">
    <div class="govcy-row">
        <div class="govcy-col-md-4">    
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="tm">Trademark Number</label>
                <span id="hint-tm" class="govcy-hint">999999</span>
                <input id="tm" type="text" class="govcy-text-input" aria-describedby="hint-tm">
            </div>
        </div>
        <div class="govcy-col-md-4">    
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="name">Name</label>
                <span id="hint-name" class="govcy-hint">Enter name</span>
                <input id="name" type="text" class="govcy-text-input" aria-describedby="hint-name">
            </div>
        </div>
        <div class="govcy-col-md-4">
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="pid">Person Id</label>
                <span id="hint-pid" class="govcy-hint">999999</span>
                <input id="pid" type="text" class="govcy-text-input" aria-describedby="hint-pid">
            </div>
        </div>
    </div>
    <div class="govcy-row">
        <div class="govcy-col-md-4">    
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="class">Class</label>
                <span id="hint-class" class="govcy-hint">Hint</span>
                <select class="govcy-select w-100" id="class" name="" aria-describedby="hint-class">
                    <option value="" selected="">None</option>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                    <option value="D">D</option>
                </select>
            </div>
        </div>
        <div class="govcy-col-md-4">    
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="type">Type</label>
                <span id="hint-type" class="govcy-hint">Hint</span>
                <select class="govcy-select w-100" id="type" name="" aria-describedby="hint-type">
                    <option value="" selected="">None</option>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                    <option value="D">D</option>
                </select>
            </div>
        </div>
        <div class="govcy-col-md-4">
            <div class="govcy-form-control">
                <label class="govcy-label govcy-label-primary" for="kind">Kind</label>
                <span id="hint-kind" class="govcy-hint">Hint</span>
                <select class="govcy-select w-100" id="kind" name="" aria-describedby="hint-kind">
                    <option value="" selected="">None</option>
                    <option value="A">A</option>
                    <option value="B">B</option>
                    <option value="C">C</option>
                    <option value="D">D</option>
                </select>
            </div>
        </div>
    </div>
    <div class="govcy-row">
        <div class="govcy-col-12">
            <button type="submit" class="govcy-btn-primary">Search</button>
        </div>
    </div>
</form>
```
## When to use this component
Use advanced search on bigger data tables with many pages.

Use advanced search when users know exactly what they are looking for (e.g. finding their name).

## When not to use this component
Do not use on smaller data tables as it may become counterintuitive.

## Accessibility 
Be sure to:
- Associate the `label` elements with the input they relate to, using the `for` attribute.
- When using a hints, add  `aria-describedby` on the `input` element, with the id of the hint element. 