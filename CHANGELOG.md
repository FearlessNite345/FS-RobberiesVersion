# Changelog v1.3.1
- Added secure bank-manager vault controls with ACE and optional Lux CAD access, configurable time locks, and optional robbery-loot spawning
- Added visible cooldown options with exact remaining-time notifications for robberies using target interactions
- Resolved Lua diagnostics and disabled internal development mode for production builds

# Changelog v1.3.0
- Added an ACE-protected in-game robbery creator for creating, editing, deleting, and visually placing robberies, vaults, polygons, loot carts, and cash piles
- Added JSON persistence for custom robberies and vaults, including automatic legacy migration and backups, while keeping built-in definitions read-only
- Replaced vault drilling with multi-stage native hacking, randomized passwords, configurable normal/hard difficulties, and a handheld tablet animation
- Added synchronized vault loot with cash and gold carts, table cash piles, server-authoritative rewards, and text, ox_target, and qb-target interactions
- Reworked the drill minigame with an optimal-speed zone, active cooling, pin resistance, frame-rate-independent acceleration, and faster pacing
- Added an optional register minigame and improved Yoga prompts with live keyboard/mouse and controller artwork
- Added Lux CAD Community API support with dedicated incident types for registers, ATMs, safes, vaults, and panic alarms
- Added authored loot layouts for Pacific Standard and the Great Ocean Highway and Legion Square Fleeca vaults

# Changelog v1.2.4
- Fixed outdated cad integration with ImperialCAD

# Changelog v1.2.3
- Added drill overheat blast settings (radius/force/upforce) and optional drill item removal on explode.
- Added drill difficulty setting (easy/normal/hard/insane/random) for overheat behavior.
- Added drill explosion shockwave for nearby players (uses the blast radius setting).
- Fixed pin‑break timing for both drill types (standard drill + laser).
- Fixed ACE permission checks not applying correctly for robberies.
- Fixed rare ATM interaction errors related to ox_target.
- UI overhaul (robbery progress + drill HUD).

# Changelog v1.2.2
- Added randomized CAD dispatch timing for timed drill robberies (no minigame) to reduce predictability
- Added separate CAD titles for vault robberies vs registers/ATMs/safes
- Added extra debug logging (CAD dispatch flow, robbery branch/timing, permissions/cooldowns, vault/inside state)
- Fixed CAD caller text so automated vs manual alarm labels display correctly
- Fixed missing CAD calls when drill minigames are disabled (timed drill flow)

# Changelog v1.2.1
- Fixed a issue with export naming for QBX

# Changelog v1.2.0
- Added support for global cooldowns so cooldowns can be shared across all ATMs, registers, and similar targets instead of being handled individually (customer request)
- Added full support for lation_ui
- Added the /openvault command to manually open a vault
- Added the /closevault command to manually close a vault
- Added a new export to open or close a vault by its ID, for example harmony_fleeca_bank_vault_door (customer request)
- Added additional CAD systems to the supported list, note that not all have been fully tested
- Added many new config options, including the ability to add or remove supported robbery models (customer request)
- Various other small fixes, tweaks, and improvements

# Changelog v1.1.1
- Added an additional deposit box (Deposit Box 6) inside the Prompts Sandy Bank, located on the right-hand wall.
- Fixed an issue where the panic button was missing from registers when using **ox_target**.

# Changelog v1.1.0

- Added an option to disable the drill minigame and switch to a timer-based system instead  
- Added support for custom location robberies (robberies at specific coordinates not tied to a prop, supports both register-style animation and drill-based robberies)  
- Added a new config option for defining custom vault doors  
- Introduced new admin helper commands: `/fs_find_closest_vault_door_coord`, `/fs_poly_start`, `/fs_poly_cancel`, and `/fs_poly_finish`  
- Restricted admin commands using `Config.PolyBuilderPermission` and `Config.FindVaultPermission`  
- Improved ped positioning logic to prevent looping or getting stuck  
- Added 4 default robbable bank vaults  
- Added 1 custom robbable vault in collaboration with Prompt Studio (disabled by default if you don’t own the MLO)  
- Adjusted `postals.json` handling to safely ignore stray comments without breaking parsing  
- And many more tweaks and improvements

# Changelog v1.0.3

- Fixed issues with the ImperialCAD integration not working correctly

# Changelog v1.0.2

- The script now pulls the `imperial_community_id` from a convar instead of requiring manual setup in `cad.lua`.

# Changelog v1.0.1

- Added official support for Night's MDT (https://store.nights-software.com/package/5667103)
- Fixed a few issues with QBX and QBCORE integrations
