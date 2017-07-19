## Steuerung:
Zur Steuerung des Schlägers wird ein Leap Motion Sensor verwendet. 
Dieser kann die Hände und Finger erkennen und ihre Bewegungen verfolgen.
Es ist außerdem möglich, verschiedene Gesten zu registieren, die vom Leap Motion erkannt werden.
Da nur eine Geste zum resetten des Balls benötigt wird, hat nur die Kreis Geste eine Funktion.


Um die Daten des Sensors zu verarbeiten gibt es zwei Möglichkeiten:

1.Ein LeapListener wird erstellt und dem LeapController zugewiesen. Innerhalb des LeapListeners werden dann CallBacks definiert,
die bei bestimmten Ereignissen vom LeapController aufgerufen werden.

2.Ein LeapController wird erstellt, welcher direkt Zugriff auf die Daten des Sensors hat. Mit Hilfe der Funktion "updatePalm" können die Daten weiter verarbeitet werden.

Da die Raktion auf Ereignisse hier nicht benötigt wird, benutzen wir nur einen LeapController.
Innerhalb der Funktion "updatePalm" muss nun noch überprüft werden, ob es sich um die richtige Hand handelt.
Die Position der Hand wird zu der Box normalisiert und dann wird Position und Beschleunigung der Hand weiter gegeben.
