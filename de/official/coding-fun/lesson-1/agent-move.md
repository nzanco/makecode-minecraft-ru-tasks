### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @flyoutOnly 1
### @explicitHints 1


# Bring den Agenten auf die goldene Platte

## Schritt 1
1. Im blauen Block ``||player:bei Chat-Befehl||`` steht das Wort **go**. Lass es so.
2. Zieh ``||agent:Agent, bewege dich||`` in den blauen Block hinein.
3. Zähl die Felder bis zur goldenen Platte und trag diese Zahl ein.
4. Drück den grünen Knopf mit dem Dreieck.
5. Geh zurück ins Spiel, drück **T**, schreib **go** und drück **Enter**.

Liegt die Platte um die Ecke? Setz vor „bewege dich" den Block ``||agent:Agent, drehe dich nach||`` und wähl die Seite.

#### ~ tutorialhint
Steht der Agent falsch? Bau das Programm nicht neu. Ändere nur die Zahl oder die Drehrichtung.


```template
player.onChat("go", function () {
})
```

```ghost
player.onChat("go", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```
