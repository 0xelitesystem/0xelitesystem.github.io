# 0xelitesystem.github.io

The searchable index for every open-source repo I publish: 335 in total, 178 single-file browser tools with live demos and 157 plain-language references.

## Live site

https://0xelitesystem.github.io/

## What is here

- `index.html` one page, no build step, no dependencies. It fetches `catalog.json` and filters in the browser.
- `catalog.json` the machine-readable catalog: one entry per repo with slug (`s`), type (`t`, tool or ref), and description (`d`).
- `llms.txt` a plain-language summary for AI crawlers, following the llms.txt convention.
- `sitemap.xml` the index plus every live tool demo.
- `feed.xml` RSS of the 40 most recently created repos.
- `.github/workflows/update-catalog.yml` rebuilds all of the above from the live GitHub API every Monday, and keeps the counts in this page in sync.

## How the catalog stays honest

The workflow reads the live repo list, drops forks and archived repos, and refuses to write a catalog with fewer than 100 entries so a bad API response cannot wipe the index. Existing tool/reference classifications win over the automatic guess, so manual corrections survive a rebuild.

## Built by

[elitesystem.ai](https://elitesystem.ai)

## License

MIT.
