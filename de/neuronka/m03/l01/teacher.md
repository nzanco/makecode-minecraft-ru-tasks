### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wo bin ich? X, Y, Z

## Lehrerfläche
1. Vorführung zur Folie: drei Plattformen — grün, rot und blau. Das Programm teleportiert in ``||positions:Welt 94 4 20||``.
2. Der Schüler nennt die Plattform vor dem Start. Starte **go**.

```template
player.onChat("go", function () {
    player.teleport(world(94, 4, 20))
})
```
