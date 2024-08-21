## 🛒 AstridMarket

AstridMarket is a plugin for managing markets on your Minecraft server. It lets you set up and control your market easily, including selling items and resetting the market. Unlike basic admin shops, AstridMarket has limited stock and allows you to add custom items.

### Commands and Permissions

- 📜 **`/market`**
  - **Description:** Opens the market interface for players.
  - **Permission:** No permission required.

- 🔄 **`/market reset`**
  - **Description:** Resets market items and configurations.
  - **Permission:** `astridmarket.reset`

### Example Configuration

Below is a sample configuration for the AstridMarket plugin. This includes settings for market reset intervals and item definitions:

```yaml
# Market configuration
max-entries: 3
reset-time: 4 hour
reset-commands:
  - 'say The market has been reset!'
  - 'broadcast Market reset has occurred. Check out the new items!'

# Items for sale in the market
items:
  TotemOfUndying:
    type: TOTEM_OF_UNDYING
    name: "&6&lTotem of Undying"
    lore:
      - '&7Item from Ancient Traveler.'
      - ''
      - '&fInformation:'
      - '  &8◊ &7Buy price: &c30 points'
      - ''
      - '  &a➥ &7Stock: &e%stock%'
      - ''
      - '&a&lClick &7to purchase'
    stock: 5
    price:
      amount: 50
      currency: playerpoints
    commands:
      - 'give %player% totem_of_undying 1'
```

### Currency Support
The AstridMarket plugin supports various currency systems, including:

- 💰 Vault
- 💎 PlayerPoints
- 🪙 Coin Engine (filename)
