## Ako vytvorit premennu 

môžeš vytvoriť premennú podla scriptu (napriklad ked davas script do triedy *part*):

```lua
part = script.Parent
```

## Ako pripojit funkciu k udalosti

mozes vytvorit premennu podla scriptu (napriklad ked chces aby sa nieco stalo po tom co sa nieco dotkne urciteho objektu (prkld. *part*)):
pouzijeme predchoziu premennu

```lua
part.Touched --Udalost--
part.Touched:Connect(function(CoSaDotklo)
  --script--
end)
```

## Ako urobit textove tlactiko v ktorom budes text (cislo) pridavat o jedno (plus 1) kliknutim

pokial pojdes do sluzby "StarterGui", vytvoris novu Instance: "ScreenGui", k tomu vytvoris Instance: "TextButton" a k tomu pridas "IntValue"(nazaciatku bude Value 0 a meno tohoto objektu je "Value") a do noveho scriptu napises:

```lua
script.Parent.Text = script.Parent.Value.Value --takze sa text TextButtonu nastavi na hodnotu v objekte "Value"--
script.Parent.MouseButton1Click:Connect(function() --znamena ze ked niekdo klikne na TextButton lavym klikom, nieco sa moze stat--
	script.Parent.Value.Value += 1 --"+=" znamena ze pridavas hodnotu do hodnoty--
	script.Parent.Text = script.Parent.Value.Value
end)
```
