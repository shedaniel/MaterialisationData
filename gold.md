Material Gold is included since Materialisation 0.1.4.
- Require Mods: Vanilla
- `gold.json`:
```json
{
  "toolColor": "-4291",
  "toolDurability": 32,
  "miningLevel": 0,
  "enchantability": 22,
  "durabilityMultiplier": 0.2,
  "breakingSpeedMultiplier": 0.4,
  "toolSpeed": 12.0,
  "attackDamage": 0.0,
  "name": "gold",
  "materialTranslationKey": "material.materialisation.gold",
  "bright": true,
  "ingredients": [
    {
      "ingredient": {
        "type": "ITEM",
        "content": "minecraft:gold_block"
      },
      "multiplier": 18.0
    },
    {
      "ingredient": {
        "type": "ITEM",
        "content": "minecraft:gold_ingot"
      },
      "multiplier": 2.0
    }
  ],
  "fullAmount": 10
}
