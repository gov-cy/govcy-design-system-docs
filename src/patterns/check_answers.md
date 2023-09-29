---
title: "Check answers"
date: 2022-02-01 00:01:02Z
tags: "help_users"
---
Let users check their answers before submitting information to a service. 

*Example Simple table*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table govcy-table-responsive-vertical">
<tbody>
    <tr>
        <th scope="row">Name</th>
        <td>Jane Smith</td>
        <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error">Name</span></a>
        </td>
    </tr>
    <tr>
        <th scope="row">Child's date of birth</th>
        <td>5 Jan 2021</td>
        <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Child's date of birth</span></a>
        </td>
    </tr>
    <tr>
        <th scope="row">Address</th>
        <td>Thornton</td>
        <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Address</span></a>
        </td>
    </tr>
    <tr>
        <th scope="row">Social insurance number</th>
        <td>7361063</td>
        <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Social insurance number</span></a>
        </td>
    </tr>
</tbody>
</table>
</div>

*Sample HTML Code*

```html
<table class="govcy-table govcy-table-responsive-vertical">
<tbody>
    <tr>
        <th scope="row">Name</th>
        <td>Jane Smith</td>
        <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error">Name</span></a>
        </td>
    </tr>
    <tr>
        <th scope="row">Child's date of birth</th>
        <td>5 Jan 2021</td>
        <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Child's date of birth</span></a>
        </td>
    </tr>
    <tr>
        <th scope="row">Address</th>
        <td>Thornton</td>
        <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Address</span></a>
        </td>
    </tr>
    <tr>
        <th scope="row">Social insurance number</th>
        <td>7361063</td>
        <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Social insurance number</span></a>
        </td>
    </tr>
</tbody>
</table>
```

*Example detailed table*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table govcy-table-responsive-vertical">
    <tbody>
        <tr>
            <th scope="row" class="col-3">Bank Details</th>
            <td class="col-7">
            <p>
                <span class="govcy-fw-bold">Account Name</span>
                <span class="govcy-d-block">Andreas Andreou</span>
            </p>
            <p>
                <span class="govcy-fw-bold">Bank</span>
                <span class="govcy-d-block">Bank of Cyprus</span>
            </p>
            <p>
                <span class="govcy-fw-bold">International Bank Account Number (IBAN)</span>
                <span class="govcy-d-block">CY**********************7654</span>
            </p>
            </td>
            <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Bank Details</span></a>
            </td>
        </tr>
        <tr>
            <th scope="row" class="col-3">Personal Details</th>
            <td class="col-7">
            <p>
                <span class="govcy-fw-bold">Email address</span>
                <span class="govcy-d-block">some@email.com</span>
            </p>
            <p>
                <span class="govcy-fw-bold">Mobile Number</span>
                <span class="govcy-d-block">99123456</span>
            </p>
            </td>
            <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Personal Details</span></a>
            </td>
        </tr>
        <tr>
            <th scope="row" class="col-3">Claim Children</th>
            <td class="col-7">
            George
            </td>
            <td class="col-2"></td>
        </tr>
    </tbody>
</table>
</div>

*Sample HTML Code*

```html
<table class="govcy-table govcy-table-responsive-vertical">
    <tbody>
        <tr>
            <th scope="row" class="col-3">Bank Details</th>
            <td class="col-7">
            <p>
                <span class="govcy-fw-bold">Account Name</span>
                <span class="govcy-d-block">Andreas Andreou</span>
            </p>
            <p>
                <span class="govcy-fw-bold">Bank</span>
                <span class="govcy-d-block">Bank of Cyprus</span>
            </p>
            <p>
                <span class="govcy-fw-bold">International Bank Account Number (IBAN)</span>
                <span class="govcy-d-block">CY**********************7654</span>
            </p>
            </td>
            <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Bank Details</span></a>
            </td>
        </tr>
        <tr>
            <th scope="row" class="col-3">Personal Details</th>
            <td class="col-7">
            <p>
                <span class="govcy-fw-bold">Email address</span>
                <span class="govcy-d-block">some@email.com</span>
            </p>
            <p>
                <span class="govcy-fw-bold">Mobile Number</span>
                <span class="govcy-d-block">99123456</span>
            </p>
            </td>
            <td class="col-2 govcy-text-sm-start govcy-text-md-end">
            <a href="">Change<span class="govcy-visually-hidden-error"> Personal Details</span></a>
            </td>
        </tr>
        <tr>
            <th scope="row" class="col-3">Claim Children</th>
            <td class="col-7">
            George
            </td>
            <td class="col-2"></td>
        </tr>
    </tbody>
</table>

```

## When to use this pattern
Show a single check answers page immediately before the confirmation screen for small to medium-sized transactions.

When designing a very large transaction with multiple sections, it may help to include a check answers pages at the end of each section.

This can be valuable for services where different users might be completing each section. You should test this approach with your users to find out if it’s helpful.

## Make the page easy to understand
On your check answers page you should:

- make it clear there’s a task to perform on the page
- make it clear that the transaction will not be complete until a user confirms their information is correct
- break the content up into sections when you can
- only show sections that are relevant to users – for example, if they’ve said they’re from the Cyprus, do not show sections for questions they have not answered about locations outside of the Cyprus
- rephrase questions if you need to – for example, you do not need to label every individual line of an address, and you can rewrite long questions as shorter statements
- make sure the submit button clearly shows the action it performs – for example ‘Change your tax details’ or ‘Send your claim form’

## Let users go back and change their answers
You should provide a ‘Change’ link next to each section on your check answers page so that users can add or change the information. ‘Change’ links contain hidden text to make them accessible to screen reader users. Update the hidden text to describe what each ‘change’ link is for, i.e., `<a href="">Change<span class="govcy-visually-hidden-error"> Personal Details</span></a>`.

The answers pages should look the same way they did when the user last used them, with all their answers pre-populated.

When they’ve finished, the ‘Continue’ button should return them to the check answers page. They should not need to go through the rest of the transaction again.

If a user changes their response in a way that means you need to ask them more questions, do this before returning them to the check answers page.
