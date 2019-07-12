[Home](https://shedaniel.me/MaterialisationData/)

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
- The durability of the tool when applied as the head of the tool
- Must be declared as an int

`miningLevel`:
- The mining level of the tool when applied as the head of the tool
- Must be declared as an int
- Example: 0 is wood, 1 is stone, 2 is iron, 3 is diamond

`enchantability`:
- The enchantability of the tool
- Must be declared as an int

`durabilityMultiplier`:
- The durability multiplier of the corresponding tool handle
- Must be declared as a double

`breakingSpeedMultiplier`:
- The mining speed multiplier of the corresponding tool handle
- Must be declared as a double

`toolSpeed`:
- The mining speed of the tool when applied as the head of the tool
- Must be declared as a double

`attackDamage`:
- The attack damage of the tool
- Must be declared as a double

`name`:
- The identifier of the material
- Must be declared as a String, containing a column with the namespace in front and the path at the end
- Example: `"minecraft:wood"` means that the material is for `minecraft` and it is `wood`

`materialTranslationKey`:
- The name of the material
- Must be declared as a String, can be a translation key or hardcoded text
- Example: `"Wood"`

`bright`:
- Whether the material is bright when it is rendered, will brighten the color when `bright` is `true`
- Must be declared as a boolean (`true` or `false`)

`ingredients`:
- List of ingredients
- Must be declared as a list of ingredients
- Example:
  ```
  [
    {
      "ingredient": {
        "type": type of the ingredient,
        "content": the identifier of the ingredient
      },
      "multiplier: multiplier of the ingredient
    }
  ]
  ```
    `ingredient`:
    - `type` is the type of the ingredient
      - Must be declared as either `"TAG"` or `"ITEM"`
      - `"ITEM"`:
	    - Will tell materialisation that that ingredient is... in fact, an item, materialisation will then load the item from the `content`
	    - Example: 
	    ```json
	    {
          "type": "ITEM",
          "content": "minecraft:stick"
        }
	    ```
	    The above ingredient is a stick
	  - `"TAG"`:
	    - Will tell materialisation that that ingredient is... in fact, a tag, materialisation will then load the tag from the `content`
	    - Example: 
	    ```json
	    {
          "type": "TAG",
          "content": "minecraft:logs"
        }
	    ```
	    The above ingredient is list of every log in the game.
	    
  `multiplier`:
  - The multiplier of the ingredient
  - Must be declared as a double
  - Example: `ingots` should be `2.0` and `blocks` should be `18.0`
  - Usage: Making a pickaxe head requires `4.0` points, as one iron ingot is `2.0` points, you will need 2 ingots.

`fullAmount`:
- The repair amount that an ingredient can repair.
- Must be declared as a double
- Example: You have an ingredient whose multiplier is `2.0` and you have `fullAmount` as `10`, then that `ingredient` can repair `10 * 2.0 = 20` durability.
