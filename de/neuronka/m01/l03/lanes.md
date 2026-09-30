### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Agent setzt und baut Blöcke ab

## Ziegel auf dem Weg
1. Im blauen Block ``||player:bei Chat-Befehl||`` steht das Wort **go**. Lass es so. Den Block ``||loops:beim Start||`` lässt du auch so: Er gibt dem Agenten Bretter.
2. Auf dem Weg liegt ein Ziegel. Der Agent kommt nicht hindurch.
3. Bring den Agenten mit ``||agent:Agent, bewege dich||`` bis vor den Ziegel.
4. Nimm ``||agent:Agent, zerstöre||`` nach vorne: Der Agent baut den Ziegel vor sich ab.
5. Noch einmal ``||agent:Agent, bewege dich||`` – bis zur goldenen Platte.
6. Sag laut, wo der Agent stehen bleibt. Drück den grünen Knopf mit dem Dreieck, geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.

#### ~ tutorialhint
Der Agent bleibt vor dem Ziegel stehen? Schau, ob „zerstöre" im Programm ist und ob es dort steht, wo der Agent schon am Ziegel ist.

## Loch in der Mauer
1. Jetzt ist der Agent auf dem zweiten Weg. In der Mauer vorne ist ein Loch zwischen zwei Goldblöcken.
2. Ändere das Programm **go**: Bring den Agenten bis vor das Loch und nimm ``||agent:Agent, platziere||`` nach vorne.
3. Sag laut, in welches Feld das Brett kommt. Starte **go**.

#### ~ tutorialhint
Der Agent setzt das Brett in das Feld direkt vor sich. Bleib ein Feld vor dem Loch stehen.

## Der rote Block (zusätzlich)
1. Auf dem dritten Weg ist in der Bretterwand ein Block rot.
2. Mach, dass statt des roten Blocks ein Brett steht: zuerst ``||agent:Agent, zerstöre||``, dann ``||agent:Agent, platziere||``.
3. Sag laut, welches Feld sich zweimal ändert. Starte **go**.


```template
agent.setItem(PLANKS_OAK, 64, 1)
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.destroy(FORWARD)
    agent.place(FORWARD)
    agent.collectAll()
})
```
