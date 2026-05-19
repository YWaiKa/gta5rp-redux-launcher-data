# GTA 5 RP Redux Launcher — Data Backend

This repository is the online backend for the GTA 5 RP Redux Launcher.

## How it works

- `data.json` — the catalog of categories and reduxes that all launcher users read on startup.
- **GitHub Releases** — every published redux gets its own release. The redux `.zip` and its cover image are uploaded as release assets, and the launcher links to `browser_download_url` in `data.json`.

The launcher never writes here unless you log in as an admin with a Personal Access Token.

## Manual edits

If you need to remove an entry by hand, edit `data.json` directly. The shape is:

```json
{
  "categories": [
    { "id": "cat_...", "name": "Graphics", "order": 0 }
  ],
  "reduxes": [
    {
      "id": "rdx_...",
      "categoryId": "cat_...",
      "name": "Realistic Reshade",
      "description": "...",
      "coverUrl": "https://github.com/YWaiKa/gta5rp-redux-launcher-data/releases/download/...",
      "downloadUrl": "https://github.com/YWaiKa/gta5rp-redux-launcher-data/releases/download/...",
      "installTarget": "",
      "version": "1.0.0",
      "fileSize": 12345
    }
  ],
  "updatedAt": "2025-..."
}
```