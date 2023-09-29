---
title: "Currency amount"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
---
Follow this pattern whenever you need to display or ask users for an amount of money.

## How to ask

Use a [text input](../../components/text_input/) to allow users input the amount of money. Consider using an [appropriately-sized text input](../../components/text_input/#use-appropriately-sized-text-inputs), depending on the maximum length of the desired input. 

If you only allow whole numbers, use set the `inputmode` attribute to `numeric` to use the numeric keypad on devices with on-screen keyboards instead of `type=”number”`. 

*Example for whole numbers*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
    <form action="" class="govcy-form" novalidate> 
        <div class="govcy-form-control"> 
            <label class="govcy-label" for="in1">Enter your income (€)</label>  
            <input type="text" spellcheck="false" pattern="[0-9]*" inputmode="numeric" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in1">  
        </div> 
    </form> 
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate> 
    <div class="govcy-form-control"> 
        <label class="govcy-label" for="in1">Enter your income (€)</label>  
        <input type="text" spellcheck="false" pattern="[0-9]*" inputmode="numeric" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in1">  
    </div> 
</form>
``` 

If you allow decimal numbers, use `type=”text”`. Do not set the `inputmode` attribute to `decimal` as it causes some devices to bring up a keypad without a key for the decimal separator. 

*Example for decimal numbers*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
    <form action="" class="govcy-form" novalidate> 
        <div class="govcy-form-control"> 
            <label class="govcy-label" for="in2">Enter your income (€)</label>  
            <input type="text" spellcheck="false" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in2">  
        </div> 
    </form> 
</div>

*Sample HTML Code*
```html
<form action="" class="govcy-form" novalidate> 
    <div class="govcy-form-control"> 
        <label class="govcy-label" for="in2">Enter your income (€)</label>  
        <input type="text" spellcheck="false" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in2">  
    </div> 
</form> 
``` 

Allow the user to enter numbers with or without: 

- comma “,” as decimals separator (if allowed by the service) 

When validating the amount, ignore leading and ending spaces and make sure to ignore these characters when converting the amount to a number.

If your service does not allow decimals, consider if it is appropriate to allow decimals on user input and round up or down any amounts before validating and storing. 

Only allow the user to enter whole numbers, or numbers with one or 2 decimal places, for example, 10, 10,4 or 10,40. Do not allow numbers with more than 2 decimal places. 

For example, the following are valid amounts: 
- 123456 
- 123456,12 
- 1234567 
- 12 
- 123,2 
- 125 

## Displaying currency amounts 

When displaying stored or summitted amounts of money, they should start with the currency sign (for example “€” for EUR) and then the amount. The amount should be displayed with digit grouping separators (i.e. using “.” to separate thousands, millions and so on). If your service allows decimals (for example cents) display 2 decimal places. 

For example: 

- €123.456 
- €1.234.567 
- €123.456.789,12 
- €123,20 
- €12 

Screen readers have trouble recognizing the thousands and decimal separators in conjunction with a currency sign. When displaying the amounts, use a combination of `aria-label` and `aria-hidden=”true”` to help screen readers read the amount as a number. In `aria-label` the whole part of the amount should be written as integer and the digits part written as cents. For example:  

*In English* 
```html 
<div aria-label="1234566 euros and 30 cents">  
	<p aria-hidden="true">€1.234.566,30</p>  
</div> 
``` 

*In Greek*
```html 
<div aria-label="1234566 ευρώ και 30 σεντ">  
	<p aria-hidden="true">€1.234.566,30</p>  
</div> 
```

When filling up stored or submitted amounts of money within text inputs, they should appear in the form that is appropriate for input, without digit grouping separators (i.e. using “.” to separate thousands, millions and so on) and 2 decimal places. 

*Example of filled up currency amount inputs:*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
    <form action="" class="govcy-form" novalidate> 
        <div class="govcy-form-control"> 
            <label class="govcy-label" for="in3">Whole number (€)</label>  
            <input type="text" value="123456" spellcheck="false" pattern="[0-9]*" inputmode="numeric" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in3">  
        </div> 
        <div class="govcy-form-control"> 
            <label class="govcy-label" for="in4">Large decimal number (€)</label>  
            <input type="text" value="123456789,12" spellcheck="false" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in4">  
        </div> 
        <div class="govcy-form-control"> 
            <label class="govcy-label" for="in5">Small whole number (€)</label>  
            <input type="text" value="123" spellcheck="false" pattern="[0-9]*" inputmode="numeric" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in5">  
        </div> 
        <div class="govcy-form-control"> 
            <label class="govcy-label" for="in6">Small decimal number (€)</label>  
            <input type="text" value="123,02" spellcheck="false" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in6">  
        </div> 
        <div class="govcy-form-control"> 
            <label class="govcy-label" for="in7">Another small decimal number (€)</label>  
            <input type="text" value="123,20" spellcheck="false" class="govcy-text-input govcy-text-input-char_20" maxlength="20" id="in7">  
        </div> 
    </form> 
</div>


## Contribute
If you have used or researched this pattern, please  et us know what you found so we can make it better for everyone.  Send us an email at <a href="mailto:dsf@dits.dmrid.gov.cy" target="_blank">dsf@dits.dmrid.gov.cy</a> to get in touch. 

We are particularly interested in: 

- research on screen readers  

