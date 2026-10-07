### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Weg zum Ziel

## Station 2 — Der Agent hat sich verlaufen
1. Der Agent soll einen Leuchtstein in die Nische unter dem Goldblock setzen. Der Block ``||loops:beim Start||`` gibt dem Agenten Leuchtsteine — lass ihn so.
2. Das Programm **go** ist schon fertig, aber es hat einen Fehler. Starte es und schau, wo der Agent stehen bleibt.
3. Sag laut: Was sollte passieren, und was ist passiert?
4. Finde den Block, wegen dem der Agent falsch gelaufen ist. Ändere darin eine Sache.
5. Drück den Knopf am Start und starte **go** noch einmal.

#### ~ tutorialhint
Schau, an welcher Reihe der Agent abgebogen ist. Die Nische ist eine Reihe näher.

```template
agent.setItem(GLOWSTONE, 64, 1)
player.onChat("go", function () {
    agent.move(FORWARD, 3)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 3)
    agent.place(FORWARD)
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(RIGHT_TURN)
    agent.place(FORWARD)
})
```
