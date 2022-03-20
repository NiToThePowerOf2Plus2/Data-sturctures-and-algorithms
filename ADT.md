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

## ADT spezifizieren: (WAS)

**alle Arten können sich gegenseitig unterstützena**

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

## prozeduale/funktionale Abstraktion:

- Beipiel: Das Implementieren einer Funktion für sich wiederholende Aufgaben.
- Wenn Datentypen nicht wichtig sind. (generics java)
- Classes in OOP funktional und auch Daten-enthaltend
	
## modellierende Spezifikation annhand von Mengen:

- Definition der Gleichheit:
	- A = B gdw. für alle x: x € A und x € B
	- kommt darauf an: Welche Element in der Menge sind.
	- Mehrfaches Vorkommen und Reihenfolge nicht wichtig (verbale Spezifikation)
	- muteable vs immuteable Beispiele in java und python

## algebraische Spezifikation

- Rechnen mit Variablen
- man hat gewisse Operationen
	- Einfügen: G x M -> M : Einfügen eines Elements (x) einer Menge G in die Menge M -> neue Menge M: einfüge(x,M)
	- Löschen: G x M -> M : gleich wie beim Einfügen
	- Leere Menge: M keine Parameter
	- istEnthalten: G x M -> {wahr, Falsch}: ist Element {x} einer Menge G in der Menge M enthalten?
	- Beispiele:
		- istEnthalten(x, leereMenge) -> Falsch **(1)**
		- istEnthalten(x, einfüge(y, M)) -> 
			- wahr, *falls x == y* **(2)**
			- istEnthalten(x, M), *sonst* **(3)**
		- istEnthalten(x, lösche(y, M)) ->
			- falsch, *falls x == y* **(4)**
			- istEnthalten(x, M), *sonst* **(5)**

## Eindeutigkeit/Vollständigkeit und Konsistenz einer Spezifikation

- sind alle Fälle abgedeckt?
- obiges Beispiel:
	- Mengen Erstellen durch:
		- Leere Mengen
		- Einfügen
		- Löschen
	- Prädikat: istEnthalten() definiert für alle 3 Fälle.
- Datentypen der Werte ist hier nicht wichtig. 
- in Algebra: wichtig allgemeine Formeln zu finden und sie zu vereinfachen und umzuformen:
	- Umformungsbeweise: 
		**zu zeigen**
		- Behauptung:
			*lösche(x, einfüge(x, M)) == lösche(x, M)*
		**in der Spezifikation oben gibt es keine Gleichungen, die mit Löschen oder Einfügen direkt umgehen.**
		- eigentlich zu zeigen:
			*istEnthalten(y, lösche(x, einfüge(x, M)))) == istEnthalten(y, lösche(x, M))*
			1. falls x = y:
				- linke Seite: falsch **(4)**
				- rechte Seite: falsch **(4)**
			2. falls x != y:
				- linke Seite: 
					- istEnthalten(y, einfüge(x,M)) **(5)**
					- x != y, also istEnthalten(y, M) **(3)**
				- rechte Seite: istEnthalten(y ,M) **(5)**

			**----------------------------------------------------**	
			
			1. Fall 1: **linke Seite *falsche* = rechte Seite *falsch***
			2. Fall 2: **linke Seite *istEnthalten(y, M)* = rechte Seite *istEnthalten(y, M)***
			
			**Behaupting beweisen**


				
					
					






	


