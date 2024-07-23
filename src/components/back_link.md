---
title: "Back Link"
date: 2022-02-01 00:01:01Z
description: "Use the back link component to help users go back to the previous page in a multi-page transaction."
---

Use the back link component to help users go back to the previous page in a multi-page transaction.

Although browsers have a back button, some sites break when you use it - so many users avoid it, instead of losing their progress in a service. Also, not all users are aware of the back button.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
    <a class="govcy-back-link" href="#">Back</a>
</div>

*HTML code*
```html
<a class="govcy-back-link" href="#">Back</a>
```

## When to use this component
Always include the back link component on [questions pages](../../patterns/question_pages/) and recurring pages. This gives the ability to the users to go back and change their decision.

You can include a back link on other pages within a multi-page transaction, if it makes sense to do so.

## When not to use this component

Never use the back link component together with [breadcrumbs](../breadcrumbs/). If necessary, you should do research with your users to learn which they find more helpful in your service.

Do not use the back component when the user has performed an action they should only do once, like make a payment or complete an application. The browser back button should still work, but show the user a sensible message rather than let them perform the action again.

## How it works
Always place back links at the top of a page, in the [Before main](../../getting-started/page-template/#sections) section. Placing them here means that the ‘Skip to main content’ link allows the user to skip all navigation links, including the back link.

Make sure the link takes users to the previous page they were on, in the state they last saw it. Where possible, ensure it works even when JavaScript is not available.

If this is not possible, you should hide the back link when JavaScript is not available.

Do not break the browser back button. Make sure it takes users to the previous page they were on, in the state they last saw it.

### Component text
Use the following text:
- In English: `Back`
- In Greek: `Πίσω`

## Accessibility
Make sure: 
- if a user decides to go back to a previous page, information they have already entered is pre-populated
- if the information is no longer valid, or when pre-populating would be a major safety or security concern, do not pre-populate
- no other interactive elements are too close to the back link. This is to make sure users can easily interact with the back link. 