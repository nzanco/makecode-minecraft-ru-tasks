### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Innen und außen

## Station 4 — Zwei Streifen
1. Vor dem Agenten liegen zwei Streifen mit je fünf Steinen. Der erste liegt direkt vorne. Der zweite rechts daneben und eine Zelle näher.
2. Das Programm **go** baut den ersten Streifen ab. Starte es und schau, wo der Agent stehen bleibt.
3. Schreib das Programm **unter** der Wiederholung weiter: Der Agent wendet einmal zum zweiten Streifen, und danach baut eine zweite Wiederholung ihn ab.
4. Drück den Knopf am Start. Sag, welche Blöcke einmal laufen, und starte **go**.

#### ~ tutorialhint
Wenden braucht man einmal — zwischen den beiden Wiederholungen, nicht drinnen: nach rechts drehen, ein Schritt, nach rechts drehen.

```template
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```

```ghost
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 1)
})
```
