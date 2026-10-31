---
layout: default
title: Adding items
nav_order: 3
---

# Adding items

*Create and edit items one at a time, and link them to each other.*

This page covers adding and editing individual items in the Omeka-S admin interface. To add many items at once from a spreadsheet, see [CSV Import](05-csv-import.md). To attach images, audio or other files, see [Adding Media](06-adding-media.md).

## Before you start: resource templates

A **resource template** is a predefined set of properties for describing one type of item, such as a Person, Place or Event. Choosing a template when you create an item gives you the right fields straight away, instead of adding every property by hand.

Omeka-S comes with a set of pre-built resource templates for common objects of study in the humanities. These can be modified, and new ones can be added.

> **Curated Collections:** The Curated Collections team is building out the standard templates so that researchers don't need to configure fields themselves. Ask the team if your collection needs a field that isn't in the templates.

## Create a new item

1. Go to the admin dashboard. Next to each type of resource there is a **+** icon.
2. Click the **+** next to **Items**.

> 🖼️ **Image needed:** The admin dashboard with the + icon next to Items highlighted.

The new item page opens. By default it shows only the bare minimum: **Title** and **Description**.

> 🖼️ **Image needed:** The new item page showing only Title and Description.

3. Choose a template from the **Resource template** drop-down. The page fills with the properties from that template. Scroll down to see them all.

> 🖼️ **Image needed:** The Resource template drop-down with a template (for example Place) selected.

> 🖼️ **Image needed:** The new item page filled with the fields from the selected resource template.

4. Fill in the fields you need. You don't have to complete every field (see [Empty fields](#empty-fields) below).
5. Use the **Media** tab to attach files and the **Mapping** tab to add a location. See [Adding Media](06-adding-media.md) and [Adding geolocation and mapping](04-geolocation-mapping.md).
6. Click **Add** in the top right to save the new item.

Your new item appears at the top of the item list.

> 🖼️ **Image needed:** The item list with the newly added item at the top.

## Understanding the edit page

The same page is used to create new items and edit existing ones. It can look complicated, but it is simply a list of **properties** and their **values**.

> 🖼️ **Image needed:** The edit item page for an existing item.

### Property labels and vocabularies

Every property in Omeka-S belongs to a **vocabulary**: a published metadata standard that defines what each term means. The vocabularies installed in your Omeka-S are listed in the panel on the right of the edit page.

> 🖼️ **Image needed:** The edit item page with the vocabularies panel highlighted.

Each field shows a small label telling you which vocabulary and property it uses. For example, `schema:name` means the field uses the *name* property from Schema.org. A template can give a property a friendlier display label (for example "Cartographic Name") while still storing it as `schema:name` behind the scenes.

> 🖼️ **Image needed:** Close-up of a single field on the edit page showing its display label, its property label (for example schema:name), the red asterisk and the Add value button.

Using standard vocabularies makes the interface look more complex, but it means your collection can be exported and archived in a form that works outside Omeka-S and lasts longer. See [Linked open data](12-linked-open-data.md) and [Making your data FAIR](07-making-your-data-fair.md).

### Required fields and multiple values

- A **red asterisk (\*)** marks a required field. You can't save the item while it's empty.
- The **Add value** button under a field lets you add another value. Any property in Omeka-S can hold more than one value.

### Empty fields

Resource templates often include fields that your data doesn't use, such as *Region*, *Locality* or *Street address*. Leave them empty. Empty fields are ignored: they aren't shown on the item page, on maps or on your public site.

> 🖼️ **Image needed:** The edit page scrolled down to show several unused, empty fields.

### Fields that aren't in a standard vocabulary

Sometimes no standard vocabulary has a suitable property for your data, such as an Indigenous language family. In that case a custom vocabulary can be created (for example with a project prefix such as `calocal:`) and the new property added to the resource template.

## Edit an existing item

1. Open the item and click **Edit item** in the top right. Or, from the item list, click the pencil icon next to the item.
2. Make your changes, for example add a description.
3. Click **Save** in the top right.

> 🖼️ **Image needed:** The edit page with a description being added.

Omeka-S returns you to the item page with a green message: *Item successfully updated*. Check that your changes appear.

> 🖼️ **Image needed:** The item page after saving, with the green "Item successfully updated" message.

> 💡 **Tip:** To find an item quickly, use the search box at the top of the left-hand panel.

## Linking items to other items

A property can hold a link to another item or item set in your collection, instead of plain text. This is how Omeka-S records relationships, for example a site that is *contained in* a place, or a person who *performed at* an event.

Link fields look different from text fields: they show **No resource selected** and a small cube icon with buttons for **Items** and **Item sets**. The cube means the field links to another resource.

> 🖼️ **Image needed:** The edit page with a link field (for example "Contained in place") highlighted, showing "No resource selected" and the Items / Item sets buttons.

### Add a link

1. Open the item you want to link *from* and click **Edit item**.
2. Scroll to the link field you need.
3. Click the **Items** button. A **Select item** panel opens on the right, with a search box and a list of items.
4. Search for the item you want to link *to* and click it. The panel shows that item's details.
5. Click **Select resource** at the bottom of the panel.

> 🖼️ **Image needed:** The Select item panel with a search for the target item.

> 🖼️ **Image needed:** The Select item panel showing the chosen item's details, with the Select resource button highlighted.

The field now shows the linked item's name followed by a small cube, which shows it is a link and not just text.

> 🖼️ **Image needed:** The link field showing the selected item with its cube icon.

6. Click **Save**. If you don't save, the link won't be stored.

> 🖼️ **Image needed:** The saved item page showing the link in the relevant field.

### Reverse links: the Linked resources tab

Links in Omeka-S go one way: from the item you edited to the item you selected. Research relationships usually go both ways, so Omeka-S gives you an easy way to see the reverse.

Click the link to open the item you linked to, then open its **Linked resources** tab. It lists every item in your collection that links to this one.

> 🖼️ **Image needed:** The Linked resources tab of the target item, listing the item that links to it.

> 💡 **Tip:** To link many items at once, for example every site to its location, use [CSV Import](05-csv-import.md) and match records by identifier.

## Related pages

- [CSV Import](05-csv-import.md)
- [Adding Media](06-adding-media.md)
- [Controlled vocabularies and Value Suggest](11-controlled-vocabularies.md)
- [Adding geolocation and mapping](04-geolocation-mapping.md)

---

*Adapted from [Introduction to Omeka S](https://sydney-informatics-hub.github.io/omeka-s-intro/), Sydney Informatics Hub, The University of Sydney (MIT licence).*
