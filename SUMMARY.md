# ModDB Submission

## Summary

An iron-friendly Petroleum Age patch for a safe-island server with limited resources: crude oil → bitumen → coke cooking, Electric Stove smelting, sealed coal-assisted barrel conversion, castable iron, and disabled rift/temporal storm spawns.

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

### Crude oil processing
- **Cooking pot:** 1 litre of crude oil cooks into 1 bitumen.
- **Cooking pot:** 1 bitumen cooks into 1 coke.
- **Electric Stove:** bitumen smelts into coke at 400°C. No cooking pot or crucible is required.
- **Barrel conversion:** 1 litre of crude oil plus 1 charcoal, brown coal, or black coal converts into 1 bitumen after the barrel is sealed for 3 in-game days.

### Barrel conversion
- The recipe is 1:1: 1 litre of crude oil to 1 of charcoal, brown coal, or black coal.
- Fill the barrel to an exact 1:1 ratio — for example, 50 L of crude oil and 50 coal — then seal it.
- A barrel will not seal unless its contents match the recipe.
- After 3 in-game days (72 hours) the crude oil and coal are consumed and each litre becomes 1 bitumen.
- The coal is consumed, not reused.

### Castable iron bits
- Iron bits melt at 1150 °C instead of the vanilla 1482 °C, putting them below the crucible's 1200 °C limit and within reach of a charcoal (1300 °C) or coke (1340 °C) firepit.
- Melt 20 iron bits in a crucible to make 100 units of liquid iron — one ingot's worth.
- Pour the liquid iron into vanilla tool and ingot molds, or into VanillaMoreMolds molds such as sawblade, nail, plate, hoop, spearhead, knife blade, scythe head, arrowhead, and the heavy ingot/plate/rod mold.
- Toolsmith drops these bits when tool bindings break; bits from SmithingPlus or from chiseling an iron ingot work the same way.
- Iron ingots now melt at 1150 °C too, so the crucible contents stay liquid and can be poured; whole ingots can also be melted and cast.
- Steel and meteoric iron keep their higher vanilla melting points.

### Spawn changes
- Drifters, shivers, bowtorns, and their variants no longer spawn.
- Temporal storm and devastation-area spawns are cleared.
- Wolves, bears, and other non-rift hazards remain in the world.

## Electrical Progressive automation

The new processing routes can be fully automated with Electrical Progressive machines and pipes:

1. **Crude oil:** Petroleum tank/valve or barrel → liquid insertion pipe → processing barrel.
2. **Coal in:** chest of the chosen coal → item pipes → insertion pipe into the barrel, filtered to that coal type only.
3. **Load and seal:** let the pipes fill the barrel to exactly 1:1 crude oil and coal (for example, 50 L and 50 coal), then seal it by hand. A barrel will not seal unless its contents match the recipe.
4. **Bitumen out:** after 3 in-game days, unseal the barrel and pipe the bitumen → insertion pipe into the Electric Stove input, filtered to bitumen only.
5. **Stove:** powered, no cooking pot installed, temperature above 400°C.
6. **Coke out:** item pipe from the stove → insertion pipe into coke storage.

Use insertion pipes as the final pipe before each container. The barrel must be sealed for the conversion, so loading and unsealing are manual steps.

## Requirements

- Vintage Story 1.22.x
- Petroleum Age
- Electrical Progressive: QoL (for the Electric Stove)
- Electrical Progressive: Transport (for pipe automation)

Tested with Vintage Story 1.22.7, Petroleum Age 0.21.0, Electrical Progressive QoL 3.3.1, and Electrical Progressive Transport 2.0.0.

### Optional compatibility

These mods are supported but **not required**:

- **Toolsmith** — the iron bits it drops when tool bindings break are castable.
- **VanillaMoreMolds** — its tool molds and heavy mold accept cast iron.
- Neither mod has to be installed; the change is applied to the vanilla `metalbit-iron` item.

## Notes

- The manual cooking-pot recipes remain available alongside the automated routes.
- Designed primarily for a custom safe-island server with limited resources; other worlds can use it if they want the same more accessible balance.
- Server restart required after installation.
