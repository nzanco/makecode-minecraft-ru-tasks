### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Weg zum Ziel

## Station 1 — Der Weg
1. Der Agent steht am Start. Vorne ist ein Weg aus Stein: Er geht geradeaus und biegt nach rechts ab. Hinter der Kurve liegt ein Ziegel, dahinter die goldene Platte.
2. Im blauen Block ``||player:bei Chat-Befehl||`` steht das Wort **go**. Lass es so.
3. Baue das Programm: ``||agent:Agent, bewege dich||`` bis zur Kurve, ``||agent:Agent, drehe dich nach||`` rechts, ``||agent:Agent, zerstöre||`` nach vorne und wieder ``||agent:Agent, bewege dich||`` — bis zur Platte.
4. Sag laut, wo der Agent stehen bleibt. Drück den grünen Knopf mit dem Dreieck, geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.
5. Der Agent ist woanders stehen geblieben? Drück den Knopf am Start: Der Agent geht zurück.

#### ~ tutorialhint
Zähl die Felder des Weges bis zur Kurve. Nach der Kurve liegt der Ziegel direkt vor dem Agenten.

```template
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(RIGHT_TURN)
    agent.destroy(FORWARD)
})
```
