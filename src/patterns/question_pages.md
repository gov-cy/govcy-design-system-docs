---
title: "Question pages"
date: 2022-02-01 00:01:02Z
tags: "pages"
description: "This pattern explains when to use question pages and what elements they need to include."
---
This pattern explains when to use question pages and what elements they need to include. Note that all code examples in this pattern shows only the `Before main` and `Main` sections. 

## When to use this pattern
Follow this pattern whenever you need to ask users questions within your service.

You should make sure you know why you’re asking every question and only ask users for information you really need.

## How it works
Before you start, review the design system’s [principles](../../getting-started/principles/) to design user-focused questions.

Question pages must include a:

- [back link](../../components/back_link/)
- [page heading (`<h1>`)](../../styles/typography/#headings) and questions
- [continue button](../../components/button/)

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<section class="govcy-container">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
 <div class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <form action="" class="govcy-form" novalidate>
                <fieldset class="govcy-fieldset">
                    <legend class="govcy-legend"><h1>Where do you live?</h1></legend>
                    <div class="govcy-form-control">
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option1" id="option1-cy">
                            <label class="govcy-label" for="option1-cy">Cyprus</label>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option1" id="option1-abroad">
                            <label class="govcy-label" for="option1-abroad">Abroad</label>
                        </div>
                    </div>
                </fieldset>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</div>
</div>

*HTML code*
```html
<!--beforeMain-->
<section class="govcy-container">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
 <main class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <form action="" class="govcy-form" novalidate>
                <fieldset class="govcy-fieldset">
                    <legend class="govcy-legend"><h1>Where do you live?</h1></legend>
                    <div class="govcy-form-control">
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option1" id="option1-cy">
                            <label class="govcy-label" for="option1-cy">Cyprus</label>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option1" id="option1-abroad">
                            <label class="govcy-label" for="option1-abroad">Abroad</label>
                        </div>
                    </div>
                </fieldset>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>
```
### Back link
Always include a [back link](../../components/back_link/) at the top of question pages to reassure the users it’s possible to go back and change previous answers.

### Page headings and questions
Page headings can be questions or statements. 

Prefer to split the questions of your service across multiple pages, with each page containing just one question. Research has shown that asking multiple questions in a page, can be more difficult for users to answer.

#### One question per page
Asking just one question per question page helps users understand what you’re asking them to do, and focus on the specific question and its answer.

When you’re asking just one question on a page, set the question as the page’s heading (`<h1>`), and as the `<label>` or `<legend>` for the input. This is good practice as it means that users of screen readers will only hear the contents once.

Read more about [single question page labels and legends](../../patterns/labels_and_legend_headings/#single-question-page).

Do not use the same page heading across multiple pages.

The page heading should relate specifically to the information being asked for on the current page, not any higher-level section the page is part of.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<section class="govcy-container">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
 <div class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <form action="" class="govcy-form" novalidate>
                <div class="govcy-form-control">
	                <h1><label class="govcy-label govcy-label-primary" for="email-in">What is your email address?</label></h1>
                    <span id="email-hint" class="govcy-hint">We’ll only use this email address for this application</span>
                    <input id="email-in" type="email" class="govcy-text-input" aria-describedby="email-hint" autocomplete="email" spellcheck="false">
                </div>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</div>
</div>

*HTML code*
```html
<!--beforeMain-->
<section class="govcy-container">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
 <main class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <form action="" class="govcy-form" novalidate>
                <div class="govcy-form-control">
	                <h1><label class="govcy-label govcy-label-primary" for="email-in">What is your email address?</label></h1>
                    <span id="email-hint" class="govcy-hint">We’ll only use this email address for this application</span>
                    <input id="email-in" type="email" class="govcy-text-input" aria-describedby="email-hint" autocomplete="email" spellcheck="false">
                </div>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>
```
#### Asking complex questions
Use hint text if you need to give a small explanation.

Do not use hint text if you need to give a lengthy explanation with lists and paragraphs. Screen readers read out the entire text when users interact with the form element. This could frustrate users if the text is long.

Do not use links in hint text. While screen readers will read out the link text when describing the field, they will not tell users the text is a link.

If you’re asking a question that needs a detailed explanation, use:

- a `<h1>` heading that’s a statement (for example, ‘Eligibility through SI contributions from Abroad’) rather than a question
- whatever mix of text, paragraphs, lists and examples best explains your question to users
- a label, above the form input, that asks users a specific question – for example, ‘Are there Social Insurance contributions in another country?’

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<section class="govcy-container">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
 <div class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <form action="" class="govcy-form" novalidate>
                <fieldset class="govcy-fieldset" aria-describedby="option4-fildset-hint">
                    <legend class="govcy-legend"><h1>Select your certificate</h1></legend>
                    <div class="govcy-form-control">
	                    <span class="govcy-hint" id="option4-fildset-hint">Different options will appear depending on your option.</span>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-1" aria-describedby="option4-1-hint">
                            <label class="govcy-label" for="option4-1">Vaccination</label>
                            <span id="option4-1-hint" class="govcy-hint">You have been vaccinated and this has been entered in the relevant database of the Ministry of Health.</span>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-2" aria-describedby="option4-2-hint">
                            <label class="govcy-label" for="option4-2">Recovery</label>
                            <span id="option4-2-hint" class="govcy-hint">You have been diagnosed with COVID-19, and the test result has been declared and entered in the relevant database of the Ministry of Health.</span>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-3" aria-describedby="option4-3-hint">
                            <label class="govcy-label" for="option4-3">Laboratory testing</label>
                            <span id="option4-3-hint" class="govcy-hint">You have been tested during the last 7 days for COVID-19 after undergoing a laboratory antigen rapid test or molecular methodology (RT-PCR) test and received a negative result which has been entered by the laboratory in the relevant database of the Ministry of Health.</span>
                        </div>
                    </div>
                </fieldset>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</div>
</div>

*HTML code*
```html
<!--beforeMain-->
<section class="govcy-container">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
 <main class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <form action="" class="govcy-form" novalidate>
                <fieldset class="govcy-fieldset" aria-describedby="option4-fildset-hint">
                    <legend class="govcy-legend"><h1>Select your certificate</h1></legend>
                    <div class="govcy-form-control">
	                    <span class="govcy-hint" id="option4-fildset-hint">Different options will appear depending on your option.</span>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-1" aria-describedby="option4-1-hint">
                            <label class="govcy-label" for="option4-1">Vaccination</label>
                            <span id="option4-1-hint" class="govcy-hint">You have been vaccinated and this has been entered in the relevant database of the Ministry of Health.</span>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-2" aria-describedby="option4-2-hint">
                            <label class="govcy-label" for="option4-2">Recovery</label>
                            <span id="option4-2-hint" class="govcy-hint">You have been diagnosed with COVID-19, and the test result has been declared and entered in the relevant database of the Ministry of Health.</span>
                        </div>
                        <div class="govcy-radio">
                            <input class="govcy-radio-input" type="radio" name="option4" id="option4-3" aria-describedby="option4-3-hint">
                            <label class="govcy-label" for="option4-3">Laboratory testing</label>
                            <span id="option4-3-hint" class="govcy-hint">You have been tested during the last 7 days for COVID-19 after undergoing a laboratory antigen rapid test or molecular methodology (RT-PCR) test and received a negative result which has been entered by the laboratory in the relevant database of the Ministry of Health.</span>
                        </div>
                    </div>
                </fieldset>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>
```
#### Asking multiple questions on a page
Sometimes it makes sense to group a number of related questions on the same page.

User research will tell you when you can group pages together. For example, if you’re designing an internal service for government users who need to repeat and switch between tasks quickly.

If you need to ask for multiple related things on a page, use a statement as the heading(`<h1>`).

Read more about [multiple question page labels and legends](../../patterns/labels_and_legend_headings/#multiple-question).

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<section class="govcy-container">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
 <div class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <h1>Password Details</h1>
            <form action="" class="govcy-form" novalidate>
                <div class="govcy-form-control">
                    <label class="govcy-label govcy-label-primary" for="pass-no">Passport Number</label>
                    <input id="pass-no" type="text" class="govcy-text-input govcy-text-input-char_20" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
                </div>
                <fieldset class="govcy-fieldset" role="group" aria-describedby="date2-hint">
                    <legend class="govcy-legend">Expiry Date</legend>
                    <div class="govcy-form-control">
                        <span class="govcy-hint" id="date2-hint">For example, 12 11 2027</span>
                        <div class="govcy-d-flex govcy-flex-wrap">
                            <div class="govcy-d-block govcy-mr-3">
                                <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_2">Day</label>
                                <input id="day_2" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric">
                            </div>
                            <div class="govcy-d-block govcy-mr-3">
                                <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_2">Month</label>
                                <select id="month_2" class="govcy-select">
                                    <option value="" selected=""></option>
                                    <option value="1">1 - January</option>
                                    <option value="2">2 - February</option>
                                    <option value="3">3 - March</option>
                                    <option value="4">4 - April</option>
                                    <option value="5">5 - May</option>
                                    <option value="6">6 - June</option>
                                    <option value="7">7 - July</option>
                                    <option value="8">8 - August</option>
                                    <option value="9">9 - September</option>
                                    <option value="10">10 - October</option>
                                    <option value="11">11 - November</option>
                                    <option value="12">12 - December</option>
                                </select>
                            </div>
                            <div class="govcy-d-block govcy-mr-3">
                                <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_2">Year</label>
                                <input id="year_2" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric">
                            </div>
                        </div>
                    </div>
                </fieldset>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</div>
</div>

*HTML code*
```html
<!--beforeMain-->
<section class="govcy-container">
    <a class="govcy-back-link" href="#">Back</a>
</section>
 <!--main-->
 <main class="govcy-container">
    <div class="govcy-row">
        <article class="govcy-col-8">
            <h1>Password Details</h1>
            <form action="" class="govcy-form" novalidate>
                <div class="govcy-form-control">
                    <label class="govcy-label govcy-label-primary" for="pass-no">Passport Number</label>
                    <input id="pass-no" type="text" class="govcy-text-input govcy-text-input-char_20" spellcheck="false" pattern="[0-9]*" inputmode="numeric" >
                </div>
                <fieldset class="govcy-fieldset" role="group" aria-describedby="date2-hint">
                    <legend class="govcy-legend">Expiry Date</legend>
                    <div class="govcy-form-control">
                        <span class="govcy-hint" id="date2-hint">For example, 12 11 2027</span>
                        <div class="govcy-d-flex govcy-flex-wrap">
                            <div class="govcy-d-block govcy-mr-3">
                                <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="day_2">Day</label>
                                <input id="day_2" class="govcy-text-input govcy-text-input-char_3" maxlength="2" type="text" pattern="[0-9]*" inputmode="numeric">
                            </div>
                            <div class="govcy-d-block govcy-mr-3">
                                <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="month_2">Month</label>
                                <select id="month_2" class="govcy-select">
                                    <option value="" selected=""></option>
                                    <option value="1">1 - January</option>
                                    <option value="2">2 - February</option>
                                    <option value="3">3 - March</option>
                                    <option value="4">4 - April</option>
                                    <option value="5">5 - May</option>
                                    <option value="6">6 - June</option>
                                    <option value="7">7 - July</option>
                                    <option value="8">8 - August</option>
                                    <option value="9">9 - September</option>
                                    <option value="10">10 - October</option>
                                    <option value="11">11 - November</option>
                                    <option value="12">12 - December</option>
                                </select>
                            </div>
                            <div class="govcy-d-block govcy-mr-3">
                                <label class="govcy-label govcy-mb-1 govcy-fw-normal govcy-mb-2" for="year_2">Year</label>
                                <input id="year_2" class="govcy-text-input govcy-text-input-char_6" placeholder="" maxlength="4" type="text" pattern="[0-9]*" inputmode="numeric">
                            </div>
                        </div>
                    </div>
                </fieldset>
                <button type="submit" class="govcy-btn-primary">Continue</button>
            </form>
        </article>
    </div>
</main>
```
### Continue button
Make sure your ‘Continue’ [button](../../components/button/) is:

- labelled ‘Continue’, not ‘Next’. 
- aligned to the left so users do not miss it

### Optional information
If you ask for optional information:

- in most contexts, add ‘(optional)’ to the labels of optional fields
- for [radios](../../components/radio/) and [checkboxes](../../components/checkbox/), add ‘(optional)’ to the legend

Never mark mandatory fields with asterisks.

On every question page you should:

- make sure it’s clear to users why you’re asking each question
- allow users to answer ‘I do not know’ or ‘I’m not sure’ if they are valid responses