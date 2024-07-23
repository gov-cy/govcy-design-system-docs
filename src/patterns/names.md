---
title: "Names"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
description: "Follow this pattern whenever you need to ask for a user’s name ."
---
You should follow this pattern whenever you need to ask for a user’s name.

## When to use this pattern
Only ask for people’s names if you need that information to deliver a service and you cannot get the information from data we already have (for example from an API call with the Civil Registry and Migration Department).  

## How it works
Make it as easy as possible for a user to enter their name.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<div class="govcy-form">
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="full-name">What is your full name?</label></h1>
        <input class="govcy-text-input" id="full-name" type="text" spellcheck="false" autocomplete="name">
    </div>
</div>
</div>

*HTML code*
```html
<form action="" class="govcy-form" novalidate>
    <div class="govcy-form-control">
        <h1><label class="govcy-label govcy-label-primary" for="full-name">What is your full name?</label></h1>
        <input class="govcy-text-input" id="full-name" type="text" spellcheck="false" autocomplete="name">
    </div>
</form>
```
When asking users for their name, you must make it clear why you’re asking.

Make sure the field is long enough to accommodate the names of your users. Support all the characters users may need to enter.

Make it clear whether you need someone’s common name, or their name as it’s written on official documents such as a passport.

Help users to enter a valid name by:
- allowing users to paste the name
- setting the `spellcheck` attribute to `false` so that browsers do not spellcheck the email address
- setting the `autocomplete` attribute to `name`. If you are asking users to enter their name in multiple fields, set the autocomplete attribute on both fields using: `given-name` for fields labelled ‘First name’ and `family-name` for fields labelled ‘Last name’.
### Single or multiple name fields
Use single or multiple fields depending on your user’s needs. Not everyone’s name fits the first-name, last-name format. Using multiple name fields mean there’s more risk that a person’s name will not fit the format you’ve chosen and that it is entered incorrectly.

A single name field can accommodate the broadest range of name types, but means you cannot reliably extract parts of a name.
### Avoid asking for a person’s title
Avoid asking users for their title.

It’s extra work for them and you’re asking them to potentially reveal their gender and marital status, which they may not want to do.

It’s also hard to predict the range of titles your users will have. If you have to ask for someone’s title, use an optional text input not a select.

Remember to correctly use people’s names in any resulting correspondence.
### Pattern text
Use the following text for name labels:

| Labels               | English    | Greek   |
| -------------------- | ---------- | ------- |
| **Single full name** | Full name  | Όνομα   |
| **First name**       | First name | Όνομα   |
| **Last name**        | Last name  | Επίθετο |

{.govcy-table}

### Error messages
Make sure to follow the instructions for [error messages](../../components/error_message) and [error summary](../../components/error_summary) when validating user input and to use the [text input error variant style](../../components/text_input/#error-messages).