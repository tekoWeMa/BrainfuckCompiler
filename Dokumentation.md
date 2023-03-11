# Teko schweizerische Fachhochschule
## L-TIN-21-T-a

### Brainfuck Compiler

TODO: Bild einfügen

Projektleiter: Mario Weilenmann, Marvin Huber

Dozent: Iwan Müeller

Datum: 18.03.2023


# Management Summary

Das Projektziel besteht darin, eine begleitende Projektdokumentation zu erstellen, die Implementierung der Brainfuck Programmiersprache durchzuführen und eine Visualisierung auf einem Embedded Hardware Tinkerforge (mit OLED Display) zu realisieren. Ein Teil des Projekts beinhaltet auch die Vertiefung der Kenntnisse in der Programmiersprache Java, indem ein Brainfuck-Compiler von Grund auf gebaut wird.

Das Projektteam setzt sich aus Mario Weilenmann und Marvin Huber zusammen. Mario wird sich auf die Entwicklung des Brainfuck-Compilers konzentrieren und dabei den Unterschied zwischen Compiler und Interpreter verstehen. Marvin wird sich auf den Aufbau unterschiedlicher Runtime-Umgebungen konzentrieren.

Der Kernaspekt des Projekts besteht darin, dass es den Aufbau der Programmierkenntnisse des Teams fördert. Durch die Zusammenarbeit und das gegenseitige Coaching bei der Entwicklung des Brainfuck-Compilers werden wir unser Verständnis für die Programmiersprache Java, die Brainfuck-Programmierung und die systematische Erstellung von Code vertiefen.

Das Projekt birgt auch Risiken, wie technische Schwierigkeiten, zeitliche Einschränkungen, mangelnde Zusammenarbeit, finanzielle Einschränkungen und fehlende Erfahrung. All diese Risiken könnten auftreten. Um diese Risiken zu minimieren, werden verschiedene Strategien eingesetzt, wie gründliche Vorbereitung und Forschung, realistische Zeitpläne, effektive Kommunikation und regelmässige Treffen sowie Schulung und Weiterbildung.

Das Projekt wurde erfolgreich abgeschlossen und wir sind mit dem Ergebnis zufrieden. Die Implementierung der Brainfuck-Programmiersprache und die Visualisierung auf dem Tinkerforge wurden erfolgreich umgesetzt und erfüllten unsere Erwartungen.

Insgesamt haben wir wertvolle Erfahrungen gesammelt und unsere Programmierkenntnisse erweitert. Wir empfehlen, die gewonnenen Erkenntnisse und Fähigkeiten in zukünftigen Projekten zu nutzen und weiterzuentwickeln.

# Inhaltsverzeichnis

- [Teko schweizerische Fachhochschule](#teko-schweizerische-fachhochschule)
  - [L-TIN-21-T-a](#l-tin-21-t-a)
    - [Brainfuck Compiler](#brainfuck-compiler)
- [Management Summary](#management-summary)
- [Inhaltsverzeichnis](#inhaltsverzeichnis)
- [Vorwort](#vorwort)
- [Initialisierungsphase](#initialisierungsphase)
  - [Ausgangslage](#ausgangslage)
  - [Projektauftrag](#projektauftrag)
    - [Zielsetzung](#zielsetzung)
      - [Ziele im Detail](#ziele-im-detail)
      - [Zusätzliche Ziele](#zusätzliche-ziele)
      - [Projektbeteiligte](#projektbeteiligte)
    - [Zusammenfassung](#zusammenfassung)
  - [Abgrenzungen](#abgrenzungen)
- [Risikoanalyse](#risikoanalyse)
  - [Risikomanagement Tabelle](#risikomanagement-tabelle)
- [Pflichtenheft](#pflichtenheft)
- [Projektplan](#projektplan)
- [Meilensteine](#meilensteine)
- [Projektstatusbericht](#projektstatusbericht)
- [Installationsanleitung](#installationsanleitung)
  - [Technische Dokumentation](#technische-dokumentation)
  - [Raspberry PI Einrichtung](#raspberry-pi-einrichtung)
  - [Raspberry Konfiguration](#raspberry-konfiguration)
  - [SSH einschalten](#ssh-einschalten)
  - [Statische IP vergeben](#statische-ip-vergeben)
- [Display HAT connector Setup](#display-hat-connector-setup)
  - [Brick Hat](#brick-hat)
  - [Features](#features)
  - [Beschreibung](#beschreibung)
  - [Ressourcen](#ressourcen)
  - [Erste Schritte](#erste-schritte)
    - [Interface](#interface)
  - [Installation Tinkerforge software](#installation-tinkerforge-software)
    - [Brick Daemon (brickd)](#brick-daemon-brickd)
  - [Installation auf Raspberry PI OS](#installation-auf-raspberry-pi-os)
  - [Einrichtung](#einrichtung)
  - [Pakete](#pakete)
  - [Übersicht Brick Viewer](#übersicht-brick-viewer)
  - [Verwendung](#verwendung)
  - [Updates](#updates)
  - [Aktuellen Stand bestimmen / Nach Updates suchen](#aktuellen-stand-bestimmen--nach-updates-suchen)
- [Interpreter und Compiler](#interpreter-und-compiler)
- [Einführung](#einführung)
- [Implementation mit Java](#implementation-mit-java)
    - [Einlesen des Brainfuck-Codes aus einer Datei](#einlesen-des-brainfuck-codes-aus-einer-datei)
    - [Speichern der Opcodes](#speichern-der-opcodes)
    - [Behandlung von Schleifen](#behandlung-von-schleifen)
    - [Ausführen des Brainfuck-Codes](#ausführen-des-brainfuck-codes)
    - [Behandlung von Fehlern](#behandlung-von-fehlern)
    - [Klasse `BracketPair`](#klasse-bracketpair)
    - [Enumeration `OpcodeEnum`](#enumeration-opcodeenum)
- [Tests und implementation marvin](#tests-und-implementation-marvin)
- [Abschlussbericht](#abschlussbericht)
  - [Erreichte Ziele](#erreichte-ziele)
  - [Schwierigkeiten](#schwierigkeiten)
  - [Verbesserungsvorschläge](#verbesserungsvorschläge)
  - [Schlussfolgerung](#schlussfolgerung)
- [Schlussteil](#schlussteil)
  - [Ausblick](#ausblick)
  - [Schlusswort](#schlusswort)
- [Anhang](#anhang)

# Vorwort

Wir haben uns für das Thema entschieden, einen Brainfuck-Compiler zu schreiben, da es für uns eine faszinierende Herausforderung darstellt. Brainfuck ist eine extrem simple, aber auch sehr abstrakte Programmiersprache, die lediglich aus acht Befehlen besteht. Aufgrund ihrer minimalistischen Natur ist es sehr schwierig, Brainfuck-Code zu lesen und zu schreiben.

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

Ddas Wissen und die Fähigkeiten, die während der Projektarbeit erworben werden, sind von unschätzbarem Wert für zukünftige Projekte und Karrieremöglichkeiten in der Softwareentwicklung und hat grosses potential in der Richtung Java.

## Projektauftrag

Projektauftrag: Erstellung einer Projektdokumentation, Implementierung von Brainfuck Programmiersprache und Visualisierung an Embedded Hardware Tinkerforge.

### Zielsetzung

Dieses Projekt zielt darauf ab, eine begleitende Projektdokumentation zu erstellen, die die Entwicklung und Implementierung eines Brainfuck Compilers umfasst. Das Ziel besteht darin, die Programmiersprache Brainfuck zu implementieren und diese auf einer Embedded Hardware Tinkerforge (OLED Display) zu visualisieren. Ein Teil des Projekts beinhaltet auch, dass wir uns gegenseitig beraten und unterstützen, um unser Wissen in Java, Brainfuck und systematischen Abläufen beim Erstellen von Codes zu vertiefen.

#### Ziele im Detail

1. Erstellung einer begleitenden Projektdokumentation: Es wird eine detaillierte Projektdokumentation erstellt, die den Entwicklungsprozess, die Implementierung und die Ergebnisse des Projekts beschreibt. Die Dokumentation umfasst auch Anweisungen und Anleitungen für die Implementierung des Brainfuck Compilers und die Visualisierung der Programmiersprache auf der Embedded Hardware Tinkerforge.

2. Implementierung von Brainfuck Programmiersprache: Ein wesentliches Ziel des Projekts besteht darin, die Programmiersprache Brainfuck zu implementieren. Dies beinhaltet die Entwicklung eines Brainfuck Compilers von Grund auf, um sicherzustellen, dass das Verständnis für Java und Brainfuck vertieft wird. Wir werden auch sicherstellen, dass wir die Unterschiede zwischen Compiler und Interpreter verstehen und in der Lage sind, diese zu erklären.

3. Visualisierung an Embedded Hardware Tinkerforge: Ein weiteres Ziel des Projekts ist es, die Brainfuck Programmiersprache auf einer Embedded Hardware wie Tinkerforge zu visualisieren. Dies beinhaltet die Entwicklung einer Runtime-Umgebung, um sicherzustellen, dass die Programmiersprache auf der Hardware effektiv und effizient dargestellt wird. Marvin wird sich auf die Entwicklung von verschiedenen Runtime-Umgebungen konzentrieren, um sicherzustellen, dass die Visualisierung der Programmiersprache auf der Hardware optimal abläuft.

#### Zusätzliche Ziele

1. Vertiefung des Verständnisses von Java: Die Entwicklung des Brainfuck Compilers von Grund auf bietet eine hervorragende Gelegenheit, unser Verständnis von Java zu vertiefen. Wir werden sicherstellen, dass wir ein tiefes Verständnis der Programmiersprache Java haben für unseren Zweck und in der Lage sind, effektiv damit zu arbeiten.

2. Vertiefung des Verständnisses von Brainfuck: Mit der Implementierung können wir unser Verständnis von Brainfuck vertiefen. Dies ist notwendig, um dem Compiler zu schreiben.

3. Entwicklung von systematischen Abläufen: Ein wichtiger Teil des Projekts ist die Entwicklung von systematischen Abläufen beim Erstellen von Codes. Wir werden sicherstellen, dass wir die besten Praktiken bei der Entwicklung von Codes einsetzen, um die Qualität unserer Arbeit zu verbessern.

4. Verbesserung der Zusammenarbeit: Ein weiteres Ziel des Projekts besteht darin, unsere Zusammenarbeit zu verbessern. Wir werden uns gegenseitig beraten und unterstützen, um sicherzustellen, dass jeder von uns das Projekt erfolgreich abschliessen kann. Wir werden auch sicherstellen, dass wir effektive Kommunikationswege benutzen, um sicherzustellen, dass wir uns während des gesamten Projekts auf dem gleichen Stand halten und effizient arbeiten können.

5. Verbesserung der technischen Fähigkeiten: Dieses Projekt bietet uns eine gute Gelegenheit, unsere technischen Fähigkeiten zu verbessern. Wir werden viel mit Brainfuck, java und Tinkerforge arbeiten und uns tief in die Materie einarbeiten müssen. Wir werden dabei viel neues dazulernen.

#### Projektbeteiligte

Mario Weilenmann: Mario ist verantwortlich für die Entwicklung des Brainfuck Compilers und die Implementierung der Programmiersprache auf der Embedded Hardware Tinkerforge (OLED Display).

Marvin Huber: Marvin wird sich auf die Entwicklung von verschiedenen Runtime-Umgebungen konzentrieren, um sicherzustellen, dass die Visualisierung der Programmiersprache auf der Embedded Hardware Tinkerforge (OLED Display) optimal ist. Er wird auch Mario bei der Entwicklung des Brainfuck Compilers unterstützen und sicherstellen, dass der Code effektiv und effizient implementiert wird.

### Zusammenfassung

Insgesamt zielt dieses Projekt darauf ab, eine begleitende Projektdokumentation zu erstellen, die die Entwicklung und Implementierung eines Brainfuck Compilers umfasst. Wir werden sicherstellen, dass wir ein tiefes Verständnis von Java, Brainfuck und systematischen Abläufen beim Erstellen von Codes haben. Wir werden auch sicherstellen, dass die Brainfuck Programmiersprache auf der Hardware Tinkerforge  visualisiert wird. Damit können wir unsere Programmier-fähigkeiten verbessern und lernen, besser zusammen zu arbeiten. Wir sind zuversichtlich, dass wir das Projekt erfolgreich abschliessen werden und die gesteckten Ziele erreichen werden.

## Abgrenzungen

Das Projekt, das von uns durchgeführt wird, hat klare Abgrenzungen hinsichtlich seines Umfangs und seiner Zielsetzungen. Eines dieser Ziele ist die Erlernung grundlegender Programmier-Methodiken. Dies bezieht sich auf die Konzepte und Techniken, die in der Programmierung verwendet werden, um effektiv und effizient zu arbeiten.

Wir werden in diesem Projekt grundlegende Programmierkonzepte wie Variablen, Schleifen, Bedingungen und Funktionen kennenlernen sowie der Unterschied zwischen Compiler und Interpreter und auf verschiedenen Runtime umgebungen arbeiten. Diese Konzepte sind von grundlegender Bedeutung für jede Programmiersprache und bilden die Grundlage für komplexe Programme. Indem wir diese Konzepte erlernen und anwenden, können wir unsere Fähigkeiten im Bereich der Programmierung verbessern.

Es ist jedoch wichtig zu betonen, dass das Projekt nicht den Anspruch hat, zur Produktionsreife zu gelangen. Das bedeutet, dass das Ziel des Projekts nicht darin besteht, ein voll funktionsfähiges Produkt zu entwickeln, das von anderen genutzt werden kann. Stattdessen soll uns das Projekt die Möglichkeit geben, grundlegende Konzepte der Programmierung zu erlernen und anzuwenden und uns iJava-programming voran zu bringen.

# Risikoanalyse

Eine Risikoanalyse ist eine wichtige Komponente bei der Planung eines Projekts, um potenzielle Risiken zu identifizieren und Strategien zu entwickeln, um diese Risiken zu minimieren oder zu vermeiden. Im Folgenden sind einige Risiken aufgeführt, die bei der Entwicklung des Brainfuck Compilers und der Visualisierung der Programmiersprache auf der Embedded Hardware Tinkerforge (OLED Display) auftreten könnten:

1. Technische Schwierigkeiten: Das Projekt erfordert ein gewisses Verständnis von Java, Brainfuck und Tinkerforge. Es besteht das Risiko, dass technische Schwierigkeiten auftreten könnten, die das Projekt verzögern oder sogar unmöglich machen können. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir eine gründliche Recherche betreiben und Vorbereitung durchführen und dass wir in der Lage sind, die technischen Herausforderungen effektiv zu bewältigen.

2. Zeitliche Einschränkungen: Das Projekt hat einen relativ kleinen Zeitrahmen, innerhalb dessen das Projekt abgeschlossen werden muss. Es besteht das Risiko, dass wir aufgrund von unvorhergesehenen Schwierigkeiten oder Komplikationen den Zeitrahmen nicht einhalten können. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir realistische Zeitpläne erstellen und dass wir unser Bestes tun, um innerhalb dieser Zeitpläne zu arbeiten.

3. Mangelnde Zusammenarbeit: Das Projekt erfordert eine enge Zusammenarbeit zwischen den Projektbeteiligten. Es besteht das Risiko, dass wir nicht effektiv zusammenarbeiten können, was zu Verzögerungen oder Problemen im Projekt führen kann. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir effektive Kommunikationswege etablieren und dass wir uns regelmässig treffen, (fast jedes Wochenende) um den Fortschritt des Projekts zu besprechen.

4. Finanzielle Einschränkungen: Das Projekt erfordert finanzielle Ressourcen für die Beschaffung von Materialien. Es besteht das Risiko, dass das Projekt aufgrund von finanziellen Einschränkungen gestoppt oder verzögert wird. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir realistische Budgets erstellen und dass wir alternative Finanzierungsoptionen prüfen, falls nötig.

5. Fehlende Erfahrung: Es besteht das Risiko, dass wir möglicherweise nicht über ausreichende Erfahrung in der Programmierung oder Implementierung von Codes verfügen, um das Projekt erfolgreich abzuschliessen. Um dieses Risiko zu minimieren, werden wir sicherstellen, dass wir uns gegenseitig unterstützen und dass wir mit Selbststudium und Recherchieren an die geünschten Informationen kommen.

Zusammenfassend kann gesagt werden, dass das Projekt einige Risiken birgt. Wir werden jedoch sicherstellen, dass wir diese Risiken im Auge behalten und dass wir Strategien entwickeln, um diese Risiken zu minimieren oder zu vermeiden. Wir sind zuversichtlich, dass wir das Projekt erfolgreich abschliessen werden und dass wir die gesteckten Meilensteine erreichen werden.

## Risikomanagement Tabelle

| Risiko                     | Eintreffwahrscheinlichkeit | Schweregrad | Strategie zur Risikominimierung |
|----------------------------|----------------------------|-------------|--------------------------------|
| Technische Schwierigkeiten | Mittel                     | Leicht-Mittel        | Gründliche Vorbereitung und Forschung, technische Expertise nutzen, um Herausforderungen effektiv zu bewältigen |
| Zeitliche Einschränkungen  | Hoch                       | Leicht      | Realistische Zeitpläne erstellen, Priorisierung der Aufgaben, um sicherzustellen, dass das Projekt innerhalb des Zeitrahmens abgeschlossen wird |
| Mangelnde Zusammenarbeit   | Leicht                     | Mittel      | Effektive Kommunikation und regelmässige Treffen, um sicherzustellen, dass das Team zusammenarbeitet und Schwierigkeiten frühzeitig erkannt und gelöst werden |
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

1. Konzeption (Benötigte Komponenten, Aufbau, Vorgehen)  
2. Versuchsaufbau mit Tinkerforge (Red Brick, OLED Display)
3. Programmierung von Interpreter und Compilier
(Auslesung und Speicherung der Daten)
4. Entwicklung der Darstellung von Output
5. (Visualisierung der Daten)
6. Finalisierung der Dokumentation

# Meilensteine

| Meilensteine                                              | Ziel der Fertigstellung | Fertiggestellt am |
| --------------------------------------------------------- | ----------------------- | ----------------- |
| Konzeption (Benötigte Komponenten, Aufbau, Vorgehen)       | bis 11.12.2022          | 11.12.2022        |
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

# Display HAT connector Setup

## Brick Hat

## Features

- Raspberry Pi HAT im Standard-HAT-Formfaktor
- **Acht** Anschlüsse für Bricklets
- Integrierte 5,3V Stromversorgung (6V-28V Eingang, bis zu 4A)
- Misst USB- und DC-Spannungsversorgung
- Bietet eine Real-Time Clock für den Raspberry Pi
- Bietet Schlafmodus (Low Power) und Watchdog

## Beschreibung

Der HAT Brick ist ein [Raspberry Pi HAT](https://www.raspberrypi.org/blog/introducing-raspberry-pi-hats/) im Standard-HAT-Formfaktor. Der Brick ist zur HAT-Spezifikation konform und funktioniert automatisch und ohne Änderungen mit Raspbian.

Mit dem HAT Brick können bis zu **acht** [Bricklets](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricklets) an ein Raspberry Pi angeschlossen werden.

Note: Der HAT Brick besitzt 7-Pol-Bricklet-Anschlüsse. Über ein 7-Pol- <-> 7-Pol-Kabel können Bricklets an den Brick angeschlossen werden. Es werden nur Bricklets unterstützt, die über einen 7-poligen Anschluss verfügen.

Der Raspberry Pi kann über den HAT Brick mit einer externen 6V-28V DC Stromversorgung betrieben werden. Die integrierte Stromversorgung liefert auch unter grosser Last stabile 5V für den Raspberry Pi. Somit können auch angeschlossene Bricklets und verbundene USB-Geräte versorgt werden. Das HAT Brick liefert hierfür eine etwas erhöhte Spannung von 5,3V.

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

- Schaltplan ([Download](https://github.com/Tinkerforge/hat-brick/raw/master/hardware/hat-schematic.pdf))
- Umriss und Bohrplan ([Download](https://www.tinkerforge.com/de/doc/_images/Dimensions/hat_brick_dimensions.png))
- Quelltexte und Platinenlayout ([Download](https://github.com/Tinkerforge/hat-brick/zipball/master))
- 3D Modell ([Online ansehen](https://autode.sk/2XiDCDT) | Download: [STEP](https://download.tinkerforge.com/3d/bricks/hat/hat.step), [FreeCAD](https://download.tinkerforge.com/3d/bricks/hat/hat.FCStd))

## Erste Schritte

![](res/Pasted%20image%2020230217121831.jpg)

Um den HAT Brick verwenden zu können, muss zuerst der [Brick Daemon](https://www.tinkerforge.com/de/doc/Software/Brickd.html#brickd) auf dem Raspberry Pi installiert werden. Der Brick Daemon agiert als Proxy zwischen den Brickletanschlüssen des HAT Brickss und den API Bindings. Er kümmert sich auch um die Real-Time Clock.

### Interface

Es wird ein Interface verwendet mit dem Namen "Brick Viewer" für eine visuelle veranschaulichung.
Der Brick Viewer kann entweder direkt auf dem Raspberry Pi oder auf einem externen PC, der über Ethernet oder WLAN Zugriff auf den Raspberry Pi besitzt, installiert werden. Von einem externen PC aus muss sich auf den Hostnamen oder die IP des Raspberry Pis verbunden werden, vom Raspberry Pi aus auf localhost.
Wir haben uns entschieden, die Installation direkt auf dem Raspberry Pi durchzuführen, um aus Gründen der Einfachheit bei einem Gerät zu bleiben.

![](res/Pasted%20image%2020230217122052.jpg)

## Installation Tinkerforge software

### Brick Daemon (brickd)

Der Brick Daemon ist ein Daemon (bzw. Service für Windows) der als eine Brücke zwischen [Bricks](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricks)/[Bricklets](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricklets) und den [API Bindings](https://www.tinkerforge.com/de/doc/Software/API_Bindings.html#api-bindings) für die verschiedenen Programmiersprachen fungiert.

Der Daemon leitet Daten zwischen der USB Verbindung und den TCP/IP Sockets hin und her. Bei der Benutzung der API Bindings wird eine TCP/IP Verbindung zum Brick Daemon hergestellt. Dieses Konzept erlaubt es Bindings für nahezu jede Programmiersprache ohne Abhängigkeiten zu erstellen. Dadurch ist es möglich Bricks und Bricklets über eingebettete Geräte wie Smartphones zu programmieren, die nur spezifische Programmiersprachen unterstützten.

Zusätzlich ist es möglich den PC auf dem der Brick Daemon läuft von dem PC auf dem der Benutzercode läuft zu trennen. Dadurch ist das Steuern über ein Smartphone oder auch über das Internet möglich.

## Installation auf Raspberry PI OS

Die auf der [Download Seite](https://www.tinkerforge.com/de/doc/Downloads.html#downloads) verfügbare Software steht auch als Debian Pakete in unserem [APT Repository](https://download.tinkerforge.com/apt/) zur Installation bereit.

Aktuell werden folgende Distributionen und Architekturen unterstützt:

- [Debian](https://www.debian.org/): amd64, i386, armhf, arm64
- [Ubuntu](https://ubuntu.com/): amd64, i386, armhf, arm64
- [Raspberry Pi OS](https://www.raspberrypi.org/downloads/raspberry-pi-os/) (ehemals Raspbian): armhf

## Einrichtung

**Schritt 1:** Öffentlichen GPG Schlüssel importieren:

`wget https://download.tinkerforge.com/apt/$(. /etc/os-release; echo $ID)/tinkerforge.gpg -q -O - | sudo tee /etc/apt/trusted.gpg.d/tinkerforge.gpg > /dev/null`

**Schritt 2:** APT Repository hinzufügen:

`echo "deb https://download.tinkerforge.com/apt/$(. /etc/os-release; echo $ID $VERSION_CODENAME) main" | sudo tee /etc/apt/sources.list.d/tinkerforge.list`

**Schritt 3:** APT Paketliste aktualisieren:

`sudo apt update`

## Pakete

Aktuell sind folgende Pakete verfügbar:

- Tools
  - [Brick Daemon](https://www.tinkerforge.com/de/doc/Software/Brickd.html#brickd): `brickd`
  - [Brick Viewer](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv): `brickv`
  - [Brick Flash](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brick-flash): `brick-flash`
- API Bindings
  - [Go](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Go.html#api-bindings-go): `golang-tinkerforge-dev`
  - [Java](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Java.html#api-bindings-java): `libtinkerforge-java` und `libtinkerforge-java-doc`
  - [JavaScript (Node.js)](https://www.tinkerforge.com/de/doc/Software/API_Bindings_JavaScript.html#api-bindings-javascript): `node-tinkerforge`
  - JSON: `tinkerforge-json`
  - [MQTT](https://www.tinkerforge.com/de/doc/Software/API_Bindings_MQTT.html#api-bindings-mqtt): `tinkerforge-mqtt`
  - [Octave](https://www.tinkerforge.com/de/doc/Software/API_Bindings_MATLAB.html#api-bindings-matlab): `octave-tinkerforge`
  - [Perl](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Perl.html#api-bindings-perl): `libtinkerforge-perl`
  - [PHP](https://www.tinkerforge.com/de/doc/Software/API_Bindings_PHP.html#api-bindings-php): `php-tinkerforge`
  - [Python](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Python.html#api-bindings-python): `python3-tinkerforge` (Python 3) und `python-tinkerforge` (Python 2)
  - [Ruby](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Perl.html#api-bindings-perl): `ruby-tinkerforge`
  - [Shell](https://www.tinkerforge.com/de/doc/Software/API_Bindings_Shell.html#api-bindings-shell): `tinkerforge-shell`

## Übersicht Brick Viewer

Der Brick Viewer bietet eine graphische Oberfläche um [Bricks](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricks) und [Bricklets](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricklets) zu testen. Jedes Gerät hat seine eigenen Tab der die Hauptfunktionen abbildet und erlaubt diese zu steuern.

Darüber hinaus kann der Brick Viewer verwendet werden, um den Analog-Digital-Wandler der Bricks zu [kalibrieren](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-adc-calibration) und so deren Messqualität zu verbessern, und um [Brick Firmwares](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-flash-brick-firmware) und [Bricklet Plugins](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-flash-bricklet-plugin) zu flashen.

## Verwendung

Zuerst muss der Brick Viewer mit dem [Brick Daemon](https://www.tinkerforge.com/de/doc/Software/Brickd.html#brickd) oder z.B. einer [WIFI Extension](https://www.tinkerforge.com/de/doc/Hardware/Master_Extensions/WIFI_Extension.html#wifi-extension) verbunden werden. Dabei kann der Brick Daemon auf dem gleichen oder einem anderen PC als der Brick Viewer laufen. Dazu zuerst die IP Adresse des PCs auf dem der Brick Daemons läuft oder die IP Adresse einer WIFI Extension als Host angeben. Falls Brick Daemon und Viewer auf dem gleichen PC laufen kann der Standardwert `localhost` beibehalten werden. Nach einem Klick auf den "Connect" Knopf werden die verbunden Bricks und Bricklets auf je einem eigenen Tab angezeigt und können getestet werden. Da wir beides auf dem Raspberry PI installiert haben, verbinden wir Brick Viewer über Localhost.

![](doc/res/Pasted%20image%2020230311191838.png)

Nun ist die Verbindung zum Display hergestellt und wir können weiterfahren.

## Updates

Ein Klick auf den "Updates / Flashing" öffnen einen Dialog mit Informationen über verfügbare Updates und der Möglichkeit Bricks und Bricklets neu zu flashen. Der "Advanced Functions" Knopf öffnet einen Dialog zur Kalibrierung des Analog-Digital-Wandler eines Bricks.

## Aktuellen Stand bestimmen / Nach Updates suchen

Nach dem Start des Brick Viewers und dem Verbinden zu einem Brick Daemon oder einer Master Extension kann überprüft werden ob eine neuere Software für die angeschlossenen Geräte verfügbar ist.

Hierzu muss auf "Updates / Flashing" geklickt werden. Der Dialog zeigt die angeschlossenen Geräte und deren Software stand. Orange unterlegte Einträge können geupdatet werden. Rot unterlegte Einträge müssen geupdatet werden damit sie korrekt funktionieren.

![](res/Pasted%20image%2020230217121414.jpg)

Der Dialog ermöglicht es alle Bricklets gleichzeitig über den Knopf "Auto-Update All Bricklets" auf die neuste Softwareversion zu bringen. Bricks können nicht automatisch auf den neusten Stand gebracht werden (siehe [Brick Firmware Flashing](https://www.tinkerforge.com/de/doc/Software/Brickv.html#brickv-flash-brick-firmware)).

# Interpreter und Compiler

Ein Compiler und ein Interpreter sind zwei Arten von Programmen, die für die Ausführung von Code verwendet werden können. Beide sind für die Umwandlung von Programmiersprache in ausführbaren Code verantwortlich, jedoch auf unterschiedliche Weise.

Ein Compiler übersetzt den gesamten Quellcode eines Programms in eine ausführbare Datei, die von einem Computer oder Gerät direkt ausgeführt werden kann. Der Compiler prüft dabei den Quellcode auf Syntax- und Semantikfehler, wandelt den Code in eine Zwischensprache um und optimiert den Code für die Zielplattform. Das Ergebnis ist eine Datei, die schnell und effizient ausgeführt werden kann. Beispiele für Compiler sind der GCC-Compiler für C und C++, der Java-Compiler für Java und der Swift-Compiler für Swift.

Ein Interpreter hingegen liest und interpretiert den Quellcode zur Laufzeit, Zeile für Zeile. Der Interpreter wandelt dabei den Quellcode in ausführbaren Code um, ohne eine ausführbare Datei zu erstellen. Der Interpreter prüft dabei ebenfalls auf Syntax- und Semantikfehler und führt den Code sofort aus. Beispiele für Interpreter sind der Python-Interpreter für Python, der Ruby-Interpreter für Ruby und der JavaScript-Interpreter für JavaScript.

Der grösste Unterschied zwischen einem Compiler und einem Interpreter besteht darin, wie sie den Code ausführen. Ein Compiler übersetzt den gesamten Quellcode in ausführbaren Code, bevor das Programm ausgeführt wird, während ein Interpreter den Code Zeile für Zeile interpretiert und ausführt. Ein Compiler erfordert somit mehr Zeit für die Übersetzung, bevor das Programm ausgeführt werden kann, während ein Interpreter sofort ausführen kann, sobald der Code eingegeben wurde. Dies führt zu unterschiedlicher Leistung und Effizienz, wobei Compiler in der Regel schneller und effizienter sind als Interpreter.

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

# Implementation mit Java

Es gibt einige wichtige Code-Ausschnitte, die wie folgt beschrieben werden können:

### Einlesen des Brainfuck-Codes aus einer Datei

In diesem Abschnitt wird der Dateipfad zur Textdatei festgelegt, die den Brainfuck-Code enthält. Mit der Methode `Files.readString` wird der Inhalt der Datei in einen String gespeichert.
![](doc/res/Pasted%20image%2020230311194631.png)

### Speichern der Opcodes

In diesem Abschnitt wird eine Liste erstellt, die die Opcodes des Brainfuck-Codes enthält. Dabei wird jede Zeichenfolge in der Brainfuck-Syntax in eine der acht Opcodes übersetzt. Diese werden in der `ArrayList` mit dem Namen `EnumList` gespeichert.
![](doc/res/Pasted%20image%2020230311195020.png)

### Behandlung von Schleifen

Dieser Abschnitt behandelt die Schleifen in Brainfuck. Hierfür wird eine `Stack`-Datenstruktur verwendet, um die Positionen der öffnenden Klammern in der `ArrayList` `EnumList` zu speichern. Wenn eine schliessende Klammer gefunden wird, wird die Position des passenden öffnenden Klammerns aus dem Stack abgerufen und ein neues `BracketPair`-Objekt erstellt, das die beiden Positionen speichert.
![](doc/res/Pasted%20image%2020230311195232.png)
  
### Ausführen des Brainfuck-Codes

Dieser Abschnitt führt den Brainfuck-Code aus, indem er jedes Opcode-Element in der `ArrayList` `EnumList` abruft und die entsprechenden Anweisungen ausführt. Die Anweisungen sind das Inkrementieren oder Dekrementieren des Zeigers, das Erhöhen oder Verringern des Wertes im Speicher, das Drucken oder Einlesen von Werten und die Verarbeitung von Schleifen.
![](doc/res/Pasted%20image%2020230311195318.png)

### Behandlung von Fehlern

Dieser Abschnitt behandelt Fehler, die während der Übersetzung oder Ausführung des Brainfuck-Codes auftreten können. Wenn beispielsweise eine schliesende Klammer ohne eine entsprechende öffnende Klammer gefunden wird, wird die Position des Fehlers ausgegeben. Ebenso wird eine Warnung ausgegeben, wenn eine öffnende Klammer gefunden wird, für die es keine passende schliesende Klammer gibt.
![](doc/res/Pasted%20image%2020230311195417.png)

### Klasse `BracketPair`

Dies ist eine einfache Klasse, die ein Paar von Klammern darstellt. Sie speichert die Positionen der öffnenden und schliessenden Klammern in der `ArrayList` `EnumList`.
![](doc/res/Pasted%20image%2020230311195443.png)

### Enumeration `OpcodeEnum`

Dies ist eine Enumeration, die die acht Opcodes des Brainfuck-Codes definiert. Sie wird verwendet, um die Opcodes in der `ArrayList` `EnumList` zu speichern.
![](doc/res/Pasted%20image%2020230311195457.png)

# Tests und implementation marvin

# Abschlussbericht

## Erreichte Ziele

Wir freuen uns, mitteilen zu können, dass wir alle unsere Ziele in diesem Projekt erreicht haben. Die Implementierung des Brainfuck Compilers und die Visualisierung auf der Embedded Hardware Tinkerforge wurden erfolgreich abgeschlossen. Wir haben viel über Java, Brainfuck und systematische Abläufe beim Erstellen von Codes gelernt und sind an den Herausforderungen gewachsen.

## Schwierigkeiten

Einige Schwierigkeiten im Zeitmanagement bei der Programmierung in Java führten jedoch zu Verzögerungen in der Dokumentation des Projekts. Wir sind uns bewusst, dass wir uns besser und genauer auf den Projektauftrag konzentrieren müssen, um solche Schwierigkeiten zu vermeiden. Wir haben uns auch vorgenommen, das Projekt von Anfang an sorgfältiger zu dokumentieren, um besser auf dem Laufenden zu bleiben und eine effektive Projektdokumentation zu erstellen.

## Verbesserungsvorschläge

Für zukünftige Projekte empfehlen wir eine sorgfältige Einschätzung des Projekts und eine klare Definition der Ziele, um sicherzustellen, dass das Projekt reibungslos verläuft. Wir schlagen auch vor, regelmässige Meetings und Überprüfungen des Fortschritts durchzuführen, um auf dem Laufenden zu bleiben und Verzögerungen zu minimieren.

## Schlussfolgerung

Zusammenfassend war dies ein erfolgreiches Projekt, das uns viel Wissen und Erfahrung gebracht hat. Wir sind stolz darauf, alle unsere Ziele erreicht zu haben und danken allen, die uns dabei unterstützt haben.

# Schlussteil

## Ausblick

Das erfolgreiche Abschliessen dieses Projekts gibt uns die Möglichkeit, uns auf zukünftige Projekte zu freuen und zu planen. Wir haben in diesem Projekt viel gelernt und sind sicher, dass dieses Wissen uns bei zukünftigen Herausforderungen helfen wird. Wir planen, das Wissen und die Erfahrung, die wir in diesem Projekt gewonnen haben, in unseren zukünftigen Projekten anzuwenden und weiterzuentwickeln.

Wir werden auch weiterhin daran arbeiten, unsere Fähigkeiten zu verbessern und uns auf unsere individuellen Interessen und Stärken zu konzentrieren. Wir sind dankbar für die Chance, an diesem Projekt teilgenommen zu haben und freuen uns darauf, unser Wissen in zukünftigen Projekten anzuwenden. Besonders in der Programmiersprache Java erwarten wir weitere Projekte und sind mit diesen Erfahrungen im gepäck nun besser vorbereitet.

## Schlusswort

Wir möchten uns bei allen bedanken, die uns bei diesem Projekt unterstützt haben. Ein besonderer Dank geht an unser Team, das engagiert zusammengearbeitet hat, um dieses Projekt erfolgreich abzuschliessen. Wir möchten auch unseren Betreuern und Lehrern danken, die uns während des Projekts unterstützt und inspiriert haben.

Dieses Projekt hat uns nicht nur gezeigt, wie wichtig eine sorgfältige Planung und Durchführung von Projekten ist, sondern auch, wie wichtig es ist, als Team zusammenzuarbeiten und sich gegenseitig zu unterstützen. Wir haben viel gelernt und sind stolz auf das, was wir erreicht haben.

Abschliessend möchten wir sagen, dass wir uns auf zukünftige Projekte freuen und uns darauf konzentrieren werden, unser Wissen und unsere Fähigkeiten zu erweitern und zu verbessern. Wir sind dankbar für die Erfahrungen, die wir in diesem Projekt gemacht haben und freuen uns auf die Herausforderungen, die uns in Zukunft erwarten.

# Anhang


Orientation Dokumentation Tinkerforge HAT: https://www.tinkerforge.com/en/


