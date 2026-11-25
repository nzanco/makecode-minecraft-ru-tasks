### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Von mir aus ~

## Station 2 — Der grüne Block
1. Stell dich auf den Goldblock: **X 30, Y 4, Z 14**. Der grüne Block: **X 35, Y 4, Z 14**.
2. Um wie viel ist X beim grünen Block größer? Ändere die erste Zahl mit ~ im Block ``||positions:~ ~ ~||``.
3. Sag, wo der Agent landet, und starte **go**.

#### ~ tutorialhint
~ zählt von dir aus. Wie viele Blöcke nach Osten sind es von deinem X bis zum X des grünen Blocks?

```template
player.onChat("go", function () {
    agent.teleport(pos(1, 0, 0), SOUTH)
})
```

```ghost
player.onChat("go", function () {
    agent.teleport(pos(0, 0, 0), SOUTH)
})
```
