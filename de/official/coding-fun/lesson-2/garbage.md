### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Müll am Strand

## Schritt 1
1. Im blauen Block ``||player:bei Chat-Befehl||`` steht das Wort **go**. Lass es so.
2. Lass den Agenten den Müll auf den Spuren mit ``||agent:Agent, zerstöre||`` abbauen und mit ``||agent:Agent, sammle alles||`` einsammeln.
3. Drück den grünen Knopf mit dem Dreieck.
4. Geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.

#### ~ tutorialhint
Der Agent kann nur abbauen, was direkt vor ihm liegt. Führ ihn zum Müll.


```ghost
player.onChat("go", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
```
