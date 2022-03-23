---
title: "Moving from Version 0.1.0"
---

Developers will need to make the following changes in order to move from Version 0.1.X to Vesion 1.X.X using the CSS provided by GOV.CY.

## Use new css 

Link to the new CSS as shown below instead of the old CSS.

```html
<!-- CSS -->
<link href="https://govcydesignsystem1.azureedge.net/bvtest/version/1.0.0/style.min.css" rel="stylesheet" >
```

## Back link and User’s name and sign out 

Both these components must appear on the same line and have specific margin bottom. To do that we use `govcy-float-start` and `govcy-mb-4` classes as follows:

```html
<!-- Back Link -->
<div class="govcy-mb-4 govcy-float-start">
	<span class="bi bi-chevron-left"></span>
	<a class="govcy-back-link" href="/">Back</a>
</div>
<!-- User’s name and sign out -->
<div class="govcy-text-end govcy-mb-4">
	Nikanos Polykarpou | <a href="/Account/LogOut" class="govcy-back-link">Log Out</a>
</div>
```

More information at [back Link](../components/back_link) and [User’s name and sign out](../components/user_name_and_sign_out).

## Responsive Tables

The responsive tables wrapper class has changed from `table-responsive` to `govcy-table-responsive`. More information at [Responsive tables](../components/table/#responsive-tables).

## Visually-hidden class for errors and check your answers

A class has been implemented `govcy-visually-hidden-error` that is hidden on the screen but readable by screen readers. 

It should be used in [error messages](../components/error_message) by adding the word `Error`. For example:

```html
<span class="govcy-visually-hidden-error">Error: </span>
<span class="govcy-input-error-msg">There is an error</span>
```

It should also be used in the [check answers](../patterns/check_answers/#let-users-go-back-and-change-their-answers) pattern on the `change` link to indicate what the link is changing. For example:

```html
<a href="">Change<span class="govcy-visually-hidden-error"> Personal Details</span></a>
```