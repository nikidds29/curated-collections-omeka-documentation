---
layout: default
title: "Cultural rights: ICIP and ICMR"
parent: Indigenous data governance
nav_order: 3
---

# Cultural rights: ICIP and ICMR

*Record the rights communities hold in their culture, even where copyright doesn't reach.*

Copyright protects individual creators for a limited time. Aboriginal and Torres Strait Islander cultural heritage works differently: it is often **owned collectively**, passed down across generations, and governed by cultural law that doesn't expire. A story, design, song or piece of knowledge may not be protected by copyright at all, and a photograph of a ceremony can be out of copyright while the community it depicts still has the right to decide how it is used.

This page explains two ideas that help close that gap, **ICIP** and **ICMR**, and shows where to record them in Omeka-S. For copyright, licences and rights statements, see [Copyright and licensing](13-copyright-and-licensing.md).

## What is ICIP?

**Indigenous Cultural and Intellectual Property (ICIP)** refers to the rights of Aboriginal and Torres Strait Islander peoples in their cultural heritage. This includes:

- Traditional knowledge, including knowledge of Country, plants, animals and seasons
- Languages
- Stories, songs, dance, ceremonies and other cultural expressions
- Art, designs and symbols
- Sites of significance and ancestral remains
- **Documentation of Indigenous heritage**, such as recordings, photographs, field notes and archival records

The last point matters for collections: material made *about* Indigenous peoples, including by researchers, governments and photographers, can contain ICIP even when someone else owns the copyright.

ICIP rights are generally described as the right of Indigenous peoples to:

- Own and control their cultural heritage
- Decide whether, and how, it is used, and refuse uses they don't agree with
- Keep secret and sacred knowledge secret
- Protect the integrity of their culture from misuse or distortion
- Be properly attributed as the source
- Share in the benefits when their culture is used

### The legal position

At the time of writing, **Australia has no specific law that protects ICIP**. Some ICIP is partly protected by copyright, trade marks or confidentiality laws, but much of it is not. ICIP rights are recognised in Article 31 of the [United Nations Declaration on the Rights of Indigenous Peoples (UNDRIP)](https://www.un.org/development/desa/indigenouspeoples/declaration-on-the-rights-of-indigenous-peoples.html), which Australia has endorsed, and the Australian Government has committed to developing standalone ICIP legislation with First Nations people.

This means respecting ICIP is mostly a matter of **ethics, protocols and good practice** rather than legal compliance. Many cultural institutions and universities, including AIATSIS and the National Library of Australia, have ICIP protocols that set out how they do this. Check whether your own institution has one.

## What is ICMR?

**Indigenous Communal Moral Rights (ICMR)** extend the idea of moral rights to communities.

Under Australian copyright law, individual creators have **moral rights**: the right to be credited for their work, the right not to have their work falsely attributed, and the right not to have it treated in a way that harms their reputation. These rights belong to individuals. ICMR would give similar rights to Indigenous communities, recognising that a work by an individual artist can also embody the knowledge and culture of their community.

In practice, ICMR means:

- **Attributing the community**, not only the individual creator, where the material draws on communal knowledge
- **Not distorting or altering** cultural material in ways the community would find derogatory or harmful

A Copyright Amendment (Indigenous Communal Moral Rights) Bill was drafted in 2003 but was **never passed**, so ICMR is not law in Australia. It remains a useful principle for how cultural material should be credited and presented, and it fits naturally alongside ICIP in a cultural rights statement.

## When to add a cultural rights statement

Add a cultural rights statement to any item or media file that contains or relates to Aboriginal or Torres Strait Islander culture or knowledge. For example:

- Material created by Aboriginal or Torres Strait Islander people or communities
- Recordings of language, song, story or ceremony
- Images, names or voices of Aboriginal and Torres Strait Islander people
- Information about Country, sites, plants, animals or cultural practices
- Historical material collected by researchers, missions, governments or photographers
- Records linked to a language group with the [AustLang vocabulary](14b-austlang-language-groups.md): this is a good prompt to check whether a statement is needed

Add it **whatever the copyright status**. A statement is just as important on public domain or Creative Commons material, because those labels say nothing about cultural rights.

> ⚠️ **Some material shouldn't be published at all.** Secret or sacred material, gender-restricted knowledge, or material the community hasn't agreed to share should stay private. Set the item and media visibility to **private**, and don't put restricted details in public metadata, since a description can reveal as much as the material itself. See the [CARE principles](14a-care-principles.md).

## Where to record cultural rights in Omeka-S

Use two properties, kept separate from your copyright fields:

| What you're recording | Property | What to include |
| --- | --- | --- |
| ICIP and communal rights statement | `schema:usageInfo` | Whose ICIP it is, who to contact, what uses need permission, and how to attribute the community |
| Cultural access restrictions or warnings | `schema:conditionsOfAccess` | Cultural warnings and any restrictions on who should view the material |

Record copyright separately in `schema:copyrightHolder`, `schema:copyrightNotice` and `schema:license` (see [Copyright and licensing](13-copyright-and-licensing.md)). The copyright holder and the ICIP holder are often different people: keeping them in separate fields makes that clear.

### Writing an ICIP statement

A good ICIP statement answers four questions:

1. **Whose culture is it?** Name the community, language group or Traditional Owners, as they wish to be named.
2. **Who has authority?** Give a contact for the community or the person authorised to speak for the material.
3. **What needs permission?** Say which uses need the community's consent.
4. **How should it be credited?** Give the attribution the community wants (this is where ICMR comes in).

Example statements (replace the text in square brackets):

> This item contains Indigenous Cultural and Intellectual Property (ICIP) of the [community / language group] people. Please contact [name, organisation, email] before using, altering or sharing this material for any purpose.

> This recording contains cultural knowledge belonging to the [community] and is shared with their permission. Attribute as: [preferred attribution]. Do not alter or reuse without consent.

### Writing a cultural access statement

Example statements for `schema:conditionsOfAccess`:

> Aboriginal and Torres Strait Islander people are advised that this item contains images, names and voices of people who have died.

> Contains culturally sensitive material. Viewing is restricted to [group], as advised by [community / organisation].

### A worked example

A photograph taken in 1950 of a community gathering. Copyright has expired, but the community holds ICIP in what it shows.

| Property | Value |
| --- | --- |
| `schema:copyrightNotice` | Out of copyright (photograph taken before 1955) |
| `schema:license` | Public Domain Mark 1.0 (`https://creativecommons.org/publicdomain/mark/1.0/`) |
| `schema:usageInfo` | This photograph contains ICIP of the [community] people. Please contact [community organisation, email] before reproducing or publishing it. Attribute as: [preferred attribution]. |
| `schema:conditionsOfAccess` | Aboriginal and Torres Strait Islander people are advised that this image contains images of people who have died. |

Together, these fields tell a visitor that the photograph is legally free to reuse, **and** that the community expects to be asked and credited.

> 💡 **Tip:** Keep a private record of who gave permission and when. You can add it as a private field (see [CSV Import](05-csv-import.md)) so it stays with the item but isn't shown on your public site.

## Local Contexts Labels and Notices

[Local Contexts](https://localcontexts.org/) provides Traditional Knowledge (TK) and Biocultural (BC) Labels and Notices: standard, recognisable statements that communities and institutions can apply to material to express cultural rights and protocols. If a community uses Local Contexts Labels, you can record the Label text or link in `schema:usageInfo` alongside, or instead of, your own ICIP statement.

## Before you publish

- **Talk with the community** about what can be shared, how it should be described and how they want to be credited.
- **Check your institution's ICIP protocol**, if it has one.
- **Check every item and its media** for a cultural rights statement and any needed warnings.
- **Use the [Pre-publication checklist](08-pre-publication-checklist.md).**

## Related pages

- [Copyright and licensing](13-copyright-and-licensing.md)
- [Indigenous data governance](14-indigenous-data-governance.md)
- [CARE principles](14a-care-principles.md)
- [AustLang language groups](14b-austlang-language-groups.md)

## References

This module has been developed using the following resources:

Arts Law Centre of Australia. (2004). Submission to Attorney-General's Department on the draft Copyright Amendment (Indigenous Communal Moral Rights) Bill 2003. [https://www.artslaw.com.au/images/uploads/ArtsLawICMRDraftBillSub.pdf](https://www.artslaw.com.au/images/uploads/ArtsLawICMRDraftBillSub.pdf)

Australian Government. (n.d.). About ICIP. Creative Workplaces. [https://creativeworkplaces.gov.au/first-nations-relations/indigenous-cultural-and-intellectual-property-icip/about-icip](https://creativeworkplaces.gov.au/first-nations-relations/indigenous-cultural-and-intellectual-property-icip/about-icip)

Australian Institute of Aboriginal and Torres Strait Islander Studies. (n.d.). PBC resources: Metadata. [https://aiatsis.gov.au/sites/default/files/research_pub/PBC%20resources%20-%20Metadata.pdf](https://aiatsis.gov.au/sites/default/files/research_pub/PBC%20resources%20-%20Metadata.pdf)

Australian Institute of Aboriginal and Torres Strait Islander Studies. (2021). PBC resources: Metadata and digital media files. [https://aiatsis.gov.au/sites/default/files/research_pub/PBC%20resources%20-%20Metadata%20and%20digital%20media%20files.pdf](https://aiatsis.gov.au/sites/default/files/research_pub/PBC%20resources%20-%20Metadata%20and%20digital%20media%20files.pdf)

Australian Institute of Aboriginal and Torres Strait Islander Studies. (2020). AIATSIS Code of Ethics for Aboriginal and Torres Strait Islander Research. [https://aiatsis.gov.au/research/ethical-research/code-ethics](https://aiatsis.gov.au/research/ethical-research/code-ethics)

Janke, T. (2021). *True tracks: Respecting Indigenous knowledge and culture*. UNSW Press.

Local Contexts. (n.d.). [https://localcontexts.org/](https://localcontexts.org/)

Senate Standing Committee on Environment, Communications, Information Technology and the Arts. (2007). Indigenous art: Securing the future. Chapter 11: Indigenous cultural and intellectual property rights. Parliament of Australia. [https://aph.gov.au/Parliamentary_Business/Committees/Senate/Environment_and_Communications/Completed_inquiries/2004-07/indigenousarts/report/c11](https://aph.gov.au/Parliamentary_Business/Committees/Senate/Environment_and_Communications/Completed_inquiries/2004-07/indigenousarts/report/c11)

United Nations. (2007). United Nations Declaration on the Rights of Indigenous Peoples. [https://www.un.org/development/desa/indigenouspeoples/declaration-on-the-rights-of-indigenous-peoples.html](https://www.un.org/development/desa/indigenouspeoples/declaration-on-the-rights-of-indigenous-peoples.html)
