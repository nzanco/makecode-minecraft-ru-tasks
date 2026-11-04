### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Mauer und Turm

## Station 1 — Die Brücke
1. Vorne ist ein Kanal. Der Agent soll sich einmal nach links drehen und eine gerade Brücke aus fünf Brettern bis zum Goldblock am anderen Ufer legen. Der Block ``||loops:beim Start||`` gibt dem Agenten Bretter — lass ihn so.
2. Starte das Programm **go** so, wie es ist: Drück den grünen Knopf mit dem Dreieck, geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**. Schau, was der Agent gemacht hat.
3. Sag laut: Was sollte herauskommen, und was ist herausgekommen? Welcher Fehler ist es — die richtige Arbeit, aber nicht so oft, oder ein Block an der falschen Stelle?
4. Repariere das Programm, indem du **einen** Block verschiebst. Drück den Knopf rechts von dir und starte **go** noch einmal.

#### ~ tutorialhint
Wie oft muss sich der Agent drehen? Und wie oft läuft der Dreh-Block?

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 5; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.place(DOWN)
    }
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    agent.turn(LEFT_TURN)
    for (let index = 0; index < 1; index++) {
        agent.move(FORWARD, 1)
        agent.place(DOWN)
    }
})
```
