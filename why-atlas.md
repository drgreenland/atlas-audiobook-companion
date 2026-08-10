# Why Atlas Audiobook Companion

## The problem with every other option

Creating a proper M4B audiobook — the kind Apple Books actually recognises, with chapters that navigate correctly, metadata that displays cleanly, and cover art that shows up — is harder than it should be.

Every existing solution forces you to choose between **power you don't need** and **simplicity that falls short**.

---

## What else is out there

### Digital Audio Workstations (Logic Pro, Pro Tools, Adobe Audition)

Built for professional recording studios. Powerful, complex, and designed around recording and mixing — not packaging audiobooks. Getting a correctly formatted M4B with Nero-style chapters out of a DAW requires plugins, scripts, or external tools. These are tools for audio engineers, not audiobook creators.

**The gap:** No guided audiobook workflow. No Apple Books validation. No M4B authoring pipeline.

---

### General audio editors (Audacity, Fission, Amadeus Pro)

More accessible than DAWs, but still general-purpose. They edit audio well — they don't author audiobooks. M4B export is either unavailable or requires manual metadata work. Chapter markers in these tools don't necessarily translate to the chapter format Apple Books navigates.

**The gap:** Audio editing without audiobook publishing. Two different jobs, two different tools.

---

### Audiobook-specific tools (Audiobook Builder, Chapter and Verse)

These come closest to the right idea, but were designed for an older macOS ecosystem. They're not App Store sandboxed, rely on legacy frameworks, and produce output that can be unreliable with modern Apple Books. Chapter navigation often fails on iPhone or CarPlay. Metadata compatibility is inconsistent.

**The gap:** Apple Books has moved on. These tools haven't kept up.

---

### Command-line tools (ffmpeg, AtomicParsley, mp4chaps)

Powerful, free, and used by developers everywhere — including, until recently, under the hood of Atlas itself. But they require terminal knowledge, correct argument syntax, understanding of MP4 container structure, and manual validation. A single wrong flag produces a file Apple Books silently mishandles.

**The gap:** Not a realistic option for anyone who isn't a developer.

---

### The DIY workflow most people end up with

```
Find a converter → Convert audio → Edit metadata in a separate tool
→ Add chapters in another tool → Export → Open in Apple Books
→ Chapters don't work → Google the problem → Try again
```

This is the workflow Atlas replaces.

---

## What Atlas does differently

### Built specifically for Apple Books

Atlas uses the exact chapter format (Nero `chpl` atoms) that Apple Books navigates on iPhone, iPad, Mac, HomePod, and CarPlay. The M4B brand, iTunes metadata atoms, and stik tag are all written correctly — the same way Apple's own tools would write them. This was validated through direct testing in Iteration 3 of development before a single line of the final app was written.

### One workflow, one app

```
Import audio  →  Arrange chapters  →  Add metadata  →  Export M4B
```

No terminal. No separate metadata editor. No chapter tool. No validator. Everything in one native macOS app.

### Batch convert for large libraries

Drop a folder of MP3s — organised by subfolder for multi-disc books — and Atlas converts the entire library overnight. Every subfolder becomes a separate M4B with its own metadata.

### ePub, PDF, and MOBI → audiobook (AAC+)

For books you own digitally but want to listen to: import an ePub, PDF, or MOBI file and Atlas generates a full M4B using Microsoft Edge's TTS narration. No upload, no account, no subscription. The text is processed on-device and the narration is generated in real time.

### Native macOS, App Store sandboxed

Atlas is a pure Swift app with no bundled CLI tools, no third-party runtimes, and no background processes. It works within Apple's security sandbox. Your files never leave your Mac during audio conversion.

---

## The positioning in one line

> **The simplest professional workflow for creating Apple-compatible audiobooks.**

Not a DAW. Not a general audio editor. Not a command-line tool with a UI bolted on. A single focused app that does one thing correctly: turns your audio and ebooks into M4B audiobooks that work in Apple Books.

---

## Feature comparison

| Capability | Atlas | DAWs | General Editors | Legacy Tools | CLI Tools |
|---|---|---|---|---|---|
| Native macOS app | ✅ | ✅ | ✅ | ✅ | — |
| Drag-and-drop audio import | ✅ | ✅ | ✅ | ✅ | — |
| Visual chapter management | ✅ | — | — | Partial | — |
| M4B authoring | ✅ | With plugins | Rarely | ✅ | ✅ |
| Apple Books chapter navigation | ✅ | Unreliable | Unreliable | Unreliable | ✅ |
| iTunes metadata (stik, covr) | ✅ | Manual | Manual | Partial | ✅ |
| Batch folder conversion | ✅ | — | — | — | Scripted |
| ePub / PDF / MOBI → M4B | ✅ | — | — | — | — |
| App Store sandboxed | ✅ | — | — | — | — |
| No technical knowledge required | ✅ | — | Partial | Partial | — |

---

*Atlas Audiobook Companion — [atlasaudiobook.app](https://drgreenland.github.io/atlas-audiobook-companion/)*
