# Aufbau des Projekts
Das Projekt ist in 3 Komponten gegliedert ein mal das Viewer, BF und den BrainfuckCompiler.

## Viewer
Das Viewer-Projekt ist eine Software, die speziell dafür entwickelt wurde, um Text auf dem OLED-Display darzustellen. Es ist ein beliebtes Display-Format für kleine elektronische Geräte wie Smartwatches oder Fitness-Tracker.

Die Texte, die auf dem OLED-Display dargestellt werden sollen, werden von den beiden anderen Projekten generiert: BF und BrainfuckCompiler.

Das Viewer-Projekt fungiert als Vermittler zwischen den beiden anderen Projekten und dem OLED-Display. Sobald die Texte von BF oder BrainfuckCompiler generiert wurden, können die ans Viewer-Projekt gesendet werden. Das Viewer-Projekt nimmt diese Texte entgegen, dass sie auf dem OLED-Display dargestellt werden können.

Das Viewer-Projekt verwendet dabei eine spezielle Programmierschnittstelle (API), um mit dem OLED-Display zu kommunizieren. Diese API ermöglicht es dem Viewer-Projekt, den Text auf dem Display anzuzeigen, indem es die richtigen Befehle an das Display sendet.

Insgesamt ist das Viewer-Projekt eine wichtige Komponente in diesem System, da es die Texte von BF und BrainfuckCompiler auf dem OLED-Display darstellt und so den Entwicklern eine einfache Möglichkeit bietet, ihre Algorithmen zu testen und zu debuggen.

TODO: insert screenshot

## bf
Das Projekt nennt sich "Brainfuck Transpiler". Es ist eine Anwendung, die geschrieben wurde, um Brainfuck-Code in C- und Rust-Code umzuwandeln. Der Zweck dieser Anwendung ist es, Brainfuck-Code in eine höhere Programmiersprache zu übersetzen, die einfacher zu lesen und zu verstehen ist.

Die Anwendung besteht aus drei Hauptkomponenten:

Tokenizer: Der Tokenizer ist für das Aufteilen des Brainfuck-Codes in Tokens zuständig. Ein Token ist eine Art von Textelement, das eine spezielle Bedeutung hat. Der Tokenizer durchsucht den Brainfuck-Code und identifiziert jedes Token. Jedes Token wird dann an den Parser weitergegeben.

Optimizer: Der Optimzier sorgt daf

Pipeline: Der Parser ist für die Umwandlung der Tokens in C- oder Rust-Code zuständig. Der Parser liest die Tokens, die vom Lexer erzeugt wurden, und übersetzt sie in eine höhere Programmiersprache. Der Parser erzeugt dann eine C- oder Rust-Datei, die den übersetzten Code enthält.

Transpiler: Der Transpiler ist das Kernstück der Anwendung. Der Transpiler ruft sowohl den Lexer als auch den Parser auf und koordiniert ihre Arbeit. Der Transpiler liest den Brainfuck-Code ein und übergibt ihn an den Lexer. Der Lexer erzeugt dann Tokens, die vom Parser verarbeitet werden. Der Parser übersetzt die Tokens in C- oder Rust-Code, der dann in eine Datei geschrieben wird.

Das Ergebnis des Projekts ist eine C- oder Rust-Datei, die den übersetzten Brainfuck-Code enthält. Diese Datei kann dann in eine ausführbare Datei kompiliert werden und auf einer beliebigen Plattform ausgeführt werden.

Dieses Projekt kann Entwicklern helfen, Brainfuck-Code auf eine höhere Programmiersprache zu übersetzen und so das Debugging und die Wartung von Brainfuck-Code zu vereinfachen.

### Tokenizer
### Pipeline
### Backends
#### VM
#### C
#### Rust
### IR
Die IR ist eine abstrakte Darstellung des Quellcodes, die unabhängig von einer bestimmten Programmiersprache ist und in der Regel in einer einfachen und standardisierten Form vorliegt. Sie wird verwendet, um den Quellcode auf semantische Eigenschaften zu analysieren und zu optimieren, bevor er in Maschinencode übersetzt wird.

Die Verwendung von IR erleichtert es auch, verschiedene Optimierungstechniken auf den Code anzuwenden, ohne dass dabei die eigentliche Programmiersprache berücksichtigt werden muss. Auf diese Weise kann der Compiler oder das Programmierwerkzeug eine optimierte Version des Codes generieren, die schneller und effizienter ausgeführt werden kann.

### IR Code
```rust
pub enum Expression {
    IncVal(u8),
    DecVal(u8),
    IncPtr(usize),
    DecPtr(usize),
    MulVal(isize, u8),
    Clear,
    Loop(Vec<Expression>),
    Output,
    Input,
}
```

### IR Erklärung
Der obenstehende Code definiert eine öffentliche Enum namens "Expression". Eine Enum ist eine Konstruktion in Rust, die es ermöglicht, eine begrenzte Anzahl von möglichen Werten zu definieren, die ein bestimmtes Konzept oder eine bestimmte Idee darstellen.

In diesem Fall enthält die "Expression" Enum sieben Varianten:

"IncVal" und "DecVal" haben beide einen Parameter vom Typ "u8". Diese Varianten repräsentieren die Operationen, um den Wert an der aktuellen Speicherposition im Speicher um 1 zu erhöhen oder zu verringern.

"IncPtr" und "DecPtr" haben beide einen Parameter vom Typ "usize". Diese Varianten repräsentieren die Operationen, um den Speicherzeiger um 1 nach rechts oder links zu verschieben.

"MulVal" hat einen Parameter vom Typ "isize" und einen Parameter vom Typ "u8". Diese Variante repräsentiert die Operation, bei der der Wert an der aktuellen Speicherposition im Speicher mit einem gegebenen Wert multipliziert wird.

"Clear" hat keine Parameter und repräsentiert die Operation, um den Wert an der aktuellen Speicherposition im Speicher auf 0 zu setzen.

"Loop" hat einen Parameter vom Typ "Vec<Expression>". Diese Variante repräsentiert eine Schleife, die aus einer Liste von Ausdrücken besteht, die wiederholt ausgeführt werden, solange der Wert an der aktuellen Speicherposition im Speicher ungleich 0 ist.

"Output" und "Input" haben keine Parameter. Diese Varianten repräsentieren die Operationen, um den Wert an der aktuellen Speicherposition im Speicher als ASCII-Zeichen auf der Konsole auszugeben oder ein ASCII-Zeichen von der Konsole einzulesen und an der aktuellen Speicherposition im Speicher zu speichern.

Zusammengefasst definiert dieser Code also eine Enum, die verschiedene Operationen für die Manipulation des Speichers in der Programmiersprache Brainfuck für die Ausführung auf einer Maschine definiert.

### Optimierungen
#### CopyOptimizer
#### ClearOptimizer
#### CopyOptimizer