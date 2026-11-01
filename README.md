Diese Erweiterung erweitert die vorhandene [MotionKit V2](https://github.com/tinysuperlab/MotionKitV2) Erweiterung um neue Blöcke. Mit diesen neuen Blöcken soll die Steuerung vereinfacht werden. Es gibt Blöcke, um den Roboter zu drehen oder eine bestimmte Strecke fahren zu lassen.

## Als Erweiterung verwenden

Dieses Repository kann als **Erweiterung** in MakeCode hinzugefügt werden.

* öffne [https://makecode.calliope.cc/](https://makecode.calliope.cc/)
* klicke auf **Neues Projekt**
* klicke auf **Erweiterungen** unter dem Zahnrad-Menü
* nach **Roboter Steuerung** suchen und importieren

## Kalibrierung

`Roboter.set_velocity(0)` Gib hier die Strecke in Zentimetern an, die der Roboter in einer Sekunde zurücklegt.
`Roboter.set_angular_velocity(0)` Gib hier den Winkel in Grad an, um den sich der Roboter innerhalb von 500 Millisekunden dreht. Dieser Wert gilt für Links- und Rechtsdrehungen gleichermaßen.

### Links und rechts getrennt kalibrieren

Die beiden Motoren sind nie ganz identisch. Deshalb kann es vorkommen, dass der Roboter bei einer Drehung nach links einen anderen Winkel schafft als bei einer Drehung nach rechts. In diesem Fall kannst du beide Richtungen getrennt kalibrieren:

* `Roboter.set_angular_velocity_left(0)` Winkel in Grad, um den sich der Roboter innerhalb von 500 Millisekunden **nach links** dreht.
* `Roboter.set_angular_velocity_right(0)` Winkel in Grad, um den sich der Roboter innerhalb von 500 Millisekunden **nach rechts** dreht.

So gehst du vor:

* Setze den Roboter auf eine Fläche und markiere seine Ausrichtung.
* Nutze den Block `für 500ms nach links drehen` und miss den Winkel, um den sich der Roboter gedreht hat. Trage den Wert bei `500ms sind [GRAD] Grad (Linksdrehung)` ein.
* Wiederhole das mit dem Block `für 500ms nach rechts drehen` und trage den Wert bei `500ms sind [GRAD] Grad (Rechtsdrehung)` ein.

Die Blöcke `90 Grad nach Links drehen`, `90 Grad nach Rechts drehen` und `um [GRAD] Grad drehen` verwenden jeweils den Wert für die passende Drehrichtung. Wenn du nur `set_angular_velocity` verwendest, verhalten sich alle Blöcke wie bisher.

## Nicht blockierendes Fahren

Der Befehl `Roboter.drive_time_non_blocking` bzw. der Block `Für [ZEIT] ms [RICHTUNG] fahren, dabei das Programm weiterlaufen lassen` sorgt dafür, dass das Programm während der Fahrt nicht angehalten wird. Nachfolgende Befehle werden sofort weiter ausgeführt.

## Dieses Projekt bearbeiten

Um dieses Repository in MakeCode zu bearbeiten.

* öffne [https://makecode.calliope.cc/](https://makecode.calliope.cc/)
* klicke auf **Importieren** und dann auf **Importiere URL**
* füge **<https://github.com/Zukunftswerkstatt-Buchholz/robot-control>** ein und klicke auf Importieren

#### Metadata (used for search, rendering)

* for PXT/calliopemini

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>

> Diese Seite bei [https://zukunftswerkstatt-buchholz.github.io/roboter-steuerung/](https://zukunftswerkstatt-buchholz.github.io/roboter-steuerung/) öffnen
