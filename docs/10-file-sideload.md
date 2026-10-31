---
layout: default
title: File Sideload
nav_order: 10
---

# File Sideload

Official documentation: [Omeka-S user manual: File Sideload](https://omeka.org/s/docs/user-manual/modules/filesideload/)

The [File Sideload module](https://omeka.org/s/modules/FileSideload/) lets you add media files that are **already stored on the server** where Omeka-S is installed, instead of uploading them one at a time through your browser.

<!-- TODO: Confirm whether File Sideload is enabled on Curated Collections, and who to contact to get files onto the server. -->

## When to use File Sideload

File Sideload is useful when:

- you have **many files** to add at once
- your files are **too large** to upload through a web form
- you want to add a **whole folder** of files to one item, such as every page image of a scanned manuscript

For a few small files, uploading them directly on the item's Media tab is usually simpler. See [Adding Media](06-adding-media.md).

## Before you start

| You need | Notes |
| --- | --- |
| The File Sideload module installed and configured | Done by a site administrator |
| A **sideload directory** on the server | A folder that Omeka-S has permission to read |
| Your files copied into that directory | Usually done by an administrator or through a file transfer tool |
| Clean, consistent file names | File names are how you will find and match your files. See [Data cleaning](09-data-cleaning.md). |

> **Curated Collections:** *To be added: how to request a sideload directory and transfer your files.*

<!-- TODO: Add Curated Collections process for getting files into the sideload directory. -->

### File naming tips

- Use only letters, numbers, hyphens and underscores. Avoid spaces and special characters.
- Keep the correct file extension (`.jpg`, `.tif`, `.pdf`, `.mp3`).
- If you will match files to records in a spreadsheet, make each file name unique.

## Adding sideloaded files to a single item

1. Open the item and go to the **Media** tab.
2. In the **Add media** panel, choose **Sideload** (for one file) or **Sideload directory** (for a folder of files).
3. Select the file or folder from the list.
4. Give the media a meaningful title.
5. Click **Save**.

<!-- Screenshot placeholder: docs/images/file-sideload/ -->

## Adding sideloaded files with CSV Import

File Sideload works with [CSV Import](05-csv-import.md), so you can attach many files to many records in one batch.

1. In your spreadsheet, add a column containing the **file name** of each item's media, exactly as it appears in the sideload directory.
2. During import, on the mapping screen, click the **+** beside the file name column.
3. From the **Media** menu, choose **Sideload**, then click **Apply changes**.
4. Complete the import as usual.

<!-- Screenshot placeholder: docs/images/file-sideload/ -->

> **Important:** File Sideload can be set to delete files from the sideload directory once they have been added. **Turn this off when using CSV Import**, so the files are still there if you need to re-run or undo an import.

## After sideloading

- Check each item to make sure the right media is attached.
- Add or check **rights and licence information** for every media file.
- Set the **primary media** if an item has more than one file.

## Troubleshooting

| Problem | Things to check |
| --- | --- |
| The file or folder doesn't appear in the list | The file is in the sideload directory; Omeka-S has permission to read it |
| CSV Import can't find a file | The file name in the spreadsheet matches exactly, including capitals and extension |
| A file is missing after import | Whether file deletion is turned on in the module settings |

<!-- TODO: Add common Curated Collections issues as they come up. -->
