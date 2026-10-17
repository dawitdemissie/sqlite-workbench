# Demissie SQLite Workbench

A browser-based SQLite database browser, inspired by DB Browser for SQLite.
It runs entirely in your browser using [sql.js](https://github.com/sql-js/sql.js)
(SQLite compiled to WebAssembly), so it can be hosted for free on GitHub Pages.
Your database files are never uploaded anywhere.

## Features

- Open `.db` / `.sqlite` files (button or drag and drop), create new databases, load a sample
- Database structure view: tables, views, indexes, triggers, columns and `CREATE` statements
- Browse data with paging, sorting by column, and filtering across all columns
- Edit cells (double-click), set NULL, add and delete rows
- Execute SQL with Ctrl + Enter, run a selection, see timing and changed-row counts
- Import files into the open database:
  - SQLite databases (`.sqlite`, `.sqlite3`, `.db`, `.db3`, `.s3db`): pick which tables to copy, with their indexes, views and triggers
  - CSV / TSV files into a new table (separator and column types detected automatically)
  - SQL scripts (`.sql`), such as dumps from `sqlite3 .dump`
- Export a table, a filtered view, or a query result to CSV
- Save the modified database back to your computer

## Deploy on GitHub Pages

1. Create a new public repository on GitHub (e.g. `sqlite-workbench`).
2. Upload `index.html`, `README.md` and `.nojekyll` to the repository root.
3. Go to **Settings → Pages**. Under "Build and deployment", choose
   **Deploy from a branch**, select `main` and `/ (root)`, then **Save**.
4. After a minute your app is live at
   `https://<your-username>.github.io/sqlite-workbench/`.

## Run locally

Just open `index.html` in a browser, or serve the folder:

```
python -m http.server 8000
```

## Notes

- Changes live in memory until you click **Save database**, which downloads the updated file.
- Very large databases (hundreds of MB) are limited by browser memory.
- Needs an internet connection the first time to load sql.js and fonts from CDNs.
