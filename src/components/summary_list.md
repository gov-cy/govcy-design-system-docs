---
title: "Summary list"
date: 2022-02-01 00:01:01Z
description: "Use the summary list to summarise information, for example, a user’s responses at the end of a service."
---
Use the summary list to summarise information, for example, a user’s responses at the end of a service.

## When to use this component
Use the summary list component to present pairs of related information, known as key-value pairs, in a list. The key is a description or label of a piece of information, like ‘Name’, and the value is the piece of information itself, like ‘John Smith’.

You can use it to display metadata like ‘Last updated’ with a date like ‘22 June 2018’, or to summarise a user’s responses at the end of a service with the [check answers](../../patterns/check_answers/) pattern or at the end of a section like in the [add multiple things](../../patterns/multiple_things/) pattern.

## When not to use this component
The summary list uses the description list (`<dl>`) HTML element, so only use it to present information that has a key and at least one value.  

Do not use it for tabular data or a simple list of information or tasks, like a [task list](../../patterns/task-list-page/). For those use a `<table>`, `<ul>` or `<ol>`.

## How it works
The component should only exist in the [main section](../../getting-started/page-template/#sections). 

Each row of a summary list is made up of a:

- ‘key’ that’s a description or label of a piece of information, like “Name”
- ‘value’ which is the piece of information itself, such as “John Smith”

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            10 March 1990
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Address
        </dt>
        <dd class="govcy-summary-list-value">
            50 Enton Street<br>Nicosia<br>2066
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Contact details
        </dt>
        <dd class="govcy-summary-list-value">
            99123456<br/>abc@windowslive.com
        </dd>
    </div>
</dl>
</div>

*HTML code*
```html
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            10 March 1990
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Address
        </dt>
        <dd class="govcy-summary-list-value">
            50 Enton Street<br>Nicosia<br>2066
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Contact details
        </dt>
        <dd class="govcy-summary-list-value">
            99123456<br/>abc@windowslive.com
        </dd>
    </div>
</dl>
```
### Adding actions
You can add actions to a summary list, like a ‘Change’ link to let users go back and edit their answer.

For sighted users, the actions get their context from the other content in the row they appear in.

Assistive technology users, like those who use a screen reader, may hear the links out of context and not know what they do. To give more context, use the `govcy-visually-hidden` class with hidden text to the links. This means a screen reader user will hear a meaningful action, like ‘Change name’ or ‘Change date of birth’.

If research shows that users prefer to print the summary list, consider using the `govcy-d-print-none` on the links to hide the action links on the print media.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> name</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            10 March 1990
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> date of birth</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Address
        </dt>
        <dd class="govcy-summary-list-value">
            50 Enton Street<br>Nicosia<br>2066
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> address</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Contact details
        </dt>
        <dd class="govcy-summary-list-value">
            99123456<br/>abc@windowslive.com
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> contact details</span></a>
        </dd>
    </div>
</dl>
</div>

*HTML code*
```html
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> name</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            10 March 1990
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> date of birth</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Address
        </dt>
        <dd class="govcy-summary-list-value">
            50 Enton Street<br>Nicosia<br>2066
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> address</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Contact details
        </dt>
        <dd class="govcy-summary-list-value">
            99123456<br/>abc@windowslive.com
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> contact details</span></a>
        </dd>
    </div>
</dl>
```
#### Multiple actions
To add multiple actions, use inline unordered lists as follows:

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
        <dd class="govcy-summary-list-actions">
            <ul class="list-inline govcy-my-0">
                <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> name</span></a></li>
                <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> name</span></a></li>
            </ul>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            10 March 1990
        </dd>
        <dd class="govcy-summary-list-actions">
            <ul class="list-inline govcy-my-0">
                <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> date of birth</span></a></li>
                <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> date of birth</span></a></li>
            </ul>
        </dd>
    </div>
</dl>
</div>

*HTML code*
```html
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
        <dd class="govcy-summary-list-actions">
            <ul class="list-inline govcy-my-0">
                <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> name</span></a></li>
                <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> name</span></a></li>
            </ul>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            10 March 1990
        </dd>
        <dd class="govcy-summary-list-actions">
            <ul class="list-inline govcy-my-0">
                <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> date of birth</span></a></li>
                <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> date of birth</span></a></li>
            </ul>
        </dd>
    </div>
</dl>
```

### Removing borders
The summary list includes separating borders to help users by joining the information on each row and its action together.

Think carefully before you remove row borders. Borders help many users find and read information that’s laid out in rows, especially users who zoom in on pages or use assistive technologies to magnify their screen.

Never remove row borders from the [check your answers page](../../patterns/check_answers/) summary list. 

If your summary list does not have any actions, you can choose to remove the separating borders with the `govcy-summary-list-no-border` class.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<dl class="govcy-summary-list govcy-summary-list-no-border">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Telephone
        </dt>
        <dd class="govcy-summary-list-value">
            99123456
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Address
        </dt>
        <dd class="govcy-summary-list-value">
            50 Enton Street<br>Nicosia<br>2066
        </dd>
    </div>
</dl>
</div>

*HTML code*
```html
<dl class="govcy-summary-list govcy-summary-list-no-border">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Telephone
        </dt>
        <dd class="govcy-summary-list-value">
            99123456
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Address
        </dt>
        <dd class="govcy-summary-list-value">
            50 Enton Street<br>Nicosia<br>2066
        </dd>
    </div>
</dl>
```
### Showing missing (or not entered) information
In some contexts, you might need to show rows that have missing information. This can happen when:

- a user returns to an incomplete journey
- you’ve added or changed the questions in a service.

Show a link to the appropriate question page in the `value` column so the user can enter the missing information, instead of showing a ‘change’ link on that row

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> name</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            10 March 1990
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> date of birth</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Address
        </dt>
        <dd class="govcy-summary-list-value">
            <a href="#">Enter address</a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Contact details
        </dt>
        <dd class="govcy-summary-list-value">
            <a href="#">Enter contact details</a>
        </dd>
    </div>
</dl>
</div>

*HTML code*
```html
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> name</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            10 March 1990
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> date of birth</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Address
        </dt>
        <dd class="govcy-summary-list-value">
            <a href="#">Enter address</a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Contact details
        </dt>
        <dd class="govcy-summary-list-value">
            <a href="#">Enter contact details</a>
        </dd>
    </div>
</dl>
    
```
### Showing complex information
Avoid using complex information in your summary lists as users might find it hard to understand complex data structures. Try to simplify the data that need to be summarised to simple key-value pairs. 

There may be cases though where you will want to summarise more complex information. 

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
		<span class="govcy-warning-text govcy-d-inline">
			<span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
			Restrict the summarised data structure to key-value, key-object and key-array of objects. Anything more complex will be very hard for users to understand.
		</p>
    </div>
</div>

Use the following classes to display key-object and key-array of objects values
- For the object `<dl>` use the `govcy-summary-list-row-internal` class
- For the object's key `<dt>` use the `govcy-summary-list-key-internal` class
- For the object's value `<dd>` use the `govcy-summary-list-value-internal` class

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> name</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            <a href="#">Enter date of birth</a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Contact telephone
        </dt>
        <dd class="govcy-summary-list-value">
            99123456
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> contact telephone</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Bank Account
        </dt>
        <dd class="govcy-summary-list-value">
            <dl class="govcy-summary-list-row-internal">
                <dt class="govcy-summary-list-key-internal">Account name</dt>
                <dd class="govcy-summary-list-value-internal">Andreas Andreou current</dd>
                <dt class="govcy-summary-list-key-internal">Bank</dt>
                <dd class="govcy-summary-list-value-internal">Bank of Cyprus</dd>
                <dt class="govcy-summary-list-key-internal">Account number</dt>
                <dd class="govcy-summary-list-value-internal">1234567890</dd>
            </dl>
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> bank account</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Payments <span class="govcy-visually-hidden"> 2 entries</span>
        </dt>
        <dd class="govcy-summary-list-value">
            <dl class="govcy-summary-list-row-internal">
                <dt><span class="govcy-visually-hidden">Entry 1</span></dt>
                <dt class="govcy-summary-list-key-internal">Date</dt>
                <dd class="govcy-summary-list-value-internal">10 February 2024</dd>
                <dt class="govcy-summary-list-key-internal">Description</dt>
                <dd class="govcy-summary-list-value-internal">Electricity bill payment</dd>
                <dt class="govcy-summary-list-key-internal">Amount</dt>
                <dd class="govcy-summary-list-value-internal">€200</dd>
            </dl>
            <dl class="govcy-summary-list-row-internal">
                <dt><span class="govcy-visually-hidden">Entry 2</span></dt>
                <dt class="govcy-summary-list-key-internal">Date</dt>
                <dd class="govcy-summary-list-value-internal">16 February 2024</dd>
                <dt class="govcy-summary-list-key-internal">Description</dt>
                <dd class="govcy-summary-list-value-internal">Telephone bill payment</dd>
                <dt class="govcy-summary-list-key-internal">Amount</dt>
                <dd class="govcy-summary-list-value-internal">50</dd>
            </dl>
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> payments</span></a>
        </dd>
    </div>
</dl>
</div>

*HTML code*
```html
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Name
        </dt>
        <dd class="govcy-summary-list-value">
            Andreas Andreou
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> name</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Date of birth
        </dt>
        <dd class="govcy-summary-list-value">
            <a href="#">Enter date of birth</a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Contact telephone
        </dt>
        <dd class="govcy-summary-list-value">
            99123456
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> contact telephone</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Bank Account
        </dt>
        <dd class="govcy-summary-list-value">
            <dl class="govcy-summary-list-row-internal">
                <dt class="govcy-summary-list-key-internal">Account name</dt>
                <dd class="govcy-summary-list-value-internal">Andreas Andreou current</dd>
                <dt class="govcy-summary-list-key-internal">Bank</dt>
                <dd class="govcy-summary-list-value-internal">Bank of Cyprus</dd>
                <dt class="govcy-summary-list-key-internal">Account number</dt>
                <dd class="govcy-summary-list-value-internal">1234567890</dd>
            </dl>
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> bank account</span></a>
        </dd>
    </div>
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Payments <span class="govcy-visually-hidden"> 2 entries</span>
        </dt>
        <dd class="govcy-summary-list-value">
            <dl class="govcy-summary-list-row-internal">
                <dt><span class="govcy-visually-hidden">Entry 1</span></dt>
                <dt class="govcy-summary-list-key-internal">Date</dt>
                <dd class="govcy-summary-list-value-internal">10 February 2024</dd>
                <dt class="govcy-summary-list-key-internal">Description</dt>
                <dd class="govcy-summary-list-value-internal">Electricity bill payment</dd>
                <dt class="govcy-summary-list-key-internal">Amount</dt>
                <dd class="govcy-summary-list-value-internal">€200</dd>
            </dl>
            <dl class="govcy-summary-list-row-internal">
                <dt><span class="govcy-visually-hidden">Entry 2</span></dt>
                <dt class="govcy-summary-list-key-internal">Date</dt>
                <dd class="govcy-summary-list-value-internal">16 February 2024</dd>
                <dt class="govcy-summary-list-key-internal">Description</dt>
                <dd class="govcy-summary-list-value-internal">Telephone bill payment</dd>
                <dt class="govcy-summary-list-key-internal">Amount</dt>
                <dd class="govcy-summary-list-value-internal">50</dd>
            </dl>
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> payments</span></a>
        </dd>
    </div>
</dl>
```
#### Making arrays screen reader friendly
When displaying key-array of objects pairs, use the `govcy-visually-hidden` on the parent key to inform the users with screen readers, how many entries they should anticipate, and at the beginning of each entry, to indicate the current entry.

For example:
*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Payments <span class="govcy-visually-hidden"> 2 entries</span>
        </dt>
        <dd class="govcy-summary-list-value">
            <dl class="govcy-summary-list-row-internal">
                <dt><span class="govcy-visually-hidden">Entry 1</span></dt>
                <dt class="govcy-summary-list-key-internal">Date</dt>
                <dd class="govcy-summary-list-value-internal">10 February 2024</dd>
                <dt class="govcy-summary-list-key-internal">Description</dt>
                <dd class="govcy-summary-list-value-internal">Electricity bill payment</dd>
                <dt class="govcy-summary-list-key-internal">Amount</dt>
                <dd class="govcy-summary-list-value-internal">€200</dd>
            </dl>
            <dl class="govcy-summary-list-row-internal">
                <dt><span class="govcy-visually-hidden">Entry 2</span></dt>
                <dt class="govcy-summary-list-key-internal">Date</dt>
                <dd class="govcy-summary-list-value-internal">16 February 2024</dd>
                <dt class="govcy-summary-list-key-internal">Description</dt>
                <dd class="govcy-summary-list-value-internal">Telephone bill payment</dd>
                <dt class="govcy-summary-list-key-internal">Amount</dt>
                <dd class="govcy-summary-list-value-internal">50</dd>
            </dl>
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> payments</span></a>
        </dd>
    </div>
</dl>
</div>

*HTML code*
```html
<dl class="govcy-summary-list">
    <div class="govcy-summary-list-row">
        <dt class="govcy-summary-list-key">
            Payments <span class="govcy-visually-hidden"> 2 entries</span>
        </dt>
        <dd class="govcy-summary-list-value">
            <dl class="govcy-summary-list-row-internal">
                <dt><span class="govcy-visually-hidden">Entry 1</span></dt>
                <dt class="govcy-summary-list-key-internal">Date</dt>
                <dd class="govcy-summary-list-value-internal">10 February 2024</dd>
                <dt class="govcy-summary-list-key-internal">Description</dt>
                <dd class="govcy-summary-list-value-internal">Electricity bill payment</dd>
                <dt class="govcy-summary-list-key-internal">Amount</dt>
                <dd class="govcy-summary-list-value-internal">€200</dd>
            </dl>
            <dl class="govcy-summary-list-row-internal">
                <dt><span class="govcy-visually-hidden">Entry 2</span></dt>
                <dt class="govcy-summary-list-key-internal">Date</dt>
                <dd class="govcy-summary-list-value-internal">16 February 2024</dd>
                <dt class="govcy-summary-list-key-internal">Description</dt>
                <dd class="govcy-summary-list-value-internal">Telephone bill payment</dd>
                <dt class="govcy-summary-list-key-internal">Amount</dt>
                <dd class="govcy-summary-list-value-internal">50</dd>
            </dl>
        </dd>
        <dd class="govcy-summary-list-actions">
            <a href="#">Change<span class="govcy-visually-hidden"> payments</span></a>
        </dd>
    </div>
</dl>
```
### Showing repeated information without a key
In some contexts, you might need to show values of the same type without showing the key. In such cases, the key is usually mentioned on the `<h1>` of the page, so there is no need to repeat it. 

This can happen when implementing the [add multiple things](../../patterns/multiple_things/) summary page.

In such cases use a `<table>` instead of a `<dl>`.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<h1>Confirm telephone numbers</h1>
<table class="govcy-table govcy-table-responsive-vertical">
    <tbody>
        <tr class="govcy-summary-list-row-internal">
            <td>
                <span class="govcy-visually-hidden">Entry 1 </span>+35799123456
            </td>
            <td class="govcy-text-sm-start govcy-text-md-end">
                <ul class="list-inline govcy-my-0">
                    <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> +35799123456</span></a></li>
                    <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> +35799123456</span></a></li>
                </ul>
            </td>
        </tr>
        <tr class="govcy-summary-list-row-internal">
            <td>
                <span class="govcy-visually-hidden">Entry 2 </span>+35799654321
            </td>
            <td class="govcy-text-sm-start govcy-text-md-end">
                <ul class="list-inline govcy-my-0">
                    <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> +35799654321</span></a></li>
                    <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> +35799654321</span></a></li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<h1>Confirm telephone numbers</h1>
<table class="govcy-table govcy-table-responsive-vertical">
    <tbody>
        <tr class="govcy-summary-list-row-internal">
            <td>
                <span class="govcy-visually-hidden">Entry 1 </span>+35799123456
            </td>
            <td class="govcy-text-sm-start govcy-text-md-end">
                <ul class="list-inline govcy-my-0">
                    <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> +35799123456</span></a></li>
                    <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> +35799123456</span></a></li>
                </ul>
            </td>
        </tr>
        <tr class="govcy-summary-list-row-internal">
            <td>
                <span class="govcy-visually-hidden">Entry 2 </span>+35799654321
            </td>
            <td class="govcy-text-sm-start govcy-text-md-end">
                <ul class="list-inline govcy-my-0">
                    <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> +35799654321</span></a></li>
                    <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> +35799654321</span></a></li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>
```

Here is an example with showing more complex information. 

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table govcy-table-responsive-vertical">
    <tbody>
        <tr class="govcy-summary-list-row-internal">
            <td>
                <dl class="govcy-summary-list-row-internal">
                    <dt><span class="govcy-visually-hidden">Entry 1</span></dt>
                    <dt class="govcy-summary-list-key-internal">Date</dt>
                    <dd class="govcy-summary-list-value-internal">10 February 2024</dd>
                    <dt class="govcy-summary-list-key-internal">Description</dt>
                    <dd class="govcy-summary-list-value-internal">Electricity bill payment</dd>
                    <dt class="govcy-summary-list-key-internal">Amount</dt>
                    <dd class="govcy-summary-list-value-internal">€200</dd>
                </dl>
            </td>
            <td class="govcy-text-sm-start govcy-text-md-end">
                <ul class="list-inline govcy-my-0">
                    <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> Entry 1</span></a></li>
                    <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> Entry 1</span></a></li>
                </ul>
            </td>
        </tr>
        <tr class="govcy-summary-list-row-internal">
            <td>
                <dl class="govcy-summary-list-row-internal">
                    <dt><span class="govcy-visually-hidden">Entry 2</span></dt>
                    <dt class="govcy-summary-list-key-internal">Date</dt>
                    <dd class="govcy-summary-list-value-internal">16 February 2024</dd>
                    <dt class="govcy-summary-list-key-internal">Description</dt>
                    <dd class="govcy-summary-list-value-internal">Telephone bill payment</dd>
                    <dt class="govcy-summary-list-key-internal">Amount</dt>
                    <dd class="govcy-summary-list-value-internal">50</dd>
                </dl>
            </td>
            <td class="govcy-text-sm-start govcy-text-md-end">
                <ul class="list-inline govcy-my-0">
                    <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> Entry 2</span></a></li>
                    <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> Entry 2</span></a></li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table govcy-table-responsive-vertical">
    <tbody>
        <tr class="govcy-summary-list-row-internal">
            <td>
                <dl class="govcy-summary-list-row-internal">
                    <dt><span class="govcy-visually-hidden">Entry 1</span></dt>
                    <dt class="govcy-summary-list-key-internal">Date</dt>
                    <dd class="govcy-summary-list-value-internal">10 February 2024</dd>
                    <dt class="govcy-summary-list-key-internal">Description</dt>
                    <dd class="govcy-summary-list-value-internal">Electricity bill payment</dd>
                    <dt class="govcy-summary-list-key-internal">Amount</dt>
                    <dd class="govcy-summary-list-value-internal">€200</dd>
                </dl>
            </td>
            <td class="govcy-text-sm-start govcy-text-md-end">
                <ul class="list-inline govcy-my-0">
                    <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> Entry 1</span></a></li>
                    <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> Entry 1</span></a></li>
                </ul>
            </td>
        </tr>
        <tr class="govcy-summary-list-row-internal">
            <td>
                <dl class="govcy-summary-list-row-internal">
                    <dt><span class="govcy-visually-hidden">Entry 2</span></dt>
                    <dt class="govcy-summary-list-key-internal">Date</dt>
                    <dd class="govcy-summary-list-value-internal">16 February 2024</dd>
                    <dt class="govcy-summary-list-key-internal">Description</dt>
                    <dd class="govcy-summary-list-value-internal">Telephone bill payment</dd>
                    <dt class="govcy-summary-list-key-internal">Amount</dt>
                    <dd class="govcy-summary-list-value-internal">50</dd>
                </dl>
            </td>
            <td class="govcy-text-sm-start govcy-text-md-end">
                <ul class="list-inline govcy-my-0">
                    <li class="list-inline-item"><a href="#">Change<span class="govcy-visually-hidden"> Entry 2</span></a></li>
                    <li class="list-inline-item"><a href="#">Remove<span class="govcy-visually-hidden"> Entry 2</span></a></li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>
```
### Component text
Use the following text for the action links:

| Link                           | English                                         | Greek                                                              |
| ------------------------------ | ----------------------------------------------- | ------------------------------------------------------------------ |
| **Change**                     | Change                                          | Αλλαγή                                                             |
| **Remove**                     | Remove                                          | Διαγραφή                                                           |
| **Enter missing information**  | Enter ...<br><br>Example: Enter contact details | Εισαγάγετε ...<br><br>Example: Εισαγάγετε τα στοιχεία επικοινωνίας |
| **Entry screen reader text**   | Entry                                           | Καταχώρηση                                                         |
| **Entries screen reader text** | Entries                                         | Καταχωρήσεις                                                       |

{.govcy-table}

## Accessibility
Make sure:
- you use the `govcy-visually-hidden` class to give each action link a unique and descriptive name and help screen readers users. For example: `<a href=''>Change <span class='govcy-visually-hidden'> address</span></a>`
- if a user decides to go back to a previous answer through an action, make sure information they have already entered is pre-populated.
- If you are displaying arrays use the `govcy-visually-hidden` class to make [arrays screen reader friendly](#making-arrays-screen-reader-friendly).