---
"title" : "File upload"
date: 2022-02-01 00:01:01Z
description: "Help users select and upload a file."
---
Help users select and upload a file.

## When to use this component
You should only ask users to upload something if it’s critical to the delivery of your service.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

To upload a file, the user can either:
- use the ‘Choose file’ button
- ‘drag and drop’ a file into the file upload input area

### Single question page
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="file1">Upload a file</label></h1>
        <span id="file1-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <input class="govcy-file-upload" type="file" id="file1" name="file1" aria-describedby="file1-hint">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="file1">Upload a file</label></h1>
        <span id="file1-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <input class="govcy-file-upload" type="file" id="file1" name="file1" aria-describedby="file1-hint">
    </div>
</form>
```
### More than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<label>` as the page heading. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="file2">Upload a file</label>
        <span id="file2-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <input class="govcy-file-upload" type="file" id="file2" name="file2" aria-describedby="file2-hint">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="file2">Upload a file</label>
        <span id="file2-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <input class="govcy-file-upload" type="file" id="file2" name="file2" aria-describedby="file2-hint">
    </div>
</form>
```
### Previously uploaded file
Allow the users to view or delete a file that they have previously uploaded within a single journey. 

Use links to:
- view the file. The links should open the file in a new tab, if the browser supports it's type.
- Delete the file. The link should lead to a question page with [radios](../radio/), asking the users if they are sure they want to delete the file. Use the file's title, not the file name. For example the question of the delete page should be 'Are you sure you want to delete the company’s certificate of liquidation file?'.

Use `<span class="govcy-visually-hidden"> the file's title</span>` in the links body to help screen readers indicate which file is to be viewed or deleted

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <p class="govcy-label govcy-label-primary">You have uploaded the company’s certificate of liquidation</p>
        <span class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <a href="#">View<span class="govcy-visually-hidden"> the company’s certificate of liquidation file</span></a>
        <a class="govcy-ml-3" href="#">Delete<span class="govcy-visually-hidden"> the company’s certificate of liquidation file</span></a>
    </div>
</div>
</div>

*HTML code*
```html
<div class="govcy-form">
    <div class="govcy-form-control">
        <p class="govcy-label govcy-label-primary">You have uploaded the company’s certificate of liquidation</p>
        <span class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <a href="#">View<span class="govcy-visually-hidden"> the company’s certificate of liquidation file</span></a>
        <a class="govcy-ml-3" href="#">Delete<span class="govcy-visually-hidden"> the company’s certificate of liquidation file</span></a>
    </div>
</div>
```

### Order of elements inside the component
Place the elements inside the component in the following order.
1. Label
2. Hint
3. Error message
4. Input

### Error messages
Make sure to follow the instructions for [error messages](../error_message) and [error summary](../error_summary) when validating user input. Error messages should be styled like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="file4">Upload a file</label></h1>
        <span id="file4-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <p id="file4-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input class="govcy-file-upload" type="file" id="file4" name="file4" aria-describedby="file4-hint file4-error">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="file4">Upload a file</label></h1>
        <span id="file4-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <p id="file4-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input class="govcy-file-upload" type="file" id="file4" name="file4" aria-describedby="file4-hint file4-error">
    </div>
</form>
```
Here is example with the component used in a more than one question page.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="file5">Upload a file</label>
        <span id="file5-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <p id="file5-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input class="govcy-file-upload" type="file" id="file5" name="file5" aria-describedby="file5-hint file5-error">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label govcy-label-primary" for="file5">Upload a file</label>
        <span id="file5-hint" class="govcy-hint">PDF, JPG, JPEG, PNG are the acceptable formats</span>
        <p id="file5-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>There is an error
        </p>
        <input class="govcy-file-upload" type="file" id="file5" name="file5" aria-describedby="file5-hint file5-error">
    </div>
</form>
```
Remember to adjust the `aria-describedby` attribute to include the error message's `id` and add  `<span class="govcy-visually-hidden-error">Error:</span>` in the error message.

### Component text
Use the following text:

| Labels and hints                        | English                                                    | Greek                                          |
| --------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------- |
| **View**                                | View                                                       | Προβολή                                        |
| **Delete**                              | Delete                                                     | Διαγραφή                                       |
| **File hint** (example)                 | PDF, JPG, JPEG, PNG are the acceptable formats             | PDF, JPG, JPEG, PNG, είναι οι αποδεκτές μορφές |
| **Previously uploaded label** (example) | You have uploaded the company’s certificate of liquidation | Έχετε ανεβάσει το πιστοποιητικό εκκαθάρισης    |

{.govcy-table}

## Accessibility
make sure:
- not to use ‘drag and drop’ as the only way to upload files. You must provide another method, such as the ‘Choose file’ button
- users can easily reuse a [previously uploaded file](#previously-uploaded-file) within a single journey
- when showing previously uploaded files, use `<span class="govcy-visually-hidden-error"> the file's title</span>` in the links body to help screen readers indicate which file is to be viewed or deleted
- you associate the `label` elements with the input they relate to, using the `for` attribute
- when using a hints, add  `aria-describedby` on the `input` element, with the id of the hint element 
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `input` element, with the id of the error message. 