# Changelog

## 1.1.4

- Fixed the hot bulb engine and diesel engine sharing an identical grid recipe after the steel-to-iron conversion.
- The hot bulb engine now uses a copper plate at the top center and a zinc plate at the bottom center, keeping it distinct from the all-iron diesel engine.

## 1.1.3

Initial ModDB release.

- Added cooking-pot recipes: 1 L crude oil → 1 bitumen, and 1 bitumen → 1 coke.
- Added Electric Stove smelting of bitumen into coke at 400°C, with no cooking pot or crucible required.
- Added barrel cracking: 1 L crude oil + 1 cracking catalyst → 1 bitumen.
- Added the `crackingcatalyst` item: crafted from 1 charcoal, non-stackable, one consumed per litre of crude oil.
- Added iron replacements for Petroleum Age recipes that previously required steel, including the oil pump, plus matching iron textures.
- Kept the original iron oil-pump recipe.
- Disabled drifter, shiver, and bowtorn spawns, including variants and temporal storm / devastation-area spawns.
- Added Electrical Progressive dependencies (`electricalprogressiveqol`, `electricalprogressivetransport`) for stove and pipe automation.

### Notes

- The manual cooking-pot routes remain available alongside the automated ones.
- Server restart required after installation.
