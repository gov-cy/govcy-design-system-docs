---
"title" : "Table"
date: 2022-02-01 00:01:01Z
---
Use the table component to make information easier to compare and scan for users.

## When to use this component
Use the table component to let users compare information in rows and columns.

## When not to use this component
Never use the table component to layout content on a page. 

## How it works
You can use the HTML below to create a table component. 

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th>Property</th>
            <th>Value</th>
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
            <td>7361063</td>
        </tr>
    </tbody>
</table>
</div>

*Sample HTML Code*

```html
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th>Property</th>
            <th>Value</th>
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
            <td>7361063</td>
        </tr>
    </tbody>
</table>
```
### Table headers
Use table headers to tell users what the rows and columns represent. Use the `scope` attribute to help users of assistive technology distinguish between row and column headers.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table">
    <thead>
        <tr>
            <th scope="col">#</th>
            <th scope="col">First</th>
            <th scope="col">Last</th>
            <th scope="col">Handle</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">1</th>
            <td>Mark</td>
            <td>Otto</td>
            <td>@mdo</td>
        </tr>
        <tr>
            <th scope="row">2</th>
            <td>Jacob</td>
            <td>Thornton</td>
            <td>@fat</td>
        </tr>
        <tr>
            <th scope="row">3</th>
            <td colspan="2">Larry the Bird</td>
            <td>@twitter</td>
        </tr>
    </tbody>
</table>
</div>

*Sample HTML Code*

```html
<table class="govcy-table">
    <thead>
        <tr>
            <th scope="col">#</th>
            <th scope="col">First</th>
            <th scope="col">Last</th>
            <th scope="col">Handle</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">1</th>
            <td>Mark</td>
            <td>Otto</td>
            <td>@mdo</td>
        </tr>
        <tr>
            <th scope="row">2</th>
            <td>Jacob</td>
            <td>Thornton</td>
            <td>@fat</td>
        </tr>
        <tr>
            <th scope="row">3</th>
            <td colspan="2">Larry the Bird</td>
            <td>@twitter</td>
        </tr>
    </tbody>
</table>
```

### Numbers in a table
When comparing columns of numbers, align the numbers to the right in table cells.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
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

*Sample HTML Code*

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
Responsive tables allow tables to be scrolled horizontally with ease. Make any table responsive across all viewports by wrapping a `.govcy-table` with `.govcy-table-responsive`. 

Always use responsive tables, unless there is a specific reason not to. 

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
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

*Sample HTML Code*

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