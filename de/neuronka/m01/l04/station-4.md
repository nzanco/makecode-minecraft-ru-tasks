### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Weg zum Ziel

## Station 4 — Die Brücke (Zusatzaufgabe)
1. Vorne ist ein Kanal mit Wasser, darüber eine Brücke aus Brettern. In der Brücke sind zwei Löcher.
2. Der Agent fällt nicht: Er kann direkt über einem Loch stehen. Der Block ``||loops:beim Start||`` gibt dem Agenten Bretter — lass ihn so.
3. Baue das Programm **go**: Der Agent stellt sich über ein Loch und setzt ein Brett **nach unten** — mit ``||agent:Agent, platziere||`` und der Richtung **nach unten**. Dann über dem zweiten Loch.
4. Sag laut, über welchen Feldern der Agent die Bretter setzt. Starte **go**.
5. Ist ein Brett falsch gelandet? Drück den Knopf am Start und ändere eine Zahl.

#### ~ tutorialhint
Zähl die Felder vom Start bis zum ersten Loch. Der Agent muss direkt darüber stehen, nicht davor.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.place(DOWN)
})
```
