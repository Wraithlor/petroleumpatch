# ModDB Submission

## Summary

An iron-friendly Petroleum Age patch for a safe-island server with limited resources: crude oil → bitumen → coke cooking, Electric Stove smelting, catalyst-based barrel cracking, and disabled rift/temporal storm spawns.

## Description

# Petroleum Age: Iron & Refining Patch

**Petroleum Age: Iron & Refining Patch** is a server-focused quality-of-life patch for **Petroleum Age**. It makes late-game oil technology accessible in a resource-limited world and adds automation-friendly refining routes, while calming rift-related hostile spawns.

## Why this patch exists

This patch was built for a custom server organized around safe islands with limited resources. Steel and other late-game materials are intentionally scarce there, so the patch downgrades key Petroleum Age technology to iron and adds compact processing routes suited to small-scale, island-based industry. The spawn changes support the same setting by removing rift creatures and temporal storm spawns.

## Features

### Iron instead of steel
- Petroleum Age recipes that normally require steel now use iron plates and iron nails/strips.
- The oil pump is retextured to match its new iron construction.
- The iron oil-pump recipe is preserved.

### Crude oil processing
- **Cooking pot:** 1 litre of crude oil cooks into 1 bitumen.
- **Cooking pot:** 1 bitumen cooks into 1 coke.
- **Electric Stove:** bitumen smelts into coke at 400°C. No cooking pot or crucible is required.
- **Barrel cracking:** 1 litre of crude oil plus 1 cracking catalyst converts into 1 bitumen.

### Cracking catalyst
- A new single-use item crafted from 1 charcoal.
- It cannot stack, so automated pipes insert only one at a time.
- One catalyst is consumed per litre of crude oil, and leftover crude oil remains in the barrel.
- The barrel processes immediately when its contents change; sealing is not required.

### Spawn changes
- Drifters, shivers, bowtorns, and their variants no longer spawn.
- Temporal storm and devastation-area spawns are cleared.
- Wolves, bears, and other non-rift hazards remain in the world.

## Electrical Progressive automation

The new processing routes can be fully automated with Electrical Progressive machines and pipes:

1. **Crude oil:** Petroleum tank/valve or barrel → liquid insertion pipe → processing barrel.
2. **Catalyst:** chest of catalysts → item pipes → insertion pipe into the barrel, filtered to cracking catalyst only.
3. **Bitumen out:** item pipe from the barrel → insertion pipe into the Electric Stove input, filtered to bitumen only.
4. **Stove:** powered, no cooking pot installed, temperature above 400°C.
5. **Coke out:** item pipe from the stove → insertion pipe into coke storage.

Use insertion pipes as the final pipe before each container. Keep the processing barrel unsealed.

## Requirements

- Vintage Story 1.22.x
- Petroleum Age
- Electrical Progressive: QoL (for the Electric Stove)
- Electrical Progressive: Transport (for pipe automation)

Tested with Vintage Story 1.22.7, Petroleum Age 0.21.0, Electrical Progressive QoL 3.3.1, and Electrical Progressive Transport 2.0.0.

## Notes

- The manual cooking-pot recipes remain available alongside the automated routes.
- Designed primarily for a custom safe-island server with limited resources; other worlds can use it if they want the same more accessible balance.
- Server restart required after installation.
