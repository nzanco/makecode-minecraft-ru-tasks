### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der letzte Raum

## Schritt 1
Im Raum liegen zwei goldene Platten: eine für dich, eine für den Agenten.

1. Stell dich auf deine goldene Platte und bleib dort stehen.
2. Ändere das Programm **go** so, dass der Agent auf der anderen Platte steht.
3. Drück den grünen Knopf mit dem Dreieck.
4. Drück **T**, schreib **go** und drück **Enter**.


```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```
