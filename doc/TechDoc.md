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

Die Anwendung besteht aus fünf Hauptkomponenten:

Tokenizer: Der Tokenizer ist für das Aufteilen des Brainfuck-Codes in Tokens zuständig. Ein Token ist eine Art von Textelement, das eine spezielle Bedeutung hat. Der Tokenizer durchsucht den Brainfuck-Code und identifiziert jedes Token. Jedes Token wird dann an den Parser weitergegeben.

Parser: Der Parser nimmt die Tokens welche er verwendet, um IR-Expressions zu generieren. Die generierten IR-Expressions werden dann an den Optimizer weitergegeben, der sie optimiert.

Optimizer: Der Optimizer ist ein Programmteil oder eine Funktion, die Brainfuck-Code analysiert und optimiert, um die Ausführung des Programms zu verbessern. Der Zweck des Optimierers besteht darin, die Ausführungszeit und den Speicherverbrauch des Programms zu reduzieren, indem der Code effizienter gestaltet wird.

Pipeline: Die Pipeline nimmt den Brainfuck-Code als Eingabe und gibt einen optimierten Brainfuck-Code als Ausgabe aus. Der optimierte Code kann dann in eine ausführbare Datei kompiliert werden, in unseren fall waere das die VM, Rust, C backends.

Transpiler: Der Transpiler ist das Kernstück der Anwendung. Der Transpiler ruft sowohl das gewuenschte Backend auf. Der Transpiler liest die Expressions ein und sorgt dasfuer das der Korrekt code erzeugt wird fuer das jeweilige backend. Der Transpiler übersetzt die Tokens in C- oder Rust-Code, der dann in eine String geschrieben wird.

Das Ergebnis des Projekts ist eine C- oder Rust-Datei, die den übersetzten Brainfuck-Code enthält. Diese Datei kann dann in eine ausführbare Datei kompiliert werden und auf einer beliebigen Plattform ausgeführt werden.

Dieses Projekt kann Entwicklern helfen, Brainfuck-Code auf eine höhere Programmiersprache zu übersetzen und so das Debugging und die Wartung von Brainfuck-Code zu vereinfachen.

### Tokenizer
Der Tokenizer analysiert die vordefinierten Zeichen von Brainfuck und erzeugt entsprechende Tokens für jeden von ihnen.

```rust

pub struct Tokenizer;

impl Tokenizer {
    pub fn tokenize(text: &str) -> Vec<Token> {
        text.chars().into_iter().map(Self::tokenize_char).collect()
    }

    fn tokenize_char(char: char) -> Token {
        match char {
            '+' => Token::Plus,
            '-' => Token::Minus,
            '.' => Token::Dot,
            '>' => Token::Shr,
            '<' => Token::Shl,
            '[' => Token::OpenBracket,
            ']' => Token::CloseBracket,
            _ => Token::Whitespace(char),
        }
    }
}
```
### Parser
Für jedes Token erstellt der Parser eine Expression.
```rust
pub struct Parser;

impl Parser {
    pub fn parse(tokens: &[Token]) -> Vec<Expression> {
        let mut expressions = vec![];
        let mut indexes: Vec<usize> = vec![];

        for token in tokens.iter().filter(Self::filter) {
            match token {
                Token::Plus => {
                    expressions.push(Expression::IncVal(1));
                }
                Token::Minus => {
                    expressions.push(Expression::DecVal(1));
                }
                Token::Dot => {
                    expressions.push(Expression::Output);
                }
                Token::Comma => {
                    expressions.push(Expression::Input);
                }
                Token::Shr => {
                    expressions.push(Expression::IncPtr(1));
                }
                Token::Shl => {
                    expressions.push(Expression::DecPtr(1));
                }
                Token::OpenBracket => {
                    indexes.push(expressions.len());
                }
                Token::CloseBracket => {
                    let start_index = indexes.pop().unwrap();
                    let r#loop = expressions.split_off(start_index);
                    expressions.push(Expression::Loop(r#loop));
                }
                Token::Whitespace(_) => {
                    unreachable!()
                }
            }
        }
        expressions
    }

    fn filter(token: &&Token) -> bool {
        !matches!(token, Token::Whitespace(_))
    }
}
```
### Pipeline
### Backends
Die Backends sind dafür verantwortlich, auf Basis der Expressions das entsprechende Backend zu generieren. In unserem Fall handelt es sich um Rust- und C-Dateien, die aus den Expressions erzeugt werden. Die Backends übernehmen dabei die Aufgabe, den erzeugten Code zu transpilieren. Sobald das Backend erstellt wurde, kann der transpilierte/generierte Code kompiliert und ausgeführt werden. In Rust mit rustc, und in C mit gcc.
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
Der Optimizer besteht aus drei Optimierungen: Copy, Clear und ConcatOptimizer.

#### ConcatOptimizer
```rust
struct ConcatOptimizer;

impl ConcatOptimizer {
    fn optimize_stage_01(expressions: &[Expression]) -> Vec<Expression> {
        let mut optimized = vec![];
        for expression in expressions {
            match (expression, optimized.last()) {
                (Expression::IncVal(1), Some(&Expression::IncVal(amount))) => {
                    replace_last(&mut optimized, Expression::IncVal(amount + 1))
                }
                (Expression::DecVal(1), Some(&Expression::DecVal(amount))) => {
                    replace_last(&mut optimized, Expression::DecVal(amount + 1))
                }
                (Expression::IncPtr(1), Some(&Expression::IncPtr(amount))) => {
                    replace_last(&mut optimized, Expression::IncPtr(amount + 1))
                }
                (Expression::DecPtr(1), Some(&Expression::DecPtr(amount))) => {
                    replace_last(&mut optimized, Expression::DecPtr(amount + 1))
                }
                (Expression::Loop(expressions), _) => {
                    optimized.push(Expression::Loop(Self::optimize_stage_01(expressions)))
                }
                (expression, _) => optimized.push(expression.clone()),
            }
        }
        optimized
    }

    fn optimize_stage_02(expressions: &[Expression]) -> Vec<Expression> {
        let mut optimized = vec![];
        for expression in expressions {
            match (expression, optimized.last()) {
                (Expression::IncVal(val), Some(&Expression::IncVal(amount))) => {
                    replace_last(&mut optimized, Expression::IncVal(amount + val))
                }
                (Expression::IncVal(val), Some(&Expression::DecVal(amount))) => {
                    concat_match!(optimized, val, DecVal, &amount, IncVal);
                }
                (Expression::DecVal(val), Some(&Expression::DecVal(amount))) => {
                    replace_last(&mut optimized, Expression::DecVal(amount + val))
                }
                (Expression::DecVal(val), Some(&Expression::IncVal(amount))) => {
                    concat_match!(optimized, val, IncVal, &amount, DecVal);
                }
                (Expression::IncPtr(val), Some(&Expression::IncPtr(amount))) => {
                    replace_last(&mut optimized, Expression::IncPtr(amount + val))
                }
                (Expression::IncPtr(val), Some(&Expression::DecPtr(amount))) => {
                    concat_match!(optimized, val, DecPtr, &amount, IncPtr);
                }
                (Expression::DecPtr(val), Some(&Expression::DecPtr(amount))) => {
                    replace_last(&mut optimized, Expression::DecPtr(amount + val))
                }
                (Expression::DecPtr(val), Some(&Expression::IncPtr(amount))) => {
                    concat_match!(optimized, val, IncPtr, &amount, DecPtr);
                }
                (Expression::Loop(expressions), _) => {
                    let sub_expressions = Self::optimize_stage_02(expressions);
                    if !sub_expressions.is_empty() {
                        optimized.push(Expression::Loop(Self::optimize_stage_02(&sub_expressions)))
                    }
                }
                (expression, _) => optimized.push(expression.clone()),
            }
        }
        optimized
    }
}

impl Optimizer for ConcatOptimizer {
    fn optimize(expressions: &[Expression]) -> Vec<Expression> {
        let expressions = ConcatOptimizer::optimize_stage_01(expressions);

        ConcatOptimizer::optimize_stage_02(&expressions)
    }
}
```
### ConcatOptimizer Erklärung
Dieser Code definiert eine Struktur namens ConcatOptimizer, die Teil des Optimizers ist. Die ConcatOptimizer Struktur enthält zwei Funktionen namens optimize_stage_01 und optimize_stage_02, die jeweils eine Vektor von Ausdrücken (Expression) als Eingabe nehmen und eine optimierte Vektor von Ausdrücken zurückgeben.

optimize_stage_01 optimiert die Ausdrücke in Bezug auf die Inkrementierung oder Dekrementierung von Werten und Zeigern sowie auf Schleifen. Die Optimierung wird durchgeführt, indem ähnliche aufeinanderfolgende Ausdrücke zusammengefasst werden. Zum Beispiel, wenn der Ausdruck IncVal(1) direkt auf einen IncVal(n) Ausdruck folgt, wird der IncVal(n) Ausdruck durch einen einzigen IncVal(n+1) Ausdruck ersetzt.

optimize_stage_02 führt eine weitere Optimierung der Ausdrücke durch, indem sie ähnliche aufeinanderfolgende Ausdrücke miteinander kombiniert. Zum Beispiel, wenn der Ausdruck IncVal(n) direkt auf einen DecVal(m) Ausdruck folgt, werden beide Ausdrücke durch einen einzigen Loop(IncVal(n-m)) Ausdruck ersetzt.

Schließlich implementiert die Struktur die optimize Funktion, die eine Kette von Optimierungen ausführt, indem sie zuerst optimize_stage_01 auf die Eingabe anwendet und dann das Ergebnis an optimize_stage_02 weitergibt.

#### ClearOptimizer
```rust
struct ClearOptimizer;

impl Optimizer for ClearOptimizer {
    fn optimize(expressions: &[Expression]) -> Vec<Expression> {
        let mut optimized: Vec<Expression> = vec![];

        for expression in expressions {
            match expression {
                Expression::Loop(expressions) => match expressions[..] {
                    [Expression::DecVal(1)] | [Expression::IncVal(1)] => {
                        optimized.push(Expression::Clear)
                    }
                    _ => {
                        let mut sub_optimized = vec![];
                        let sub_expressions = ClearOptimizer::optimize(expressions);
                        sub_optimized.extend(sub_expressions);

                        if !sub_optimized.is_empty() {
                            optimized.push(Expression::Loop(sub_optimized));
                        }
                    }
                },
                _ => {
                    optimized.push(expression.clone());
                }
            }
        }
        optimized
    }
}
```

Die optimize-Methode nimmt eine Liste von Expression-Werten und gibt eine optimierte Liste von Expression-Werten zurück. Der Optimierer entfernt alle Schleifen, die lediglich aus einer einzigen Inkrementierung oder Dekrementierung des Zellwerts bestehen, und ersetzt sie durch einen einzigen Clear-Befehl.

Die Funktion iteriert durch die gegebene Liste von Expressions und prüft, ob die Expression eine Schleife ist. Wenn dies der Fall ist, wird überprüft, ob die Schleife aus einer einzigen Inkrementierung oder Dekrementierung besteht. In diesem Fall wird ein Clear-Befehl zur optimierten Liste hinzugefügt. Andernfalls wird die Schleife rekursiv optimiert und zur optimierten Liste hinzugefügt.

Wenn die Expression keine Schleife ist, wird sie unverändert zur optimierten Liste hinzugefügt.

Am Ende gibt die Funktion die optimierte Liste von Expression-Werten zurück.

#### CopyOptimizer
```rust
struct CopyOptimizer;

impl Optimizer for CopyOptimizer {
    fn optimize(expressions: &[Expression]) -> Vec<Expression> {
        let mut optimized = vec![];

        for expression in expressions {
            match expression {
                Expression::Loop(r#loop) => {
                    let mut loop_optimized = vec![];
                    let mut context =
                        CopyOptimizerContext::new(optimized.len().wrapping_sub(1) % usize::MAX);
                    for expression in r#loop {
                        match expression {
                            Expression::Clear => {
                                loop_optimized.push(expression.clone());
                                context.set_side_effect(true);
                            }
                            Expression::IncVal(val) => {
                                loop_optimized.push(expression.clone());
                                context.add_inc_val(*val);
                            }
                            Expression::DecVal(val) => {
                                loop_optimized.push(expression.clone());
                                context.add_dec_val(*val);
                            }
                            Expression::MulVal(_, _) => {
                                loop_optimized.push(expression.clone());
                                context.set_side_effect(true);
                            }
                            Expression::IncPtr(val) => {
                                loop_optimized.push(expression.clone());
                                context.add_inc_ptrs(*val);
                            }
                            Expression::DecPtr(val) => {
                                loop_optimized.push(expression.clone());
                                context.add_dec_ptrs(*val);
                            }
                            Expression::Loop(r#loop) => {
                                loop_optimized
                                    .extend(Self::optimize(&[Expression::Loop(r#loop.clone())]));
                                context.set_side_effect(true);
                            }
                            Expression::Output => {
                                loop_optimized.push(expression.clone());
                                context.set_side_effect(true);
                            }
                            Expression::Input => {
                                loop_optimized.push(expression.clone());
                                context.set_side_effect(true);
                            }
                        }
                    }

                    if let Some(expressions) = context.generate_expressions() {
                        optimized.extend(expressions);
                    } else {
                        optimized.push(Expression::Loop(loop_optimized))
                    }
                }
                _ => {
                    optimized.push(expression.clone());
                }
            }
        }

        optimized
    }
}
```

Die CopyOptimizer-Struktur implementiert die Optimizer-Trait. Die Methode optimize der CopyOptimizer-Struktur erhält eine Slice von Expression-Instanzen und gibt eine optimierte Version zurück.

Die Optimierung, die CopyOptimizer durchführt, versucht, die aufeinanderfolgenden Operationen, die eine Kopie von Daten ausführen, zusammenzufassen. Die optimierten Ausdrücke werden in einem Vektor namens optimized gesammelt.

In der Methode optimize wird für jedes Expression in der übergebenen Slice ein Match-Block durchlaufen, um den Expression-Typ zu bestimmen und die Optimierung durchzuführen. Wenn der Expression-Typ eine Schleife ist, wird für jeden Expression in der Schleife ein weiteres Match-Block durchlaufen, um zu bestimmen, welche Art von Expression vorliegt. Wenn eine Expression vorliegt, die eine Kopie von Daten ausführt, wird ein CopyOptimizerContext erstellt, um Informationen über die Ausführung dieser Expression zu sammeln.

Am Ende der Schleife wird geprüft, ob es sich lohnt, die Operationen zusammenzufassen. Wenn ja, wird eine optimierte Version der aufeinanderfolgenden Operationen erzeugt. Andernfalls wird die Schleife unverändert in die optimierte Version eingefügt.

Der Code ist relativ komplex und erfordert ein gutes Verständnis der Brainfuck-Syntax und der Optimierungstechniken, um vollständig verstanden zu werden.