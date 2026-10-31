---
layout: default
title: Persistent identifiers
nav_order: 15
---

# Persistent identifiers

*Make your collection, and the items in it, citable and findable for the long term.*

A **persistent identifier (PID)** is a long-lasting reference to a digital resource. Unlike an ordinary web address, a PID is designed to keep working even if the resource moves to a new website or domain. PIDs make your collection citable, help others find it, and are a core part of making data FAIR (see [Making your data FAIR](07-making-your-data-fair.md)).

There are two levels where PIDs matter in Omeka-S:

- **The collection as a whole:** a DOI for your published collection or dataset, so it can be cited like a publication.
- **Individual items:** a PID for each item, so people can cite and link to a single record.

## Types of persistent identifier

### Identifiers for collections, datasets and items

| Identifier | What it is | Typical use |
| --- | --- | --- |
| **DOI** (Digital Object Identifier) | Resolves through `https://doi.org/`. For research data, DOIs are issued by DataCite. | Citing a published dataset or collection |
| **ARK** (Archival Resource Key) | A free identifier scheme for archives and cultural heritage. Requires a Name Assigning Authority Number (NAAN). Resolves through `https://n2t.net/`. | Identifying individual items or records |
| **Handle** | The system that underpins DOIs. Also available directly, for example through the ARDC Handle Service. | Identifying repository records |
| **PURL** (Persistent URL) | A web address that redirects to the current location of a resource. | Stable links to pages or vocabularies |
| **URN** (Uniform Resource Name) | A location-independent name, such as `urn:isbn:`. | Library and publishing standards |

### Identifiers for people, organisations and projects

Your collection's metadata can also use PIDs to identify who made it and where it came from:

| Identifier | Identifies | Where to use it in Omeka-S |
| --- | --- | --- |
| **ORCID** | Researchers and contributors | Creator and contributor fields, and in your collection's DOI metadata |
| **ROR** (Research Organization Registry) | Research organisations, such as your university | Publisher or funder fields |
| **RAiD** (Research Activity Identifier) | Research projects. Issued in Australia by the ARDC. | Linking your collection to the project that produced it |

> **Note:** Having a PID doesn't make a resource persistent by itself. Someone has to keep the PID's metadata and target URL up to date when things move. Plan who will be responsible for this.

## Getting a DOI for your collection

A DOI tells people that your collection is a stable, citable research output. It needs to point to a **landing page** that describes the collection and how to access it. For an Omeka-S collection, this is usually your public site's home page or About page.

### Where to get a DOI

| Option | Who it's for | Notes |
| --- | --- | --- |
| **University of Sydney Library** | University of Sydney researchers | The Library can provide DOIs for some non-published materials. Contact ses.admin@sydney.edu.au. |
| **ARDC DataCite DOI service** | Australian research organisations, not individuals | Free for publicly funded Australian institutions. Your institution mints DOIs through DataCite Fabrica, manually or through the API. In scope: research datasets and collections, workflows, software and models. |
| **Zenodo** or another data repository | Anyone | Deposit an export or snapshot of your collection (for example CSV files or an RO-Crate) and the repository issues a DOI for the deposit. Link the deposit to your live site, and your site to the deposit. |

> ✏️ **Content needed (Curated Collections):** Which route the Curated Collections team recommends for project DOIs, who to contact, and how long it takes.

### Before you request a DOI

Check that your collection meets the usual requirements:

- ☐ The collection is **publicly available** at a stable web address (the landing page). DataCite DOIs must resolve to published data.
- ☐ The collection is **part of the scholarly record** and **will remain available**.
- ☐ You can supply the **required metadata**: title, creator(s), publisher, publication year and resource type (for example *Dataset* or *Collection*).
- ☐ You've decided **who will maintain the DOI**: updating its URL if the site moves, and updating its metadata for new versions.
- ☐ You've added ORCIDs for creators and a ROR for your institution where possible.

See also the [Pre-publication checklist](08-pre-publication-checklist.md).

### Where the DOI should go on your Omeka-S site

Once you have a DOI, make it visible wherever someone might want to cite your collection:

1. **Home page or About page (landing page).** Add a *How to cite this collection* section with a full citation that includes the DOI as a link, for example:

   > Surname, Given name (Year). *Collection title* [Data set]. Publisher. https://doi.org/10.xxxx/xxxxx

2. **Site footer.** Add the DOI or a short citation to the footer so it appears on every page.
3. **Collection item set.** If your collection is organised as an item set, record the DOI on it in an identifier field such as `dcterms:identifier` or `bibo:doi`.
4. **Version information.** If you mint a new DOI for each major version, show the version number and last-updated date next to the citation.

> 🖼️ **Image needed:** An Omeka-S site About page showing a "How to cite this collection" section with a DOI link.

> 🖼️ **Image needed:** The site footer settings showing a citation and DOI.

> 💡 **Tip:** Always write DOIs as full links (`https://doi.org/10.xxxx/xxxxx`), not as `doi:10.xxxx` or a bare number, so they are clickable and machine-readable. In Omeka-S, enter them with the **URI** data type.

## Persistent identifiers for individual items

By default, every Omeka-S item has a web address based on its internal number (for example `.../s/my-site/item/42`). These addresses are stable while your installation stays the same, but they break if the collection moves to a new domain or platform.

You can strengthen item-level identification in two ways.

### 1. Record a stable identifier in the item's metadata

Give every item a unique, stable identifier in its metadata, such as `PH-1901-042`, using `dcterms:identifier` or `schema:identifier`. This doesn't resolve on its own, but it stays with the record wherever it goes. It's also what other systems, and the PID modules below, can use to find existing identifiers. See the [Pre-publication checklist](08-pre-publication-checklist.md#identifiers-and-linked-data).

### 2. Mint a resolvable PID for each item with a module

Omeka-S modules can create or attach a resolvable PID (an ARK or DOI) for each item. When someone opens the PID in a browser, it resolves to a page for that item.

> 🖼️ **Image needed:** An item page in Omeka-S showing its persistent identifier.

## Omeka-S modules for persistent identifiers

| Module | Developer | Identifiers | What it does |
| --- | --- | --- | --- |
| [Persistent Identifiers](https://omeka.org/s/modules/PersistentIdentifiers/) | Omeka Team | ARKs (local, or through EZID for existing EZID users) and DOIs (through DataCite) | Creates, imports and assigns PIDs to items. Resolves each PID to a stable landing page for the item. |
| [Ark & Noid](https://omeka.org/s/modules/Ark) | Daniel Berthereau | ARKs | Creates ARKs and can use them as item URLs instead of internal numbers. Requires the Common module. Use with the Clean Url module to apply ARK links across the site. |
| [Quark](https://omeka.org/s/modules/Quark) | BibLibre | ARKs (UUID-based) | A simpler alternative to Ark that doesn't need an external library, and is faster with large collections. |

> ✏️ **Content needed (Curated Collections):** Which PID module, if any, is installed on Curated Collections, and whether item-level PIDs are available to all projects.

### Using the Persistent Identifiers module

Official documentation: [Omeka-S user manual: Persistent Identifiers](https://omeka.org/s/docs/user-manual/modules/persistentidentifiers/)

**Setting up** (Global Administrator or Supervisor only):

- Choose **one PID service** for minting: local ARK, DataCite DOI, or EZID ARK.
- **Local ARKs** need a free NAAN from the ARK Alliance.
- **DataCite DOIs** need your institution's DataCite repository prefix, ID and password. You must also map five required fields: Title, Creator, Publisher, Publication Year and Resource Type. The Resource Type value must exactly match a DataCite term.
- Choose whether to **assign PIDs to new items automatically**, which fields to check for **existing PIDs** (such as `dcterms:identifier`), and optionally a field to **store** each PID in.

**Assigning PIDs:**

| Method | How |
| --- | --- |
| New items | If automatic assignment is on, each new or imported item gets a PID. If a configured field already holds a PID, that PID is used instead. Enter existing PIDs before the first save. |
| One item | Edit the item, open the **Advanced** tab, click **Mint PID**, then **Save**. |
| Many items | On the Items page, select items, choose **Batch edit**, set **Persistent Identifiers** to **Mint PIDs**, then **Save**. |

> 🖼️ **Image needed:** The Advanced tab on the item edit page with the Mint PID button.

> 🖼️ **Image needed:** The batch edit screen with the Persistent Identifiers option.

> ⚠️ **Removing a PID breaks every link that points to it.** Only remove a PID if you're sure, and never reuse it for a different item. Also note that users below Supervisor can't switch off automatic assignment, which can create PIDs by accident.

## Further reading

- [ARDC DataCite DOI service](https://documentation.ardc.edu.au/doi/introduction-to-the-doi-fabrica-service)
- [ARDC DOI service minting checklist](https://documentation.ardc.edu.au/doi/doi-service-minting-checklist)
- [University of Sydney Library: Persistent identifiers](https://library.sydney.edu.au/support/publishing/making-your-research-findable/dois-and-isbns)
- [Omeka-S user manual: Persistent Identifiers module](https://omeka.org/s/docs/user-manual/modules/persistentidentifiers/)
- [Linked open data](12-linked-open-data.md)
