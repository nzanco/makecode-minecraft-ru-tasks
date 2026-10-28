### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Wiederholung in der Wiederholung

## Station 1 — Der Turm
1. Der Agent steht auf dem Bauplatz. Links von ihm steht ein Pfosten aus Stein. Der Block ``||loops:beim Start||`` gibt dem Agenten Bretter — lass ihn so.
2. Im Programm **go** ist eine Wiederholung: Der Agent steigt um 1 nach oben und legt ein Brett unter sich — Richtung **nach unten**. So wächst der Turm.
3. Stell die Zahl in der Wiederholung so ein, dass der Turm so hoch wird wie der Pfosten. Sag laut, wie viele Bretter es werden und wo der Agent ankommt.
4. Drück den grünen Knopf mit dem Dreieck, geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**. Stimmt der Turm nicht, drück den Knopf rechts von dir und versuch es noch einmal.

#### ~ tutorialhint
Zähl die Steine im Pfosten. Einmal — ein Brett.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 2; index++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
})
```
