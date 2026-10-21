### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Innen und außen

## Station 2 — Rund um den Teich
1. Vor dem Agenten ist Gras, rechts ein Teich. Wo der Agent geht, legt die Welt einen Weg.
2. Das Programm **go**: viermal wiederholen — „vorwärts um 3", und nach der Wiederholung eine Drehung nach rechts. Sag laut, wo der Agent ankommt. Starte **go** und prüfe es.
3. Der Agent soll um den Teich gehen und zum Start zurückkommen. Schieb **einen Block** — die Drehung — in die Wiederholung, unter „vorwärts um 3". Sonst nichts ändern.
4. Drück den Knopf am Start. Sag, wie oft sich der Agent dreht und wo er stehen bleibt, und starte **go**.

#### ~ tutorialhint
Eine Drehung nach der Wiederholung läuft einmal. Drehen muss der Agent aber an jeder Ecke des Teichs.

```template
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 3)
    }
    agent.turn(RIGHT_TURN)
})
```
