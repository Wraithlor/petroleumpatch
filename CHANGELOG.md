# Changelog

## 1.4.0

- Added the `powdermaker` trait to the vanilla Blackguard class. It is a plain game trait and class patch, so it does not require the Specialized Classes mod.
- Powdermakers can turn powder directly into blasting powder: 3 powdered charcoal → 1 blasting powder, or 2 powdered coke → 1 blasting powder.
- Coke can now be ground into powdered coke (`petroleumpatch:powder-coke`) in a quern or pulverizer, giving the coke from bitumen a second use.

## 1.3.2

- The barrel no longer needs coal. Sealing a barrel containing only crude oil converts it to bitumen after 3 in-game days (72 hours).
- Bitumen can now be baked into coke in a clay oven or an Electric Oven (Electrical Progressive: QoL).
- Bitumen has `bakingProperties` at 200 °C, so both ovens accept it. The Electric Oven supports pipe automation: bitumen in, coke out, with the finished coke available for extraction.
- Iron bits and iron ingots now melt at 1320 °C. A charcoal firepit peaks at 1300 °C and cannot reach this; coke at 1340 °C is required.
- Enlarged the fired crucible's `maxContentDimensions` so whole ingots fit. All ingots can now be melted and poured, not just bits.
- Added the missing smelting properties for stainless steel (1530 °C) and uranium (1133 °C) ingots and metal bits.
- The existing cooking-pot routes and the Electric Stove bitumen-to-coke smelting route remain available.

## 1.3.1

- Fixed pouring molten iron. 1.3.0 lowered the iron bits' melting point, but the crucible stores smelted bits as an iron ingot, which still melted at 1482 °C. The crucible therefore treated its contents as solidified and refused to pour.
- Iron ingots now melt at 1150 °C as well, so the stored contents stay liquid and can be poured into molds.
- Side effect: whole iron ingots are now castable too. You can melt bits or ingots in a crucible and pour them into tool and ingot molds.
- Steel, meteoric iron, and the other metals keep their vanilla melting points.

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
