# ModDB Submission

## Summary

An iron-friendly Petroleum Age patch for a safe-island server with limited resources: crude oil → bitumen → coke cooking and baking, Electric Oven automation, coal-free sealed barrel conversion, coke-gated castable iron, a Blackguard powdermaker trait for charcoal and coke blasting powder, disabled rift/temporal storm spawns, and optional iron-age Colonial Firearms ammunition and low-grade firearm recipes.

## Description

# Petroleum Age: Iron & Refining Patch

**Petroleum Age: Iron & Refining Patch** is a server-focused quality-of-life patch for **Petroleum Age**. It makes late-game oil technology accessible in a resource-limited world and adds automation-friendly refining routes, while calming rift-related hostile spawns.

## Why this patch exists

This patch was built for a custom server organized around safe islands with limited resources. Steel and other late-game materials are intentionally scarce there, so the patch downgrades key Petroleum Age technology to iron and adds compact processing routes suited to small-scale, island-based industry. The spawn changes support the same setting by removing rift creatures and temporal storm spawns.

## Features

### Iron instead of steel
- Petroleum Age recipes that normally require steel now use iron plates and iron nails/strips.
- The hot bulb engine uses a copper plate at the top center and a zinc plate at the bottom center, so it stays distinct from the diesel engine.
- The oil pump is retextured to match its new iron construction.
- The iron oil-pump recipe is preserved.

### Colonial Firearms compatibility (optional)
- When Colonial Firearms is installed, its ammunition manufacturing is iron-age: the Primer Press, Cartridge Draw Press, Cartridge Loading Press, Shot Dripper, and all four casing dies use iron instead of steel.
- The double-barrel shotgun, Webley revolver, and Trapdoor rifle are craftable from iron components: rifle barrel halves, gun springs, Trapdoor actions, Webley barreled frames, and Webley cylinders are forged from iron ingots.
- The Martini-Henry remains steel-gated: its Martini action still requires a steel ingot.
- Bullet molds and trigger/sear sets were already iron and are unchanged.
- Primers can be made from fine gunpowder. The Primer Press's inputs are hardcoded in Colonial Firearms, so the patch adds routes instead: 1 fine gunpowder → 1 saltpeter and 1 fine gunpowder → 1 powdered sulfur in the crafting grid, which lets the press run on 2 fine gunpowder + 1 native copper nugget per 16 primers. Primers can also be hand-assembled: 1 fine gunpowder + 1 native copper nugget → 4 primers, shapeless.
- The Primer Press handbook text now mentions the gunpowder routes.
- No hard dependency: the patch is skipped automatically if Colonial Firearms is not installed.

### Crude oil processing
- **Cooking pot:** 1 litre of crude oil cooks into 1 bitumen.
- **Cooking pot:** 1 bitumen cooks into 1 coke.
- **Clay oven:** 1 bitumen bakes into 1 coke at 200 °C.
- **Electric Oven (Electrical Progressive: QoL):** 1 bitumen bakes into 1 coke at 200 °C, with manual or pipe input and output.
- **Electric Stove:** bitumen smelts into coke at 400 °C. No cooking pot or crucible is required.
- **Barrel conversion:** 1 litre of crude oil converts into 1 bitumen after the barrel is sealed for 3 in-game days. No coal is needed.

### Barrel conversion
- Load the barrel with crude oil only. No coal or other additive is required.
- A barrel will not seal unless its contents match the recipe, so fill it with whole litres of crude oil.
- After 3 in-game days (72 hours) the crude oil is consumed and each litre becomes 1 bitumen.

### Bitumen to coke in ovens
- Bitumen bakes into coke in a vanilla clay oven or an Electrical Progressive: QoL Electric Oven.
- Bitumen bakes at 200 °C, below the 300 °C maximum of both ovens.
- The Electric Oven supports automatic input and output through pipes: bitumen in, coke out.
- The clay oven is the manual option. Place bitumen in a hot oven after the fire has burned out and wait for it to turn into coke.

### Castable iron bits
- Iron bits and iron ingots melt at 1320 °C instead of the vanilla 1482 °C.
- A charcoal firepit peaks at 1300 °C, which is not hot enough. A coke firepit reaches 1340 °C, so coke is required to cast iron.
- Melt 20 iron bits in a crucible to make 100 units of liquid iron — one ingot's worth.
- Pour the liquid iron into vanilla tool and ingot molds, or into VanillaMoreMolds molds such as sawblade, nail, plate, hoop, spearhead, knife blade, scythe head, arrowhead, and the heavy ingot/plate/rod mold.
- Toolsmith drops these bits when tool bindings break; bits from SmithingPlus or from chiseling an iron ingot work the same way.
- The fired crucible now accepts whole ingots, so any metal can be stored as ingots and melted and poured later. This includes copper, bronze, iron, and the other vanilla ingots.
- Smelting properties were added for stainless steel (1530 °C) and uranium (1133 °C) ingots and bits, which were missing them in vanilla.
- Steel and meteoric iron keep their higher vanilla melting points.

### Powdermaker (Blackguard)
- The vanilla Blackguard class gains the `powdermaker` trait. It is a plain game trait and class patch, so the Specialized Classes mod is not required.
- Powdered charcoal and powdered coke can be turned into blasting powder:
  - 3 powdered charcoal → 1 blasting powder
  - 2 powdered coke → 1 blasting powder
- Coke can be ground into `petroleumpatch:powder-coke` in a quern or pulverizer. Charcoal already grinds into vanilla powdered charcoal.
- Both recipes are shapeless and only match for players whose class has the `powdermaker` trait.

### Spawn changes
- Drifters, shivers, bowtorns, and their variants no longer spawn.
- Temporal storm and devastation-area spawns are cleared.
- Wolves, bears, and other non-rift hazards remain in the world.

## Electrical Progressive automation

The bitumen → coke step can run fully on Electrical Progressive machines with an Electric Oven:

1. **Bitumen in:** barrel or storage → item pipe → Electric Oven input, filtered to bitumen only.
2. **Oven:** powered. The Electric Oven accepts bitumen automatically.
3. **Coke out:** Electric Oven output → item pipe → coke storage or a chest.

The Electric Oven accepts bitumen automatically and exposes the finished coke for extraction; coke
has no baking properties, so it is not baked further. The barrel conversion still needs a manual
seal and unseal, but it no longer needs a coal feed:

1. **Crude oil:** Petroleum tank/valve or liquid pipe → processing barrel, or fill the barrel by hand.
2. **Seal:** seal the barrel by hand. No coal or other additive is needed.
3. **Bitumen out:** after 3 in-game days, unseal the barrel; it holds 1 bitumen per litre of crude oil.
4. **Coke:** move the bitumen to the Electric Oven as described above.

Use insertion pipes as the final pipe before each container. The clay oven and cooking pot remain
manual alternatives, and the Electric Stove route can still smelt bitumen at 400 °C.

## Requirements

- Vintage Story 1.22.x
- Petroleum Age
- Electrical Progressive: QoL (for the Electric Oven)
- Electrical Progressive: Transport (for pipe automation)

Tested with Vintage Story 1.22.7, Petroleum Age 0.21.0, Electrical Progressive QoL 3.3.1, and Electrical Progressive Transport 2.0.0. The optional Colonial Firearms patch targets 0.9.88.

### Optional compatibility

These mods are supported but **not required**:

- **Toolsmith** — the iron bits it drops when tool bindings break are castable.
- **VanillaMoreMolds** — its tool molds and heavy mold accept cast iron.
- **Colonial Firearms** — ammunition manufacturing and the low-grade firearms use iron, primers can be made from fine gunpowder, and the Martini-Henry stays steel-gated.
- None of these mods has to be installed; their patches are skipped when the mod is absent.

## Notes

- The manual cooking-pot recipes remain available alongside the automated routes.
- Designed primarily for a custom safe-island server with limited resources; other worlds can use it if they want the same more accessible balance.
- Server restart required after installation.

## AI disclosure

AI was used for nearly all processes during the creation, testing and debugging of this mod. No code from other mods were used or copied for any of these tweaks other than dependancies.

**NOTE to other mod makers:**

Your code is STILL YOUR CODE, I did not copy nor do I take credit for any of your hard work.
