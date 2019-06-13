[Home](https://shedaniel.me/MaterialisationData/)

Be sure that you understand [Overriding](https://shedaniel.me/MaterialisationData/overriding_a_material).
To disable a material, simply do 
```json
{
  "type": "override",
  "name": "<Identifier of the material (not the file name)>",
  "enabled": false
}
```
Tip: Add a high `priority` if this fails.