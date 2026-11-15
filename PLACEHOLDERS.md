# Placeholders Reference

Replace these placeholders in all template files when setting up a new tool's Office add-ins.

## Placeholders

| Placeholder | Description | Example (model-diff) | Example (recon) |
|---|---|---|---|
| `__TOOL_NAME__` | Display name | Yoraito Model Diff | Yoraito Recon |
| `__TOOL_NAME_LOWER__` | Lowercase, hyphenated | yoraito-model-diff | yoraito-recon |
| `__TOOL_DESCRIPTION__` | Short description | Diff two Excel models | Reconcile transactions |
| `__PORT__` | Default port | 17842 | 17843 |
| `__API_ENDPOINT__` | Main API endpoint | /api/diff | /api/match |
| `__CLI_COMMAND__` | CLI command name | yoraito-model-diff | yoraito-recon |
| `__FILE_ACCEPT__` | File types | .xlsx,.csv | .csv,.xlsx,.pdf |
| `__MENU_ACTION__` | Sheets menu action | Compare Models | Run Reconciliation |
| `__ADDIN_ID__` | Unique GUID for manifest | (generate new) | (generate new) |

## Files to Update

1. `excel/manifest.xml.template` → `excel/manifest.xml`
2. `excel/addin.html.template` → `excel/addin.html`
3. `sheets/Code.gs.template` → `sheets/Code.gs`

## Steps

1. Copy this template into your tool's `addins/` directory
2. Replace all placeholders in all files
3. Rename `.template` files (remove `.template` suffix)
4. For Excel: Sideload `manifest.xml` in Excel
5. For Sheets: Copy `Code.gs` into Apps Script

## Sideloading (Excel)

1. Start the local server: `yoraito-<tool>-web`
2. Excel → Insert → My Add-ins → Upload My Add-in
3. Select `manifest.xml`
4. Click the add-in button in the ribbon

## Google Sheets (Apps Script)

1. Open your Google Sheet
2. Extensions → Apps Script
3. Paste `Code.gs` content
4. Save and refresh
5. Use the menu: `__TOOL_NAME__` → `__MENU_ACTION__`

Note: Google Sheets add-ons run on Google's servers and cannot reach localhost.
The add-on opens the local web app in a new browser tab for the actual processing.
