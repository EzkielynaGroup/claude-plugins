---
name: indonesia-data
description: Use when the user asks about Indonesian earthquakes or weather (BMKG), Indonesian regions and Kemendagri codes, Indonesian public holidays or working days, Rupiah formatting/terbilang/PPN, or reading and validating a QRIS code.
---

# Indonesian data tools

This plugin adds five MCP servers. None needs an API key or an account.

| Need | Server | Notes |
|---|---|---|
| Latest earthquakes, felt quakes, village weather forecast | `bmkg` (`gempa_terbaru`, `gempa_dirasakan`, `gempa_m5`, `prakiraan_cuaca`) | Live BMKG open data; cite "BMKG" as the source in answers |
| Province → village names and Kemendagri codes | `wilayah-indonesia` (`cari_wilayah`, `detail_kode`, `daftar_anak`, `validasi_kode`) | Offline, typo tolerant |
| Public holidays, cuti bersama, working-day math | `hari-libur-indonesia` (`daftar_libur`, `cek_tanggal`, `hitung_hari_kerja`, `hari_kerja_berikutnya`) | Offline; covers the SKB 3 Menteri decrees it ships with; say so if a year is not covered |
| Terbilang, format/parse Rupiah, PPN 12% × 11/12 | `rupiah` (`terbilang`, `format_rupiah`, `parse_rupiah`, `hitung_ppn`) | Pure calculation |
| Parse/validate QRIS, add an amount, render SVG | `qris` (`parse_qris`, `validate_qris`, `set_qris_amount`, `qris_to_svg`) | Offline; it never moves money or contacts a bank |

Guidance:
- Prefer the tool over memory for any date, code, amount or quake data; these change.
- For QRIS, never claim a payment was made; the tool only reads and builds QR payloads.
- Answer in the user's language (Indonesian or English).
