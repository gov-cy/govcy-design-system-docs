---
title: "Dates"
date: 2022-02-01 00:01:02Z
tags: "ask_users_for"
description: "Follow this pattern whenever you need users to provide or view a date as part of your service."
---
Help users enter or select a date.

## When to use this pattern
Follow this pattern whenever you need users to provide or view a date as part of your service.

## How it works
Dates should only exist in the [main section](../../getting-started/page-template/#sections).

The way you should ask users for dates depends on the types of date you’re asking for and the proximity to today's date.

Dates you may need users to provide include:
- memorable dates, like a date of birth or marriage
- dates from documents or cards, like a passport or credit card
- approximate dates, like ‘December 2017’
- relative dates, like ‘4 days from today’

In some cases you might need users to pick a date from a given selection.

### Asking for memorable dates
If you are asking for a memorable date that is not in the near future or recent past, for example birth date, use the [date input component](../../components/date_input/).

### Asking for dates from documents and cards
When asking for a date exactly as it’s shown on a passport, credit card or other document, make the fields match the format of the original. This makes it easier for users to copy the date across accurately.

### Asking for approximate dates
Allow users to enter an approximate date when you are asking them for information they may not know or may struggle to remember. For example, allow users to enter ‘December 2020’ for a field that says ‘the date you lost your passport’.

### Asking for relative dates
You may need to ask for dates that are relative to today’s date or another date - this is common if a user is setting a reminder.

To do this let users enter or select relative dates like ‘tomorrow’ or ‘1 day before’. If the day of the week is important, show this as well.

### Helping users to pick a date
Users might need to pick a date from a selection, for example, to book an appointment.

To do this, you can present dates in a calendar format using the [date picker component](../../components/date_picker/). Users are shown one month’s worth of dates at a time, and can skip through months and years.

Only use the date picker if users need to:
- pick a date in the near future or recent past
- know the day of the week, or the week of the month, as well as the date
- be able to see dates in relation to other dates

### How to write dates
Display dates in the format `d/m/yyyy`, where: 
- **d**, stands for one-digit day of the month for days below 10, _e.g. 2_
- **m**, stands for one-digit month for months below 10, _e.g. 3_
- **yyyy**, stands for four-digit year, _e.g. 2024_

For example `13/9/2021`.

If you give an example date, use 13 or more for the day and 9 or less for the month - for example ‘27 3 2020’. This helps users enter the date in the correct order and shows them they do not need to include leading zeroes.