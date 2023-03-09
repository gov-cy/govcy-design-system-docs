---
title: "Names"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
---
Follow this pattern whenever you need to ask for a user’s name .

## How it works

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="full-name">Full name</label>
        <input class="govcy-text-input" id="full-name" name="full-name" type="text" spellcheck="false" autocomplete="name">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <label class="govcy-label" for="full-name">Full name</label>
        <input class="govcy-text-input" id="full-name" name="full-name" type="text" spellcheck="false" autocomplete="name">
    </div>
</form>
```

When asking users for their name, you must make it clear why you’re asking.

Make sure the field is long enough to accommodate the names of your users. Support all the characters users may need to enter.

Make it clear whether you need someone’s common name, or their name as it’s written on official documents such as a passport.

Help users to enter a valid email address by:
- allowing users to paste the name
- setting the `spellcheck` attribute to `false` so that browsers do not spellcheck the email address
- setting the `autocomplete` attribute to `name`. If you are asking users to enter their name in multiple fields, set the autocomplete attribute on both fields using: `given-name` for fields labelled ‘First name’ and `family-name` for fields labelled ‘Last name’

### Single or multiple name fields
Use single or multiple fields depending on your user’s needs. Not everyone’s name fits the first-name, last-name format. Using multiple name fields mean there’s more risk that a person’s name will not fit the format you’ve chosen and that it is entered incorrectly.

A single name field can accommodate the broadest range of name types, but means you cannot reliably extract parts of a name.

Label single name fields:
- ‘Full name’

For multiple name fields, use:
- ‘First name’
- ‘Last name’

### Show errors
Error messages should follow the guidance in [error message](../../components/error_message) as shown in the example below.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="full-name-2">Full name</label>
        <p class="govcy-input-error-msg" id="error2"><span class="govcy-visually-hidden-error">Error: </span>Name is required</p>
        <input class="govcy-text-input govcy-text-input-error" id="full-name-2" name="full-name-2" type="text" spellcheck="false" autocomplete="name" aria-describedby="error2">
    </div>
</form>
</div>

*Sample HTML Code*

```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control govcy-form-control-error">
        <label class="govcy-label" for="full-name-2">Full name</label>
        <p class="govcy-input-error-msg" id="error2"><span class="govcy-visually-hidden-error">Error: </span>Name is required</p>
        <input class="govcy-text-input govcy-text-input-error" id="full-name-2" name="full-name-2" type="text" spellcheck="false" autocomplete="name" aria-describedby="error2">
    </div>
</form>
```