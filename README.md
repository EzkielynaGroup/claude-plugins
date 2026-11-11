# Ezkielyna plugins for Claude Code

A small [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces). Everything here is MIT licensed and open source.

| Plugin | What it adds | API key |
|---|---|---|
| `indonesia-data` | 5 MCP servers + a skill: BMKG earthquakes and weather, Kemendagri regions, public holidays and working days, Rupiah tools, offline QRIS parsing | none |

## Install

```bash
claude plugin marketplace add EzkielynaGroup/claude-plugins
claude plugin install indonesia-data@ezkielyna
```

Requires Node.js 18+ (the servers run with `npx`). Restart Claude Code after installing; check with `/mcp`.

## What runs on your machine
The plugin starts these npm packages locally with `npx`: [mcp-bmkg](https://github.com/EzkielynaGroup/mcp-bmkg), [mcp-wilayah-indonesia](https://github.com/EzkielynaGroup/mcp-wilayah-indonesia), [mcp-hari-libur-indonesia](https://github.com/EzkielynaGroup/mcp-hari-libur-indonesia), [mcp-rupiah](https://github.com/EzkielynaGroup/mcp-rupiah), [mcp-qris](https://github.com/EzkielynaGroup/mcp-qris). Only `mcp-bmkg` uses the network (BMKG's public open-data endpoints). The others are offline. Nothing is sent to Ezkielyna.

## Bahasa Indonesia
Plugin `indonesia-data` menambahkan data Indonesia ke Claude Code tanpa API key: gempa dan cuaca BMKG, kode wilayah Kemendagri, hari libur dan hari kerja, terbilang/PPN Rupiah, serta baca QRIS secara offline. Pasang dengan dua perintah di atas.

---
Made by [Ezkielyna](https://ezkielyna.store/?utm_source=github&utm_medium=readme&utm_campaign=claude-plugins), an independent AI API gateway.
