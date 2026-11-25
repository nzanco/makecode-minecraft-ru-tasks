### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Von mir aus ~

## Lehrervorführung
1. Goldblöcke: X 90, Z 10 und X 94, Z 17. Das Programm **go** bleibt gleich.
2. Starte **go** vom ersten, vom zweiten und wieder vom ersten Goldblock, diesmal mit Blick nach Norden.

```template
player.onChat("go", function () {
    agent.teleport(pos(3, 0, 0), SOUTH)
})
```

```ghost
player.onChat("go", function () {
    agent.teleport(pos(3, 0, 0), SOUTH)
})
```
