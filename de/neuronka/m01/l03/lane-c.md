### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Agent setzt und baut Blöcke ab

## Der rote Block
1. Auf dem dritten Weg ist in der Bretterwand ein Block rot. Die Steinziegel am Rand liegen im Boden.
2. Mach, dass statt des roten Blocks ein Brett steht: zuerst ``||agent:Agent, zerstöre||``, dann ``||agent:Agent, platziere||``.
3. Sag laut, welches Feld sich zweimal ändert. Starte **go**.

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
