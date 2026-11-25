### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Von mir aus ~

## Station 1 — Drei Starts
1. Das Programm **go** ist fertig, du musst nichts ändern. Stell dich auf den Goldblock am Start.
2. Sag, auf welchem farbigen Block der Agent landet. Starte **go** im Chat.
3. Stell dich auf den zweiten Goldblock. Sag, wo der Agent landet, und starte **go**.
4. Geh zurück auf den ersten Goldblock und dreh dich zum roten Turm. Sag, wo der Agent landet, und starte **go**.

#### ~ tutorialhint
Ein Platz mit ~ wird von dir aus gezählt: von da, wo du beim Start des Programms stehst.

```template
player.onChat("go", function () {
    agent.teleport(pos(0, 0, 4), SOUTH)
})
```

```ghost
player.onChat("go", function () {
    agent.teleport(pos(0, 0, 4), SOUTH)
})
```
