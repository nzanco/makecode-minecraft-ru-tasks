### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wo bin ich? X, Y, Z

## Station 2 — Die Plattform
1. Die grüne Plattform ist hinter Glas: **X 34, Y 4, Z 14**. Hinlaufen geht nicht — nur teleportieren.
2. Das Programm **go** teleportiert dich in die ``||positions:Welt||`` mit drei Zahlen. Vergleiche sie mit den Zahlen der Plattform: Welche Zahl ist anders?
3. Ändere diese Zahl. Sag laut, wo du landen wirst.
4. Starte **go**: Drück T, schreib **go** und drück Enter. Dann drück den Knopf hinter dir rechts und starte **go** noch einmal.

#### ~ tutorialhint
Die erste Zahl ist X, die zweite Y, die dritte Z. Die Plattform hat X 34.

```template
player.onChat("go", function () {
    player.teleport(world(30, 4, 14))
})
```

```ghost
player.onChat("go", function () {
    player.teleport(world(34, 4, 14))
})
```
