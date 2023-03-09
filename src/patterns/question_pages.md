---
title: "Question pages"
date: 2022-02-01 00:01:02Z
tags: "pages"
---
This pattern explains when to use question pages and what elements they need to include. 

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<section class="govcy-container govcy-mb-4" id="beforeMainContainer">
    <span class="bi bi-chevron-left"></span>
    <a href="#" class="govcy-back-link">Back</a>
</section>
<!--main-->
<main class="govcy-container" id="mainContainer">
    <form action="" class="govcy-form" novalidate>
        <fieldset class="govcy-fieldset govcy-mb-4">
            <legend class="govcy-legend"><h1>Where do you live?</h1></legend>
            <div class="govcy-form-control">
                <label class="govcy-radio">Cyprus
                    <input class="govcy-radio-input" type="radio" name="radio">
                    <span class="govcy-radio-checked"></span>
                </label>
                <label class="govcy-radio">Abroad
                    <input class="govcy-radio-input" type="radio" name="radio">
                    <span class="govcy-radio-checked"></span>
                </label>
            </div>
        </fieldset>
    <button type="button" class="govcy-btn-primary govcy-mb-4">Next</button>
    </form>
</main>
</div>

## When to use this pattern
Follow this pattern whenever you need to ask users questions within your service.

You should make sure you know why you’re asking every question and only ask users for information you really need.

If you ask for optional information:
- in most contexts, add ‘(optional)’ to the labels of optional fields
- for radios and checkboxes, add ‘(optional)’ to the legend

Never mark mandatory fields with asterisks.

On every question page you should:
- make sure it’s clear to users why you’re asking each question
- allow users to answer ‘I do not know’ or ‘I’m not sure’ if they are valid responses

## How it works
Question pages must include a:
- back link
- page heading
- continue button

If research it’s helpful for users, you can also include a progress indicator.

### Back link
Always include a [back link](../../components/back_link) at the top of question pages to reassure them it’s possible to go back and change previous answers.

However, do not break the browser back button. Make sure it takes users to the previous page they were on, in the state they last saw it.

An exception to this is when the user has performed an action they should only do once, like make a payment or complete an application. The browser back button should still work, but show the user a sensible message rather than let them perform the action again.

### Page headings
Page headings can be questions or statements.

#### Start by asking one question per page
Asking just one question per question page helps users understand what you’re asking them to do, and focus on the specific question and its answer.

To help you follow this approach, you can set the contents of a `<legend>` or `<label>` for a page’s input as the page heading. This is good practice as it means that users of screen readers will only hear the contents once.

Read more about why and [how to set labels and legends as headings](../labels_and_legend_headings).

Do not use the same page heading across multiple pages.

The page heading should relate specifically to the information being asked for on the current page, not any higher-level section the page is part of.

#### Asking complex questions
Use [hint text](../hint_text) if you need to give a small explanation. 

Do not use hint text if you need to give a lengthy explanation with lists and paragraphs. Screen readers read out the entire text when users interact with the form element. This could frustrate users if the text is long.

Do not use links in hint text. While screen readers will read out the link text when describing the field, they will not tell users the text is a link.

If you’re asking a question that needs a detailed explanation, use:
- a `<h1>` heading that’s a statement (for example, ‘Eligibility through SI contributions from Abroad’) rather than a question
- whatever mix of text, paragraphs, lists and examples best explains your question to users
- a label, above the form input, that asks users a specific question – for example, ‘Are there Social Insurance contributions in another country?’

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<section class="govcy-container govcy-mb-4" id="beforeMainContainer">
    <span class="bi bi-chevron-left"></span>
    <a href="#" class="govcy-back-link">Back</a>
</section>
<!--main-->
<main class="govcy-container" id="mainContainer">
    <h1>Eligibility through SI contributions from Abroad</h1>
    <p>You may still ne eligible, if there are social insurance contributions in another country.</p>
    <form action="" class="govcy-form" novalidate>
        <fieldset class="govcy-fieldset govcy-mb-4">
            <legend class="govcy-legend">Are there Social Insurance Contributions in another country?</legend>
            <div class="govcy-form-control">
                <label class="govcy-radio">Yes
                    <input class="govcy-radio-input" type="radio" name="radio">
                    <span class="govcy-radio-checked"></span>
                </label>
                <label class="govcy-radio">No
                    <input class="govcy-radio-input" type="radio" name="radio">
                    <span class="govcy-radio-checked"></span>
                </label>
            </div>
        </fieldset>
    <button type="button" class="govcy-btn-primary govcy-mb-4">Next</button>
    </form>
</main>
</div>

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<section class="govcy-container govcy-mb-4" id="beforeMainContainer">
    <span class="bi bi-chevron-left"></span>
    <a href="#" class="govcy-back-link">Back</a>
</section>
<!--main-->
<main class="govcy-container" id="mainContainer">
    <form action="" class="govcy-form" novalidate>
        <fieldset class="govcy-fieldset">
            <legend class="govcy-legend"><h1>Select your certificate</h1></legend>
            <div class="govcy-form-control">
                <label class="govcy-radio">Vaccination
                    <input class="govcy-radio-input" type="radio" name="radio">
                    <span class="govcy-radio-checked"></span>
                    <span class="govcy-hint govcy-mt-2">You have been vaccinated and this has been entered in the relevant database of the Ministry of Health.</span>
                </label>
                <label class="govcy-radio">Recovery
                    <input class="govcy-radio-input" type="radio" name="radio">
                    <span class="govcy-radio-checked"></span>
                    <span class="govcy-hint govcy-mt-2">You have been diagnosed with COVID-19, and the test result has been declared and entered in the relevant database of the Ministry of Health.</span>
                </label>
                <label class="govcy-radio">Laboratory testing
                    <input class="govcy-radio-input" type="radio" name="radio">
                    <span class="govcy-radio-checked"></span>
                    <span class="govcy-hint govcy-mt-2">You have been tested during the last 7 days for COVID-19 after undergoing a laboratory antigen rapid test or molecular methodology (RT-PCR) test and received a negative result which has been entered by the laboratory in the relevant database of the Ministry of Health.</span>
                </label>
            </div>
        </fieldset>
        <button type="button" class="govcy-btn-primary govcy-mb-4">Next</button>
    </form>
</main>
</div>

#### Asking multiple questions on a page
Sometimes it makes sense to group a number of related questions on the same page.

User research will tell you when you can group pages together. For example, if you’re designing an internal service for government users who need to repeat and switch between tasks quickly.

If you need to ask for multiple related things on a page, use a statement as the heading.

Use bold font weight for `<labels>` or `<legends>` that describe each field.

*Example*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<section class="govcy-container govcy-mb-4" id="beforeMainContainer">
    <span class="bi bi-chevron-left"></span>
    <a href="#" class="govcy-back-link">Back</a>
</section>
<!--main-->
<main class="govcy-container" id="mainContainer">
    <h1>Password Details</h1>
    <form action="" class="govcy-form" novalidate>
        <div class="govcy-form-control govcy-mb-4">
        <label class="govcy-label" for="passport">Passport Number</label>
        <input type="text" class="govcy-text-input" spellcheck="false" pattern="[0-9]*" inputmode="numeric" id="passport">
    </div>
    <fieldset class="govcy-fieldset govcy-mb-4">
        <div class="govcy-form-control">
            <legend class="govcy-label govcy-mb-1">Expiry Date</legend>
            <span class="govcy-hint govcy-mb-3">For example, 12 11 2027</span>
            <div class="govcy-d-flex">
                <div class="govcy-d-block">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day">Day</label>
                    <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" id="day">
                </div>
                <div class="govcy-d-block govcy-ml-2">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month">Month</label>
                    <input class="govcy-text-input govcy-text-input-char_3 govcy-p-2" placeholder="" maxlength="2" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" id="month">
                </div>
                <div class="govcy-d-block govcy-ml-2">
                    <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year">Year</label>
                    <input class="govcy-text-input govcy-text-input-char_6 govcy-p-3" placeholder="" maxlength="4" type="text" maxlength="2" pattern="[0-9]*" inputmode="numeric" id="year">
                </div>
            </div>
        </div>
    </fieldset>    
    <button type="button" class="govcy-btn-primary govcy-mb-4">Next</button>
    </form>
</main>
</div>

### Continue button
Make sure your ‘Continue’ button is:
- labelled ‘Continue’, not ‘Next’
- aligned to the left so users do not miss it
