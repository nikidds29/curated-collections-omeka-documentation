---
layout: default
title: Getting started
nav_order: 2
---

# Getting started with Omeka-S

*Key ideas, logging in, and finding your way around the admin dashboard.*

This page introduces the basic building blocks of Omeka-S and shows you how to log in and move around. If you are new to Omeka-S, start here before moving on to [Adding items](03-adding-items.md) and [Adding geolocation and mapping](04-geolocation-mapping.md).

## What is Omeka-S?

Omeka-S is a web-based platform for creating and storing collections of items and the relationships between them, and for publishing those collections as websites.

Omeka-S was first designed for museums and galleries, where the main "thing" is an artefact, image or scanned document, and the information about it (who made it, when, where it was found) is its metadata. In most Curated Collections projects the opposite is true: the metadata *is* the research data, and media files support it.

## Key terms

| Term | What it means in Omeka-S |
| --- | --- |
| **Item** | The basic unit of a collection. An item can be anything your research needs it to be: a person, a place, a building, an event, a document. |
| **Item set** | A group of items, for example all the people or all the places in your collection. |
| **Resource** | A general term for an item or an item set. Some screens say "resources" instead of "items". |
| **Property** | A field that describes an item, such as *title* or *description*. Each property comes from a vocabulary (see below). |
| **Value** | The information entered in a property, for example "Wybalenna Aboriginal Establishment". A property can hold more than one value. |
| **Vocabulary** | A published metadata standard that defines what properties mean, such as Dublin Core (`dcterms:`) or Schema.org (`schema:`). |
| **Resource template** | A predefined set of properties used to describe one type of item, so you don't have to add each property by hand. |
| **Site** | A public website built from items in your Omeka-S installation. One installation can host several sites, each showing its own selection of items. |

## Thinking about your data model

Before you add or import data, it helps to sketch out a **data model**: the types of things in your collection, the properties each one has, and how they relate to each other. For example, a collection might have *Locations* and *Sites*, where every site belongs to a location and some sites are related to each other.

> 🖼️ **Image needed:** A simple data model diagram showing two types of item, their properties, and arrows for the relationships between them.

A data model doesn't depend on Omeka-S: it's simply a way of organising how you want to represent your collection. Traditional databases require you to design every table up front, and all data has to fit that mould. Omeka-S is more flexible, but it still needs some standardisation, which is what resource templates and vocabularies provide.

> 🖼️ **Image needed:** Diagram showing items grouped into two item sets, with arrows for the links between items.

### How items, item sets and sites fit together

All the items in your Omeka-S installation sit in one shared pool. Item sets group them. Sites are public websites that each display a chosen selection of those items, so different sites can show different parts of the same collection.

> 🖼️ **Image needed:** Diagram showing the pool of items in Omeka-S on one side and two sites on the other, with dotted lines showing which items each site can see.

## Logging in

1. Go to the web address for your Omeka-S installation. Curated Collections users receive this address, and their login details, from the Curated Collections team.
2. Click the **Admin dashboard** link (or **Log in**) on the public home page.
3. Enter your email address and password.

> 🖼️ **Image needed:** The public home page of an Omeka-S installation, with the login link highlighted.

> 🖼️ **Image needed:** The Omeka-S login screen.

> **Curated Collections:** New installations start with a long default web address provided by the national research cloud (Nectar). Collections can move to a Curated Collections address or their own custom domain later.

## The admin dashboard

Once you've logged in, you'll see the admin dashboard. This is where you manage everything in your installation.

> 🖼️ **Image needed:** The admin dashboard, with the left-hand navigation panel and the Manage Resources and Manage Sites areas highlighted.

The **left-hand navigation panel** is how you move around Omeka-S. The two sections you'll use most are:

- **Sites** (under the search box): set up and edit the public-facing websites.
- **Resources**: view, add and edit the items, item sets and media that your sites are built from.

The main area of the dashboard repeats these two sections: **Manage Resources** summarises what's in your installation, and **Manage Sites** lists your websites.

## Viewing items

Click **Items** in the left-hand panel to see a list of all the items in your installation. Click any title to open that item.

> 🖼️ **Image needed:** The item list view.

Each item page has three tabs:

| Tab | What it shows |
| --- | --- |
| **Metadata** | The item's properties and values, such as name, identifier and description. |
| **Linked resources** | Other items that link *to* this item. See [Linking items](03-adding-items.md#linking-items-to-other-items). |
| **Mapping** | The item's location on a map, if it has one. See [Adding geolocation and mapping](04-geolocation-mapping.md). |

> 🖼️ **Image needed:** A single item open on the Metadata tab.

To change an item, click **Edit item** in the top right of the item page. Editing is covered in [Adding items](03-adding-items.md).

## Next steps

- [Adding items](03-adding-items.md): create and edit items one at a time, and link them together
- [CSV Import](05-csv-import.md): import many items at once from a spreadsheet
- [Adding geolocation and mapping](04-geolocation-mapping.md): put your items on a map

---

*Adapted from [Introduction to Omeka S](https://sydney-informatics-hub.github.io/omeka-s-intro/), Sydney Informatics Hub, The University of Sydney (MIT licence).*
