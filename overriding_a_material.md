[Home](https://shedaniel.me/MaterialisationData/)

Create a json file like this:
```json
{
  "type": "override",
  "name": "<Identifier of the material (not the file name)>"
}
```
You can add a `priority` field to add priority to your override, this is how you override the mining level of gold to obsidian.
```json
{
  "type": "override",
  "name": "gold",
  "miningLevel": 3
}
```