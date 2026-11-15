# Publishing Guide

## Excel (Microsoft AppSource)

### Requirements
- HTTPS hosting for the add-in HTML (GitHub Pages, Vercel, Cloudflare)
- Updated manifest.xml with HTTPS SourceLocation
- Microsoft Partner Center account

### Steps
1. Host `addin.html` on an HTTPS endpoint
2. Update `manifest.xml` SourceLocation to HTTPS URL
3. Go to https://partner.microsoft.com
4. Create a new Office Add-in submission
5. Upload the manifest.xml
6. Submit for review (2-4 weeks)

### Notes
- AppSource review checks for security, performance, and UX
- The add-in must work without the local server (or clearly state the dependency)
- For our use case (local server required), sideloading is the primary distribution

## Google Sheets (Google Workspace Marketplace)

### Requirements
- Google Cloud project
- OAuth consent screen configured
- Apps Script project published

### Steps
1. Go to https://console.cloud.google.com
2. Create a new project
3. Enable Google Sheets API
4. Configure OAuth consent screen
5. Go to Apps Script → Deploy → New deployment
6. Select "Add-on" type
7. Submit to Marketplace (1-2 weeks review)

### Notes
- Google Workspace Marketplace review checks for security and functionality
- Apps Script add-ons run on Google's servers
- For our use case (local processing), the add-on is a launcher, not a full integration
