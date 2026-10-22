# Auto-Modpacker-Beta


# 🛠️ Minecraft Mod Toolkit

**Powerful CLI for searching, collecting, building and updating Minecraft modpacks across Modrinth & CurseForge.**

A single tool that unifies both platforms, automatically discovers addons, resolves dependencies, builds complete modpacks, and keeps them up to date — with almost zero manual work.

---

### ✨ Key Features

- 🔍 **Unified Search** — Search both Modrinth and CurseForge by tags, categories or name
- 📦 **Smart Collection** — Bulk-download entire categories + all related addons (deduplicated)
- 🧩 **Deep Addon Discovery** — Find every possible addon (including brand-new ones)
- 🏗️ **Full Modpack Builder** — Recursively pull dependency trees, filter by loader/version, download jars & generate `.mrpack`
- 🔗 **Link Importer** — Paste any list of links → get the newest compatible files + dependencies
- 🔄 **One-Command Updater** — Point at a folder and update everything cleanly
- 🤖 **Dual Output** — Human-readable lists + compact AI-friendly format

---

### 📋 Commands

| Command | Description |
|---------|-------------|
| `search <tag\|name:title\|link ...>` | Search Modrinth & CurseForge. Supports tags (AND), category links, or `name:hulk` / `"iron man"` |
| `show <N>` | Full card of result №N (description, links, dependencies, incompatibilities) |
| `save <N>` | Add result №N to the common list |
| `saveall` | Add **all** results from the last search |
| `bulk <tag\|name:title\|link ...>` | Take TOP of a category → find every addon of every mod (parallel, progressive) |
| `addons <slug\|modid>` | Find possible addons of a specific mod |
| `build <link\|slug> [loader] [version] [mr=N] [cf=N]` | Full modpack builder with recursive dependencies |
| `newaddons <link\|slug> [period] [loader] [version]` | Find new addons created in the last 7d / 2w / 1m / 3m / 1y |
| `importlink [prefer CF\|M] [min mr=N cf=N]` | Import by links with smart version selection |
| `update [version] [loader] [prefer ...] [min ...]` | Update all mods in a folder |

---

### 🚀 Quick Start Guide

1. **Search for mods**
   ```bash
   search optimization
   search name:sodium
   search "iris shaders"
   ```

2. **Inspect a result**
   ```bash
   show 3
   ```

3. **Save interesting mods**
   ```bash
   save 1
   save 5
   saveall          # save everything from last search
   ```

4. **Bulk collect a whole category + addons**
   ```bash
   bulk optimization
   bulk name:create
   ```

5. **Build a complete modpack from one core mod**
   ```bash
   build sodium fabric 1.21.1
   build create neoforge 1.20.1 mr=10000
   ```

6. **Find fresh addons**
   ```bash
   newaddons sodium 2w
   newaddons create 1m fabric 1.20.1
   ```

7. **Import by links**
   ```bash
   importlink
   # then paste links (one per line or space-separated)
   ```

8. **Update an existing folder**
   ```bash
   update 1.21.1 fabric
   ```

---

**Pro tips:**
- Results are saved to `found_mods/mods.txt` (readable) and `found_mods/mods_ai.txt` (compact for LLMs)
- Delete the `found_mods` folder to start clean
- The `build` command can generate ready-to-use `.mrpack` files
- All cross-platform matching is done by file hash

---

Made for people who build and maintain serious modpacks.
the description was made with the help of grok, I myself do not use AI in the code and I did it with the help of grok due to the fact that it is 2 pm and the person asked to describe the script
```


