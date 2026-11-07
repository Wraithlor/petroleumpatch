# Changelog

## 1.3.0

- Iron bits are now castable. Their melting point is 1150 °C instead of 1482 °C, which is below the crucible's 1200 °C limit and within reach of a charcoal (1300 °C) or coke (1340 °C) firepit.
- Melt iron bits in a crucible and pour the liquid iron into vanilla tool and ingot molds, or into molds from VanillaMoreMolds such as sawblade, nail, plate, hoop, spearhead, knife blade, scythe head, and arrowhead molds.
- This covers the iron bits dropped by Toolsmith when tool bindings break, as well as bits from SmithingPlus or from chiseling an iron ingot.
- No new dependency: the patch changes the vanilla `metalbit-iron` item, so it applies whether or not Toolsmith or a mold mod is installed.
- Iron ingots keep their normal 1482 °C melting point; only bits can be re-cast.

## 1.2.1

- Adjusted the barrel conversion fuel list to charcoal, brown coal, and black coal. The 1.2.0 release also accepted anthracite; that recipe has been removed.

## 1.2.0

- Replaced the cracking-catalyst barrel recipe with a sealed coal conversion.
- A barrel loaded at an exact 1:1 ratio of crude oil to coal now becomes bitumen after 3 in-game days (72 hours): 1 L of crude oil per 1 charcoal, brown coal, black coal, or anthracite.
- Removed the `crackingcatalyst` item and its crafting recipe.
- The barrel consumes both the crude oil and the coal; the four coal types are interchangeable.

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
