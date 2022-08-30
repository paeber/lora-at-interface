# Dokumentation

Auf dieser Seite werden einzelne Blöcke der Erweiterung beschrieben.

## Blöcke
### Event
```blocks
if (IoTCube.checkEvent(eRAK_EVT.JOINED)) {

    }
```

## Examples
```blocks
loops.everyInterval(1000, function () {
    if (IoTCube.checkEvent(eRAK_EVT.JOINED)) {
        music.playTone(988, music.beat(BeatFraction.Eighth))
        basic.showIcon(IconNames.Yes)
        OLED.writeStringNewLine("Verbunden")
    } else if (IoTCube.checkEvent(eRAK_EVT.JOIN_FAILED)) {
        basic.showIcon(IconNames.No)
    } else {
        basic.showIcon(IconNames.Diamond)
        basic.pause(500)
        basic.showIcon(IconNames.SmallDiamond)
    }
})
```

