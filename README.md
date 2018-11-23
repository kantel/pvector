# pvector

Eine einfache Vektorklasse für Python, die ich ursprünglich für die Nutzung mit [NodeBox 1](https://github.com/karstenw/nodebox-pyobjc) geschrieben hatte. Sie ist in Anlehnung an die pvector-Klasse von Processing (Java) geschrieben und so allgemein gehalten, daß sie auch mit anderen Bibliotheken laufen sollte. Getestet habe ich sie -- neben der NodeBox -- bisher mit Pythons Turtle-Modul und mit [P5 (Python)](https://github.com/p5py/p5).

Die Klasse läuft mit Python 2.7 **und** mit Python >0= 3.5, sie sollte daher auch unter PyGame und unter Jython[ (TigerJython](http://jython.tobiaskohn.ch/index-de.html)) lauffähig sein. Bisher einzige Abhängigkeiten sind die Module `math` und `random` aus der Standardbibliothek.

## Dokumentation

Bisher sind folgende Funktionen in der Klasse implementiert:

- `pvector.set(v)`: *Setter*-Methode
- `pvector.get()`: *Getter*-Methode
- `pvector.add(v)`: Elementweise Addition
- `pvector.sub(v)`: Elementweise Subtraktion
- `pvector.mult(s)`: Multiplikation mit einem Skalar
- `pvector.div(s)`: Division durch einen Skalar
- `pvector.mult2(v)`: Elementweise Multiplikation eines Vektor mit einem anderen Vektor
- `pvector.div2(v)`: Elementweise Division eines Vektor mit einem anderen Vektor
- `pvector.mag()`: Magnitude
- `pvector.normalize()`: Normalisierung 
- `pvector.dist(v)`: Berechnung der euklidischen Distanz zwischen zwei Vektoren
- `pvector.dot(v)`: Berechnung des Skalarprodukts (inneren Produkts) eines Vektors
- `pvector.limit(max)`: Begrenzt die Magnitude eines Vektors auf max
- `pvector.heading()`: Berechnet den Winkel der Rotation eines Vektors

Und als Klassenmethode:

- `PVector.random2D()` Erzeugt einen zufälligen Vektor der Länge 1

Außerdem die folgenden Methoden:

- `pvector.__add__`: Erlaubt die elementweise Addition zweier Vektoren in der Version `v3 = v1 + v2`
- `pvector.__sub__`: Erlaubt die Subtraktion zweier zweier Vektoren in der Version `v3 = v1 - v2`
- `pvector.__str__`: Gibt eine textliche Repräsentation des Vektors aus.

Die Methoden sollten so aufgerufen werden können und funktionieren, wie es in der [Referenz zur PVector-Klasse](https://www.processing.org/reference/PVector.html) in der Processing-Dokumentation beschrieben ist. Es ist jedoch eine reine 2D-Klasse, mit 3D- oder noch höherwertigen Vektoren funktioniert sie nicht.