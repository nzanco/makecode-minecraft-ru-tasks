### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Агент ставит и ломает блоки

## Красный блок (дополнительно)
1. На третьей дорожке в стене из досок один блок красный.
2. Сделай так, чтобы вместо красного блока стояла доска: сначала ``||agent:агент: уничтожить||``, потом ``||agent:агент: разместить||``.
3. Скажи вслух, какая клетка поменяется дважды. Запусти **go**.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.destroy(FORWARD)
    agent.place(FORWARD)
})
```
