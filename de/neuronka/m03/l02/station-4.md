### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Von mir aus ~

## Station 4 — Zwei Befehle
1. Der Befehl **base** soll den Agenten immer auf den Diamanten **X 72, Y 4, Z 20** setzen, egal von welchem Goldblock aus du startest.
2. Der Befehl **me** soll den Agenten zwei Blöcke östlich von dir hinsetzen, egal von welchem Goldblock aus du startest.
3. Starte beide vom ersten Goldblock aus, dann vom zweiten. Was stimmt nicht?
4. Tausche in den Befehlen die Positionsblöcke: Wo brauchst du ``||positions:Welt||``, wo ``||positions:~ ~ ~||``? Setze die Zahlen ein und starte beide von beiden Goldblöcken aus.

#### ~ tutorialhint
Immer derselbe Platz — „Welt“. Der Platz geht mit dir mit — ~.

```template
player.onChat("base", function () {
    agent.teleport(pos(2, 0, 10), SOUTH)
})
player.onChat("me", function () {
    agent.teleport(world(72, 4, 10), SOUTH)
})
```

```ghost
player.onChat("base", function () {
    agent.teleport(world(0, 0, 0), SOUTH)
})
player.onChat("me", function () {
    agent.teleport(pos(0, 0, 0), SOUTH)
})
```
