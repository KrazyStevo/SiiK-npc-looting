
# SiiK_Npc_Looting

**SiiK_Npc_Looting** is a FiveM script for the **QBCore Framework** that allows players to loot dead NPCs. This script adds functionality for NPC looting, police notification, and can be easily integrated into any QBCore-based server.

## Features

- Loot dead NPCs by pressing a key (default: **E**).
- Randomized loot items such as **pistol_ammo** and **bread**.
- **Police Notification**: Notifies the police of looting activity using **qb-dispatch**.
- **NPC Combat**: Nearby NPCs may become hostile if they see the player looting.
- **Configurable loot items** and **police notification time**.
- Easily customizable and ready for use in any QBCore server.

## Installation

### Prerequisites

- **FiveM Server** with **QBCore Framework**.
- **qb-dispatch** resource installed and working.

### Steps to Install

1. **Download the script**: Download the zip file of **SiiK_Npc_Looting** from the [GitHub repository](https://github.com/your-repository-link).
   
2. **Add to your resources**:
   - Extract the zip file to the **resources** folder in your FiveM server.
   - Rename the folder to `SiiK_Npc_Looting`.

3. **Edit `server.cfg`**:
   - Add the following line to your `server.cfg` to ensure the script is started on server boot:
     ```
     ensure SiiK_Npc_Looting
     ```

4. **Start your server**: Run your FiveM server as usual, and the **SiiK_Npc_Looting** script will be active.

## Configuration

- **config.lua** allows you to configure the loot items and police notification times.

### Example `config.lua`:

```lua
Config = {}

Config.LootItems = {
    { name = "pistol_ammo", min = 5, max = 15 },
    { name = "bread", min = 1, max = 3 }
}

Config.notifyTime = 5000 -- Time in ms for police notification after looting

return Config
