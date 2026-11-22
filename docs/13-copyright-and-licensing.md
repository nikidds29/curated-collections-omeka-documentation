---
layout: default
title: Copyright and licensing
nav_order: 13
---

# Copyright and licensing

*Tell people who owns your material and how they can use it.*

Every item and media file in your collection should say two things: **who holds the rights** and **what people are allowed to do with it**. Clear rights information protects creators and communities, helps people reuse your collection properly, and is a core part of making data FAIR (see [Making your data FAIR](07-making-your-data-fair.md)).

There are three layers of rights to think about:

1. **Copyright status:** is the material in copyright, out of copyright (public domain), or unknown?
2. **Licence or rights statement:** what can people do with it?
3. **Cultural rights:** are there Indigenous cultural rights or access protocols that apply, whatever its copyright status?

This page covers the first two layers and shows where all three go in Omeka-S. Cultural rights are covered in detail in [Cultural rights: ICIP and ICMR](14c-cultural-rights.md).

## Key terms

| Term | What it means |
| --- | --- |
| **Copyright** | The legal right to copy, publish, adapt and share a work. In Australia it applies automatically when a work is created; there's no need to register it. |
| **Copyright holder** | The person or organisation who owns the copyright. This isn't always the creator: an employer, publisher or institution may own it. |
| **Public domain** | Material that is no longer (or was never) protected by copyright, so anyone can use it. |
| **Licence** | Permission from the copyright holder that sets out how others can use a work. |
| **Rights statement** | A standard label that describes an item's copyright status when you can't (or don't need to) license it. |
| **ICIP** | Indigenous Cultural and Intellectual Property: the rights of Aboriginal and Torres Strait Islander peoples in their cultural heritage. See [Cultural rights: ICIP and ICMR](14c-cultural-rights.md). |

## How long copyright lasts in Australia

For most works (text, artworks, music and photographs taken from 1955 onwards), copyright generally lasts for the **life of the creator plus 70 years**. Because of changes to Australian law over time, the National Library of Australia gives this general rule of thumb:

- **Published works** are generally in the public domain if the creator **died before 1 January 1955**.
- **Photographs** taken **before 1955** are generally in the public domain.
- **Unpublished works** are generally in the public domain if the creator died before 1 January 1950 (this date moves forward each year).

Other types of material have their own rules. Sound recordings, films, government (Crown) material and works by unknown creators can all differ. If you're not sure, check the [National Library of Australia's guide](https://www.library.gov.au/services/copyright-library-collections/how-long-does-copyright-last) or the [Australian Copyright Council](https://www.copyright.org.au/) fact sheets.

> ⚠️ **Out of copyright doesn't mean free of obligations.** Material can be in the public domain and still be subject to Indigenous cultural rights, donor conditions or privacy concerns. A photograph of a ceremony taken in 1940 is out of copyright, but the community it depicts may still have the right to decide how it is shown. See [Cultural rights: ICIP and ICMR](14c-cultural-rights.md).

## Public domain material

When material is in the public domain, label it clearly so people know they can reuse it. Creative Commons provides two tools for this:

| Tool | Use it when | URI |
| --- | --- | --- |
| **Public Domain Mark** | Copyright has **expired** (for example, a photograph taken in 1930) | `https://creativecommons.org/publicdomain/mark/1.0/` |
| **CC0** | A copyright holder **chooses to give up** their rights and place a work in the public domain (for example, your own collection metadata) | `https://creativecommons.org/publicdomain/zero/1.0/` |

Only use CC0 for material you own the rights to. Use the Public Domain Mark for material where copyright has run out.

## Creative Commons licences

[Creative Commons](https://creativecommons.org/licenses/) (CC) licences let a copyright holder give everyone permission to use a work, on conditions they choose. All six licences require users to credit the creator (**BY**). The other conditions are:

- **SA (ShareAlike):** new works based on this one must use the same licence.
- **NC (NonCommercial):** no commercial use.
- **ND (NoDerivatives):** the work can be shared but not changed.

| Licence | People can... | URI |
| --- | --- | --- |
| **CC BY** | Share, adapt and use commercially, with credit | `https://creativecommons.org/licenses/by/4.0/` |
| **CC BY-SA** | Share, adapt and use commercially, with credit, using the same licence | `https://creativecommons.org/licenses/by-sa/4.0/` |
| **CC BY-NC** | Share and adapt for non-commercial purposes, with credit | `https://creativecommons.org/licenses/by-nc/4.0/` |
| **CC BY-NC-SA** | Share and adapt for non-commercial purposes, with credit, using the same licence | `https://creativecommons.org/licenses/by-nc-sa/4.0/` |
| **CC BY-ND** | Share unchanged, including commercially, with credit | `https://creativecommons.org/licenses/by-nd/4.0/` |
| **CC BY-NC-ND** | Share unchanged for non-commercial purposes, with credit | `https://creativecommons.org/licenses/by-nc-nd/4.0/` |

Before you apply a CC licence, check two things:

- **You must hold the copyright, or have permission from the copyright holder.** You can't license someone else's work. If you've digitised material owned by someone else, the original copyright holder's rights still apply.
- **A CC licence only deals with copyright.** It doesn't cover cultural rights. An open licence on Indigenous cultural material could allow uses the community would not agree to, so talk with the relevant community before licensing it. See [Cultural rights: ICIP and ICMR](14c-cultural-rights.md).

## Rights statements

If you can't license an item, for example because you don't own the copyright or don't know who does, use a rights statement instead. [RightsStatements.org](https://rightsstatements.org/en/statements/) provides 12 standard statements, each with its own URI, in three groups: **In Copyright**, **No Copyright** and **Other**.

The statements most useful for Australian collections are:

| Statement | Use it when | URI |
| --- | --- | --- |
| **In Copyright** | The item is in copyright and you have permission to show it, but not to license it | `http://rightsstatements.org/vocab/InC/1.0/` |
| **In Copyright – Educational Use Permitted** | The rights holder allows educational use only | `http://rightsstatements.org/vocab/InC-EDU/1.0/` |
| **In Copyright – Non-Commercial Use Permitted** | The rights holder allows non-commercial use only | `http://rightsstatements.org/vocab/InC-NC/1.0/` |
| **In Copyright – Rights-holder(s) Unlocatable or Unidentifiable** | The item is in copyright but you can't find or identify the rights holder | `http://rightsstatements.org/vocab/InC-RUU/1.0/` |
| **No Copyright – Contractual Restrictions** | The item is out of copyright, but an agreement (such as a donor agreement) limits its use | `http://rightsstatements.org/vocab/NoC-CR/1.0/` |
| **No Copyright – Other Known Legal Restrictions** | The item is out of copyright, but another law limits its use | `http://rightsstatements.org/vocab/NoC-OKLR/1.0/` |
| **Copyright Not Evaluated** | You haven't checked the copyright status yet | `http://rightsstatements.org/vocab/CNE/1.0/` |
| **Copyright Undetermined** | You've tried but can't work out the copyright status | `http://rightsstatements.org/vocab/UND/1.0/` |
| **No Known Copyright** | You believe the item is out of copyright but can't be certain | `http://rightsstatements.org/vocab/NKC/1.0/` |

Some statements apply only to particular countries, such as **No Copyright – United States** and **In Copyright – EU Orphan Work**. These usually don't suit Australian collections.

> 💡 **Tip:** "Copyright Not Evaluated" is honest, but aim to replace it with a more specific statement before you publish. The [Pre-publication checklist](08-pre-publication-checklist.md) includes rights checks.

## Choosing the right option

Work through these questions for each item or media file:

1. **Is it out of copyright?** Use the **Public Domain Mark**.
2. **Do you (or your institution) hold the copyright, and want people to reuse it?** Choose a **Creative Commons licence**, or **CC0** for metadata and data you're happy to give away.
3. **Is it in copyright and owned by someone else?** Use a **rights statement** that matches the permission you have.
4. **Don't know?** Use **Copyright Not Evaluated** or **Copyright Undetermined**, and come back to it.
5. **Does it contain Aboriginal or Torres Strait Islander cultural material?** Whatever you chose above, also add a **cultural rights statement**. See [Cultural rights: ICIP and ICMR](14c-cultural-rights.md).

## Recording rights in Omeka-S

Use these properties to record rights information. Keeping copyright, cultural rights and access conditions in separate fields means each one stays clear, and people can see that cultural obligations apply even when copyright doesn't.

| What you're recording | Property | Example |
| --- | --- | --- |
| Who owns copyright | `schema:copyrightHolder` | The photographer, or the institution |
| The copyright notice | `schema:copyrightNotice` | © 1968, [name], all rights reserved |
| The licence or rights statement | `schema:license` | `https://creativecommons.org/licenses/by/4.0/` |
| ICIP and communal rights statement | `schema:usageInfo` | This material contains ICIP of the [community]. Please contact [ICIP holder] before using, altering or sharing it. |
| Cultural access restrictions or warnings | `schema:conditionsOfAccess` | Contains images of people who have died; restricted to [group] |

A few tips:

- **Use the URI data type for `schema:license`.** Enter the licence or rights statement URI (from the tables above) with a short label, such as `CC BY 4.0` or `In Copyright`. On your site it then displays as a link to the full licence.
- **The copyright holder and the ICIP holder are often different.** A photographer may own the copyright in a photograph, while the community it depicts holds the ICIP. Record each in its own field.
- **Rights can differ between an item and its media.** An item record might describe an object, while an attached photograph of it has its own photographer and licence. Add rights fields to your media as well as your items (see [Adding Media](06-adding-media.md)).
- **License your metadata too.** Your descriptions are separate from the material they describe. Many collections release metadata under CC0 or CC BY so others can reuse it freely.
- **Check your property list.** If `schema:usageInfo` or `schema:conditionsOfAccess` doesn't appear when you add properties to a resource template, contact your platform administrator. Newer schema.org properties depend on which version of the vocabulary is installed.

The ICIP statement and cultural access fields are explained in [Cultural rights: ICIP and ICMR](14c-cultural-rights.md), including when to use them and example wording.

## Related pages

- [Making your data FAIR](07-making-your-data-fair.md)
- [Pre-publication checklist](08-pre-publication-checklist.md)
- [Linked open data](12-linked-open-data.md)
- [Indigenous data governance](14-indigenous-data-governance.md)
- [Cultural rights: ICIP and ICMR](14c-cultural-rights.md)

## References

This module has been developed using the following resources:

Australian Copyright Council. (n.d.). [https://www.copyright.org.au/](https://www.copyright.org.au/)

Australian Institute of Aboriginal and Torres Strait Islander Studies. (n.d.). PBC resources: Metadata. [https://aiatsis.gov.au/sites/default/files/research_pub/PBC%20resources%20-%20Metadata.pdf](https://aiatsis.gov.au/sites/default/files/research_pub/PBC%20resources%20-%20Metadata.pdf)

Creative Commons. (n.d.). About CC licenses. [https://creativecommons.org/licenses/](https://creativecommons.org/licenses/)

National Library of Australia. (2024). How long does copyright last? [https://www.library.gov.au/services/copyright-library-collections/how-long-does-copyright-last](https://www.library.gov.au/services/copyright-library-collections/how-long-does-copyright-last)

RightsStatements.org. (n.d.). Rights statements. [https://rightsstatements.org/en/statements/](https://rightsstatements.org/en/statements/)

Schema.org. (n.d.). CreativeWork. [https://schema.org/CreativeWork](https://schema.org/CreativeWork)
