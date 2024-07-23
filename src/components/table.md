---
"title" : "Table"
date: 2022-02-01 00:01:01Z
description: "Use the table component to make information easier to compare and scan for users."
---
Use the table component to make information easier to compare and scan for users.

## When to use this component
Use the table component to let users compare information in rows and columns.

## When not to use this component
Never use the table component to layout content on a page. Instead, use the [grid system](../../styles/grid/).

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

You can use the HTML below to create a table component.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th scope="col">Property</th>
            <th scope="col">Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>Name</th>
            <td>Jane Smith</td>
        </tr>
        <tr>
            <th>Child's date of birth</th>
            <td>5 Jan 2021</td>
        </tr>
        <tr>
            <th>Address</th>
            <td>Thornton</td>
        </tr>
        <tr>
            <th>Social insurance number</th>
            <td>123456</td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th scope="col">Property</th>
            <th scope="col">Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>Name</th>
            <td>Jane Smith</td>
        </tr>
        <tr>
            <th>Child's date of birth</th>
            <td>5 Jan 2021</td>
        </tr>
        <tr>
            <th>Address</th>
            <td>Thornton</td>
        </tr>
        <tr>
            <th>Social insurance number</th>
            <td>123456</td>
        </tr>
    </tbody>
</table>
```
### Table headers
Use table headers to tell users what the rows and columns represent. Use the `scope` attribute to help users of assistive technology distinguish between row and column headers.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table">
    <thead>
        <tr>
            <th scope="col">#</th>
            <th scope="col">Expence</th>
            <th scope="col">Notes</th>
            <th scope="col" class="govcy-text-end">Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">1</th>
            <td>Server</td>
            <td>120 GB RAM, xxx processor</td>
            <td class="govcy-text-end">5000</td>
        </tr>
        <tr>
            <th scope="row">2</th>
            <td>Monitor</td>
            <td>22 inch</td>
            <td class="govcy-text-end">100</td>
        </tr>
        <tr>
            <th scope="row">3</th>
            <td>Keyboard</td>
            <td>Greek Layout</td>
            <td class="govcy-text-end">20</td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table">
    <thead>
        <tr>
            <th scope="col">#</th>
            <th scope="col">Expence</th>
            <th scope="col">Notes</th>
            <th scope="col" class="govcy-text-end">Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">1</th>
            <td>Server</td>
            <td>120 GB RAM, xxx processor</td>
            <td class="govcy-text-end">5000</td>
        </tr>
        <tr>
            <th scope="row">2</th>
            <td>Monitor</td>
            <td>22 inch</td>
            <td class="govcy-text-end">100</td>
        </tr>
        <tr>
            <th scope="row">3</th>
            <td>Keyboard</td>
            <td>Greek Layout</td>
            <td class="govcy-text-end">20</td>
        </tr>
    </tbody>
</table>
```
### Numbers in table
When comparing columns of numbers, align the numbers to the right in table cells using the `govcy-text-end` class.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table">
    <thead>
        <tr>
            <th scope="col">#</th>
            <th scope="col">Expence</th>
            <th scope="col">Notes</th>
            <th scope="col" class="govcy-text-end">Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">1</th>
            <td>Server</td>
            <td>120 GB RAM, xxx processor</td>
            <td class="govcy-text-end">5000</td>
        </tr>
        <tr>
            <th scope="row">2</th>
            <td>Monitor</td>
            <td>22 inch</td>
            <td class="govcy-text-end">100</td>
        </tr>
        <tr>
            <th scope="row">2</th>
            <td>Keyboard</td>
            <td>Greek layout</td>
            <td class="govcy-text-end">20</td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table">
    <thead>
        <tr>
            <th scope="col">#</th>
            <th scope="col">Expence</th>
            <th scope="col">Notes</th>
            <th scope="col" class="govcy-text-end">Amount</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">1</th>
            <td>Server</td>
            <td>120 GB RAM, xxx processor</td>
            <td class="govcy-text-end">5000</td>
        </tr>
        <tr>
            <th scope="row">2</th>
            <td>Monitor</td>
            <td>22 inch</td>
            <td class="govcy-text-end">100</td>
        </tr>
        <tr>
            <th scope="row">2</th>
            <td>Keyboard</td>
            <td>Greek layout</td>
            <td class="govcy-text-end">20</td>
        </tr>
    </tbody>
</table>
```
### Responsive tables
Responsive tables allow tables to adjusting designs to accommodate screens of different sizes. Always use responsive tables, unless there is a specific reason not to.

There are two ways you can achive this.

#### Vertical responsive tables
Vertical responsive tables place each cell of a row in a single column. This is the preferred method for responsive tables.

Make any table vertically responsive by adding a `.govcy-table-responsive-vertical` class in a table.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table govcy-table-responsive-vertical">
    <tbody>
        <tr>
            <th>Account Name</th>
            <td>Andreas Andreou</td>
        </tr>
        <tr>
            <th>Bank</th>
            <td>Bank of Cyprus</td>
        </tr>
        <tr>
            <th>International Bank Account Number (IBAN)</th>
            <td>CY**********************7654</td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table govcy-table-responsive-vertical">
    <tbody>
        <tr>
            <th>Account Name</th>
            <td>Andreas Andreou</td>
        </tr>
        <tr>
            <th>Bank</th>
            <td>Bank of Cyprus</td>
        </tr>
        <tr>
            <th>International Bank Account Number (IBAN)</th>
            <td>CY**********************7654</td>
        </tr>
    </tbody>
</table>
```

Using the `.govcy-table-responsive-vertical` class, will hide the table header in small viewports. If you wish to show the the headers while using this variant, you can add `<div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">{ HEADER-NAME }</div>` in each cell as shown in the example below:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table govcy-table-responsive-vertical">
    <thead>
        <tr>
            <th>Input</th>
            <th>Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Input</div>
                Account Name
            </td>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Value</div>
                Andreas Andreou
            </td>
        </tr>
        <tr>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Input</div>
                Bank
            </td>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Value</div>
                Bank of Cyprus
            </td>
        </tr>
        <tr>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Input</div>
                International Bank Account Number (IBAN)
            </td>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Value</div>
                CY**********************7654
            </td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table govcy-table-responsive-vertical">
    <thead>
        <tr>
            <th>Input</th>
            <th>Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Input</div>
                Account Name
            </td>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Value</div>
                Andreas Andreou
            </td>
        </tr>
        <tr>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Input</div>
                Bank
            </td>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Value</div>
                Bank of Cyprus
            </td>
        </tr>
        <tr>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Input</div>
                International Bank Account Number (IBAN)
            </td>
            <td>
                <div class="govcy-d-md-none govcy-fw-bolder govcy-my-2">Value</div>
                CY**********************7654
            </td>
        </tr>
    </tbody>
</table>
```

#### Horizontal responsive tables
Horizontal responsive tables allow tables to be scrolled horizontally with ease.

Make any table horizontally responsive across all viewports by wrapping a `.govcy-table` with `.govcy-table-responsive`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-table-responsive">
    <table class="govcy-table">
        <thead>
            <tr>
                <th scope="col">#</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">1</th>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
            </tr>
            <tr>
                <th scope="row">2</th>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
            </tr>
            <tr>
                <th scope="row">3</th>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
            </tr>
        </tbody>
    </table>
</div>
</div>

*HTML code*
```html
<div class="govcy-table-responsive">
    <table class="govcy-table">
        <thead>
            <tr>
                <th scope="col">#</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
                <th scope="col">Heading</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <th scope="row">1</th>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
            </tr>
            <tr>
                <th scope="row">2</th>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
            </tr>
            <tr>
                <th scope="row">3</th>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
                <td>Cell</td>
            </tr>
        </tbody>
    </table>
</div>
```
## Accessibility
Make sure:
- you use [table headers](#table-headers) when applicable
- you test your tables in smaller viewports, for example on mobile devices. Consider using a [responsive table](#responsive-tables) variant 
