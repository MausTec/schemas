# Maus-Tec JSON Schemas

This repository hosts JSON Schema definitions for Maus-Tec developer tooling.
Schemas are published at `https://schemas.maus-tec.com/` via GitHub Pages.

## Published Schemas

| Schema | URL | Description |
|--------|-----|-------------|
| EOM Package Common Definitions (v1.0.0) | `https://schemas.maus-tec.com/package/v1.0.0/common.json` | Shared definitions (Hub metadata, permissions, config schema) for all EOM artifact manifests |
| EOM Plugin Manifest (v1.0.0) | `https://schemas.maus-tec.com/mt-actions/v1.0.0/plugin.json` | Validates `plugin.json` files for Edge-o-Matic 3000 JSON plugins |
| EOM Plugin API Descriptor (v1.0.0) | `https://schemas.maus-tec.com/plugin-api/v1.0.0/plugin-api.json` | Validates firmware-generated `plugin-api.json` and SDK overlay files |

## Usage

### Plugin Manifest (`plugin.json`)

Add a `$schema` field to your `plugin.json` to enable editor validation and
autocompletion in VS Code and other tools:

```json
{
  "$schema": "https://schemas.maus-tec.com/mt-actions/v1.0.0/plugin.json",
  "displayName": "My Plugin",
  ...
}
```

### Plugin API Descriptor (`plugin-api.json`)

This schema is consumed by the `eom-sdk` toolchain and by the Hub backend to
validate firmware-generated API descriptor files. Plugin authors do not use
this schema directly.

## Versioning

Schemas are versioned independently of firmware releases. A new schema version
is published only when the schema structure changes in a breaking or significant
way. Older versions remain at their original URLs indefinitely to avoid breaking
existing tooling. The schema version is not the same as the firmware version.

## Maintenance

Schemas are maintained by Maus-Tec and updated alongside SDK releases.
Schema sources are kept in their respective internal SDK and firmware tooling
repositories and published here. External contributions are not accepted.
