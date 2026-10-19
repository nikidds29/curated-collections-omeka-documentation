---
layout: default
title: Controlled vocabularies and Value Suggest
nav_order: 8
---

# Controlled vocabularies and Value Suggest

Official documentation: [Omeka-S user manual: Value Suggest](https://omeka.org/s/docs/user-manual/modules/valuesuggest/)

A **controlled vocabulary** is an agreed list of terms used to describe things consistently. Instead of everyone typing their own version of a subject, place or name, you choose from the same list. Library subject headings are a familiar example.

Controlled vocabularies make your collection easier to search, browse and link to other collections. They are also one of the best ways to keep your data clean (see [Data cleaning](06-data-cleaning.md)).

## Two ways to use controlled vocabularies in Omeka-S

| | Custom Vocab | Value Suggest |
| --- | --- | --- |
| **What it is** | A list of terms **you create** inside Omeka-S | Auto-suggested terms from **external vocabulary services** |
| **Best for** | Terms specific to your project, such as a local list of document types | Widely used terms such as subjects, places, people and rights |
| **What gets saved** | The term | The term **and a link (URI)** to it in the external vocabulary |

<!-- TODO: Confirm which of these modules are enabled on Curated Collections. -->

## Choosing a vocabulary

Pick vocabularies that suit your collection and are already used in your field. A few of those available through Value Suggest:

| Vocabulary | Use it for |
| --- | --- |
| Library of Congress Subject Headings and Name Authority File | Subjects and names |
| Getty vocabularies (AAT, TGN, ULAN) | Art and architecture terms, places, artists |
| GeoNames | Places |
| VIAF and FAST (OCLC) | Names and subjects |
| ORCID | Researchers |
| ROR | Research organisations |
| RightsStatements.org and Creative Commons | Rights and licences |
| PeriodO | Historical periods |

See the [Value Suggest module page](https://omeka.org/s/modules/ValueSuggest/) for the full list.

> **Curated Collections:** *To be added: recommended vocabularies for HASS and Indigenous collections.*

<!-- TODO: Add guidance on vocabularies for Aboriginal and Torres Strait Islander collections (e.g. AUSTLANG for languages) and when local or community-defined terms are more appropriate. -->

## Setting up a field to use a vocabulary

Controlled vocabularies are attached to a field in a **resource template**. This is usually done by a project administrator.

1. Go to **Resource templates** and open the template you want to change.
2. Find the property, for example **Subject**, and click the edit (pencil) icon.
3. Under **Data types**, choose the vocabulary you want, for example **LC: Subject Headings**.
4. Click **Set changes**, then **Save**.

<!-- Screenshot placeholder: docs/images/controlled-vocabularies/ -->

## Creating a custom vocabulary

1. Go to **Modules** > **Custom Vocab** and click **Add new vocab**.
2. Give the vocabulary a clear label.
3. Enter your terms, one per line.
4. Click **Add**.
5. Attach it to a field in a resource template, as above.

<!-- Screenshot placeholder: docs/images/controlled-vocabularies/ -->

## Adding a term to a record

1. Open the item and go to the field that uses the vocabulary.
2. Start typing. A list of suggested terms appears.
3. Click the right term. Check the details shown to make sure it is the one you mean, such as the correct place among several with the same name.
4. Save the item.

<!-- Screenshot placeholder: docs/images/controlled-vocabularies/ -->

> **Tip:** If you can't find a suitable term, don't force one that is only nearly right. Use the closest broader term, or ask your project administrator whether a local term should be added.

## Using vocabularies with CSV Import

<!-- TODO: Explain how to map spreadsheet columns to Value Suggest or Custom Vocab data types during CSV Import, and whether URIs need to be in the spreadsheet. -->

*To be added.* See [CSV Import](02-csv-import.md) in the meantime.
