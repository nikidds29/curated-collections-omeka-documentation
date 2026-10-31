---
layout: default
title: Data cleaning
nav_order: 9
---

# Data cleaning

Good records start with clean data. This page explains what data cleaning is and walks you through a simple, repeatable way to clean a dataset before you import it into Omeka-S, for example with [CSV Import](05-csv-import.md).

You don't need any special software. Most of these steps can be done in a spreadsheet such as Excel or Google Sheets, and the [Tools](#tools-that-can-help) section suggests a free tool for larger datasets.

## Data cleaning and data cleansing

The two terms are often used as if they mean the same thing, and some sources treat them as synonyms. In this guide they mean different things, and **this guide covers data cleaning only**.

| | Data cleaning | Data cleansing |
| --- | --- | --- |
| **What it is** | Finding and fixing errors and inconsistencies **within your own dataset** | A broader, ongoing process of managing data quality **across systems over time** |
| **Typical tasks** | Removing duplicates, fixing typos, making formats consistent, dealing with missing values | Checking records against external authoritative sources, enriching records with new information, setting data quality rules and monitoring them |
| **When it happens** | Usually once, before you import, share or archive a dataset | Continuously, as part of how an organisation manages its data |
| **Who does it** | You, the person preparing the collection | Usually data managers or system administrators |

In short, data cleaning gets **your dataset** ready to use. Data cleansing keeps **an organisation's data** healthy over time.

## What is data cleaning?

Data cleaning is the process of finding and fixing data that is incorrect, badly formatted, duplicated or incomplete. It is especially important when you combine data from more than one source, because that is when duplicates and inconsistencies creep in.

Cleaning is not the same as **transforming** data, which means converting it from one format or structure into another (for example, reshaping a spreadsheet to match an Omeka-S resource template). You will often do both, but clean first.

### Why it matters

- **Your records are only as good as your data.** Errors in a spreadsheet become errors in your published collection, and they are much harder to fix after import.
- **Clean data is easier to find and reuse.** Consistent names, dates and terms mean searches and filters in Omeka-S work as expected.
- **Clean data supports FAIR principles.** Cleaning data before it is published or archived means it is preserved correctly, less likely to be misread by others, and easier to combine with other datasets. See [Making your data FAIR](07-making-your-data-fair.md).

## What clean data looks like

Use these five characteristics as a checklist for your dataset.

| Characteristic | Ask yourself |
| --- | --- |
| **Validity** | Does each value follow the rules for its field? (A date field only contains dates; a field with a set list of terms only uses those terms.) |
| **Accuracy** | Is each value correct, as far as you can check against your sources? |
| **Completeness** | Is all the required information there? |
| **Consistency** | Is the same thing always recorded the same way, across the whole dataset? |
| **Uniformity** | Are values recorded in the same format and units throughout? |

## How to clean your data

Every dataset is different, so there's no single recipe. These steps give you a framework you can follow every time, which matters as much as the steps themselves: a consistent process means consistent results.

### Step 1: Keep an untouched copy

Before you change anything:

1. Save a copy of your original data and **don't edit it**. If something goes wrong, you can always go back.
2. Do all your cleaning on a working copy.
3. Start a **cleaning log**: a simple text file or a separate sheet in your spreadsheet where you note each change you make (see [Step 8](#step-8-record-what-you-did)).

> **Tip:** Name your files clearly so you can tell them apart, for example `letters-original.csv` and `letters-cleaned.csv`.

<!-- Screenshot placeholder: docs/images/data-cleaning/ -->

### Step 2: Remove duplicate and irrelevant records

**Duplicates** are the most common problem, especially when data has been combined from several spreadsheets, sources or contributors.

- Sort your data by a key field (such as title or name) so duplicates sit next to each other.
- Check that two rows really are the same before you delete one. Two people can share a name; two letters can share a date.
- Most spreadsheets have a **Remove duplicates** function, but use it carefully and only on columns that should never repeat, such as an identifier.

**Irrelevant records** are rows that don't belong in this collection, such as test entries, placeholder rows, or material outside the collection's scope. Remove them, or move them to a separate file if you might need them later.

### Step 3: Fix structural errors

Structural errors are small inconsistencies in how values are typed. They are easy to miss, but they matter because Omeka-S treats every variation as a different value.

Look for:

- **Typos and misspellings**: `Sydeny` instead of `Sydney`.
- **Inconsistent capitalisation**: `photograph`, `Photograph`, `PHOTOGRAPH`.
- **Extra spaces** at the start or end of a value, or double spaces in the middle. These are invisible but will stop values from matching.
- **Different words for the same thing**: `N/A`, `n.a.`, `Not applicable`, `-`.

Choose one form for each value and use it everywhere. **Find and replace** is your friend here, as is sorting or filtering a column to see all its different values at once.

<!-- Screenshot placeholder: docs/images/data-cleaning/ -->

### Step 4: Standardise formats

Agree on one format for each type of value and apply it across the whole dataset.

| Type of value | Make it consistent | Example |
| --- | --- | --- |
| **Dates** | Use one format throughout. Year-month-day (ISO 8601) is the most reliable choice. | `1915-03-12`, `1915-03`, `1915` |
| **Personal names** | Pick an order and stick to it. | `Lawson, Henry` |
| **Places** | Use the same name and level of detail each time. | `Sydney, New South Wales` |
| **Terms from a set list** | Use exactly the wording in your list or vocabulary. | `Photograph`, not `Photo` |
| **Multiple values in one cell** | Separate them with the same character every time. | `Lawson, Henry \| Paterson, A.B.` |

> **Curated Collections:** if your data will go through CSV Import, the separator for multiple values must match the one you set in the importer. See [CSV Import](05-csv-import.md).

### Step 5: Check unusual values

Sometimes a value just looks wrong: a birth year of 1066 in a collection of 20th-century records, or a date in the future.

- **Check it against your source** before changing it. An unusual value isn't necessarily an error; it might be the most interesting thing in your collection.
- If it is a data entry mistake, correct it and note the change in your log.
- If you can't tell, leave it as it is and flag it for someone who knows the material.

### Step 6: Deal with missing data

Gaps are normal, especially in historical and archival data. You have a few options, and none of them is perfect:

1. **Leave the value blank.** This is usually the best choice. It's honest, and it's clear to everyone that the information isn't known.
2. **Fill it in from a reliable source.** Only do this if you can check the information; don't guess. Note the source in your log.
3. **Remove the record.** Only if it is so incomplete that it isn't useful. Remember that you lose whatever information it did have.

Whatever you choose, **be consistent**. Don't mix blanks with `unknown`, `?` and `N/A` in the same column. Pick one approach (a blank cell is simplest) and use it everywhere.

### Step 7: Check your work

When you think you're done, step back and check the dataset as a whole:

- Does the data make sense?
- Does each field follow the rules for that field?
- Go back to the five characteristics in [What clean data looks like](#what-clean-data-looks-like). Does your dataset meet them?
- If something still looks odd, is it a real feature of the material or a data quality problem you've missed?

A good final check is to sort or filter each column and scan the list of values. Inconsistencies jump out when similar values sit side by side.

### Step 8: Record what you did

Finish your cleaning log so that you, or anyone else, can understand later what was changed and why. For each change, note:

- what you changed (for example, "standardised all dates to YYYY-MM-DD")
- why you changed it
- which records or columns were affected
- any decisions you made about unusual or missing values

Keep the log with your original and cleaned files. If you share or archive the dataset later, the log can go with it as a readme file.

## Tools that can help

- **Spreadsheets (Excel, Google Sheets, LibreOffice Calc):** sort and filter, find and replace, remove duplicates, and a trim function to strip extra spaces. Enough for most small and medium datasets.
- **[OpenRefine](https://openrefine.org/):** a free, open-source tool designed for cleaning messy data. It's especially good at spotting values that are *nearly* the same (such as `Sydney`, `Sydney.` and `sydney`) and fixing them all at once. It also keeps a record of every change, so you can undo steps. Worth learning if you work with large or messy datasets.

## Further reading

- [Guide to data cleaning](https://www.tableau.com/learn/articles/what-is-data-cleaning) (Tableau)
- [Documenting and cleaning data](https://researchguides.uic.edu/dataplans/document) (University of Illinois Chicago Library)
- [Data wrangling (cleaning)](https://www.jcu.edu.au/rdim/step-2-manage/data-analysis/data-wrangling-cleaning) (James Cook University)
