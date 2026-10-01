---
layout: default
title: Pre-publication checklist
nav_order: 5
---

# Pre-publication checklist

Use this checklist before making your Omeka-S collection public.

> 📄 **[Download the printable checklist (PDF)](../downloads/CC-Pre-Publication-Checklist.pdf)**

## 1. Rights and Permissions

- ☐ I know the copyright status of each item, including for any items with overlapping copyright (eg. Photographs that identify a person)
- ☐ Where copyright status is unknown, I have marked this field as “unknown” and not left it blank
- ☐ I have checked any restrictions on public reuse of items in my collection

| Omeka-S fields (DC) | Omeka-S fields (Schema) | Example             |
|---------------------|-------------------------|---------------------|
| Creator             | Creator                 | S. Mithridites      |
| Rights              | Licence                 | Public Domain       |
| Rights holder       | Copyright holder        | Library of Congress |

## 2. Accessibility

- ☐ Media includes meaningful alt text that describes what a sighted reader would want to know for research purposes
- ☐ Page display choices meet basic legibility standards
- ☐ Embedded multi-media includes transcripts

| Omeka-S attributes |                                                                       | Example                                                                  |
|--------------------|-----------------------------------------------------------------------|--------------------------------------------------------------------------|
| Media → Advanced tab | Alt text                                                              | Portrait photograph of a woman, looking left                             |
| Pages              | Page template/design                                                  | Dark text on a light background, clear headings and a readable font size |
| Media item         | Transcription not built in to Omeka-S, must be in original media item | Oral history MP3 with a PDF transcript attached as a second media file   |

## 3. Identifiers and Linked Data

- ☐ Each item has a stable, unique identifier
- ☐ Each points to an external authority link
- ☐ Controlled identifiers (URIs) are used to identify key fields

| Omeka-S fields (DC) | Omeka-S fields (Schema) | Example                                        |
|---------------------|-------------------------|------------------------------------------------|
| Identifier          | Identifier              | PH-1901-042                                    |
| URI                 | URL                     | https://example.org/s/my-collection/item/42    |
| Relation            | sameAs                  | https://id.loc.gov/authorities/names/n50006412 |

## 4. Metadata Quality

- ☐ All essential fields are complete
- ☐ Dates and names follow a consistent format

| Omeka-S fields (DC)                                                                        | Omeka-S fields (Schema)                                                                      | Example                                                                       |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Essential fields: title, description, creator, rights, rights holder, identifier, relation | Essential fields: title, description, creator, licence, copyright holder, identifier, sameAs | Dates as YYYY-MM-DD (1847-03-12); names as Surname, Given name (Opie, Amelia) |

## 5. Research collection as dataset

- ☐ I have checked the licences that apply to my own metadata and media objects
- ☐ Citations for the items and collection are correct
- ☐ Each page includes site version or last updated information
