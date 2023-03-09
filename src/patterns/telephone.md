---
title: "Telephone"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
---
Follow this pattern whenever you need to ask for a telephone address.

## How it works

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in-tel">Cyprus telephone number</label>
        <span class="govcy-hint" id="tel-hint">We’ll only use this for this application</span>
        <input class="govcy-text-input govcy-text-input-char_20" id="in-tel" name="in-tel" type="tel" spellcheck="false" aria-describedby="tel-hint" autocomplete="tel">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="in-tel">Cyprus telephone number</label>
        <span class="govcy-hint" id="tel-hint">We’ll only use this for this application</span>
        <input class="govcy-text-input govcy-text-input-char_20" id="in-tel" name="in-tel" type="tel" spellcheck="false" aria-describedby="tel-hint" autocomplete="tel">
    </div>
</form>
```

When asking users for their telephone, you must make it clear why you’re asking.

Users should be allowed to enter telephone numbers in whatever format is familiar to them. You should allow for additional spaces, hyphens, brackets and dashes, and be able to accommodate country and area codes.

Make it clear what type of telephone number you need whether that is a Cypriot, international or mobile telephone number.

Help users to enter a valid tel address by:
- checking they have entered the correct format
- allowing users to paste the telephone address
- setting the `type` attribute to `tel` so that devices display the correct keyboard
- setting the `spellcheck` attribute to `false` so that browsers do not spellcheck the telephone
- setting the `autocomplete` attribute to `tel`. This lets browsers autofill the telephone on a user’s behalf if they’ve entered it previously.

### When to ask for repeat or loop 
Only ask users to repeat their telephone if your user research shows it to be effective.

If telphone is an essential part of your service - for example for two step authentication - you can confirm whether the user has access to the telephone they give you using an sms confirmation loop. However, these are disruptive and should be avoided as far as possible.

### Show errors
Error messages should follow the guidance in [error message](../../components/error_message) as shown in the example below.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="in-tel-2">Telephone Number</label>
        <p class="govcy-input-error-msg" id="error2"><span class="govcy-visually-hidden-error">Error: </span>Enter a telephone number in the correct format, like 99 123456</p>
        <input class="govcy-text-input govcy-text-input-char_20 govcy-text-input-error" id="in-tel-2" name="in-tel-2" type="tel" spellcheck="false" aria-describedby="tel-hint" autocomplete="tel" aria-describedby="error2">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="in-tel-2">Telephone Number</label>
        <p class="govcy-input-error-msg" id="error2"><span class="govcy-visually-hidden-error">Error: </span>Enter a telephone number in the correct format, like 99 123456</p>
        <input class="govcy-text-input govcy-text-input-char_20 govcy-text-input-error" id="in-tel-2" name="in-tel-2" type="tel" spellcheck="false" aria-describedby="tel-hint" autocomplete="tel" aria-describedby="error2">
    </div>
</form>
```

### Displaying phone number

When displaying a submitted or stored international phone number (either in a text input, hyperlink or text) replace `00` with `+` as users are more familiar with these format.

*Sample HTML Code*

```html
<a href="tel:+4412345678">+4412345678</a>
```

When displaying a local phone number, make sure you include `+357` in the hyperlink. 


*Sample HTML Code*

```html
<a href="tel:+35722123456">22123456</a>
```

### Storing phone number

If the phone numbers will be used to send notifications, prefer to store them in the following form:

```json
00[county code][local phone number]
``` 
This format will reduce the risk of unsuccessful SMS being sent by a notification gateway.

To convert a phone number to the preferred stored format:

1. Remove space and `-` dash characters.
2. If the 1st character is `+` replace it with `00`.
3. If phone doesn’t start with `00` add `00357` at the start of the number.

The preferred stored format also makes it easier to perform validations such as:

- Validating that the phone number consists of only digits with 8 to 15 digits length.
- Validating if they are Cypriot phone number for numbers starting with `00357` or International for the rest.
- Validating that the phone number is a mobile number (if mobile number is required).

Here are some examples of the Preferred stored and Display format :

| Input by user          | Preferred stored format  | Display form         |
| -----------------------| -------------------------------- | ---------------------   |
| 99 123456              | 0035799123456               | +35799123456    |
| +44-1234 567           | 00441234567                    | +441234567        |
| 001 1234 567           | 0011234567                      | +11234567           |
| 00357 99123456         | 0035799123456                | +35799123456    |

{.govcy-table}
