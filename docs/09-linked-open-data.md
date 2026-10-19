---
layout: default
title: Linked open data
nav_order: 9
---

# Linked open data

**Linked open data** is a way of publishing data so that it connects to other data across the web. Omeka-S is built for it: every record you create can be shared as linked data, and the more you link your records to trusted sources, the more useful they become.

This page explains the basic ideas and the simple steps you can take to make your collection part of the wider web of data.

## The basic ideas

| Term | What it means |
| --- | --- |
| **Linked data** | Data that uses web links to identify things and connect them to each other |
| **Open** | Published under a licence that lets others reuse it |
| **URI** | A unique web address that identifies one specific thing, such as a person, place or subject |
| **Vocabulary** | A standard set of properties used to describe things, such as Dublin Core or schema.org |
| **Authority** | A trusted source of identifiers for people, places or subjects, such as VIAF or GeoNames |

The key idea is simple: **use a link instead of just a name**. The text "Sydney" could mean several places. A link to Sydney's GeoNames record means exactly one.

## Why it matters

- **Clarity:** links remove doubt about which person, place or subject you mean.
- **Discovery:** your records can be found and connected to other collections about the same people, places and topics.
- **FAIR data:** linked open data supports the FAIR principles, especially being interoperable and reusable. See [Making your data FAIR](04-making-your-data-fair.md).

## How Omeka-S supports linked data

- **Standard vocabularies.** Omeka-S describes records with properties from established vocabularies such as Dublin Core (`dcterms:title`, `dcterms:creator`). Using these makes your data understandable outside your own site.
- **URIs as values.** Any field can hold a URI with a label, linking to a record somewhere else on the web.
- **Value Suggest.** Chooses terms from external authorities and saves their URIs for you. See [Controlled vocabularies and Value Suggest](08-controlled-vocabularies.md).
- **Linked data output.** Every Omeka-S resource is also available in JSON-LD, a machine-readable linked data format, through the site's API.

<!-- TODO: Confirm whether the Curated Collections API is public, and add an example API URL for an item. -->

## Simple steps to make your collection more linked

### Step 1: Use standard properties

When you build or choose a resource template, use properties from established vocabularies rather than creating new ones where you can.

<!-- TODO: Add Curated Collections guidance on recommended vocabularies and templates. -->

### Step 2: Link people, places and subjects to authorities

Wherever possible, record people, places and subjects as links to a trusted authority, not just as text.

| Type | Suggested authorities |
| --- | --- |
| People | VIAF, Library of Congress Name Authority File, Wikidata, ORCID (researchers) |
| Organisations | VIAF, ROR (research organisations), Wikidata |
| Places | GeoNames, Getty TGN, Wikidata |
| Subjects | Library of Congress Subject Headings, FAST, Getty AAT |

> **Curated Collections:** *To be added: Australian authorities and identifiers, such as Trove People and Organisations, AUSTLANG and the Australian Dictionary of Biography.*

### Step 3: Add links to related records elsewhere

If a person, object or document in your collection is also described elsewhere, such as in Trove, a museum catalogue or an archive, add a link to that record.

<!-- Screenshot placeholder: docs/images/linked-open-data/ -->

### Step 4: Link records within your collection

Use **Omeka resource** links to connect records in your own collection, for example linking a letter to the person who wrote it, rather than typing the person's name as text.

### Step 5: Choose an open licence

Data is only *open* linked data if others are allowed to reuse it. Make sure the licence for your metadata is clear.

<!-- TODO: Add Curated Collections licensing guidance and link to the Pre-publication checklist. -->

## Things to keep in mind

- **Check before you link.** Make sure the authority record is really the same person, place or thing.
- **Prefer stable links.** Use the authority's permanent URI, not a search results page.
- **Not everything should be open.** Some material, including culturally sensitive Indigenous knowledge, should not be published as open data. Follow community protocols and the CARE principles.

<!-- TODO: Link to Curated Collections guidance on Indigenous data sovereignty and the CARE principles. -->

## Further reading

<!-- TODO: Add further reading. -->

*To be added.*
