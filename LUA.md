## Ako vytvorit premennu 

môžeš vytvoriť premennú podla scriptu (napriklad ked davas script do triedy *part*):

```lua
part = script.Parent
```

## Ako pripojit funkciu k udalosti

mozes vytvorit premennu podla scriptu (napriklad ked chces aby sa nieco stalo po tom co se nieco dotkne urciteho objektu (prkld. *part*)):
pouzijeme predchoziu premennu

```lua
part.Touched --Udalost--
part.Touched:Connect(function(CoSaDotklo)
  --script--
end)
```
