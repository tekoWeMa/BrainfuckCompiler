# Titelblatt
# Management Summary
Das Projektziel besteht darin, eine begleitende Projektdokumentation zu erstellen, die Implementierung der Brainfuck Programmiersprache durchzuführen und eine Visualisierung auf einem Embedded Hardware Tinkerforge (OLED Display) zu realisieren. Ein Teil des Projekts beinhaltet auch die Vertiefung der Kenntnisse in der Programmiersprache Java, indem ein Brainfuck-Compiler von Grund auf gebaut wird.

Das Projektteam setzt sich aus Mario Weilenmann und Marvin Huber zusammen. Mario wird sich auf die Entwicklung des Brainfuck-Compilers konzentrieren und dabei den Unterschied zwischen Compiler und Interpreter verstehen. Marvin wird sich auf den Aufbau unterschiedlicher Runtime-Umgebungen konzentrieren.

Der Kernaspekt des Projekts besteht darin, dass es den Aufbau der Programmierkenntnisse des Teams fördert. Durch die Zusammenarbeit und das gegenseitige Coaching bei der Entwicklung des Brainfuck-Compilers werden wir unser Verständnis für die Programmiersprache Java, die Brainfuck-Programmierung und die systematische Erstellung von Code vertiefen.

Das Projekt birgt auch Risiken, wie technische Schwierigkeiten, zeitliche Einschränkungen, mangelnde Zusammenarbeit, finanzielle Einschränkungen und fehlende Erfahrung. Um diese Risiken zu minimieren, werden verschiedene Strategien eingesetzt, wie gründliche Vorbereitung und Forschung, realistische Zeitpläne, effektive Kommunikation und regelmäßige Treffen sowie Schulung und Weiterbildung.

Das Projekt wurde erfolgreich abgeschlossen und wir sind mit dem Ergebnis zufrieden. Die Implementierung der Brainfuck-Programmiersprache und die Visualisierung auf dem Tinkerforge wurden erfolgreich umgesetzt und erfüllten unsere Erwartungen.

Insgesamt haben wir wertvolle Erfahrungen gesammelt und unsere Programmierkenntnisse erweitert. Wir empfehlen, die gewonnenen Erkenntnisse und Fähigkeiten in zukünftigen Projekten zu nutzen und weiterzuentwickeln.
# Inhaltsverzeichnis
# Vorwort
Wieso wir das Thema gewählt haben, einen Brainfuck-Compiler zu schreiben, ist für uns eine faszinierende Herausforderung. Brainfuck ist eine sehr einfache, aber auch sehr abstrakte Programmiersprache, die nur aus acht Befehlen besteht und aufgrund ihrer minimalistischen Natur sehr schwierig zu lesen und zu schreiben ist.

Ein Brainfuck-Compiler ist ein Programm, das geschrieben wurde, um Brainfuck-Code in eine ausführbare Form zu übersetzen, die von einer Maschine verstanden werden kann. Ein Brainfuck-Compiler zu schreiben ist für uns aus folgenden Gründen interessant:

Erstens ist es eine grossartige Möglichkeit, um Programmierkenntnisse zu vertiefen und zu verbessern. Brainfuck ist eine sehr einfache Programmiersprache, die jedoch viele Konzepte der Informatik wie das Konzept des "Speichers" oder "Pointer" erfordert, um sie effektiv zu nutzen. Durch das Schreiben eines Compilers für diese Sprache kann man das Verständnis für diese Konzepte vertiefen und gleichzeitig das eigene Programmiervermögen verbessern.

Zweitens kann es für die Forschung in der theoretischen Informatik von Nutzen sein. Brainfuck wird oft als Beispiel für eine sogenannte "Turing-vollständige" Sprache verwendet, was bedeutet, dass sie in der Lage ist, jede Berechnung durchzuführen, die auch von einem Universalcomputer durchgeführt werden kann. Dies bedeutet, dass das Schreiben eines Compilers für Brainfuck ein interessantes Beispiel für die Erforschung von Berechnungen und Programmiersprachen sein kann.

Drittens kann es einfach aus Gründen der Unterhaltung sein. Wir haben ein grosses intresses an spannend Informatik Theman, finden es einfach faszinierend, mit Brainfuck zu arbeiten und zu sehen, wie sich komplexe Algorithmen mit nur wenigen Befehlen schreiben lassen.

Es bietet die Möglichkeit, Programmierkenntnisse zu verbessern, theoretische Konzepte zu erforschen und sich einfach mit einer faszinierenden Programmiersprache zu beschäftigen. Insgesamt ist das Schreiben eines Brainfuck-Compilers eine herausfordernde und interessante Aufgabe, die wir uns Stellen möchten aufgrund von den oberen genannten Gründen, deswegen haben wir uns entschieden dafür.
# Initialisierungsphase
## Ausgangslage

Die Ausgangslage für die Projektarbeit besteht darin, dass wir über limitierte Java-Kenntnisse verfügen und diese gerne erweitern möchten. Dies ist ein wichtiger Aspekt, da die Programmiersprache Java eine der am häufigsten verwendeten Programmiersprachen ist und in vielen Bereichen der Softwareentwicklung eingesetzt wird.

Doch nicht nur das Erlernen von Java ist ein Ziel der Projektarbeit. Vielmehr möchten wir verstehen, wie ein Compiler funktioniert. Ein Compiler ist ein Programm, das Quellcode einer Programmiersprache in Maschinencode übersetzt, damit dieser vom Computer ausgeführt werden kann. Das Verständnis der Funktionsweise eines Compilers ist daher von entscheidender Bedeutung für die Entwicklung von Software und die Verbesserung von Programmen.

Um dieses Ziel zu erreichen, haben wir uns dazu entschieden, simplen Programmcode der Programmiersprache Brainfuck zu schreiben und zu kompilieren. Brainfuck ist eine Turing-vollständige Programmiersprache, die nur aus acht Befehlen besteht und daher als einfach zu erlernen gilt. Doch obwohl Brainfuck eine einfache Sprache ist, ist sie aufgrund ihrer geringen Abstraktionsebene und der beschränkten Anzahl von Befehlen eine Herausforderung für jeden Compiler.

Daher ist die Projektarbeit ein wichtiger Schritt, um die Kenntnisse von uns in Java zu erweitern und das Verständnis für Compiler zu vertiefen. Es erfordert Engagement, Ausdauer und eine gute Planung, um das Ziel zu erreichen. Aber das Wissen und die Fähigkeiten, die während der Projektarbeit erworben werden, sind von unschätzbarem Wert für zukünftige Projekte und Karrieremöglichkeiten in der Softwareentwicklung.

## Projektauftrag

Projektauftrag: Erstellung einer Projektdokumentation, Implementierung von Brainfuck Programmiersprache und Visualisierung an Embedded Hardware Tinkerforge (OLED Display)

Zielsetzung:

Dieses Projekt zielt darauf ab, eine begleitende Projektdokumentation zu erstellen, die die Entwicklung und Implementierung eines Brainfuck Compilers umfasst. Das Ziel besteht darin, die Programmiersprache Brainfuck zu implementieren und diese auf einer Embedded Hardware Tinkerforge (OLED Display) zu visualisieren. Ein Teil des Projekts beinhaltet auch, dass wir uns gegenseitig beraten und unterstützen, um unser Wissen in Java, Brainfuck und systematischen Abläufen beim Erstellen von Codes zu vertiefen.

Ziele im Detail:

1.  Erstellung einer begleitenden Projektdokumentation: Es wird eine detaillierte Projektdokumentation erstellt, die den Entwicklungsprozess, die Implementierung und die Ergebnisse des Projekts beschreibt. Die Dokumentation umfasst auch Anweisungen und Anleitungen für die Implementierung des Brainfuck Compilers und die Visualisierung der Programmiersprache auf der Embedded Hardware Tinkerforge (OLED Display).
    
2.  Implementierung von Brainfuck Programmiersprache: Ein wesentliches Ziel des Projekts besteht darin, die Programmiersprache Brainfuck zu implementieren. Dies beinhaltet die Entwicklung eines Brainfuck Compilers von Grund auf, um sicherzustellen, dass das Verständnis für Java und Brainfuck vertieft wird. Wir werden auch sicherstellen, dass wir die Unterschiede zwischen Compiler und Interpreter verstehen und in der Lage sind, diese zu erklären.
    
3.  Visualisierung an Embedded Hardware Tinkerforge (OLED Display): Ein weiteres Ziel des Projekts ist es, die Brainfuck Programmiersprache auf einer Embedded Hardware Tinkerforge (OLED Display) zu visualisieren. Dies beinhaltet die Entwicklung einer Runtime-Umgebung, um sicherzustellen, dass die Programmiersprache auf der Hardware effektiv und effizient dargestellt wird. Marvin wird sich auf die Entwicklung von verschiedenen Runtime-Umgebungen konzentrieren, um sicherzustellen, dass die Visualisierung der Programmiersprache auf der Hardware optimal ist.
    

Zusätzliche Ziele:

1.  Vertiefung des Verständnisses von Java: Die Entwicklung des Brainfuck Compilers von Grund auf bietet eine hervorragende Gelegenheit, unser Verständnis von Java zu vertiefen. Wir werden sicherstellen, dass wir ein tiefes Verständnis der Programmiersprache Java haben und in der Lage sind, effektiv damit zu arbeiten.
    
2.  Vertiefung des Verständnisses von Brainfuck: Die Implementierung der Brainfuck Programmiersprache bietet eine hervorragende Gelegenheit, unser Verständnis von Brainfuck zu vertiefen. Wir werden sicherstellen, dass wir ein tiefes Verständnis der Programmiersprache haben und in der Lage sind, effektiv damit zu arbeiten.
    
3.  Entwicklung von systematischen Abläufen: Ein wichtiger Teil des Projekts ist die Entwicklung von systematischen Abläufen beim Erstellen von Codes. Wir werden sicherstellen, dass wir die besten Praktiken bei der Entwicklung von Codes einsetzen, um die Qualität unserer Arbeit zu verbessern.
    
4.   Verbesserung der Zusammenarbeit: Ein weiteres Ziel des Projekts besteht darin, unsere Zusammenarbeit zu verbessern. Wir werden uns gegenseitig beraten und unterstützen, um sicherzustellen, dass jeder von uns das Projekt erfolgreich abschließen kann. Wir werden auch sicherstellen, dass wir effektive Kommunikationswege etablieren, um sicherzustellen, dass wir uns während des gesamten Projekts auf dem gleichen Stand halten.
    
5.  Verbesserung der technischen Fähigkeiten: Dieses Projekt bietet uns eine hervorragende Gelegenheit, unsere technischen Fähigkeiten zu verbessern. Wir werden sicherstellen, dass wir unser Verständnis von Java, Brainfuck und Embedded Hardware Tinkerforge (OLED Display) vertiefen und unsere Fähigkeiten in der Programmierung und Implementierung von Codes verbessern.
    

Projektbeteiligte:

Mario Weilenmann: Mario ist verantwortlich für die Entwicklung des Brainfuck Compilers und die Implementierung der Programmiersprache auf der Embedded Hardware Tinkerforge (OLED Display). 

Marvin Huber: Marvin wird sich auf die Entwicklung von verschiedenen Runtime-Umgebungen konzentrieren, um sicherzustellen, dass die Visualisierung der Programmiersprache auf der Embedded Hardware Tinkerforge (OLED Display) optimal ist. Er wird auch Mario bei der Entwicklung des Brainfuck Compilers unterstützen und sicherstellen, dass der Code effektiv und effizient implementiert wird.

Zusammenfassung:

Insgesamt zielt dieses Projekt darauf ab, eine begleitende Projektdokumentation zu erstellen, die die Entwicklung und Implementierung eines Brainfuck Compilers umfasst. Wir werden sicherstellen, dass wir ein tiefes Verständnis von Java, Brainfuck und systematischen Abläufen beim Erstellen von Codes haben. Wir werden auch sicherstellen, dass die Brainfuck Programmiersprache effektiv auf der Embedded Hardware Tinkerforge (OLED Display) visualisiert wird. Das Projekt bietet uns eine hervorragende Gelegenheit, unsere technischen Fähigkeiten zu verbessern und unsere Zusammenarbeit zu verbessern. Wir sind zuversichtlich, dass wir das Projekt erfolgreich abschließen werden und die gesteckten Ziele erreichen werden.

## Abgrenzungen

Das Projekt, das von uns durchgeführt wird, hat klare Abgrenzungen hinsichtlich seines Umfangs und seiner Zielsetzungen. Eines dieser Ziele ist die Erlernung grundlegender Programmier-Methodiken. Dies bezieht sich auf die Konzepte und Techniken, die in der Programmierung verwendet werden, um effektiv und effizient zu arbeiten.

Wir werden in diesem Projekt grundlegende Programmierkonzepte wie Variablen, Schleifen, Bedingungen und Funktionen kennenlernen sowie der Unterschied zwischen Compiler und Interpreter und auf verschiedenen Runtime umgebungen arbeiten. Diese Konzepte sind von grundlegender Bedeutung für jede Programmiersprache und bilden die Grundlage für komplexe Programme. Indem wir diese Konzepte erlernen und anwenden, können wir unsere Fähigkeiten im Bereich der Programmierung verbessern.

Es ist jedoch wichtig zu betonen, dass das Projekt nicht den Anspruch hat, zur Produktionsreife zu gelangen. Das bedeutet, dass das Ziel des Projekts nicht darin besteht, ein voll funktionsfähiges Produkt zu entwickeln, das von anderen genutzt werden kann. Stattdessen soll uns das Projekt die Möglichkeit geben, grundlegende Konzepte der Programmierung zu erlernen und anzuwenden und uns iJava-programming voran zu bringen.

# Risikoanalyse
Eine Risikoanalyse ist eine wichtige Komponente bei der Planung eines Projekts, um potenzielle Risiken zu identifizieren und Strategien zu entwickeln, um diese Risiken zu minimieren oder zu vermeiden. Im Folgenden sind einige Risiken aufgeführt, die bei der Entwicklung des Brainfuck Compilers und der Visualisierung der Programmiersprache auf der Embedded Hardware Tinkerforge (OLED Display) auftreten könnten:

1.  Technische Schwierigkeiten: Das Projekt erfordert ein tiefes Verständnis von Java, Brainfuck und Embedded Hardware Tinkerforge (OLED Display). Es besteht das Risiko, dass technische Schwierigkeiten auftreten können, die das Projekt verzögern oder sogar unmöglich machen können. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir eine gründliche Forschung und Vorbereitung durchführen und dass wir in der Lage sind, die technischen Herausforderungen effektiv zu bewältigen.
    
2.  Zeitliche Einschränkungen: Das Projekt hat einen relativ kleinen Zeitrahmen, innerhalb dessen das Projekt abgeschlossen werden muss. Es besteht das Risiko, dass wir aufgrund von unvorhergesehenen Schwierigkeiten oder Komplikationen den Zeitrahmen nicht einhalten können. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir realistische Zeitpläne erstellen und dass wir unser Bestes tun, um innerhalb dieser Zeitpläne zu arbeiten.
    
3.  Mangelnde Zusammenarbeit: Das Projekt erfordert eine enge Zusammenarbeit zwischen den Projektbeteiligten. Es besteht das Risiko, dass wir nicht effektiv zusammenarbeiten können, was zu Verzögerungen oder Problemen im Projekt führen kann. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir effektive Kommunikationswege etablieren und dass wir uns regelmäßig treffen, (fast jedes Wochenende) um den Fortschritt des Projekts zu besprechen.
    
4.  Finanzielle Einschränkungen: Das Projekt erfordert möglicherweise finanzielle Ressourcen für die Beschaffung von Materialien oder für die Anmietung von Räumlichkeiten. Es besteht das Risiko, dass das Projekt aufgrund von finanziellen Einschränkungen gestoppt oder verzögert wird. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir realistische Budgets erstellen und dass wir alternative Finanzierungsoptionen prüfen, falls nötig.
    
5.  Fehlende Erfahrung: Es besteht das Risiko, dass wir möglicherweise nicht über ausreichende Erfahrung in der Programmierung oder Implementierung von Codes verfügen, um das Projekt erfolgreich abzuschließen. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir uns gegenseitig unterstützen und dass wir uns regelmäßig schulen und weiterbilden, um unsere technischen Fähigkeiten zu verbessern.
    

Zusammenfassend kann gesagt werden, dass das Projekt einige Risiken birgt. Wir werden jedoch sicherstellen, dass wir diese Risiken im Auge behalten und dass wir Strategien entwickeln, um diese Risiken zu minimieren oder zu vermeiden. Wir sind zuversichtlich, dass wir das Projekt erfolgreich abschließen werden und dass wir die gesteckten Ziele erreichen werden.

## Risikomanagement Tabelle

| Risiko                     | Eintreffwahrscheinlichkeit | Schweregrad | Strategie zur Risikominimierung |
|----------------------------|----------------------------|-------------|--------------------------------|
| Technische Schwierigkeiten | Mittel                     | Leicht-Mittel        | Gründliche Vorbereitung und Forschung, technische Expertise nutzen, um Herausforderungen effektiv zu bewältigen |
| Zeitliche Einschränkungen  | Hoch                       | Leicht      | Realistische Zeitpläne erstellen, Priorisierung der Aufgaben, um sicherzustellen, dass das Projekt innerhalb des Zeitrahmens abgeschlossen wird |
| Mangelnde Zusammenarbeit   | Leicht                     | Mittel      | Effektive Kommunikation und regelmäßige Treffen, um sicherzustellen, dass das Team zusammenarbeitet und Schwierigkeiten frühzeitig erkannt und gelöst werden |
| Finanzielle Einschränkungen| Niedrig                    | Mittel      | Realistische Budgets erstellen, alternative Finanzierungsmöglichkeiten prüfen, falls nötig |
| Fehlende Erfahrung         | Hoch                       | Leicht-Mittel        | Selbststudium, gegenseitige Unterstützung und Mentoring, um sicherzustellen, dass das Team über ausreichende Fähigkeiten verfügt. Profitierung von Marvins kenntnissen. |

# Pflichtenheft
| Mario                                          | Marvin                                            |
| ---------------------------------------------- | ------------------------------------------------- |
| Erstellen der Tabelle und Meilenstein Daten    | Vorbereitung des Programmkonzeptes                |
| Aufsetzung RASPI                               | Überarbeitung des Programmcodes in Rust           |
| Einlesen Brainfuck                             | Rust Vorbereitung für RPI                         |
| Enums in Java vorbereiten                      |                                                   |
| Filereader Selbststudium: Print file content as text |                                               |
| Zeichen Brainfuck Erklärung verstehen          |                                                   |
| Raspberry PI mit Brick hat fertigstellen       |                                                   |
| Memory Pointer Selbststudium                   |                                                   |
| Byte Arrays Verständnis aufbauen               | Workshop erstellen mit Erklärung für Mario        |
| Bracket Implementation verstehen               | Vorbereitung der Erklärung: Stacks / Pair Funktion / Logik der Bracketpairs |
| Dokumentation Java Code                        | Dokumentation Brainfuck und Rust                   |

# Projektplan
1.	Konzeption (Benötigte Komponenten, Aufbau, Vorgehen)  
2.	Versuchsaufbau mit Tinkerforge (Red Brick, OLED Display) 
3.	Programmierung von Interpreter und Compilier 
(Auslesung und Speicherung der Daten) 
4.	Entwicklung der Darstellung von Output 
5.	(Visualisierung der Daten) 
6.	Finalisierung der Dokumentation 

# Meilensteine 

| Meilensteine                                              | Ziel der Fertigstellung | Fertiggestellt am |
| --------------------------------------------------------- | ----------------------- | ----------------- |
| Konzeption (Benötigte Komponenten, Aufbau, Vorgehen)       | bis 11.02.2022          | 11.02.2022        |
| Versuchsaufbau mit Tinkerforge (Red Brick, OLED Display)   | bis 01.03.2023          | 19.02.2023        |
| Programmierung von Interpreter und Compilier               | bis 18.02.2023          | 04.03.2023        |
| Entwicklung der Darstellung von Output                     | bis 25.02.2023          | 04.03.2023        |
| Visualisierung der Daten                                  | bis 25.02.2023          | 04.03.2023        |
| Finalisierung der Dokumentation                            | bis 12.03.2023          | 12.03.2023        |

# Projektstatusbericht

| Datum      | Ausgeübte Tätigkeiten                                                                                                                                         | Wer   |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| 4.12.2022  | - Erstellen des Repositorys, Besprechung der Richtlinien und Anlegen der Dateien. <br> - Überarbeitung des Projektantrages. <br> - Besprechung und Bestellung Hardware | MV, MA|
| 10.12.2022 | - Absprache von Codeidee, erste Entwürfe und Codespezifizierungen                                                                                               | MV, MA|
| 17.12.2022 | - Start Einlesen der Programmiersprache <br> - Absprache der Funktionalität der Programmiersprache                                                           | MV, MA|
| 31.12.2022 | - Start der Entwicklung und Konzeptbesprechung der jeweiligen Programmieraufgaben <br> - Entwicklungsstart und Einlesen von Enums                               | MV, MA|
| 8.01.2023  | - Entwicklung der Funktionalität des FileReaders                                                                                                               | MA    |
| 14.01.2023 | - Entwicklung der Funktionalität der Zeichen-Semantik                                                                                                          | MV, MA|
| 21.01.2023 | - Raspberry PI Setup und Testing des Brick-hats                                                                                                                | MA    |
| 29.01.2023 | - Entwicklung des Memory Pointers <br> - Workshop Byte Arrays                                                                                                 | MV, MA|
| 4.02.2023  | - Entwicklung der Stackfunktion <br>- Theorieblock Bracketlist                                                                                                 | MV, MA|
| 18.02.2023 | - Implementation Bracketlist <br> - Implementation Bracketpair                                                                                                | MV, MA|
| 5.03.2023  | - Errorhandling der Bracketpair Funktion <br>- Entwicklung Bracket.get und Indexing Funktion                                                                 | MV, MA|
| 11.03.2023 | - Code Cleanup, Finishing Touch <br> - Dokumentation Raspberry PI Setup <br> - Layout Anpassungen <br> - Dokumentation Code                                    | MV, MA|
| 12.03.2023 | - Dokumentationserweiterungen                                                                                                                                  | MV, MA|


# Installationsanleitung
## Technische Dokumentation

## Raspberry PI Einrichtung

Für die Visuelle demo benötigen wir einen Host. Wir haben uns hier für ein Raspberry PI entschieden, da dieses einfach zu warten ist und wenig Platz benötigt.<br />

Mit Hilfe von Raspberry PI Imager kann das gewünschte Betriebssystem installiert werden. Wir verwenden das PI OS 64-bit und schreiben dieses auf die Micro SD Karte.
Bei erfolgreichem schreiben des Betriebssystems können wir die SD Karte einsetzen und mit einem USB-C den Raspberry Pi Computer mit Strom versorgen.

## Raspberry Konfiguration

Mittels HDMI können wir den Desktop des Betriebssystem anzeigen lassen und die ersten Konfigurationen vornehmen. <br />

Mittels Setupmanager wählen wir als erstes die korrekte Region, Zeitzone und Sprache. Danach setzen wir ein Passwort sowie den Namen für den User. Wir benennen ihn nach unserem Projekt, also sugu. Wir benötigen den Namen und Passwort später, wenn wir via SSH darauf zugreifen wollen. <br />

Wir setzen den Haken für das Screen Setup um optimierte Auflösungen zu erhalten für den Bildschirm. Da wir Ethernet verwenden, müssen wir uns nicht mit einem W-LAN verbinden. <br />

Sobald wir mit einem Netzwerk verbunden sind, können wir im Setupmanager ein Update der Software durchführen.

## SSH einschalten

Um auf unseren User zugreifen zu können, müssen wir SSH aktivieren. Dafür klicken wir auf dem Desktop auf das Raspberry logo, wählen **Preferences** und dann **Raspberry PI Configuration**. Unter dem **Interfaces** Tab können wir SSH anwählen.
![](Raspi-Interface.png)
![](SSH.png)

## Statische IP vergeben

Um mit keinen Komplikationen konfrontiert zu werden, vergeben wir dem Raspberry PI eine Statische IP Addresse. Dafür öffnen wir das Terminal auf dem Desktop. Mittels ``ifconfig`` können wir die momentan zugeweiste IP des netzwerkes ansehen. In unserem Fall ist dies **192.168.1.17**.<br />Mittels ``sudo nano /etc/dhcpcd.conf`` können wir direkt in die config file unsere gewünschte IP Addresse schreiben. Dies machen wir wiefolgt:

```
interface eth0
static ip_address=192.168.1.17
static routers=192.168.1.1
static domain_name_servers=8.8.8.8 8.8.4.4

```

Einstellungen mit ``Ctrl + o`` schreiben und den Editor mit ``Ctrl + x`` verlassen. Danach den Raspi neustarten:

`sudo reboot`

## Brick Hat 

## Features

-   Raspberry Pi HAT im Standard-HAT-Formfaktor
-   **Acht** Anschlüsse für Bricklets
-   Integrierte 5,3V Stromversorgung (6V-28V Eingang, bis zu 4A)
-   Misst USB- und DC-Spannungsversorgung
-   Bietet eine Real-Time Clock für den Raspberry Pi
-   Bietet Schlafmodus (Low Power) und Watchdog

## Beschreibung

Der HAT Brick ist ein [Raspberry Pi HAT](https://www.raspberrypi.org/blog/introducing-raspberry-pi-hats/) im Standard-HAT-Formfaktor. Der Brick ist zur HAT-Spezifikation konform und funktioniert automatisch und ohne Änderungen mit Raspbian.

Mit dem HAT Brick können bis zu **acht** [Bricklets](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricklets) an ein Raspberry Pi angeschlossen werden.

Note: Der HAT Brick besitzt 7-Pol-Bricklet-Anschlüsse. Über ein 7-Pol- <-> 7-Pol-Kabel können Bricklets an den Brick angeschlossen werden. Es werden nur Bricklets unterstützt, die über einen 7-poligen Anschluss verfügen.

Der Raspberry Pi kann über den HAT Brick mit einer externen 6V-28V DC Stromversorgung betrieben werden. Die integrierte Stromversorgung liefert auch unter großer Last stabile 5V für den Raspberry Pi. Somit können auch angeschlossene Bricklets und verbundene USB-Geräte versorgt werden. Das HAT Brick liefert hierfür eine etwas erhöhte Spannung von 5,3V.

Alternativ können HAT Brick und Raspberry Pi auch über USB-C versorgt werden. In diesem Fall muss allerdings sichergestellt werden, dass die Stromversorgung stabile 5V bietet. Dies ist zum Beispiel mit dem offiziellen Raspberry Pi Universal-Netzteil möglich. Die USB/DC Versorgungsspannungen werden vom HAT gemessen und sind über die API zugänglich.

Der HAT Brick bietet eine [Real-Time Clock mit Super-Cap Backup](https://www.tinkerforge.com/de/doc/Hardware/Bricks/HAT_Brick.html#hat-brick-real-time-clock), die direkt mit dem Raspberry Pi verbunden ist. Mit dieser kann [der Raspberry Pi für eine angegebene Zeit ausgeschaltet werden](https://www.tinkerforge.com/de/doc/Hardware/Bricks/HAT_Brick.html#hat-brick-low-power-sleep-mode). Somit kann der Raspberry Pi auch in batteriebetriebenen Anwendungen eingesetzt werden, zum Beispiel in einer Anwendung, in der Sensorinformationen jede Stunde in die Cloud geschickt werden sollen.

Mit dem HAT Brick kann ein [Watchdog](https://www.tinkerforge.com/de/doc/Hardware/Bricks/HAT_Brick.html#hat-brick-watchdog) implementiert werden, der den Raspberry Pi neustartet, wenn sich dieser aufhängt oder das eigene Programm steckenbleibt.

Der HAT Brick ist elektronisch kompatibel zu den Raspberry Pis 2B, 3B, 3B+, 4B, Zero und Zero W. Die Befestigungslöcher sind kompatibel zum Raspberry Pi 2/3/4. Zusätzlich bieten wir mit dem [HAT Zero Brick](https://www.tinkerforge.com/de/doc/Hardware/Bricks/HAT_Zero_Brick.html#hat-zero-brick) eine kleinere Version, deren Befestigungslöcher zum Raspberry Pi Zero kompatibel sind.

| Eigenschaft                          | Wert                                           |
|--------------------------------------|------------------------------------------------|
| Stromverbrauch                       | 100mW (20mA bei 5V)                            |
| Bricklet-Anschlüsse                  | 8                                              |
| DC Eingangsspannungsbereich           | 6V-28V                                         |
| DC Ausgang                            | 5,3V, max. 4A                                  |
| Stromverbrauch im Sleepmodus (≤1.4)* | 70mW (14mA bei 5V) + 1.5mW wenn die Sleep-LED aktiv ist |
| Abmessungen (B x T x H)              | 65 x 56 x 25mm (2,56 x 2,20 x 0,98")           |
| Gewicht                               | 30g                                            |


## Ressourcen

-   Schaltplan ([Download](https://github.com/Tinkerforge/hat-brick/raw/master/hardware/hat-schematic.pdf))
-   Umriss und Bohrplan ([Download](https://www.tinkerforge.com/de/doc/_images/Dimensions/hat_brick_dimensions.png))
-   Quelltexte und Platinenlayout ([Download](https://github.com/Tinkerforge/hat-brick/zipball/master))
-   3D Modell ([Online ansehen](https://autode.sk/2XiDCDT) | Download: [STEP](https://download.tinkerforge.com/3d/bricks/hat/hat.step), [FreeCAD](https://download.tinkerforge.com/3d/bricks/hat/hat.FCStd))

## Erste Schritte

![](res/Pasted%20image%2020230217121831.jpg)

Um den HAT Brick verwenden zu können, muss zuerst der [Brick Daemon](https://www.tinkerforge.com/de/doc/Software/Brickd.html#brickd) auf dem Raspberry Pi installiert werden. Der Brick Daemon agiert als Proxy zwischen den Brickletanschlüssen des HAT Brickss und den API Bindings. Er kümmert sich auch um die Real-Time Clock.

### Interface
Es wird ein Interface verwendet mit dem Namen "Brick Viewer" für eine visuelle veranschaulichung.
Der Brick Viewer kann entweder direkt auf dem Raspberry Pi oder auf einem externen PC, der über Ethernet oder WLAN Zugriff auf den Raspberry Pi besitzt, installiert werden. Von einem externen PC aus muss sich auf den Hostnamen oder die IP des Raspberry Pis verbunden werden, vom Raspberry Pi aus auf localhost.

![](res/Pasted%20image%2020230217122052.jpg)

## Installation Tinkerforge software

### Brick Daemon (brickd)

Der Brick Daemon ist ein Daemon (bzw. Service für Windows) der als eine Brücke zwischen [Bricks](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricks)/[Bricklets](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricklets) und den [API Bindings](https://www.tinkerforge.com/de/doc/Software/API_Bindings.html#api-bindings) für die verschiedenen Programmiersprachen fungiert.

Der Daemon leitet Daten zwischen der USB Verbindung und den TCP/IP Sockets hin und her. Bei der Benutzung der API Bindings wird eine TCP/IP Verbindung zum Brick Daemon hergestellt. Dieses Konzept erlaubt es Bindings für nahezu jede Programmiersprache ohne Abhängigkeiten zu erstellen. Dadurch ist es möglich Bricks und Bricklets über eingebettete Geräte wie Smartphones zu programmieren, die nur spezifische Programmiersprachen unterstützten.

Zusätzlich ist es möglich den PC auf dem der Brick Daemon läuft von dem PC auf dem der Benutzercode läuft zu trennen. Dadurch ist das Steuern über ein Smartphone oder auch über das Internet möglich.

# Brick Daemon Installation auf Linux


## Installation
**Voraussetzungen**: libusb 1.0.6 oder neuer

Der [Brick Daemon](https://www.tinkerforge.com/de/doc/Software/Brickd.html#brickd) kann auf einer Debian basierten Distribution (Ubuntu, Mint, etc.) aus einer `.deb` Datei installiert werden. Für Arch Linux steht im AUR das Paket [brickd](https://aur.archlinux.org/packages/brickd/) zur Verfügung. Auf anderen Distributionen kann der Brick Daemon aus dem Quelltext installiert werden.

## Debian Paket

Das Brick Daemon Debian Paket steht im [APT Repository](https://download.tinkerforge.com/apt/) bereit, kann aber auch händisch installiert werden.

### APT Repository

Zuerst entsprechend der [Anleitung](https://www.tinkerforge.com/de/doc/Software/APT_Repository.html#apt-repository) das APT Repository hinzufügen. Dann das Brick Daemon Paket installieren:

sudo apt install brickd

Der Brick Daemon wird nach der Installation und beim Hochfahren des Systems automatisch gestartet.

### Händische Installation

Als erstes muss das passende Brick Daemon `.deb` von der [Download-Seite](https://www.tinkerforge.com/de/doc/Downloads.html#downloads-tools) heruntergeladen werden. Nach einem Rechtsklick auf die Datei kann "Open with GDebi Package Installer" ausgewählt werden:

![](res/Pasted%20image%2020230217111112.png)

Klick auf "Install Package":

![](res/Pasted%20image%2020230217111134.png)

Fertig:

![](res/Pasted%20image%2020230217111159.png)

## Logging

Standardmäßig loggt Brick Daemon Nachrichten über Informationen, Warnungen und Fehler. Diese beinhalten auch Informationen über USB Hotplug und TCP/IP Verbindungen.

-   Linux und macOS: Nachrichten werden in diesem Log-Datei geschrieben:
    
    `/var/log/brickd.log`
    
-   Windows: Nachrichten werden einer Log-Datei namens `brickd.log` im Brick Daemon Data-Verzeichnis gespeichert:
    
    -   Windows XP:
        
        `C:\Dokumente und Einstellungen\All Users\Application Data\Tinkerforge\Brickd\brickd.log`
        
    -   Windows Vista oder neuer:
        
        `C:\ProgramData\Tinkerforge\Brickd\brickd.log`
        
    
    Das `logviewer.exe` Tool (Teil der brickd Installation) kann diese Log-Datei anzeigen und beinhaltet auch eine Live Log Ansicht.
    

Falls der Standard Logging Einstellung nicht genug Details ausgibt, um ein Problem debuggen zu können, dann kann das Debug Log Level aktiviert werden. Dies ist standardmäßig nicht aktiviert, da es die Menge der ausgegebenen Log-Nachrichten stark erhöht, so dass es einen Einfluss auf den Nachrichtendurchsatz von brickd haben kann.

-   Windows: Das `logviewer.exe` Tool stellt ebenfalls Live Log Ansicht bereit, die auf Debug Level gestellt werden kann.

## Konfiguration

Brick Daemon verwendet eine Konfigurationsdatei mit Schlüssel-Wert Format:

-   Linux und macOS: Die Konfigurationsdatei heißt `brickd.conf` und ist hier gespeichert:
    
    `/etc/brickd.conf`
    
-   Windows: Die Konfigurationsdatei heißt `brickd.ini` und ist im Brick Daemon Data-Verzeichnis gespeichert:
    
    -   Windows XP:
        
        `C:\Dokumente und Einstellungen\All Users\Application Data\Tinkerforge\Brickd\brickd.ini`
        
    -   Windows Vista oder neuer:
        
       ` C:\ProgramData\Tinkerforge\Brickd\brickd.ini`
        
    
    Das `logviewer.exe` Tool (Teil der brickd Installation) kann diese Konfigurationsdatei bearbeiten.


### WebSockets

Brick Daemon unterstützt seit Version 2.1.0 [WebSockets](https://de.wikipedia.org/wiki/WebSocket). Diese sind standardmäßig deaktiviert. Um WebSockets zu aktivieren muss ein WebSockets-Port in der Brick Daemon Konfigurationsdatei eingetragen werden.

Die WebSockets-Port Option hat den Schlüssel `listen.websocket_port`. Ein Wert von 0 oder das Fehlen des `listen.websocket_port` Schlüssels führt zur deaktiviert der WebSocket-Unterstützung. Hier der Authentifizierungsabschnitt einer Beispiel-Konfiguration, das dem empfohlenen Wert 4280 als WebSockets-Port verwendet:

listen.websocket_port = 4280`

Danach muss Brick Daemon neugestartet werden, um die Änderungen an der Konfigurationsdatei zu übernehmen. Ab jetzt kann die Browser-Version der [JavaScript Bindings](https://www.tinkerforge.com/de/doc/Software/API_Bindings_JavaScript.html#api-bindings-javascript) sich zum Brick Daemon verbinden und Bricks und Brickets steuern.

Bemerkung: Da WebSockets es grundsätzlich ermöglichen, dass jede Webseite in ihrem Browser sich mit ihren Bricks und Bricklets verbinden kann, empfehlen wir [Authentifizierung](https://www.tinkerforge.com/de/doc/Tutorials/Tutorial_Authentication/Tutorial.html#tutorial-authentication) in Kombination mit WebSockets zu verwenden.

### Authentifizierung

Brick Daemon unterstützt seit Version 2.1.0 Authentifizierung. Diese ist standardmäßig deaktiviert. Um Authentifizierung zu aktivieren muss ein Authentifizierungsgeheimnis in der Brick Daemon Konfigurationsdatei eingetragen werden.

Das Authentifizierungsgeheimnis kann maximal 64 ASCII Zeichen lang sein und hat den Schlüssel `authentication.secret`. Ein leerer Wert oder das Fehlen des `authentication.secret` Schlüssels führt zur deaktiviert der Authentifizierung. Hier der Authentifizierungsabschnitt einer Beispiel-Konfiguration die `My Authentication Secret!` als Authentifizierungsgeheimnis verwendet:

`authentication.secret = My Authentication Secret!`

Danach muss Brick Daemon neugestartet werden, um die Änderungen an der Konfigurationsdatei zu übernehmen. Ab jetzt muss jede TCP/IP Verbindung zum Brick Daemon zuerst nachweisen, dass sie das Authentifizierungsgeheimnis kennt, bevor normale Kommunikation stattfinden kann. Für mehr Informationen zur Authentifizierung siehe das dazugehörige [Tutorial](https://www.tinkerforge.com/de/doc/Tutorials/Tutorial_Authentication/Tutorial.html#tutorial-authentication).

## Installierte Version bestimmen

Seit Brick Daemon Version 1.0.8 ist es möglich die aktuell installierte Brick Daemon Version zu erfragen. Dafür unterstützt der Brick Daemon den Kommandozeilenparameter --version:

-   Linux:
    
    `brickd --version`
    
-   Windows XP:
    
    `"C:\Programme\Tinkerforge\Brickd\brickd.exe" --version`
    
-   Windows Vista oder neuer:
    
    `"C:\Programme (x86)\Tinkerforge\Brickd\brickd.exe" --version`
    
-   macOS (bis Brick Daemon 2.2.1):
    
    `/usr/libexec/brickd.app/Contents/MacOS/brickd --version`
    
-   macOS (seit Brick Daemon 2.2.2):
    
   ` /usr/local/libexec/brickd.app/Contents/MacOS/brickd --version`

## Brick Viewer installation

### Linux Installation
**Voraussetzungen**: Python 3.5 und PyQt 5.5 mit QtOpenGL oder neuer

Der [Brick Viewer](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv) kann auf einer Debian basierten Distribution (Ubuntu, Mint, etc.) aus einer `.deb` Datei installiert werden. Für Arch Linux steht im AUR das Paket [brickv](https://aur.archlinux.org/packages/brickv/) zur Verfügung. Auf anderen Distributionen kann der Brick Viewer aus seinem Quelltext installiert werden.

## Debian Paket

Das Brick Viewer Debian Paket steht in unserem [APT Repository](https://download.tinkerforge.com/apt/) bereit, kann aber auch händisch installiert werden.

### APT Repository

Zuerst entsprechend der [Anleitung](https://www.tinkerforge.com/de/doc/Software/APT_Repository.html#apt-repository) das APT Repository hinzufügen. Dann das Brick Viewer Paket installieren:

sudo apt install brickv`

Der Brick Viewer kann jetzt über das Anwendungsmenü aus der Unterkategorie Sonstiges gestartet werden, oder aus einem Terminal heraus mit:

`brickv`

### Händische Installation

Als erstes muss das Brick Viewer `.deb` von der [Download-Seite](https://www.tinkerforge.com/de/doc/Downloads.html#downloads-tools) heruntergeladen werden. Durch einen Rechtsklick auf die Datei und auswählen von "Mit GDebi-Paket-Installationsprogramm öffnen" wird das Installationsprogramm gestartet:

![](res/Pasted%20image%2020230217120719.jpg)

Ein Klick auf "Paket Installieren" startet dann die eigentliche Installation:

![](res/Pasted%20image%2020230217120731.jpg)

Der Installationsprozess ist nun abgeschlossen:

![](res/Pasted%20image%2020230217120745.jpg)

Auf Ubuntu kann auch das Ubuntu Software Center verwendet werden, andere Debian basierte Distributionen bieten ähnliche Werkzeuge zur Paketverwaltung. Der Brick Viewer kann jetzt über das Anwendungsmenü aus der Unterkategorie Sonstiges gestartet werden, oder aus einem Terminal heraus mit:

`brickv`

Statt mittels eines graphischen Installationsprogramms kann der Brick Viewer auch über einen Terminal durch folgende Befehle installiert werden:

`sudo apt-get install python3 python3-pyqt5 python3-pyqt5.qtopengl python3-serial python3-tz python3-tzlocal
wget --backups=1 https://download.tinkerforge.com/tools/brickv/linux/brickv_linux_latest.deb
sudo dpkg -i brickv_linux_latest.deb`

## Aus Quelltext

Um den Brick Viewer aus dem Quelltext heraus zu verwenden kann der Quelltext ebenfalls im [Downloadbereich](https://www.tinkerforge.com/de/doc/Downloads.html#downloads-tools) heruntergeladen werden. Auch hier müssen die benötigten Abhängigkeiten installiert werden:

-   python3 (>= 3.5)
-   python3-pyqt5 (>= 5.5)
-   python3-pyqt5.qtopengl
-   python3-serial
-   python3-tz
-   python3-tzlocal

Auf Debian basierte Distributionen können diese Pakete wie zuvor per `apt-get` installiert werden. Für andere Distributionen sollte es äquivalente Pakete geben:

`sudo apt-get install python3 python3-pyqt5 python3-pyqt5.qtopengl python3-serial python3-tz python3-tzlocal`

Als erstes müssen die Qt `.ui` Dateien übersetzt werden. Dazu in den `src/` Ordner innerhalb des entpackten Quelltexts wechseln und dort folgenden Befehl ausführen:

`python build_src.py`

Um den Brick Viewer zu starten muss in den `src/brickv/` Ordner gewechselt und dort folgender Befehl ausgeführt werden:

`python main.py`

## Installation auf Raspberry PI OS

Die auf der [Download Seite](https://www.tinkerforge.com/de/doc/Downloads.html#downloads) verfügbare Software steht auch als Debian Pakete in unserem [APT Repository](https://download.tinkerforge.com/apt/) zur Installation bereit.

Aktuell werden folgende Distributionen und Architekturen unterstützt:

-   [Debian](https://www.debian.org/): amd64, i386, armhf, arm64
-   [Ubuntu](https://ubuntu.com/): amd64, i386, armhf, arm64
-   [Raspberry Pi OS](https://www.raspberrypi.org/downloads/raspberry-pi-os/) (ehemals Raspbian): armhf

## Einrichtung

**Schritt 1:** Öffentlichen GPG Schlüssel importieren:

`wget https://download.tinkerforge.com/apt/$(. /etc/os-release; echo $ID)/tinkerforge.gpg -q -O - | sudo tee /etc/apt/trusted.gpg.d/tinkerforge.gpg > /dev/null`

**Schritt 2:** APT Repository hinzufügen:

`echo "deb https://download.tinkerforge.com/apt/$(. /etc/os-release; echo $ID $VERSION_CODENAME) main" | sudo tee /etc/apt/sources.list.d/tinkerforge.list`

**Schritt 3:** APT Paketliste aktualisieren:

`sudo apt update`

## Pakete

Aktuell sind folgende Pakete verfügbar:

-   Tools
    -   [Brick Daemon](https://www.tinkerforge.com/de/doc/Software/Brickd.html#brickd): `brickd`
    -   [Brick Viewer](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv): `brickv`
    -   [Brick Flash](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brick-flash): `brick-flash`
-   API Bindings
    -   [Go](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Go.html#api-bindings-go): `golang-tinkerforge-dev`
    -   [Java](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Java.html#api-bindings-java): `libtinkerforge-java` und `libtinkerforge-java-doc`
    -   [JavaScript (Node.js)](https://www.tinkerforge.com/de/doc/Software/API_Bindings_JavaScript.html#api-bindings-javascript): `node-tinkerforge`
    -   JSON: `tinkerforge-json`
    -   [MQTT](https://www.tinkerforge.com/de/doc/Software/API_Bindings_MQTT.html#api-bindings-mqtt): `tinkerforge-mqtt`
    -   [Octave](https://www.tinkerforge.com/de/doc/Software/API_Bindings_MATLAB.html#api-bindings-matlab): `octave-tinkerforge`
    -   [Perl](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Perl.html#api-bindings-perl): `libtinkerforge-perl`
    -   [PHP](https://www.tinkerforge.com/de/doc/Software/API_Bindings_PHP.html#api-bindings-php): `php-tinkerforge`
    -   [Python](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Python.html#api-bindings-python): `python3-tinkerforge` (Python 3) und `python-tinkerforge` (Python 2)
    -   [Ruby](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Perl.html#api-bindings-perl): `ruby-tinkerforge`
    -   [Shell](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Shell.html#api-bindings-shell): `tinkerforge-shell`


## Übersicht Brick Viewer

Der Brick Viewer bietet eine graphische Oberfläche um [Bricks](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricks) und [Bricklets](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricklets) zu testen. Jedes Gerät hat seine eigenen Tab der die Hauptfunktionen abbildet und erlaubt diese zu steuern.

Darüber hinaus kann der Brick Viewer verwendet werden, um den Analog-Digital-Wandler der Bricks zu [kalibrieren](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-adc-calibration) und so deren Messqualität zu verbessern, und um [Brick Firmwares](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-flash-brick-firmware) und [Bricklet Plugins](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-flash-bricklet-plugin) zu flashen.

## Verwendung

Zuerst muss der Brick Viewer mit dem [Brick Daemon](https://www.tinkerforge.com/de/doc/Software/Brickd.html#brickd) oder z.B. einer [WIFI Extension](https://www.tinkerforge.com/de/doc/Hardware/Master_Extensions/WIFI_Extension.html#wifi-extension) verbunden werden. Dabei kann der Brick Daemon auf dem gleichen oder einem anderen PC als der Brick Viewer laufen. Dazu zuerst die IP Adresse des PCs auf dem der Brick Daemons läuft oder die IP Adresse einer WIFI Extension als Host angeben. Falls Brick Daemon und Viewer auf dem gleichen PC laufen kann der Standardwert `localhost` beibehalten werden. Nach einem Klick auf den "Connect" Knopf werden die verbunden Bricks und Bricklets auf je einem eigenen Tab angezeigt und können getestet werden. Da wir beides auf dem Raspberry PI installiert haben, verbinden wir Brick Viewer über Localhost.

![](res/Pasted%20image%2020230217121252.jpg)

Ein Klick auf den "Updates / Flashing" öffnen einen Dialog mit Informationen über verfügbare Updates und der Möglichkeit Bricks und Bricklets neu zu flashen. Der "Advanced Functions" Knopf öffnet einen Dialog zur Kalibrierung des Analog-Digital-Wandler eines Bricks.

## Aktuellen Stand bestimmen / Nach Updates suchen

Nach dem Start des Brick Viewers und dem Verbinden zu einem Brick Daemon oder einer Master Extension kann überprüft werden ob eine neuere Software für die angeschlossenen Geräte verfügbar ist.

Hierzu muss auf "Updates / Flashing" geklickt werden. Der Dialog zeigt die angeschlossenen Geräte und deren Software stand. Orange unterlegte Einträge können geupdatet werden. Rot unterlegte Einträge müssen geupdatet werden damit sie korrekt funktionieren.

![](res/Pasted%20image%2020230217121414.jpg)

Der Dialog ermöglicht es alle Bricklets gleichzeitig über den Knopf "Auto-Update All Bricklets" auf die neuste Softwareversion zu bringen. Bricks können nicht automatisch auf den neusten Stand gebracht werden (siehe [Brick Firmware Flashing](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-flash-brick-firmware)).

## Brick Firmware Flashing

Wir empfehlen Brick Viewer zum Flashen von Firmwares zu verwenden. Für Linux System ohne graphische Benutzeroberfläche steht aber auch `brick-flash` zur Verfügung.

### Mit Brick Viewer

Seit Version 1.1.0 kann der Brick Viewer Firmwares auf Bricks flashen. Die jeweils neuste Firmwareversion wird dabei automatisch vom Brick Viewer ermittelt und heruntergeladen. Diese können aber auch manuell im [Downloadbereich](https://www.tinkerforge.com/de/doc/Downloads.html#downloads-brick-firmwares) heruntergeladen werden.

#### Vorbereitung

Um einen Brick flashen zu können, muss dieser per USB zu einem PC mit Brick Viewer verbunden sein. Abhängig vom Typ des Brick ist noch Folgendes zu beachten:

-   Bevor ein **IMU Brick (1.0)** neu geflasht wird sollte dessen Kalibrierung exportiert werden, da diese beim Flashen verloren geht. Dies ist allerdings nur dann notwendig, falls eine eigenen Kalibrierung vorgenommen wurde, da die Werkskalibrierung seit Brick Viewer Version 1.1.13 automatisch wiederhergestellt werden kann.
-   Die Hardware Version 2.0 des **Master Bricks** hat eine Änderung im Leiterplattenlayout, die den Bootloader Modus stört, wenn eine Master Extension wie WIFI, RS485 oder Ethernet im Stack vorhanden ist. In diesem Fall muss die Master Extension aus dem Stack entfernt werden, damit der Bootloader Modus richtig funktioniert. Diese Problem wurde in Hardware Version 2.1 korrigiert.

Zum Flashen einer neuen Firmware muss der Brick in den Bootloader Modus versetzt werden. Der **ESP32 Brick** und **ESP32 Ethernet Brick** werden dazu einfach per USB an den PC angeschlossen.

Für alle anderen 4x4cm Brick müssen dazu folgende Schritte durchgeführt:

1.  Brick per USB an PC anschließen.
2.  Erase Knopf drücken und gedrückt halten.
3.  Reset Knopf drücken und wieder loslassen.
4.  Erase Knopf wieder loslassen.

Jetzt sollten alle LEDs am 4x4cm Brick aus sein, der Brick sich im Bootloader Modus befinden und am PC sollte eine neue seriellen Schnittstelle auftauchen.

#### Serielle Schnittstelle

Als nächstes muss der Brick Viewer gestartet und der "Updates / Flashing" Dialog geöffnet werden:

![](res/Pasted%20image%2020230217121445.jpg)

Die "Serial Port" Dropdown-Box zeigt alle verfügbaren seriellen Schnittstellen des PCs an. Diese kann mittels des "Refresh" Knopfes aktualisiert werden, falls keine oder nicht die richtige serielle Schnittstelle aufgelistet wird. Falls der Brick nicht als serielle Schnittstelle auftaucht, befindet sich der Brick entweder nicht im Bootloader Modus, oder das Betriebssystem hat ihn nicht richtig als serielle Schnittstelle erkannt:

-   Auf **Windows** XP und Vista kann es nötig sein den Atmel Treiber `atm6124_cdc.inf` aus dem `drivers` Unterordner der Brick Viewer Installation zu installieren, damit ein Brick im Bootloader Modus richtig als serielle Schnittstelle erkannt wird. Windows 7, 8, 8.1 und 10 erkennt einen Brick im Bootloader Modus von sich aus als "GPS Camera Detect" oder "Bossa Program Port" Gerät. Dies ist auch eine serielle Schnittstelle so das Flashen dennoch möglich ist.
-   Für **alte Linux** Kernel Versionen kann es notwendig sein diesen [SAM-BA Linux USB Kernel Treiber](http://mail.embedded-it.de/microcontroller/eNet-sam7X.php) zu installieren, damit ein Brick im Bootloader Modus richtig funktioniert.
-   Auf **macOS** kann einen Brick im Bootloader Modus als DVB-T Stick erkannt und automatisch EyeTV oder ein ähnliches Programm gestartet werden. Dann einfach EyeTV schließen und mit dem Flash-Vorgang fortfahren.

Wird die serielle Schnittstelle des Bricks richtig erkannt muss diese nun im Brick Viewer ausgewählt werden, typische Namen sind:

-   Windows: "AT91 USB to Serial Converter" oder "GPS Camera Detect" oder "Bossa Program Port"
-   Linux: `/dev/ttyACM0` oder `/dev/ttyUSB0`
-   macOS: `/dev/tty.usbmodemfd131`

#### Flashen

Jetzt noch die richtige Firmware für den Brick auswählen. Passend die Einstellungen kann das Flashen per Klick auf den "Save" Knopf gestartet werden. Die aktuelle Firmware für den Brick wird heruntergeladen, auf den Brick geschrieben und dann wieder zurück gelesen, um sicherzustellen, dass das Schreiben der Firmware richtig funktioniert hat.

Falls das Flashen fehlschlägt, sollte zunächst überprüft werden, ob die richtige serielle Schnittstelle ausgewählt wurde. Wenn Brick Viewer auf Linux "No permission to open serial port" meldet, dann liegt dies normalerweise daran, dass der Nutzer nicht der Gruppe `dialout` angehört. Um dieses Problem zu beheben kann entweder der Nutzer der Gruppe `dialout` hinzugefügt oder Brick Viewer als root gestartet werden (`sudo brickv`).

Anstatt den Brick Viewer die jeweils neuste Firmware herunterladen zu lassen, kann auch "Custom..." als Firmware gewählt werden und dann die zu flashende Firmware als lokale Datei über den "Browse..." Knopf ausgewählt werden.

### Mit brick-flash auf Linux

Brick Viewer benötigt eine graphische Benutzeroberfläche. Falls Bricks an Linux Rechnern ohne graphische Benutzeroberfläche geflasht werden sollen kann `brick-flash` verwendet werden. Es steht als [Debian Packet](https://download.tinkerforge.com/tools/brick_flash/linux/brick-flash_linux_latest.deb) zum Download bereit:

wget --backups=1 https://download.tinkerforge.com/tools/brick_flash/linux/brick-flash_linux_latest.deb
sudo dpkg -i brick-flash_linux_latest.deb

Im Gegensatz zum Brick Viewer lädt `brick-flash` die Firmware nicht automatisch herunter. Die jeweils neusten Firmwares sind [hier](https://www.tinkerforge.com/de/doc/Downloads.html#downloads-brick-firmwares) zu finden. Lade die zu flashende Firmware herunter, z.B. die neuste Master Brick Firmware:

wget --backups=1 https://download.tinkerforge.com/firmwares/bricks/master/brick_master_firmware_latest.bin

Stelle sicher, dass sich der Brick im Bootloader Modus befindet (siehe Brick Viewer Abschnitt weiter oben) und bestimme die serielle Schnittstelle des Bricks. Typischerweise ist dies `/dev/ttyACM0` oder `/dev/ttyUSB0`.

Jetzt kann `brick-flash` mit dem Namen der serielle Schnittstelle und dem Dateinamen der Firmware ausgeführt werden:

brick-flash -p /dev/ttyACM0 -f brick_master_firmware_latest.bin

Nach dem Flash-Vorgang startet der Brick automatisch neu und verwendet die neue Firmware.

## Bricklet Plugin Flashing

Der Brick Viewer kann auch Plugins auf Bricklets flashen. Hierfür gibt es die Möglichkeit alle Bricklets auf die neuste Version zu bringen (siehe "Auto-Update All Bricklets" unter [Aktuellen Stand bestimmen](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-auto-update)). Alternativ können Bricklets auch einzeln geflasht werden. Die jeweils neuste Plugin-Version wird dabei automatisch vom Brick Viewer ermittelt und heruntergeladen. Diese können aber auch manuell im [Downloadbereich](https://www.tinkerforge.com/de/doc/Downloads.html#downloads-bricklet-plugins) heruntergeladen werden.

Um ein Bricklet flashen zu können, muss es an einem Brick angeschlossen sein, der im Brick Viewer aufgelistet ist. Ein Klick auf den "Flashing" Knopf im lässt den passenden Dialog erscheinen:

![](res/Pasted%20image%2020230217121503.jpg)

Als nächstes muss der Brick und dessen Port ausgewählt werden, an dem das zu flashende Bricklet angeschlossen ist, sowie das passenden Plugin für das Bricklet. Passend die Einstellungen kann das Flashen per Klick auf den "Save" Knopf gestartet werden. Jetzt wird das aktuelle Plugin für das Bricklet heruntergeladen, auf das Bricklet geschrieben und dann wieder zurück gelesen, um sicherzustellen, dass das Schreiben des Plugin richtig funktioniert hat. Falls das Flashen scheitert, sollte zunächst überprüft werden, ob der richtige Brick und der richtige Port ausgewählt wurde und ob das Bricklet auch richtig angeschlossen ist.

Anstatt den Brick Viewer das jeweils neuste Plugin herunterladen zu lassen, kann auch "Custom..." als Plugin gewählt werden und dann die zu flashende Plugin als lokale Datei über den "Browse..." Knopf ausgewählt werden.

Darüber hinaus kann die UID des Bricklets ausgelesen und auch neu geschrieben werden. Die UID ist Base58 kodiert, die erlaubten Zeichen umfassen 0-9, a-z und A-Z ohne 0 (Null), I (groß i), O (groß o) und l (klein L). Die einzige weitere Einschränkung ist, dass die UIDs aller Bricklets eindeutig sind.

# Tests und implementation marvin
# Einführung
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

# Abschlussbericht

## Erreichte Ziele
Wir freuen uns, mitteilen zu können, dass wir alle unsere Ziele in diesem Projekt erreicht haben. Die Implementierung des Brainfuck Compilers und die Visualisierung auf der Embedded Hardware Tinkerforge (OLED Display) wurden erfolgreich abgeschlossen. Wir haben viel über Java, Brainfuck und systematische Abläufe beim Erstellen von Codes gelernt und sind an den Herausforderungen gewachsen.

## Schwierigkeiten
Einige Schwierigkeiten im Zeitmanagement bei der Programmierung in Java führten jedoch zu Verzögerungen in der Dokumentation des Projekts. Wir sind uns bewusst, dass wir uns besser und genauer auf den Projektauftrag konzentrieren müssen, um solche Schwierigkeiten zu vermeiden. Wir haben uns auch vorgenommen, das Projekt von Anfang an sorgfältiger zu dokumentieren, um besser auf dem Laufenden zu bleiben und eine effektive Projektdokumentation zu erstellen.

## Verbesserungsvorschläge
Für zukünftige Projekte empfehlen wir eine sorgfältige Einschätzung des Projekts und eine klare Definition der Ziele, um sicherzustellen, dass das Projekt reibungslos verläuft. Wir schlagen auch vor, regelmäßige Meetings und Überprüfungen des Fortschritts durchzuführen, um auf dem Laufenden zu bleiben und Verzögerungen zu minimieren.

## Schlussfolgerung

Zusammenfassend war dies ein erfolgreiches Projekt, das uns viel Wissen und Erfahrung gebracht hat. Wir sind stolz darauf, alle unsere Ziele erreicht zu haben und danken allen, die uns dabei unterstützt haben.

# Schlussteil

## Ausblick

Das erfolgreiche Abschließen dieses Projekts gibt uns die Möglichkeit, uns auf zukünftige Projekte zu freuen und zu planen. Wir haben in diesem Projekt viel gelernt und sind sicher, dass dieses Wissen uns bei zukünftigen Herausforderungen helfen wird. Wir planen, das Wissen und die Erfahrung, die wir in diesem Projekt gewonnen haben, in unseren zukünftigen Projekten anzuwenden und weiterzuentwickeln.

Wir werden auch weiterhin daran arbeiten, unsere Fähigkeiten zu verbessern und uns auf unsere individuellen Interessen und Stärken zu konzentrieren. Wir sind dankbar für die Chance, an diesem Projekt teilgenommen zu haben und freuen uns darauf, unser Wissen in zukünftigen Projekten anzuwenden. Besonders in der Programmiersprache Java erwarten wir weitere Projekte und sind mit diesen Erfahrungen im gepäck nun besser vorbereitet.

## Schlusswort

Wir möchten uns bei allen bedanken, die uns bei diesem Projekt unterstützt haben. Ein besonderer Dank geht an unser Team, das engagiert zusammengearbeitet hat, um dieses Projekt erfolgreich abzuschließen. Wir möchten auch unseren Betreuern und Lehrern danken, die uns während des Projekts unterstützt und inspiriert haben.

Dieses Projekt hat uns nicht nur gezeigt, wie wichtig eine sorgfältige Planung und Durchführung von Projekten ist, sondern auch, wie wichtig es ist, als Team zusammenzuarbeiten und sich gegenseitig zu unterstützen. Wir haben viel gelernt und sind stolz auf das, was wir erreicht haben.

Abschließend möchten wir sagen, dass wir uns auf zukünftige Projekte freuen und uns darauf konzentrieren werden, unser Wissen und unsere Fähigkeiten zu erweitern und zu verbessern. Wir sind dankbar für die Erfahrungen, die wir in diesem Projekt gemacht haben und freuen uns auf die Herausforderungen, die uns in Zukunft erwarten.


