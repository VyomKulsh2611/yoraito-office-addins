# Sideloading Guide

## Excel (Office.js Add-in)

### Prerequisites
- Excel desktop (Windows or Mac)
- Local server running (`yoraito-<tool>-web`)

### Steps
1. Start the local server: `yoraito-<tool>-web` (opens browser at localhost:PORT)
2. Open Excel with a workbook
3. Go to **Insert** → **My Add-ins** → **Upload My Add-in**
4. Click **Browse** and select `manifest.xml`
5. Click **Upload**
6. The add-in appears in the ribbon under the **Yoraito** tab
7. Click the button to start

### Notes
- Sideloading is per-user, per-machine
- The local server must be running for the add-in to work
- HTTP localhost is allowed for sideloaded add-ins (no HTTPS needed)
- To remove: Insert → My Add-ins → right-click → Remove

## Google Sheets (Apps Script Add-on)

### Prerequisites
- Google account
- Local server running (`yoraito-<tool>-web`)

### Steps
1. Open your Google Sheet
2. Go to **Extensions** → **Apps Script**
3. Delete any existing code
4. Paste the contents of `Code.gs`
5. Click **Save** (Ctrl+S)
6. Refresh the Google Sheet
7. A new menu `__TOOL_NAME__` appears in the menu bar

### Notes
- Apps Script runs on Google's servers — it cannot reach localhost directly
- The add-on opens the local web app in a new browser tab
- For fully local processing, export your sheet as xlsx and use the web app directly
