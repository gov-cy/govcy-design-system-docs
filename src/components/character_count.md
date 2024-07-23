---
title: "Character count"
date: 2022-02-01 00:01:01Z
description: "Help users know how much text they can enter when there is a limit on the number of characters."
---

Help users know how much text they can enter when there is a limit on the number of characters.

## When to use this component
Always test your service without a character count first.

Only use the character count component when there is a good reason for limiting the number of characters users can enter. For example, if there is:

- evidence that users are likely to enter more information than they need to
- a legal or technical reason that means an entry must be no more than a certain number of characters

## When not to use this component
If your users keep hitting the character limit imposed by the backend of your service, then try to increase the limit rather than use a character count.

## How it works
The character count component should only exist in the [main section](../../getting-started/page-template/#sections). The component uses JavaScript. To use it with the gov.cy [developer assets](../../getting-started/developer-assets/), make sure to include the main JavaScript file in your page.

The character count tells users how many characters they have remaining as they type into a [textarea](../textarea) with a character limit. Do this by setting the `data-maxchars` in the component markup. For example, `data-maxchars="150"` will set a character limit of 150.

Users will get updates at a pace that works best for the way they interact with the textarea. This means:

- sighted users will see a count message that updates as they type
- screen reader users will hear the count announcement when they stop typing.

This component does not restrict the user from entering information. The user can enter more than the character limit, but are told they’ve entered too many characters. This lets them type or copy and paste their full answer, then edit it down.

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Do not depend only on the character count for validating the input. Make sure to run the validations on the textarea after the users distinctly indicate that their input is ready to be submitted, for example when clicking the “continue” button, as indicated in the <a href="../error_message">error message</a> component.
		</p>
    </div>
</div>

The count message appears below the textarea so that:

- it’s clearly separate from any hint text or error message above the textarea
- if it’s below the visible screen area, users will still see it again when they scroll down to send their response

### Single question page
If you are asking just one question on a page, follow the instructions for [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page) and adjust the header and label accordingly. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="input4">Can you provide more detail?</label></h1>
        <span class="govcy-hint" id="govcy-hint4">Do not include personal or financial information like your National Insurance number or credit card details.</span>
        <textarea id="input4" class="govcy-text-area" rows="5" aria-describedby="govcy-hint-hint4 govcy-hint4"></textarea>
        <div id="govcy-hint-hint4" class="govcy-character-count" data-maxchars="150">
            <div class="govcy-character-remaining-counter">You have <span></span> characters remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> characters more</div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="input4">Can you provide more detail?</label></h1>
        <span class="govcy-hint" id="govcy-hint4">Do not include personal or financial information like your National Insurance number or credit card details.</span>
        <textarea id="input4" class="govcy-text-area" rows="5" aria-describedby="govcy-hint-hint4 govcy-hint4"></textarea>
        <div id="govcy-hint-hint4" class="govcy-character-count" data-maxchars="150">
            <div class="govcy-character-remaining-counter">You have <span></span> characters remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> characters more</div>
        </div>
    </div>
</form>
```
### More than one question on the page
If you’re asking more than one question on the page, do not set the contents of the `<label>` as the page heading. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input1">Can you provide more detail?</label>
        <span class="govcy-hint" id="govcy-hint1">Do not include personal or financial information like your National Insurance number or credit card details.</span>
        <textarea id="input1" class="govcy-text-area" rows="5" aria-describedby="govcy-hint-hint1 govcy-hint1"></textarea>
        <div id="govcy-hint-hint1" class="govcy-character-count" data-maxchars="150">
            <div class="govcy-character-remaining-counter">You have <span></span> characters remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> characters more</div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input1">Can you provide more detail?</label>
        <span class="govcy-hint" id="govcy-hint1">Do not include personal or financial information like your National Insurance number or credit card details.</span>
        <textarea id="input1" class="govcy-text-area" rows="5" aria-describedby="govcy-hint-hint1 govcy-hint1"></textarea>
        <div id="govcy-hint-hint1" class="govcy-character-count" data-maxchars="150">
            <div class="govcy-character-remaining-counter">You have <span></span> characters remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> characters more</div>
        </div>
    </div>
</form>
```
### Word count instead of character count
In some cases it may be more helpful to show a word count. For example, if your question requires a longer answer.  

Do this by setting the `data-maxwords` in the component markup. For example, `data-maxwords="150"` will set a word limit of 150.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input2">Enter a job description</label>
        <textarea id="input2" class="govcy-text-area" rows="5" aria-describedby="govcy-hint-hint2"></textarea>
        <div id="govcy-hint-hint2" class="govcy-character-count" data-maxwords="150">
            <div class="govcy-character-remaining-counter">You have <span></span> words remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> words more</div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control">
        <label class="govcy-label govcy-label-primary" for="input2">Enter a job description</label>
        <textarea id="input2" class="govcy-text-area" rows="5" aria-describedby="govcy-hint-hint2"></textarea>
        <div id="govcy-hint-hint2" class="govcy-character-count" data-maxwords="150">
            <div class="govcy-character-remaining-counter">You have <span></span> words remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> words more</div>
        </div>
    </div>
</form>
```
### Avoid narrow limits
When using a character count, try to set the limit higher than most users will need.  Find out what this is by doing user research and data analysis.

### Order of elements inside the component
Place the elements inside the component in the following order.
1. Label
2. Hint
3. Error message
4. Textarea
5. Count message

### Error messages
Make sure to follow the instructions for [error messages](../error_message) and [error summary](../error_summary) when validating user input. Error messages should be styled like this:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="input3">Enter a job description</label></h1>
        <p id="job-description-input-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Job description must be 150 characters or less
        </p>
        <textarea id="input3" class="govcy-text-area govcy-text-area-error" aria-describedby="govcy-hint-hint3 job-description-input-error" rows="5">A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format. A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format. A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format.
        </textarea>
        <div  id="govcy-hint-hint3" class="govcy-character-count" data-maxwords="150">
            <div class="govcy-character-remaining-counter">You have <span></span> words remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> words more</div>
        </div>
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate="">
    <div class="govcy-form-control govcy-form-control-error">
        <h1><label class="govcy-label govcy-label-primary" for="input3">Enter a job description</label></h1>
        <p id="job-description-input-error" class="govcy-input-error-msg">
            <span class="govcy-visually-hidden-error">Error:</span>Job description must be 150 characters or less
        </p>
        <textarea id="input3" class="govcy-text-area govcy-text-area-error" aria-describedby="govcy-hint-hint3 job-description-input-error" rows="5">A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format. A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format. A content designer works on the end-to-end journey of a service to help users complete their goal and government deliver a policy intent. Their work may involve the creation of, or change to, a transaction, product or single piece of content that stretches across digital and offline channels. They make sure appropriate content is shown to a user in the right place and in the best format.
        </textarea>
        <div  id="govcy-hint-hint3" class="govcy-character-count" data-maxwords="150">
            <div class="govcy-character-remaining-counter">You have <span></span> words remaining</div>
            <div class="govcy-character-more-counter">You have entered <span></span> words more</div>
        </div>
    </div>
</form>
```
If a user tries to send their response with too many characters, you must show an error message above the field as well as the count message below it.

The error message tells users what went wrong and how to fix it. The count message provides live feedback and updates as a user types.

Remember to adjust the `aria-describedby` attribute to include the error message's `id` and add  `<span class="govcy-visually-hidden-error">Error:</span>` in the error message.

### Component text
Use the following text for the count messages:

| Message                  | English                              | Greek                                      |
| ------------------------ | ------------------------------------ | ------------------------------------------ |
| **Characters remaining** | You have ... characters remaining    | Έχετε ...  χαρακτήρες που απομένουν        |
| **Characters exceeding** | You have entered ... characters more | Έχετε περάσει ... χαρακτήρες περισσότερους |
| **Words remaining**      | You have ... words remaining         | Έχετε ...  λέξεις που απομένουν            |
| **Words exceeding**      | You have entered ... words more      | Έχετε περάσει ... λέξεις περισσότερες      |

{.govcy-table}

## Accessibility
Make sure:
- you add the `aria-describedby` attribute to the inputs. The aria-describedby should always include the `id` of the count message element (with class `govcy-character-count`) and depending on the case, the hint and error message elements 
- the `label` elements are associated with the input they relate to, using the `for` attribute
- when using a hints, add  `aria-describedby` on the `input` element, with the id of the hint element 
- when displaying error massages, use `<span class="govcy-visually-hidden-error">Error:</span>` in the Error message area, and add  `aria-describedby` on the `textarea` element, with the id of the error message 
- not to disable copy and paste
- not to restrict maximum length with the `maxlength` attribute exactly to the allowed limit of the input