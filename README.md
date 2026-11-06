# Petroleum Age: Iron & Refining Patch

A server-focused patch for [Petroleum Age](https://mods.vintagestory.at/petroleumage) on Vintage Story 1.22.x.
It makes late-game oil technology reachable in a resource-limited world, adds automation-friendly
refining routes, and calms rift-related hostile spawns.

- **ModID:** `petroleumpatch`
- **Version:** 1.1.3
- **Side:** Universal (server-side changes; no client code)

## Why this patch exists

This patch was built for a custom server organized around safe islands with limited resources.
Steel and other late-game materials are intentionally scarce there, so the patch downgrades key
Petroleum Age technology to iron and adds compact processing routes suited to small-scale,
island-based industry. The spawn changes support the same setting.

## Features

### Iron instead of steel
- Petroleum Age recipes that normally require steel now use iron plates and iron nails/strips.
- The oil pump is retextured to match its new iron construction.
- The original iron oil-pump recipe is kept.

### Crude oil processing
| Route | Input | Output | Notes |
| --- | --- | --- | --- |
| Cooking pot | 1 L crude oil | 1 bitumen | manual |
| Cooking pot | 1 bitumen | 1 coke | manual |
| Electric Stove | 1 bitumen | 1 coke | 400 °C, no pot/crucible |
| Barrel | 1 L crude oil + 1 cracking catalyst | 1 bitumen | automatable |

### Cracking catalyst
- Single-use item crafted from 1 charcoal; cannot stack.
- One catalyst is consumed per litre of crude oil; leftover crude oil stays in the barrel.
- The barrel processes immediately when its contents change — sealing is not required.

### Spawn changes
- Drifters, shivers, bowtorns, and their variants no longer spawn.
- Temporal storm and devastation-area spawns are cleared.
- Wolves, bears, and other non-rift hazards remain.

## Requirements

- Vintage Story 1.22.x
- Petroleum Age
- Electrical Progressive: QoL (Electric Stove)
- Electrical Progressive: Transport (pipe automation)

Tested with Vintage Story 1.22.7, Petroleum Age 0.21.0, Electrical Progressive QoL 3.3.1,
and Electrical Progressive Transport 2.0.0.

## Installation

1. Download the release zip (do **not** unpack it).
2. Drop it into your `Mods` folder.
3. Restart the game or server.

## Automation

The full crude oil → bitumen → coke chain can run on Electrical Progressive machines:

1. Petroleum tank/valve or barrel → liquid insertion pipe → processing barrel.
2. Chest of catalysts → item pipes → insertion pipe into the barrel, filtered to cracking catalyst.
3. Barrel → item pipe → Electric Stove input, filtered to bitumen.
4. Stove powered, no cooking pot installed, above 400 °C.
5. Stove output → item pipe → coke storage.

Use insertion pipes as the final pipe before each container, and leave the processing barrel unsealed.

## Building a release

The mod lives at the repository root, so the archive is built directly from it:

```sh
zip -r petroleumpatch_<version>.zip modinfo.json modicon.png assets
```

Development docs (`README.md`, `CHANGELOG.md`, `SUMMARY.md`, `MODDB.md`, `moddb-logo.png`)
are deliberately excluded from the archive.

See `CHANGELOG.md` for version history and `SUMMARY.md` for the text used on the mod page.

## Links

- ModDB: _(add after first release)_

## License

MIT — see `LICENSE`.
