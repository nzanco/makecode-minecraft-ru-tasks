### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wo bin ich? X, Y, Z

## Station 3 — Drei Plattformen
1. Drei Plattformen hinter Glas: **rot X 54, Y 4, Z 16**, **blau X 54, Y 4, Z 22**, **gelb X 54, Y 7, Z 22** — auf dem Dach der blauen.
2. Ändere die Zahlen in ``||positions:Welt||``, damit du auf die rote Plattform kommst. Sag vor dem Start, welche Zahl du geändert hast.
3. Jetzt auf die blaue: Welche Zahl ist anders als bei der roten? Ändere nur sie und starte **go**.
4. Jetzt auf die gelbe — sie ist drei Blöcke höher als die blaue. Welche Zahl ist anders? Ändere sie und starte **go**.

#### ~ tutorialhint
Die Höhe ist die zweite Zahl. Auf dem Boden ist sie 4. Auf einem Dach drei Blöcke hoch ist sie um drei größer.

```template
player.onChat("go", function () {
    player.teleport(world(50, 4, 16))
})
```

```ghost
player.onChat("go", function () {
    player.teleport(world(54, 7, 22))
})
```
