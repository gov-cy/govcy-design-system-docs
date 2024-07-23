---
title: "There is a problem with the service pages"
date: 2022-02-01 00:01:02Z
tags: "pages"
description: "Use this page to tell users there is something wrong with the service."
---
Tell users there is something wrong with the service. These are also known as 500 or internal server error pages. 

## When to use this pattern
Use this page when there is an unexpected problem with the service. Use the same page for all unexpected problems.

Log all errors and fix them as quickly as possible.

Only display this page for a short time. If a problem cannot be fixed quickly, consider to close the service and use a [service unavailable page](../service-unavailable-pages/).

## How it works
These pages should have:
- as the [title in the page’s](../../getting-started/page-template/#title%2C-description) `<head>` 
    - in Greek ‘Λυπούμαστε, υπάρχει πρόβλημα με την υπηρεσία – service name – gov.cy’
    - in English ‘Sorry, there is a problem with the service – service name – gov.cy’
- as the `H1`
    - in Greek ‘Λυπούμαστε, υπάρχει πρόβλημα με την υπηρεσία’
    - in English ‘Sorry, there is a problem with the service’
- if possible, information about what has happened to users' answers if they were in the middle of a transaction
- contact information, if it exists and helps meet a user need
- a link to another service, if users can use it to do what they came to do

Contact information should either include contact details or a link to a [contact page](../contact_department_or_team/). 

Have clear and concise content and do not use:
- breadcrumbs
- jargon like 500 or bad request
- ‘We are experiencing technical difficulties’
- red text to warn people

If possible, store previously entered information for a reasonable amount of time so users can resume a journey with re-populated information when the service becomes available again.

Here are some examples of this pattern.
### 1. Service has offline support but no specific page that includes contact details

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Λυπούμαστε, υπάρχει πρόβλημα με την υπηρεσία

Δοκιμάστε ξανά αργότερα.

Δεν έχουμε αποθηκεύσει τις απαντήσεις σας. Όταν η υπηρεσία είναι διαθέσιμη, θα πρέπει να ξεκινήσετε ξανά.

Επικοινωνήστε με το [Τμήμα Φορολογίας](#) αν έχετε οποιεσδήποτε ερωτήσεις.

**Τηλέφωνο**
[22123456](#)

**Ώρες λειτουργίας**
Δευτέρα έως Παρασκευή, 08:30 π.μ. έως 2:30 μ.μ

Κλειστά την Κυριακή του Πάσχα, τα Χριστούγεννα και την Πρωτοχρονιά.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Sorry, there is a problem with the service

Try again later.

We have not saved your answers. When the service is available, you will have to start again.

Contact the [Tax Department](*) if you have any questions.

**Telephone**
[22123456](#)

**Opening times**
Monday to Friday, 8:30 am to 2:30 pm

Closed Easter Sunday, Christmas Day and New Year’s Day.

</div>

### 2. Service has a specific page that includes contact details
*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Λυπούμαστε, υπάρχει πρόβλημα με την υπηρεσία

Δοκιμάστε ξανά αργότερα.

Αποθηκεύαμε τις απαντήσεις σας. Θα είναι διαθέσιμες για 30 ημέρες.

Επικοινωνήστε με το [Τμήμα Φορολογίας](#) αν θέλετε να κάνετε αλλαγές στην αίτησή σας ή για να μιλήσετε με κάποιον σχετικά με τους φόρους σας.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Sorry, there is a problem with the service

Try again later.

We saved your answers. They will be available for 30 days.

Contact the [Tax Department](*) if you need to make changes to your application or speak to someone about your taxes.

</div>

### 3. Link to another service

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Λυπούμαστε, υπάρχει πρόβλημα με την υπηρεσία

Δοκιμάστε ξανά αργότερα.

Μπορείτε να [αλλάξετε άλλα στοιχεία ΦΠΑ](#)

Επικοινωνήστε με το [Τμήμα Φορολογίας](#) αν θέλετε να κάνετε αλλαγές στην αίτησή σας ή για να μιλήσετε με κάποιον σχετικά με τους φόρους σας.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Sorry, there is a problem with the service

Try again later.

You can [change other VAT details](#)

Contact the [Tax Department](*) if you need to make changes to your application or speak to someone about your taxes.

</div>