### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Weg zum Ziel

## Station 3 — Dein eigener Auftrag
1. Hier sind drei farbige Felder: rot, blau und gelb. Zu jedem führt ein Weg mit einer Kurve, und auf jedem Weg liegt ein Ziegel.
2. Such dir ein Feld aus und sag deinem Lehrer, welches.
3. Baue das Programm **go** von Anfang bis Ende: Der Agent fährt, dreht sich, zerstört den Ziegel und setzt einen Leuchtstein auf dein Feld.
4. Sag laut, wo der Agent stehen bleibt und auf welchem Feld der Leuchtstein leuchtet. Starte **go**.
5. Die Lampe leuchtet? Drück den Knopf am Start und starte **go** noch einmal — so prüfst du, dass dein Programm immer klappt.
6. Extra: Lass ein Programm zwei Lampen anzünden.

```template
agent.setItem(GLOWSTONE, 64, 1)
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.destroy(FORWARD)
    agent.place(FORWARD)
})
```
