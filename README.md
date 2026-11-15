# yoraito-office-addins — Shared Office Add-in Template

Shared template for Excel (Office.js) and Google Sheets (Apps Script) add-ins for all Yoraito tools.

## What's Included

- **Excel add-in** (Office.js): Sideloaded, fully local. Reads workbook → calls localhost API → shows results.
- **Google Sheets add-on** (Apps Script): Export sheet → opens local web app for comparison.
- **Templates**: Parameterized manifest.xml, HTML/JS, and Code.gs.
- **Documentation**: Sideloading guide, AppSource/Marketplace submission guide.

## How to Use

1. Copy this template into your tool's `addins/` directory
2. Replace placeholders (see `PLACEHOLDERS.md`)
3. For Excel: Sideload `manifest.xml` in Excel
4. For Sheets: Copy `Code.gs` into Apps Script

## Files

- `excel/manifest.xml.template` — Office.js manifest (parameterized)
- `excel/addin.html.template` — HTML/JS boilerplate (parameterized)
- `sheets/Code.gs.template` — Apps Script template (parameterized)
- `PLACEHOLDERS.md` — Placeholder reference
- `docs/SIDELOADING.md` — Sideloading guide
- `docs/PUBLISHING.md` — AppSource/Marketplace guide

## License

MIT License. Part of the Yoraito open-source finance stack.
