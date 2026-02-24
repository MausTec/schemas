# Maus-Tec JSON Schemas

This repository hosts JSON Schema definitions for Maus-Tec developer tooling.
Schemas are published at `https://schemas.maus-tec.com/` via GitHub Pages.

## Published Schemas

| Schema | URL |
|--------|-----|
| mt-actions plugin (v1.0.0) | `https://schemas.maus-tec.com/mt-actions/v1.0.0/plugin.json` |

## Usage

Add a `$schema` field to your plugin JSON file to enable editor validation and
autocompletion in VS Code and other tools:

```json
{
  "$schema": "https://schemas.maus-tec.com/mt-actions/v1.0.0/plugin.json",
  "displayName": "My Plugin",
  ...
}
```

## Versioning

Schemas are versioned independently of firmware releases. A new version is
published only when the schema changes in a breaking or significant way. Older
versions remain at their original URLs indefinitely to avoid breaking existing
tooling.

## Contributing

Schema sources live in their respective library repos:

- `mt-actions` schema: `edge-o-matic-3000/lib/mt-actions/schema.json`

Publish a new version by copying the schema to the correct versioned path here
and updating the table above.
