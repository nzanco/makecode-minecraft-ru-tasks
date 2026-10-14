### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wiederholen und wie oft

## Station 2 — Der Stamm
1. Vor dem Agenten liegt ein Baumstamm: acht Holzblöcke in einer Reihe.
2. Das Programm **go** zerstört einen Block und geht einen Schritt — und das zweimal. Sag laut, wie viele Blöcke es zerstört. Starte **go** und prüfe es.
3. Für den ganzen Stamm müsste man dasselbe Paar achtmal schreiben. Nimm den Block ``||loops:wiederholen||``, leg ein Paar hinein — ``||agent:Agent, zerstöre||`` und ``||agent:Agent, bewege dich||`` — und stell die richtige Zahl ein. Die übrigen Blöcke nimm heraus.
4. Drück den Knopf am Start. Sag, wo der Agent stehen bleibt, und starte **go**.

#### ~ tutorialhint
Ein Holzblock — einmal. So viele Holzblöcke, so oft.

```template
player.onChat("go", function () {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
})
```

```ghost
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```
