### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Agent setzt und baut Blöcke ab

## Loch in der Mauer
1. Jetzt ist der Agent auf dem zweiten Weg. In der Bretterwand vorne ist ein Loch zwischen zwei Goldblöcken. Die Steinziegel am Rand liegen im Boden.
2. Baue das Programm **go**: Bring den Agenten bis vor das Loch und nimm ``||agent:Agent, platziere||`` nach vorne.
3. Sag laut, in welches Feld das Brett kommt. Starte **go**.

#### ~ tutorialhint
Der Agent setzt das Brett in das Feld direkt vor sich. Bleib ein Feld vor dem Loch stehen.

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
