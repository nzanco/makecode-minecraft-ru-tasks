### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Der Agent klettert zur goldenen Platte

## Schritt 1
1. Ändere das Programm **go** so, dass der Agent auf der goldenen Platte steht.
2. Im Block ``||agent:Agent, bewege dich||`` kannst du die Richtung **nach oben** wählen.
3. Drück den grünen Knopf mit dem Dreieck.
4. Geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.


```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```
