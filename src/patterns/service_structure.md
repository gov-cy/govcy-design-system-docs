---
title: "Structuring a service"
date: 2022-02-01 00:01:02Z
tags: "how_to"
---
This guide explains how to structure an online service. 

## Basic structure 

The basic structure of a service should: 
1. Start with an informative start page 
2. If needed, ask the users to sign-in
3. Gather information from the users, one question at a time 
4. Let the users check their answers before submitting 
5. Show the users a confirmation of successful completion page.

![An example flow of a standard service](../../img/example_flow_of_a_standard_service.png){.img-fluid}

## Start page
Before starting the service, users should be presented with a page describing all the information they will need from the start, such as:
- What the service does 
- Who it is for 
- What is needed to use the service 
- Other ways to apply 
- How they can get help

![Illustration of a start page](../../img/illustration_start_page.png){.img-fluid}

Keep in mind that research has shown that users avoid reading long text, so keep your information minimal, and to the point and avoid using legal jargon. 

This page usually resides on the GOV.CY portal.  

## One thing at a time

Prefer to split the [questions](../question_pages) across multiple pages with each page containing just one thing, for example:
- one piece of information you’re telling a user
- one decision they have to make
- one question they have to answer

![Illustration of splitting questions to ask one thing at a time](../../img/one-thing-at-a-time.png){.img-fluid}

User research will tell you when you can merge pages together. For example, if you’re designing an internal service for government users who need to repeat and switch between tasks quickly.
Keeping one thing on a page helps users to:
- understand what you’re asking them to do
- focus on the specific question and its answer
- reduce the stress of filling out humongous forms
- find their way through an unfamiliar process
- use the service on a mobile device
- recover easily from errors

It may also help to:
- save users’ answers automatically as they go
- capture analytics and statistics about each question
- handle branching questions and [loops](../multiple_things)
- apply conditional logic and guide users to complete the service in a more relaxed manner
- direct the users to a specific question where they can change their answer (see [check answers pattern](../check_answers)).

## Check your answers page
Use the [check answers pattern](../check_answers) to let users check their answers before submitting information to a service.

![Illustration a check your answers page](../../img/illustration_check_answers.png){.img-fluid}

## Confirmation page
After the users have submitted their application, present a confirmation page with a [panel](../../components/panel) to tell them that they have successfully completed the transaction. This reassures the users their application has been filed and provides useful information on what will happen next. 

![Illustration a confirmation page](../../img/illustration_confirmation_page.png){.img-fluid}

Research has shown that users feel more at ease when:
- they are presented with a reference number for their application 
- they receive a notification either by SMS or by email 
- they can print or save the confirmation.

## Contribute
If you have used or researched this pattern, please let us have your feedback, so we can make it better for everyone. Send us an email at <a href="mailto:dsf@dits.dmrid.gov.cy" target="_blank">dsf@dits.dmrid.gov.cy</a> to get in touch. 
