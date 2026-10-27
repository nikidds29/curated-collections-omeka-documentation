# Curated Collections Omeka Documentation

Source for the Curated Collections Omeka Documentation, a help guide for Omeka-S users, published via GitHub Pages.

**Live site:** https://nikidds29.github.io/curated-collections-omeka-documentation/

## Structure

Every page in this guide is flat: nothing is nested, so the sidebar never hides a page under a collapse/expand arrow. The sidebar order is controlled by each page's `nav_order`, and the number at the start of each filename in `docs/` matches that page's `nav_order`, so listing the folder shows the pages in the order they appear in the guide.

All guide pages live in the `docs/` folder. Don't put pages at the top level of the repo: they will still appear in the sidebar, but their links and images will break.

```
index.md                                1. Home
docs/
  02-csv-import.md                      2. CSV Import
  03-adding-media.md                    3. Adding Media
  04-making-your-data-fair.md           4. Making your data FAIR (with PDF download)
  05-pre-publication-checklist.md       5. Pre-publication checklist (with PDF download)
  06-data-cleaning.md                   6. Data cleaning
  07-file-sideload.md                   7. File Sideload
  08-controlled-vocabularies.md         8. Controlled vocabularies and Value Suggest
  09-linked-open-data.md                9. Linked open data
  10-care-principles.md                10. CARE principles
  11-austlang-language-codes.md        11. AustLang language codes
  images/                               Screenshots and figures, one folder per page
    adding-media/
    austlang/
    csv-import/
    fair-data-access/
downloads/
  CC-FAIR-Data-Access.pdf               PDF version of page 4
  CC-Pre-Publication-Checklist.pdf      PDF version of page 5
_config.yml                             Site settings (theme, title, baseurl)
```

### Planned pages

These are listed under "Coming soon" on the home page. When you add one, give it the next number and add it to the table on the home page.

- Persistent identifiers
- RO-Crate
- AI use and acknowledgement

## Adding a new page

1. Create a Markdown file in `docs/`, named with a number prefix one higher than the last page (e.g. `12-your-page-name.md`).
2. Add front matter at the top:

   ```
   ---
   layout: default
   title: Your Page Title
   nav_order: 12
   ---
   ```

   `nav_order` should match the number in the filename.
3. Add a row for the page to the "In this guide" table in `index.md`, linking to `docs/12-your-page-name.md`. Only link to pages that exist; list planned pages under "Coming soon" without a link.
4. To slot a page in between two existing ones, renumber every later file (both the filename prefix and its `nav_order`) and update any links that point to a renumbered file.
5. Put screenshots in a folder under `docs/images/` and reference them with a description, e.g. `![Description of the screenshot](images/your-folder/your-file.png)`.
6. Link to other pages using their `.md` filename (e.g. `[CSV Import](02-csv-import.md)`). GitHub Pages converts these to working links.
7. Commit or upload the changes. The live site rebuilds automatically within a minute or two.

To hide a page while you're drafting it, add `nav_exclude: true` to its front matter.

## Updating the PDFs

The PDFs in `downloads/` are made from the same source documents as pages 4 and 5. When you change either page, update and re-upload the matching PDF with the same filename so the download links keep working.

## If the structure changes

- **Renaming a file** changes that page's URL. Search the repo for the old filename and update every link to it.
- **Renaming the repository** changes the live address. Update `baseurl` in `_config.yml` and the live site link above to match.
- **Deleting a page** leaves dead links on any page that linked to it. The site doesn't warn about broken links, so check by eye.
