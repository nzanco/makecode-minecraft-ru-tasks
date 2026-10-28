### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wiederholung in der Wiederholung

## Station 5 — Die Ecke
1. Das ist eine Zusatzaufgabe. Der Bauplatz aus Stein biegt um eine Ecke. Das Programm **go** baut die erste Seite der Mauer.
2. Schreib darunter weiter: Der Agent dreht sich einmal und baut dann die zweite Seite als gleiche Mauer.
3. Sag laut, wohin sich der Agent drehen muss, wie viele Säulen die zweite Seite hat und welche Blöcke einmal laufen.
4. Drück den Knopf rechts von dir und starte **go**.

#### ~ tutorialhint
Nach der ersten Mauer steht der Agent auf dem Eckfeld. Nach links drehen muss er einmal — zwischen den zwei Mauern.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        for (let index2 = 0; index2 < 3; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 3)
    }
    agent.turn(LEFT_TURN)
})
```
