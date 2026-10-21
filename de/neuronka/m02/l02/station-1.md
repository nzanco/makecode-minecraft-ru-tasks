### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Innen und außen

## Station 1 — Der Streifen
1. Rechts vom Agenten liegt ein Streifen aus sechs Steinen. Der Agent schaut nach vorne, nicht auf den Streifen.
2. Im Programm **go** gibt es eine Wiederholung: Der Agent zerstört einen Stein und geht einen Schritt. Um die Steine im Streifen abzubauen, muss sich der Agent zuerst einmal nach rechts drehen.
3. Nimm den Block ``||agent:Agent, drehe dich||`` und setz ihn so ein, dass sich der Agent **einmal** dreht — vor der Wiederholung. Stell in der Wiederholung die Zahl ein, damit der ganze Streifen verschwindet.
4. Sag laut, welcher Block einmal läuft und welche jedes Mal. Drück den grünen Knopf mit dem Dreieck, geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.

#### ~ tutorialhint
Die Drehung braucht man einmal — sie steht über der Wiederholung. So viele Steine, so oft.

```template
player.onChat("go", function () {
    for (let index = 0; index < 1; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```

```ghost
player.onChat("go", function () {
    agent.turn(RIGHT_TURN)
    for (let index = 0; index < 4; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
```
