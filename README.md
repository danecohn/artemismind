# Artemis Mind

Mind is a local Markdown notebook with linked notes, backlinks, tags, outlines, pinned notes, daily notes, a graph, image attachments, full-text search, and separate writing/reading views.

By **Artemis Softworks LLC**, founded by **Demetria Althea Cohn**. GPL-3.0-only.

## Install

Download your platform from the repository Releases page. Windows Intel/AMD and ARM64, macOS Intel and Apple silicon, and Linux x64 and ARM64 are built on matching native runners. Windows uses an EXE installer, macOS a DMG, and Linux an AppImage. On Linux, make the AppImage executable before opening it. Native launch and local file checks must pass on all six platforms before a release is published.

Mac bundles are ad-hoc signed and strictly verified, including the mounted DMG. They are not Apple-notarized. Windows installers are unsigned.

## Your files

On first launch the app creates a small starter notebook in Documents/Artemis Mind. Open another Markdown folder with File → Open folder. Notes remain ordinary .md files. Obsidian folders can be opened as Markdown, while .obsidian settings and plugins are ignored. This is independently implemented original software; Obsidian application code, branding and plugin compatibility are not included. See NOTICE.md.

The editor displays the Markdown body; existing YAML properties are retained when saving. App-created files have stable IDs and metadata. The .artemis folder holds project structure, recent note revisions, and recoverable removed files. External edits cause a conflict instead of being silently overwritten. Recent versions are in .artemis/history; removed notes are in .artemis/trash and can be moved back with your file manager. Symbolic links are not followed. Indexing limits: 10,000 notes, 8 MB per note, and 128 MB total.

## Keyboard and writing

- Command/Control+N: new note or prompt block
- Command/Control+O: open a Markdown folder
- Command/Control+S: save now (autosave is also enabled)
- Command/Control+K: quick switcher
- Command/Control+G: connections or prompt web
- Type [[ for note links and / for text commands

## Development

Use Node 24, npm ci, npm test, npm run build, then npm start. npm run package creates a native installer on the current platform. The release workflow builds all six. Set ARTEMIS_QA_HOME to a temporary folder for isolated manual QA; --smoke-test <png> uses a separate temporary vault and validates the packaged app.

## Future services

This release is desktop-only and works offline. Web apps, MCP endpoints, sign-in, synchronization and Artemis Drive integration are planned separately and are not included. The versioned local Markdown/JSON schema and stable IDs are designed to support that work without replacing your files. No Obsidian Sync or community plugins are used.
