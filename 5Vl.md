# modellierende Spezifikation von ADT anhand des Mengenbeispiels:

## Operationen:
- Erstellen x = new Menge()
- Einfügen boolean x.insert(i)
- Löschen boolean x.remove(i)
- Ist Enthalten boolean x.contains(i)

**i ist int**

**jede Operation ist spezifiziert durch:**
- Vorbedingung
- Nachbedingung

# Vor- und Nachbedingungen:

- Erstellen: 
    - Vorbedingung: ---
    - Nachbedinung: M = Q (Leere Menge)
- Einfügen:
    - Vorbedingung: ---
    - Nachbedinung: M = M_alt U {i}
    - Ergebnis: True gdw. i !€ M 
- Löschen: 
    - Vorbedingung: ---
    - Nachbedinung: M = M_alt \ {i}
    - Ergebnis: True gdw. i € M 
- ist Enthalten:
    - Vorbedingung: ---
    - Nachbedinung: Ergebnis: i € M ?


# Implementierung mit Java: 
- in den Folien

# Implementierung eines ADT

- konkrete Implementierung:
    - Felder
    - Bäume
    - Listen

- ADT abstraktes Modell:
    - Mengen
    - Relationen

- (wichtig) Abstraktionsfunktion
    - A(U,m) = {U[0],U[1], ... ,U[m-1]}
             = {U[j] | 0 <= j < m}

    


