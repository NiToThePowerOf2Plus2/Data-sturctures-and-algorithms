
# STÜCKWEISE KONSTANTE FUNKTIONEN
## ZIEL: gewisse mathematische Objekt behandlen und darstellen.

## Definition:
- Eine Funktion, die konstant ist, aber ab und zu Sprünge macht.
- Sprünge passieren im bestimmten Intervall.
- häufig: stückweise lineare Funktionen
    - stetig

## Schreibweise:
- Beispiel:
    - f(x) =
        - 2 falls 3<=x<6 <=> x € [3,6)
        - 2,7 falls 6<=x<9 <=> x € [6,9)
        - usw..
    - Grenzen:
        - zu entscheiden ist die Art des Intervalls: hier bspw. halboffenes Intervall **[..)**
        - bei halboffenen Intervallen kriegt man ein lückenloses Bild von dem allgemeinen Intervall wenn man alle kleinen Intervalle zusammenfügt.

- funktion f: [a,b) -> IR, bestehend aus endlich vielen konstanten Stücken.
    - der Einfachheit halber: halboffenes Intervall
    - als ADT: 
        - Operationen:
            - Funktionen berechnen für gegebenen Wert x. *f(x)*
            - Addieren zweier Funktionen f, g. (gemeinsamer Definitionsbereich)
            - Verknüpfen zweier Funktionen f, g. *h(x) = g(f(x))* **irrelevat**

## Darstellung:
1. Folge von Sprungstellen: verschieden & sortiert
    - [a,b): a = a0 < a1 < a2 < .. < a_n = b
2. Folge von Werten
    - h1, h2, h3, .., h_n € IR für a_i-1 <= x < a_i : f(x) = h_i für 1 >= i < n 

## Implementierung in Python:
Speichern des Intervalls und der Werte in einem Tupel (Schlechte Idee)
(a0,h1,a1,h2,a2,...,h_n,a_n)
```python
#f = (a0,h1,a1,h2,a2,...,h_n,a_n)
def berechne(f,x):
    if x<f[0] or x>=f[-1]:
        return None
    i = 0
    while x>=f[i]:
        i+=2
    return f[i-1]
```
    









