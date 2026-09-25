# Java Core & Fundamentals

## Status
- **Overall Level**: 3/5
- **Theory**: 3/5
- **Practical**: 2/5
- **Troubleshooting**: 1/5
- **Design**: 2/5
- **Confidence**: Medium

## What I Have Learned
- **Java Basics & Environment**: Installing JDK & Eclipse IDE, Java program execution flow (`.java` -> `javac` -> `.class` bytecode -> JVM), main class structure (`public static void main(String[] args)`).
- **Data Types & Variables**: Primitive types (`byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`), wrapper classes, reference types, variable declaration, constants (`final`), comments (`//`, `/* */`, `/** */`), compilation error handling.
- **Input/Output & Type Casting**: `Scanner` class (`nextInt()`, `nextLine()`, `nextDouble()`), implicit casting (widening) and explicit casting (narrowing), string conversion.
- **Operators**: Arithmetic (`+`, `-`, `*`, `/`, `%`), Unary (`++`, `--`), Assignment (`=`, `+=`, `-=`), Comparison (`==`, `!=`, `>`, `<`, `>=`, `<=`), Logical (`&&`, `||`, `!`), Ternary operator (`condition ? val1 : val2`), `Math` class methods (`Math.abs()`, `Math.max()`, `Math.min()`, `Math.sqrt()`, `Math.pow()`).
- **Control Flow**: `if`, `else if`, `else`, `switch-case` statements, quadratic equation solver implementation (`ax^2 + bx + c = 0`), days-in-month calculation.
- **Loops & Branching**: `for` loop, nested `for` loops (multiplication table), `while` loop, `do-while` loop, decimal-to-binary conversion algorithm, `break`, `continue`, `return`.
- **Arrays & Strings**: 1D arrays (`type[] arr = new type[size]`), array copy (`System.arraycopy`, `Arrays.copyOf`), String methods (`length()`, `charAt()`, `compareTo()`, `equals()`, `equalsIgnoreCase()`, `indexOf()`, `substring()`, `concat()`, `replace()`, `toLowerCase()`, `toUpperCase()`, `trim()`, `split()`), `Comparable` interface implementation.
- **Error & Exception Handling**: Basic exception handling using `try-catch-finally` blocks.
- **Utility Classes & Data Serialization**: `Date`, `Calendar`, `SimpleDateFormat`, `Random`, `NumberFormat` (Tai Xiu mini-game exercise), `Enum` types.
- **Java Collections Framework**: `ArrayList`, `LinkedList`, `Stack`, `Queue`, `Deque`, `HashSet`, `TreeSet`, `HashMap`, `TreeMap`, Generics (`<T>`).
- **File & I/O Handling**: `File` class (create, file properties, directory listing, delete, rename, move, copy), character streams (`FileReader`, `FileWriter`, `BufferedReader`, `BufferedWriter`), byte streams (`FileInputStream`, `FileOutputStream`), Object Serialization (`Serializable`, `ObjectOutputStream`, `ObjectInputStream`), Zip/Unzip files (`ZipOutputStream`, `ZipInputStream`).
- **Java Swing GUI**: `JFrame`, `JPanel`, Layout Managers (`BorderLayout`, `FlowLayout`, `GridLayout`, `BoxLayout`), Look and Feel configuration, MVC Pattern in Swing, Event Listeners (`ActionListener`, `MouseListener`), Fonts and Colors, `JTextField`, `JTextArea`, `JScrollPane`, Drawing graphics (`Graphics2D`), `JMenu`, `JMenuItem`, `JToolBar`, `JPopupMenu`, `JRadioButton`, `JCheckBox`, `JComboBox`, `JList`, `JOptionPane`, `JFileChooser`, GUI Drag & Drop, Export to JAR file.

## What I Understand
- Mechanism of JVM bytecode execution and platform independence ("Write Once, Run Anywhere").
- Value vs Reference data types and memory stack vs heap allocation behavior in Java.
- How control flow and iteration loops manage execution branching.
- Mechanism of String immutability in Java and how string pool memory optimization works.
- Mechanism of Exception propagation in `try-catch` blocks.
- Concept of Generics in preventing runtime `ClassCastException` by enforcing compile-time type safety.
- File system abstraction and stream pipelines (character vs byte streams, serialization of object graphs).

## What I Can Do
- Write core Java console programs using standard control structures, arrays, and methods.
- Manipulate strings, convert data types, and apply arithmetic/logical operations.
- Utilize Java Collections (`ArrayList`, `HashMap`, `HashSet`, `Stack`, `Queue`) for basic data management.
- Read and write text files and serialize Java objects to disk.
- Build basic desktop GUI applications using Java Swing with MVC architecture.

## What I Cannot Yet Do
- Build high-concurrency Java applications using `java.util.concurrent` (Executors, Locks, CompletableFuture, ThreadPools).
- Leverage modern Java 8+ features extensively (Lambda expressions, Stream API, Optional, Var handles, Modules).
- Optimize Java memory performance, analyze garbage collection (GC) pauses, or profile JVM memory leaks.
- Unit test Java code using JUnit 5 and Mockito framework.

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-001** — Lập trình Java – Java Core (TITV) | URL: https://titv.vn/courses-page/lap-trinh-java-java-core/ | Lessons 01-27a, 49-76, 77-104
- **SRC-006** — Lập trình mạng sử dụng Java (TITV) | URL: https://titv.vn/courses-page/lap-trinh-mang-su-dung-java/ | Lessons 06-17 (Stream I/O & File management refresher)

Master Sources Catalog: [`00-sources/learning-sources.md`](../00-sources/learning-sources.md)

## Weaknesses
- Lack of hands-on experience with modern Java versions (Java 11/17/21 LTS features).
- Limited understanding of JVM internals (ClassLoader, JIT compilation, GC algorithms).
- No automated testing (JUnit/TestNG) integrated into Java projects.

## Missing Knowledge
- Java 8+ Stream API & Lambdas depth.
- JVM Tuning & Garbage Collection flags (`-Xms`, `-Xmx`, GC log analysis).
- Build tools: Maven / Gradle (Dependency management, build lifecycle).

## Recommended Supplement
1. Learn Maven/Gradle build tools for Java dependency management.
2. Study Java 8+ features: Streams API, Functional Interfaces, Lambdas, `Optional`.
3. Implement unit testing with JUnit 5 and Mockito.
