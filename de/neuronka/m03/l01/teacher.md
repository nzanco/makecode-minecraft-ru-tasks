### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wo bin ich? X, Y, Z

## Lehrervorführung
1. Vorführung zur Folie: drei Blöcke — grün, rot und blau. Das Programm teleportiert in ``||positions:Welt 94 4 20||``.
2. Der Schüler nennt den Block vor dem Start. Starte **go**.

```template
player.onChat("go", function () {
    player.teleport(world(94, 4, 20))
})
```
