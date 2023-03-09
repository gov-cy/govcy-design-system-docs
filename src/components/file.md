---
"title" : "File"
date: 2022-02-01 00:01:01Z
---
Help users select and upload a file.

## When to use this component
You should only ask users to upload something if it’s critical to the delivery of your service.

## How it works
You can use the HTML below to create a file component. 

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-mb-1" for="infile">Upload a file</label>
        <span class="govcy-hint" id="infile_hint">The file must be a PDF</span>
        <input class="govcy-file-upload" type="file" id="infile" name="infile" aria-describedby="infile_hint">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label govcy-mb-1" for="infile">Upload a file</label>
        <span class="govcy-hint" id="infile_hint">The file must be a PDF</span>
        <input class="govcy-file-upload" type="file" id="infile" name="infile" aria-describedby="infile_hint">
    </div>
</form>
```

### Show errors
Error messages should follow the guidance in error message and have specific error messages for specific error states.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error govcy-pb-1">
        <label class="govcy-label govcy-mb-1" for="infile1">Upload a file</label>
        <p class="govcy-input-error-msg govcy-mb-3" id="infile_error"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
        <input class="govcy-file-upload" type="file" id="infile1" name="infile1" aria-describedby="infile_error">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error govcy-pb-1">
        <label class="govcy-label govcy-mb-1" for="infile1">Upload a file</label>
        <p class="govcy-input-error-msg govcy-mb-3" id="infile_error"><span class="govcy-visually-hidden-error">Error: </span>There is an error</p>
        <input class="govcy-file-upload" type="file" id="infile1" name="infile1" aria-describedby="infile_error">
    </div>
</form>
```