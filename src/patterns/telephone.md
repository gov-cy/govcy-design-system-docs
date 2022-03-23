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
        <label class="govcy-label" for="input">Cyprus telephone number</label>
        <span class="govcy-hint" id="tel-hint">We’ll only use this for this application</span>
        <input class="govcy-text-input govcy-text-input-char_20" id="tel" name="tel" type="tel" spellcheck="false" aria-describedby="tel-hint" autocomplete="tel">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="input">Cyprus telephone number</label>
        <span class="govcy-hint" id="tel-hint">We’ll only use this for this application</span>
        <input class="govcy-text-input govcy-text-input-char_20" id="tel" name="tel" type="tel" spellcheck="false" aria-describedby="tel-hint" autocomplete="tel">
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
        <label class="govcy-label" for="input">Telephone Number</label>
        <span class="govcy-visually-hidden-error">Error: </span>
        <span class="govcy-input-error-msg">Enter a telephone number in the correct format, like 99 123456</span>
        <input class="govcy-text-input govcy-text-input-char_20 govcy-text-input-error" id="tel" name="tel" type="tel" spellcheck="false" aria-describedby="tel-hint" autocomplete="tel">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="input">Telephone Number</label>
        <span class="govcy-visually-hidden-error">Error: </span>
        <span class="govcy-input-error-msg">Enter a telephone number in the correct format, like 99 123456</span>
        <input class="govcy-text-input govcy-text-input-char_20 govcy-text-input-error" id="tel" name="tel" type="tel" spellcheck="false" aria-describedby="tel-hint" autocomplete="tel">
    </div>
</form>
```