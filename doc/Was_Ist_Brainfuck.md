Was ist brainfuck überhaupt?
Brainfuck ist eine esoterische Programmiersprache, die extrem minimalistisch ist und nur aus acht Befehlen besteht. Die Sprache wurde von Urban Müller im Jahr 1993 entwickelt und ist dafür bekannt, dass sie sehr schwer zu lesen und zu schreiben ist. Obwohl Brainfuck nur aus wenigen Befehlen besteht, können dennoch komplexe Programme geschrieben werden. Die Sprache erfordert jedoch viel Übung und Geduld, um effektiv verwendet werden zu können.

Die Befehle:
| Befehl | Bedeutung |
| --- | --- |
| > | Verschiebe den Datenzeiger um eine Zelle nach rechts |
| < | Verschiebe den Datenzeiger um eine Zelle nach links |
| + | Erhöhe den Wert der aktuellen Zelle um eins |
| - | Verringere den Wert der aktuellen Zelle um eins |
| . | Gib den Wert der aktuellen Zelle als ASCII-Code aus |
| , | Nimm eine Eingabe entgegen und speichere sie in der aktuellen Zelle |
| [ | Beginne eine Schleife. Führe die Schleife aus, solange der Wert der aktuellen Zelle nicht null ist. || ] | Beende eine Schleife. |

Diese Befehle können in verschiedenen Kombinationen verwendet werden, um komplexere Programme zu schreiben. Es ist jedoch wichtig zu beachten, dass Brainfuck aufgrund seiner minimalistischen Natur sehr schwer lesbar und schreibbar ist. Es erfordert viel Übung und Geduld, um effektiv in dieser Sprache zu programmieren.


Ein kleines beispiel von Hello World! programm in Brainfuck:
```brainfuck
++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.
```

Jetzt die Erklärung was das Program macht Step bz Step.
| Brainfuck-Code | Aktion |
| --- | --- |
| +++++ +++++ | Initialisiert den Zähler (Speicherzelle #0) mit dem Wert 10 |
| [ | Beginn einer Schleife, um die nächsten vier Speicherzellen auf 70/100/30/10 zu setzen |
| >+++++ ++ | Bewegt den Zeiger auf die nächste Speicherzelle (#1), erhöht den Wert um 7 |
| >+++++ +++++ | Bewegt den Zeiger auf die zweite Speicherzelle (#2), erhöht den Wert um 10 |
| >+++ | Bewegt den Zeiger auf die dritte Speicherzelle (#3), erhöht den Wert um 3 |
| >+ | Bewegt den Zeiger auf die vierte Speicherzelle (#4), erhöht den Wert um 1 |
| <<<<- | Bewegt den Zeiger auf die erste Speicherzelle (#0) und verringert den Wert um 1 |
| ] | Ende der Schleife |
| >++. | Bewegt den Zeiger auf die zweite Speicherzelle (#2) und gibt den ASCII-Code 72 ("H") aus |
| >+. | Bewegt den Zeiger auf die dritte Speicherzelle (#3) und gibt den ASCII-Code 101 ("e") aus |
| +++++ ++. | Erhöht den Wert der dritten Speicherzelle (#3) um 5 und gibt den ASCII-Code 108 ("l") aus |
| . | Gibt den ASCII-Code 108 ("l") aus |
| +++. | Erhöht den Wert der dritten Speicherzelle (#3) um 3 und gibt den ASCII-Code 111 ("o") aus |
| >++. | Bewegt den Zeiger auf die vierte Speicherzelle (#4) und gibt den ASCII-Code 32 (" ") aus |
| <<+++++ +++++ +++++. | Bewegt den Zeiger auf die erste Speicherzelle (#0) und gibt den ASCII-Code 87 ("W") aus |
| >. | Bewegt den Zeiger auf die zweite Speicherzelle (#2) und gibt den ASCII-Code 111 ("o") aus |
| +++. | Erhöht den Wert der zweiten Speicherzelle (#2) um 3 und gibt den ASCII-Code 114 ("r") aus |
| ----- -. | Verringert den Wert der zweiten Speicherzelle (#2) um 6 und gibt den ASCII-Code 108 ("l") aus |
| ----- ---. | Verringert den Wert der zweiten Speicherzelle (#2) um 3 und gibt den ASCII-Code 100 ("d") aus |
| >+. | Bewegt den Zeiger auf die dritte Speicherzelle (#3) und gibt den ASCII-Code 33 ("!") aus |
| >. | Gibt den ASCII-Code 10 (newline) aus |