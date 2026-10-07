### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Weg zum Ziel

## Station 1 — Der Weg
1. Der Agent steht am Start. Vorne ist ein Weg aus Stein: Er geht geradeaus und biegt nach rechts ab. Hinter der Kurve liegt ein Ziegel, dahinter die goldene Platte.
2. Das Programm **go** ist fast fertig. Sag laut, wo der Agent stehen bleibt, wenn du es so startest. Drück den grünen Knopf mit dem Dreieck, geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.
3. Der Agent steht vor dem Ziegel. Füge ``||agent:Agent, zerstöre||`` nach vorne ein — an der Stelle, wo der Ziegel direkt vor dem Agenten liegt.
4. Drück den Knopf am Start: Der Agent geht zurück. Sag, wo er jetzt stehen bleibt, und starte **go** noch einmal.

#### ~ tutorialhint
«Zerstöre» gehört direkt nach die Drehung: Dann liegt der Ziegel direkt vor dem Agenten.

```template
player.onChat("go", function () {
    agent.move(FORWARD, 3)
    agent.turn(RIGHT_TURN)
    agent.move(FORWARD, 3)
})
```

```ghost
player.onChat("go", function () {
    agent.destroy(FORWARD)
})
```
