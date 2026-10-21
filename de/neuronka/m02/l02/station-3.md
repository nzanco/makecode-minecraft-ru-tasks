### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Innen und außen

## Station 3 — Der Zickzack
1. Die Steine liegen wie Stufen: vorwärts und rechts, vorwärts und rechts. Insgesamt acht Steine.
2. Das Programm **go** ist für eine Stufe geschrieben: zerstören, Schritt, nach rechts drehen, zerstören, Schritt, nach links drehen. Starte **go** — zwei Steine verschwinden.
3. Nimm den Block ``||loops:wiederholen||`` und leg **alle sechs** Blöcke hinein. Beide Drehungen müssen drinnen sein: Der Agent dreht sich auf jeder Stufe. Stell die Zahl ein, damit alle acht Steine verschwinden.
4. Drück den Knopf am Start. Sag die Zahl vor dem Start und starte **go**.

#### ~ tutorialhint
Eine Stufe — zwei Steine. Acht Steine — wie viele Stufen?

```template
player.onChat("go", function () {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.turn(RIGHT_TURN)
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```

```ghost
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.turn(RIGHT_TURN)
    }
})
```
