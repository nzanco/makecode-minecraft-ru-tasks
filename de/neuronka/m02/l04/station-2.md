### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Mauer und Turm

## Station 2 — Der letzte Auftrag
1. Das ist der letzte Auftrag der Baustelle. Links vom Agenten stehen zwei Pfosten aus Stein — 2 und 3 hoch. Die grauen Felder des Bauplatzes sind immer Mauer; das erste grüne Feld ist Mauer oder Turm.
2. Wähl deine Mauer: Länge 4 oder 5, Höhe 2 oder 3. Der Turm am Ende der Mauer ist ein Brett höher als die Mauer.
3. Bau im blauen Block **go** ein Programm: die Mauer als Wiederholung in der Wiederholung und darunter den Turm mit einer Wiederholung. Der Block ``||loops:beim Start||`` gibt dem Agenten Bretter — lass ihn so.
4. Sag laut, wie lang und wie hoch die Mauer wird, wie hoch der Turm und wo der Agent ankommt. Starte **go**. Die Welt schreibt die Größen, die sie gesehen hat. Drück den Knopf rechts und starte noch einmal.

#### ~ tutorialhint
Die innere Wiederholung baut eine Säule, die äußere wiederholt „Säule und Schritt“. Der Turm wird einmal gebaut — nach der Mauer.

```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
})
```

```ghost
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
    for (let index = 0; index < 1; index++) {
        for (let index2 = 0; index2 < 1; index2++) {
            agent.move(UP, 1)
            agent.place(DOWN)
        }
        agent.move(FORWARD, 1)
        agent.move(DOWN, 1)
    }
    for (let index3 = 0; index3 < 1; index3++) {
        agent.move(UP, 1)
        agent.place(DOWN)
    }
})
```
