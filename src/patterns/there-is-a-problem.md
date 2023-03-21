---
title: "There is a problem with the service pages"
date: 2022-02-01 00:01:02Z
tags: "pages"
---
Tell the user there is something wrong with the service. These are also known as 500 and internal server error pages. 

## When to use this pattern 

Use this page when there is an unexpected problem with the service. Use the same page for all unexpected problems. 

Log all errors and fix them as quickly as possible. 

Only display the page for a short time. If a problem cannot be fixed quickly, close the service and use a [service unavailable page](../service-unavailable-pages). 

## How it works 

The page should have: 
- as the page title: 
  - in Greek ‘Λυπούμαστε, υπάρχει πρόβλημα με την υπηρεσία – service name – gov.cy’ 
  - in English ‘Sorry, there is a problem with the service – service name – gov.cy’
- as the H1 
  - in Greek ‘Λυπούμαστε, υπάρχει πρόβλημα με την υπηρεσία’ 
  - in English ‘Sorry, there is a problem with the service’  
- if possible, information about what has happened to their answers if they are in the middle of a transaction 
- contact information, if it exists and helps meet a user need 
- a link to another service, if they can use it to do what they came to do 

Have clear and concise content and do not use: 
- breadcrumbs 
- jargon like 500 or bad request 
- ‘We are experiencing technical difficulties’ 
- red text to warn people 

*Example in Greek*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<!--main-->
<main class="govcy-container" id="mainContainer">
    <h1>Λυπούμαστε, υπάρχει πρόβλημα με την υπηρεσία</h1> 
    <p>Προσπαθούμε να το διορθώσουμε το συντομότερο δυνατόν. Δοκιμάστε ξανά αργότερα.</p>
</main>
</div>

*Example in English*
<div class="govcy-container govcy-p-4  govcy-br-1 govcy-br-standard govcy-mb-4">
<!--beforeMain-->
<!--main-->
<main class="govcy-container" id="mainContainer">
    <h1>Sorry, there is a problem with the service</h1> 
    <p>We're working to fix the issue as soon as possible. Try again later.</p>
</main>
</div>

