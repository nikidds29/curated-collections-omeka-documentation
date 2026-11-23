# Curated Collections Omeka Documentation

Source for the Curated Collections Omeka Documentation, a help guide for Omeka-S users, published via GitHub Pages.

**Live site:** https://nikidds29.github.io/curated-collections-omeka-documentation/

## Structure

Every page in this guide is flat: nothing is nested, so the sidebar never hides a page under a collapse/expand arrow. The sidebar order is controlled by each page's `nav_order`, and the number at the start of each filename in `docs/` matches that page's `nav_order`, so listing the folder shows the pages in the order they appear in the guide.

Pages 14a, 14b and 14c follow page 14 (Indigenous data governance) as a group. They use decimal `nav_order` values (`14.1`, `14.2` and `14.3`) so they sit together in the sidebar without renumbering the pages after them. Don't add `parent:` or `has_children:` to any page, as that nests pages in the sidebar.

All guide pages live in the `docs/` folder. Don't put pages at the top level of the repo: they will still appear in the sidebar, but their links and images will break.

```
index.md                                1. Home
docs/
  02-getting-started.md                 2. Getting started
  03-adding-items.md                    3. Adding items
  04-geolocation-mapping.md             4. Adding geolocation and mapping
  05-csv-import.md                      5. CSV Import
  06-adding-media.md                    6. Adding Media
  07-making-your-data-fair.md           7. Making your data FAIR (with PDF download)
  08-pre-publication-checklist.md       8. Pre-publication checklist (with PDF download)
  09-data-cleaning.md                   9. Data cleaning
  10-file-sideload.md                  10. File Sideload
  11-controlled-vocabularies.md        11. Controlled vocabularies and Value Suggest
  12-linked-open-data.md               12. Linked open data
  13-copyright-and-licensing.md        13. Copyright and licensing
  14-indigenous-data-governance.md     14. Indigenous data governance
  14a-care-principles.md               14.1 CARE principles
  14b-austlang-language-groups.md      14.2 AustLang language groups
  14c-cultural-rights.md               14.3 Cultural rights: ICIP and ICMR
  15-persistent-identifiers.md         15. Persistent identifiers
  16-ro-crate-digital-preservation.md  16. RO-Crate and digital preservation (outline)
  17-ai-use-and-acknowledgement.md     17. Using AI and acknowledging AI use (outline)
  18-search-and-query.md               18. Search and query
  _archive_13-care-principles.md       Retired (not published)
  _archive_14-austlang-language-codes.md  Retired (not published)
  images/                               Screenshots and figures, mostly one folder per page
    search-and-query-01-items-list.png  Screenshots for page 18 (kept at the top of images/)
    search-and-query-02-advanced-search.png
    adding-media/
    austlang/
    csv-import/
    fair-data-access/
downloads/
  CC-FAIR-Data-Access.pdf               PDF version of page 7
  CC-Pre-Publication-Checklist.pdf      PDF version of page 8
_config.yml                             Site settings (theme, title, baseurl)
```

### Pages in progress

Pages 16 and 17 are outlines. Sections still to be written are marked **✏️ Content needed**, and places where a screenshot is needed are marked **🖼️ Image needed** (pages 2 to 4 and 15 to 17).

## Adding a new page

1. Create a Markdown file in `docs/`, named with a number prefix one higher than the last page (e.g. `18-your-page-name.md`).
2. Add front matter at the top:

   ```
   ---
   layout: default
   title: Your Page Title
   nav_order: 18
   ---
   ```

   `nav_order` should match the number in the filename.
3. Add a row for the page to the "In this guide" table in `index.md`, linking to `docs/18-your-page-name.md`. Only link to pages that exist; list planned pages under "Coming soon" without a link.
4. To slot a page in between two existing ones, renumber every later file (both the filename prefix and its `nav_order`) and update any links that point to a renumbered file.
5. Put screenshots in a folder under `docs/images/` and reference them with a description, e.g. `![Description of the screenshot](images/your-folder/your-file.png)`.
6. Link to other pages using their `.md` filename (e.g. `[CSV Import](05-csv-import.md)`). GitHub Pages converts these to working links.
7. Commit or upload the changes. The live site rebuilds automatically within a minute or two.

To hide a page while you're drafting it, add `nav_exclude: true` to its front matter.

## Archiving a page

To retire a page without deleting it:

1. Rename the file with an `_archive_` prefix (for example, `_archive_13-care-principles.md`). Jekyll doesn't publish files whose names start with an underscore.
2. Add `published: false` to its front matter.

The page disappears from the live site and the sidebar, but stays in the repository and its history. Search the repo for the old filename and update any links that pointed to it.

## Updating the PDFs

The PDFs in `downloads/` are made from the same source documents as pages 7 and 8. When you change either page, update and re-upload the matching PDF with the same filename so the download links keep working.

## If the structure changes

- **Renaming a file** changes that page's URL. Search the repo for the old filename and update every link to it.
- **Renaming the repository** changes the live address. Update `baseurl` in `_config.yml` and the live site link above to match.
- **Deleting a page** leaves dead links on any page that linked to it. The site doesn't warn about broken links, so check by eye.
