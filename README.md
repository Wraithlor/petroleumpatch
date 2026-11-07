# Petroleum Age: Iron & Refining Patch

A server-focused patch for [Petroleum Age](https://mods.vintagestory.at/petroleumage) on Vintage Story 1.22.x.
It makes late-game oil technology reachable in a resource-limited world, adds automation-friendly
refining routes, and calms rift-related hostile spawns.

- **ModID:** `petroleumpatch`
- **Version:** 1.3.1
- **Side:** Universal (server-side changes; no client code)

## Why this patch exists

This patch was built for a custom server organized around safe islands with limited resources.
Steel and other late-game materials are intentionally scarce there, so the patch downgrades key
Petroleum Age technology to iron and adds compact processing routes suited to small-scale,
island-based industry. The spawn changes support the same setting.

## Features

### Iron instead of steel
- Petroleum Age recipes that normally require steel now use iron plates and iron nails/strips.
- The hot bulb engine uses a copper plate at the top center and a zinc plate at the bottom center, so it stays distinct from the diesel engine.
- The oil pump is retextured to match its new iron construction.
- The original iron oil-pump recipe is kept.

### Crude oil processing
| Route | Input | Output | Notes |
| --- | --- | --- | --- |
| Cooking pot | 1 L crude oil | 1 bitumen | manual |
| Cooking pot | 1 bitumen | 1 coke | manual |
| Electric Stove | 1 bitumen | 1 coke | 400 °C, no pot/crucible |
| Barrel | 1 L crude oil + 1 charcoal, brown coal, or black coal | 1 bitumen | sealed 3 days, 1:1 |

### Barrel conversion
- Load a barrel with equal parts crude oil and coal: 1 L of crude oil per 1 coal item.
- Charcoal, brown coal, and black coal all work, and they are interchangeable.
- Fill the barrel to an exact 1:1 ratio — for example, 50 coal for 50 L of crude oil. A barrel will not seal unless its contents match the recipe.
- Seal the barrel. After 3 in-game days (72 hours) the crude oil and coal are consumed and each litre becomes 1 bitumen.
- The coal is consumed, not reused.

### Castable iron bits
- Iron bits melt at 1150 °C instead of the vanilla 1482 °C, so a crucible can actually reach their melting point.
- A charcoal firepit reaches 1300 °C and a coke firepit reaches 1340 °C, both comfortably above 1150 °C.
- Melt 20 iron bits in a crucible to make 100 units of liquid iron — one ingot's worth.
- Pour the liquid iron into vanilla tool molds (axe, pickaxe, shovel, hammer, hoe, anvil, helve hammer) or ingot molds.
- Molds from **VanillaMoreMolds** also work: sawblade, nail, plate, hoop, spearhead, knife blade, scythe head, arrowhead, and the heavy ingot/plate/rod mold.
- **Toolsmith** drops these bits when tool bindings break; bits from SmithingPlus or from chiseling an iron ingot work the same way.
- Iron ingots now melt at 1150 °C as well, so the crucible contents stay liquid after the bits are smelted and can be poured. Whole iron ingots can also be melted and cast.
- Steel and meteoric iron keep their higher vanilla melting points.

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

### Optional compatibility

These mods are supported but **not required**:

- **Toolsmith** — the iron bits it drops when tool bindings break are castable.
- **VanillaMoreMolds** — its tool molds and heavy mold accept cast iron.
- Neither mod has to be installed; the change is applied to the vanilla `metalbit-iron` item.

## Installation

1. Download the release zip (do **not** unpack it).
2. Drop it into your `Mods` folder.
3. Restart the game or server.

## Automation

The full crude oil → bitumen → coke chain can run on Electrical Progressive machines:

1. Petroleum tank/valve or barrel → liquid insertion pipe → processing barrel.
2. Chest of charcoal, brown coal, or black coal → item pipes → insertion pipe into the barrel, filtered to the chosen coal type.
3. Let the pipes load the barrel to exactly 1:1 crude oil and coal (for example, 50 L and 50 coal), then seal it by hand. A barrel will not seal unless its contents match the recipe.
4. After 3 in-game days, unseal the barrel; it holds 1 bitumen per litre of crude oil.
5. Barrel → item pipe → Electric Stove input, filtered to bitumen.
6. Stove powered, no cooking pot installed, above 400 °C.
7. Stove output → item pipe → coke storage.

Use insertion pipes as the final pipe before each container. The barrel must be sealed for the conversion, so loading and unsealing are manual steps.

## Building a release

The mod lives at the repository root, so the archive is built directly from it:

```sh
zip -r petroleumpatch_<version>.zip modinfo.json modicon.png assets
```

Development docs (`README.md`, `CHANGELOG.md`, `SUMMARY.md`, `MODDB.md`, `moddb-logo.png`)
are deliberately excluded from the archive.

See `CHANGELOG.md` for version history and `SUMMARY.md` for the text used on the mod page.

## Links

- ModDB: <https://mods.vintagestory.at/show/mod/77909>
- Releases: <https://github.com/Wraithlor/petroleumpatch/releases>

## License

MIT — see `LICENSE`.
