# Abstrakte Datentypen:
- GRUNDIDEE: was(Spezifikation) von wie(Implementierung) zu trennen?
- was -> Abstrakte Datentypen.
- welche Werte und welche Operationen.
- Beispiel: (Mengen)
	- Mengen von Objekten (Werte)
	- Einfügen und Löschen und etc. (Operationen)
	- Operationen: 
		- Einfügen: M:= M U {x}
		- Löschen: M:= M \ {x}
		- Abfragen(enthalten): ist x € M ?
		- Erstellen einer neuen Menge: M:= Q (leere Menge erstellen)
		- Durchlaufen: für alle x € M ... 
# ADT spezifizieren: (WAS)
	**alle Arten können sich gegenseitig unterstützen**
	- VERBAL: in Worten was die Operationen machen sollen.
	- modellierende Spezi. :
		- ein Modell nehmen und sagen: die ADT soll sich wie dieses Modell verhalten (vorheriges Beipeiel -> mathe. Modell: die Mengen)
	- Referenz-Implementierung:
		- soll einfach sein damit es nicht die tatsächliche Implementierung ist. (in einfacher Programmiersprache) 
		- kleines Progamm
		- lauffähig
		- (vorteil) mit Test die tatsächliche Implementierung vergleichen.
	- algebraisch: am abstaktsten
		- sagt nicht was die Operationen machen
		- sagt: welche Beziegungen bestehen zwischen Operationen
		- Daten(Werte) verschwinden in dieser Methode

# prozeduale/funktionale Abstraktion:
	- Beipiel: Das Implementieren einer Funktion für sich wiederholende Aufgaben.
	- Wenn Datentypen nicht wichtig sind. (generics java)
	- Classes in OOP funktional und auch Daten-enthaltend
	
