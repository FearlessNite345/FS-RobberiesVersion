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
