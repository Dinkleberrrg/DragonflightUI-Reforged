# Changelog OctoWoW – DragonflightUI-Reforged

> Branch `octowow` = the state from Henry's "OctoWoW – HD Upgrade" install (WoW 1.12). Own changes are marked with `-- [patch]` in the code.

**Base:** Stormhand-dev/DragonflightUI-Reforged `2a8d2ff` (2026-04-24)

## Changes

### modules/bars/bars.lua – side action bars (MultiBarLeft/Right)
- **Mirror only for multi-row layouts:** The right-hand action bars were always mirrored, so a single-row bar ran backwards (12 on the left, 1 on the right). They are now mirrored only when `layout.rows > 1`.
- **Grid layout is respected:** Changing the spacing called a hard-coded `setSpacing(..., 'vertical')` and overwrote the configured grid. It now calls `setGridLayout` with the saved values (`multiBarThreeGrid` / `multiBarFourGrid`).
