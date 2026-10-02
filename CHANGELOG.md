# Changelog OctoWoW – DragonflightUI-Reforged

> Branch `octowow` = Stand aus Henrys Installation „OctoWoW – HD Upgrade“ (WoW 1.12). Eigene Anpassungen sind im Code mit `-- [patch]` markiert.

**Basis:** Stormhand-dev/DragonflightUI-Reforged `2a8d2ff` (2026-04-24)

## Änderungen

### modules/bars/bars.lua – Seitenleisten (MultiBarLeft/Right)
- **Spiegelung nur bei mehrzeiligem Layout:** Die rechten Aktionsleisten wurden immer gespiegelt. Bei einer einreihigen Leiste lief die Reihenfolge dadurch rückwärts (12 links, 1 rechts). Jetzt wird nur gespiegelt, wenn `layout.rows > 1`.
- **Grid-Layout wird respektiert:** Beim Ändern des Abstands wurde hart `setSpacing(..., 'vertical')` aufgerufen und das eingestellte Grid überschrieben. Jetzt wird `setGridLayout` mit den gespeicherten Werten (`multiBarThreeGrid` / `multiBarFourGrid`) genutzt.
