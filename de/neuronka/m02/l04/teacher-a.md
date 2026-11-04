### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Mauer und Turm

## Lehrerprüfung — Kanal
1. Das ist keine Schüleraufgabe. Hier prüft die Lehrkraft zwei Programme vom Anfang der Stunde.
2. Starte **gap**: Drei Bretter sollen mit Lücken liegen, auf den Feldern 2, 4 und 6.
3. Drück den Knopf rechts und starte **out**: Ein Brett soll auf Feld 4 liegen.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("gap", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(FORWARD, 2)
        agent.place(DOWN)
    }
})
player.onChat("out", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 1)
    }
    agent.place(DOWN)
})
```
