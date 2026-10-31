---
layout: default
title: Adding geolocation and mapping
nav_order: 4
---

# Adding geolocation and mapping

*Give your items a location and display them on a map on your public site.*

Omeka-S can store a location for any item and show your items on an interactive map. This uses the **Mapping** module, which adds a **Mapping** tab to items and a **Map by query** block for site pages.

## Viewing an item's location

Open an item and select its **Mapping** tab to see the location stored for it.

> 🖼️ **Image needed:** An item's Mapping tab showing a marker on the map.

The map opens zoomed in very close. Click the **minus (−)** button, or use your scroll wheel or trackpad, to zoom out and see where the item is.

## Adding a location to an item

You can add a location when you create a new item or edit an existing one.

1. Open the new or existing item in the edit page (see [Adding items](03-adding-items.md)).
2. Select the **Mapping** tab.
3. Use the map's drawing tools to place the location.
4. Click **Add** (new item) or **Save** (existing item).

> 🖼️ **Image needed:** The Mapping tab on the edit page, showing the drawing tools and a shape drawn on the map.

Locations don't have to be single points. Omeka-S supports:

| Type | Use it for |
| --- | --- |
| **Point** | A single spot, such as a building or site |
| **Line** | A route or boundary drawn as connected line segments |
| **Polygon** | An area with an irregular shape, such as a suburb |
| **Rectangle** | A bounding box around an area |

> ⚠️ **Approximate locations:** Make it clear when a location is approximate. For example, AustLang coordinates mark an approximate point for a language variety, not the boundaries of Country. See [AustLang language codes](14-austlang-language-codes.md).

## Adding locations in bulk

If your spreadsheet has latitude and longitude columns, you can add locations to many items at once during [CSV Import](05-csv-import.md). Imported coordinates appear as points on each item's Mapping tab.

## Showing your items on a map

To display items on a map on your public site, you need to do two things: assign the items to your site, then add a page with a map block.

### Step 1: Assign items to your site

Each site only "knows about" the items assigned to it. Only those items appear in the site's searches, maps and other displays. By default a new site has no items, and Omeka-S won't remind you to add them.

> ⚠️ **Common mistake:** If your map is empty, check that you have assigned items to the site.

1. In the left-hand panel, find your site and click **Resources** in its section.
2. Select **Add - keep existing items and assign items from a new search query**.
3. To add every item, leave the search query empty. To add only some items, fill in the query.
4. Click **Save**.

> 🖼️ **Image needed:** The site's Resources page with the Add option selected and the empty search query.

Open your site's **Resources** again to check the items have been added.

> 🖼️ **Image needed:** The site's Resources page showing that items are now assigned.

> 💡 **Tip:** A site can be set to include new items automatically, so items you add later appear without repeating this step.

### Step 2: Add a map page

1. Click **Pages** in your site's section of the left-hand panel, then click **Add new page**.
2. Give the page a **Title**. The URL slug fills in from the title. You can change it if you like.

> 🖼️ **Image needed:** The site Pages screen with the Add new page button.

> 🖼️ **Image needed:** The new page form with the Title and URL slug fields.

3. In the page editor, add a **Map by query** block. A page is built from blocks, each providing one feature, such as a map, a timeline or a piece of text.
4. You can leave the block's settings at their defaults for now.
5. Click **Save**. A green message confirms *Page successfully updated*.
6. Click **View** to open the public page in a new browser tab.

> 🖼️ **Image needed:** The page editor with a Map by query block added.

> 🖼️ **Image needed:** The public view of the new map page.

### How the map displays items

- Different types of item can appear as different coloured markers.
- Where items are close together, the map groups them into a **cluster** showing how many items it contains. Zoom in to separate them.
- Clicking a marker opens a **popup** with the item's name. Clicking the name opens the item's public page.

> 🖼️ **Image needed:** The map zoomed in to a region, showing clusters, markers and an open popup.

## Adding more information to map popups

By default the popup shows only the item's name. You can choose more properties to display.

1. Go back to the admin dashboard, open your site's map page and scroll to the **Map by query** block.
2. Find **Display properties in Popup** and search for the property you want to show.
3. Click **+ Add property** to add more.
4. Click **Save**, then **View** to check the result.

You must search using the property's internal name, not its display label. For example, a field labelled "Indigenous name" that uses `schema:alternateName` must be found by searching for **alternateName**. The edit page shows each field's internal name (see [Adding items](03-adding-items.md#property-labels-and-vocabularies)).

> 🖼️ **Image needed:** The Display properties in Popup field with a property being selected.

> 🖼️ **Image needed:** The popup on the public map showing the extra properties.

> 💡 **Tip:** Long text fields can make popups crowded and hard to read. Choose a few short, useful properties.

## Related pages

- [Getting started](02-getting-started.md)
- [Adding items](03-adding-items.md)
- [CSV Import](05-csv-import.md)
- [AustLang language codes](14-austlang-language-codes.md)

---

*Adapted from [Introduction to Omeka S](https://sydney-informatics-hub.github.io/omeka-s-intro/), Sydney Informatics Hub, The University of Sydney (MIT licence).*
