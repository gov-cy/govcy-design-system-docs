---
title: "Cannot use the service pages (eligibility)"
date: 2022-02-01 00:01:02Z
tags: "pages"
description: "Use this page to tell users that they are not eligible to use or continue with a service."
---
Tell users that they are not eligible to use or continue with a service.

## When to use this pattern
Use this page when a user cannot use or continue with a service because they do not meet the service’s eligibility rules. 

This can happen:

- after the user signs in and the service checks their eligibility
- when the user submits an application and a final eligibility or submission check fails
- when the user does not have the required role, registration, status, authorisation, or profile type

If there is a problem with the service that is not related to eligibility, use a [there is a problem with the service page](../there-is-a-problem/).

## When not to use this pattern
Do not use this page for:

- technical problems with the service (use a [there is a problem with the service page](../there-is-a-problem/) instead)
- validation errors on a form (use the error [error messages](../../components/error_message) and [error summary](../../components/error_summary) )
- planned service downtime (see [service unavailable pages](../service-unavailable-pages/))

## How it works
The page should have:
- as the [title in the page’s](../../getting-started/page-template/#title%2C-description) `<head>` 
    - in Greek ‘[Λόγος που ο χρήστης δεν μπορεί να χρησιμοποιήσει την υπηρεσία] – service name – gov.cy’
    - in English: ‘[Reason user cannot use service] – service name – gov.cy’
- as the `H1`
    - in Greek: ‘[Λόγος που ο χρήστης δεν μπορεί να χρησιμοποιήσει την υπηρεσία]’
    - in English: ‘[Reason user cannot use service]’
- a short explanation of what this means
- information about what the user can do next, if there is a next step
- contact information, if it helps meet a user need
- a link to another service or guidance page, if users can use it to do what they came to do

Contact information should either include contact details or a link to a [contact page](../contact_department_or_team/). 

Use clear and concise content. Do not use:
- breadcrumbs
- red text to warn people
- technical terms like API, failed check, eligibility endpoint, error code, submission failed
- vague headings like “Error” or “Access denied”
- language that blames the user

## Examples

See below some examples of this pattern for common reasons a user cannot use a service.

<div class="govcy-alert-notification govcy-br-5 govcy-br-info govcy-px-0">
    <div class="govcy-alert-notification-header govcy-fw-bold govcy-bg-info govcy-fs-4">Warning</div>
    <div class="govcy-alert-notification-body">
        <p class="govcy-pl-4 govcy-pt-6">
        <span class="govcy-warning-text govcy-d-inline">
            <span class="govcy-warning-text-icon" aria-hidden="true">!</span></span>
            The eligibility checks differ from service to service, depending on the business logic of each service. Adjust what checks are performed by the service and the content of the eligibility page to match your service's needs.
        </p>
    </div>
</div>

### Civil Registry checks

#### 1. Person not found in Civil Registry

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Δεν σας βρήκαμε στα αρχεία μας

Αν πιστεύετε ότι υπάρχει κάποιο λάθος στα αρχεία μας, επισκεφθείτε το κοντινότερο [Γραφείο Επαρχιακής Διοίκησης](https://www.gov.cy/moi/documents/simeia-ypovolis-aitiseon/){rel="noreferrer noopener" target="_blank"}.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# You are not registered

If you think that there is a mistake in our records, please visit your nearest [District Administration Office](https://www.gov.cy/moi/en/documents/application-submission-offices/){rel="noreferrer noopener" target="_blank"}.

</div>

---------

#### 2. Civil Registry has a date of death for the person

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Έχει βρεθεί ημερομηνία θανάτου για αυτό το άτομο

Αν πιστεύετε ότι υπάρχει κάποιο λάθος στα αρχεία μας, επισκεφθείτε το κοντινότερο [Γραφείο Επαρχιακής Διοίκησης](https://www.gov.cy/moi/documents/simeia-ypovolis-aitiseon/){rel="noreferrer noopener" target="_blank"}.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Date of death found for this person

If you think that there is a mistake in our records, please visit your nearest [District Administration Office](https://www.gov.cy/moi/en/documents/application-submission-offices/){rel="noreferrer noopener" target="_blank"}.

</div>

---------

#### 3. Person found in Civil Registry does not have a Cypriot citizenship

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Η υπηκοότητά σας δεν είναι κυπριακή

Για να χρησιμοποιήσετε την υπηρεσία αυτή θα πρέπει να είστε Κύπριος ή Κύπρια.

Αν πιστεύετε ότι υπάρχει κάποιο λάθος στα αρχεία μας, επισκεφθείτε το κοντινότερο [Γραφείο Επαρχιακής Διοίκησης](https://www.gov.cy/moi/documents/simeia-ypovolis-aitiseon/){rel="noreferrer noopener" target="_blank"}.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Your citizenship is not Cypriot

To use this service, you need to be a Cypriot citizen.

If you think that there is a mistake in our records, please visit your nearest [District Administration Office](https://www.gov.cy/moi/en/documents/application-submission-offices/){rel="noreferrer noopener" target="_blank"}.

</div>

---------

#### 4. Person found in Civil Registry is not Greek Cypriot

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Δεν μπορείτε να προχωρήσετε διαδικτυακά

Για να χρησιμοποιήσετε την υπηρεσία αυτή θα πρέπει να είστε Έλληνοκύπριος ή Ελληνοκύπρια.

Αν πιστεύετε ότι υπάρχει κάποιο λάθος στα αρχεία μας, επισκεφθείτε το κοντινότερο [Γραφείο Επαρχιακής Διοίκησης](https://www.gov.cy/moi/documents/simeia-ypovolis-aitiseon/){rel="noreferrer noopener" target="_blank"}.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# You cannot continue online

To use this service, you need to be Greek Cypriot.

If you think that there is a mistake in our records, please visit your nearest [District Administration Office](https://www.gov.cy/moi/en/documents/application-submission-offices/){rel="noreferrer noopener" target="_blank"}.

</div>

---------

#### 5. Person found in Civil Registry is not Turkish Cypriot

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Δεν μπορείτε να προχωρήσετε διαδικτυακά

Για να χρησιμοποιήσετε την υπηρεσία αυτή θα πρέπει να είστε Τουρκοκύπριος ή Τουρκοκύπρια.

Αν πιστεύετε ότι υπάρχει κάποιο λάθος στα αρχεία μας, επισκεφθείτε το κοντινότερο [Γραφείο Επαρχιακής Διοίκησης](https://www.gov.cy/moi/documents/simeia-ypovolis-aitiseon/){rel="noreferrer noopener" target="_blank"}.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# You cannot continue online

To use this service, you need to be Turkish Cypriot.

If you think that there is a mistake in our records, please visit your nearest [District Administration Office](https://www.gov.cy/moi/en/documents/application-submission-offices/){rel="noreferrer noopener" target="_blank"}.

</div>

---------

#### 6. Person found in Civil Registry is under [xx] years old (for example 18 years old)

Replace [xx] with a number.

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Είστε κάτω των [xx] χρόνων

Για να χρησιμοποιήσετε την υπηρεσία αυτή θα πρέπει να είστε πάνω από [xx] χρόνων.

Αν πιστεύετε ότι υπάρχει κάποιο λάθος στα αρχεία μας, επισκεφθείτε το κοντινότερο [Γραφείο Επαρχιακής Διοίκησης](https://www.gov.cy/moi/documents/simeia-ypovolis-aitiseon/){rel="noreferrer noopener" target="_blank"}.

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# You cannot continue online

To use this service you need to be over [xx] years old.

If you think that there is a mistake in our records, please visit your nearest [District Administration Office](https://www.gov.cy/moi/en/documents/application-submission-offices/){rel="noreferrer noopener" target="_blank"}.

</div>

---------

### Generic checks

#### 7. Person not found in specific users database

Replace: 
- [xx] with the name of the users' list
- [yy] with the action
- [zz] with the name of the department

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Δεν σας έχουμε εντοπίσει στη λίστα των [xx]

Δεν σας έχουμε εντοπίσει στη λίστα [xx] για να μπορέσετε να [yy].

Αν πιστεύετε ότι υπάρχει κάποιο λάθος, επικοινωνήστε με [[zz]](#).

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# We could not find you in the list of [xx]

We could not verify you in the list of [xx], so you cannot [yy].

If you believe there is a mistake, contact the [[zz]](#).

</div>

---------

#### 8. User already submitted an application

Replace: 
- [xx] application name 
- [yy] with the action
- [zz] with the name of the department

*Example in Greek*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# Έχετε ήδη καταχωρισμένη [xx]

Δεν μπορείτε να [yy] επειδή έχετε ήδη καταχωρισμένη [xx].

Για πληροφορίες σχετικά με την αίτησή σας, επικοινωνήστε με [[zz]](#).

</div>

*Example in English*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">

# You already have a submitted [xx]

You cannot [yy] because you already have a submitted [xx].

For information about your application, contact the [[zz]](#).

</div>

---------

