# HRM Prototypes

Static hub for live UX prototypes, hosted on GitHub Pages.

**Live hub:** `https://<org>.github.io/hrm-prototypes/`

---

## Adding a new prototype

1. Create a subfolder in the repo root, e.g. `my-new-feature/`
2. Add an `index.html` inside it (your prototype entry point)
3. Open `index.html` (the hub root) and add your folder name to the `FOLDERS` array:

   ```js
   const FOLDERS = [
     "employee-profile-branding",
     "permissions-layout-update",
     "my-new-feature",   // ← add this line
   ];
   ```

4. Commit and push — the hub will show the new card automatically.

---

## Adding metadata (optional)

Create a `meta.json` file inside your prototype folder:

```json
{
  "title": "My New Feature",
  "description": "Short description shown on the hub card.",
  "tags": ["navigation", "v2"],
  "updated": "2024-06-01"
}
```

All fields are optional. Without `meta.json`, the hub falls back to the humanized folder name and shows no description, tags, or date.

---

## How URLs work on GitHub Pages

| Context | URL |
|---|---|
| Hub root | `https://<org>.github.io/hrm-prototypes/` |
| Prototype | `https://<org>.github.io/hrm-prototypes/permissions-layout-update/` |

Links in the hub are **relative** (`./folder-name/`), so they work both locally (open `index.html` in a browser) and on GitHub Pages without any configuration changes.

> GitHub Pages serves the repo from the `main` branch by default. Enable it under **Settings → Pages → Source**.
