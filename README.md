# QVD Viewer

QVD Viewer lets you look inside Qlik QVD (Qlik View Data) files without opening Qlik Sense. It is a single HTML file that runs in Microsoft Edge or Google Chrome.

> Internal tool created by Kiril Kirin, Qlik Professional Services. It is not an official Qlik product.

## Use it

1. Download `index.html` from this repository.
2. Open the file in Edge or Chrome.
3. Drag one or more QVD files onto the page, or select **Open QVD files**.

You can open several files at the same time. Each file gets its own tab.

## What you can do

- **Dashboard:** see row and field counts, file size, distinct values, nulls, how unique each field is, and how the file's bytes are split between header, symbol tables and index table.
- **Data:** browse all records. Search all fields or one field, sort any column, and copy up to 100,000 rows to Excel.
- **Fields:** check each field's number format, tags and bit layout. Select a field to see its distinct values and how many rows have each one.
- **Lineage:** see each source and the statement that loaded it. Copy the list to Excel.
- **Header XML:** read and copy the full XML header.

## Privacy

- The browser reads files on your computer. Nothing is uploaded.
- A Content Security Policy blocks all network connections, so the page cannot send data anywhere.
- Passwords, user IDs and tokens in lineage are hidden by default, including when you copy. Select **Show credentials** to see them.

## Limits

- Encrypted QVD files cannot be read.
- The whole file is loaded into browser memory. Files over about 1.5 GB may not open.
- Dates and timestamps stored only as numbers show in ISO format (for example 2024-01-05), not in the field's own format pattern.

## Versions

See [CHANGELOG.md](CHANGELOG.md).
