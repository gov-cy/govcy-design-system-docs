---
title: "Button"
date: 2022-02-01 00:01:01Z
description: "Use the button component to help users carry out an action like starting an application or saving their information."
---

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<button type="button" class="govcy-btn-primary">Button</button>
</div>

*HTML code*
```html
<button type="button" class="govcy-btn-primary">Button</button>
```
## When to use this component
Use the button component to help users carry out an action like starting an application or saving their information.

## How it works
Buttons should only exist in the [main section](../../getting-started/page-template/#sections). 

Align the primary action button to the left edge of your form.

Depending on your implementation set the `type` attribute to "button" or "submit". 

### Primary button
Use a primary button for the main call to action on a page.  

Avoid using multiple primary buttons on a single page. Having more than one main call to action reduces their impact, and makes it harder for users to know what to do next.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<button type="button" class="govcy-btn-primary">Primary</button>
</div>

*HTML code*
```html
<button type="button" class="govcy-btn-primary">Primary</button>
```
### Secondary button
Use secondary buttons for secondary calls to action on a page.

Pages with too many calls to action make it hard for users to know what to do next. Before adding lots of secondary buttons, try to simplify the page or break the content down across multiple pages.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<button type="button" class="govcy-btn-secondary">Secondary</button>
</div>

*HTML code*
```html
<button type="button" class="govcy-btn-secondary">Secondary</button>
```
### Warning button
Warning buttons are designed to make users think carefully before they use them. They only work if used very sparingly. Most services should not need one. Only use warning buttons for actions with serious destructive consequences that cannot be easily undone by a user. For example, permanently deleting an account.

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Do not rely only on the red colour of a warning button to communicate the serious nature of the action. This is because not all users will be able to see the colour or will understand what it signifies. Make sure the context and button text make clear what will happen if the user selects it.
		</p>
    </div>
</div>

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<button type="button" class="govcy-btn-warning">Warning</button>
</div>

*HTML code*
```html
<button type="button" class="govcy-btn-warning">Warning</button>
```
### Success button
Use success buttons to mark the success of an activity or submission. 

They only work if used very sparingly. Most services should only need one, for example, the "submit" button in the final [check your answers page](../../patterns/check_answers/) permanently deleting an account.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<button type="button" class="govcy-btn-success">Submit</button>
</div>

*HTML code*
```html
<button type="button" class="govcy-btn-success">Submit</button>
```
### Component text
Write button text in sentence case, describing the action it performs. For example:

| Case | English | Greek |
| ---- | ---- | ---- |
| At the start of the service | Get Started | Ξεκινήστε |
| To enter a service. This is more valid when the service is revisited frequently | Enter | Είσοδος |
| Sign in to an account a user has already created | Sign in | Σύνδεση |
| Continue when the service does not save a user’s information | Continue | Συνέχεια |
| Continue when the service does save a user’s information | Save and continue | Αποθήκευση και συνέχεια |
| When a user can save their information and come back later | Save and come back later | Αποθηκεύστε και επιστρέψτε αργότερα |
| To add another item to a list or group | Add another | Προσθέστε άλλο ή Προσθήκη |
| To make a payment | Pay | Πληρωμή |
| On a check answers page that does not have any legal content a user must agree to | Submit | Υποβολή |
| Οn a check answers page that has legal content a user must agree to | Accept and submit | Αποδοχή και υποβολή |
| To sign out when a user is signed in to an account | Sign out | Αποσύνδεση |

{.govcy-table}

 You may need to include more or different words to better describe the action. For example, ‘Add another address’ and ‘Accept and claim a tax refund’.

## Accessibility
Make sure:
- not to decrease the height or target area of buttons. This is to make sure users can easily interact with buttons
- if your using a `<form>` make sure it contains a submit button (input type="submit", input type="image", or button type="submit")
- not to use the `disabled` attribute on buttons. If you need to make sure that the users have entered the required information, use the [error message](../error_message) component instead.