[Home](https://shedaniel.me/MaterialisationData/)

Material Iron is included since Materialisation 0.1.4.
- Require Mods: Vanilla
- `iron.json`:
```json
{
  "toolColor": "-1",
  "toolDurability": 250,
  "miningLevel": 2,
  "enchantability": 14,
  "durabilityMultiplier": 0.9,
  "breakingSpeedMultiplier": 1.0,
  "toolSpeed": 6.0,
  "attackDamage": 2.0,
  "name": "iron",
  "materialTranslationKey": "material.materialisation.iron",
  "bright": true,
  "ingredients": [
    {
      "ingredient": {
        "type": "ITEM",
        "content": "minecraft:iron_ingot"
      },
      "multiplier": 2.0
    },
    {
      "ingredient": {
        "type": "ITEM",
        "content": "minecraft:iron_block"
      },
      "multiplier": 18.0
    }
  ],
  "fullAmount": 100
}
```
