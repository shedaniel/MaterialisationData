Locate your self to the `materialisation/material` folder in `config`, and create a json file (the name doesn't matter), following this template:
```
{
  "enabled": true or false,
  "toolColor": color,
  "toolDurability": durability of the tool head,
  "miningLevel": mining level (0 is wood, 1 is stone, 2 is iron, 3 is diamond),
  "enchantability": enchantability of the tool,
  "durabilityMultiplier": durability multiplier of the corresponding tool handle,
  "breakingSpeedMultiplier": breaking speed multiplier of the corresponding tool handle,
  "toolSpeed": breaking speed of the tool head,
  "attackDamage": attack damage of the material,
  "name": identifier of the material,
  "materialTranslationKey": name of the material, can be a translation key,
  "bright": if the material is bright,
  "ingredients": [list of materials],
  "fullAmount": how much durability one part of the material will recover
}
```
`enabled`:
- Whether the material will be loaded by materialisation
- Must be declared as a boolean (`true` or `false`)
 
`toolColor`:
- The color of the material
- Must be declared as an int, or #AARRGGBB
- Example: `"-1"` or `"#FFFFFFFF"` for white

`toolDurability`:
- The durability of the tool if applied as the head of the tool
- Must be declared as an int

`miningLevel`:
- The mining level of the tool when applied as the head of the tool
- Must be declared as an int
- Example: 0 is wood, 1 is stone, 2 is iron, 3 is diamond
