# Changelog

## v1.0 — October 2026

First shared version.

### Features
- Opens several QVD files at once, each in its own tab.
- Dashboard with summary tiles, a field profile (distinct values, uniqueness, cardinality, nulls) and the file's byte layout.
- Data tab with search, sorting and copy to Excel (up to 100,000 rows).
- Fields tab with number formats, tags, bit layout and a table of each field's distinct values.
- Lineage tab with a sources table and an entries table.
- Header XML tab.
- Qlik branding, light and dark themes.

### Security
- Checks header values against the file before loading, so damaged or crafted files show an error instead of freezing the browser.
- Rejects headers that contain DOCTYPE or ENTITY declarations.
- Hides credential values in lineage and the XML header by default, including when you copy.
- Blocks all network connections with a Content Security Policy.
- Uses local fonts only. The earlier draft loaded a font from Google.

### Performance
- Sorting uses a counting sort: about 0.2 seconds for 3 million rows.
- Profiling, search and sort run in small steps with a progress display, so the page does not freeze.
- Text values are decoded only when they are shown.
- The data grid draws only the visible rows and columns.
