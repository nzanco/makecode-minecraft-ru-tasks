### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wo bin ich? X, Y, Z

## Station 4 — Die Säule
1. Vorne steht eine Steinsäule, oben liegt ein Diamant. Hochklettern geht nicht, aber auf den Diamanten musst du — mit Teleport.
2. Stell dich auf den Goldblock am Fuß der Säule. Lies die Zahlen. Die Säule ist einen Schritt weiter östlich — welches X hat sie?
3. Zähl die Blöcke der Säule. Auf dem Boden bist du auf Höhe 4 — auf welcher Höhe bist du, wenn du auf dem Diamanten stehst?
4. Setz die drei Zahlen in ``||positions:Welt||`` und starte **go**.

#### ~ tutorialhint
Nach Osten wächst X. Jeder Block der Säule ist eins mehr Höhe.

```template
player.onChat("go", function () {
    player.teleport(world(70, 4, 10))
})
```

```ghost
player.onChat("go", function () {
    player.teleport(world(74, 9, 16))
})
```
