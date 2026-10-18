# FruitBasketJava

**FruitBasketJava** is a simple Java console application that simulates catching and eating fruits using a stack data structure. Users choose how many fruits to catch, select from four fruit types, and then remove fruits from the basket one at a time.

This project demonstrates Java collections, stack operations, loops, conditional statements, and console input.

## Features

- Allows users to choose how many fruits to catch.
- Supports four fruit types:
  - Apple
  - Orange
  - Mango
  - Guava
- Uses Java's built-in `Stack<String>` collection to store fruits.
- Displays the contents of the basket.
- Allows users to eat fruits one at a time.
- Displays the remaining fruits after each removal.
- Notifies users when no fruits remain.

## Requirements

- Java Development Kit (JDK) 21 or compatible environment
- A Java-compatible IDE, such as NetBeans, or a terminal

## How It Works

1. The program asks how many fruits the user wants to catch.
2. The user selects a fruit using the corresponding letter:
   - `A` — Apple
   - `O` — Orange
   - `M` — Mango
   - `G` — Guava
3. Each selected fruit is added to the stack using `push()`.
4. The program displays the basket.
5. The user enters `E` to eat the top fruit, which is removed using `pop()`.
6. The program continues displaying the basket until the user stops or all fruits have been removed.

**Note:** The current source code checks lowercase letters (`a`, `o`, `m`, `g`, and `e`). Enter lowercase letters for the commands to work as intended.

## Example

```text
Catch and eat any of these fruits:('apple', 'orange', 'mango', 'guava')
How many fruits would you like to catch? 3
Choose a fruit to catch. Press A, O, M or G.
Fruit 1 of 3:a
Fruit 2 of 3:m
Fruit 3 of 3:g
Your basket now has :[Apple, Mango, Guava]
Press E to eat Fruit : e
Fruit(s) in the basket : [Apple, Mango]
Press E to eat Fruit : e
Fruit(s) in the basket : [Apple]
Press E to eat Fruit : e
No more Fruits.
```

## Project Structure

```text
FruitBasketJava/
├── pom.xml
├── README.md
└── src/
    └── main/
        └── java/
            └── com/
                └── mycompany/
                    └── fruitbasket/
                        └── FruitBasket.java
```

## How to Run

### Option 1: Using NetBeans

1. Clone or download the repository.
2. Open the project in NetBeans as a Maven project.
3. Ensure JDK 21 is configured.
4. Run the `FruitBasket` main class.
5. Follow the prompts in the console.

### Option 2: Using Maven

Clone the repository:

```bash
git clone https://github.com/ichiroyamazaki/FruitBasketJava.git
cd FruitBasketJava
```

Compile the project:

```bash
mvn compile
```

Run the application using the Maven Exec Plugin, if configured:

```bash
mvn exec:java -Dexec.mainClass="com.mycompany.fruitbasket.FruitBasket"
```

If the Exec Plugin is not configured in your Maven project, run the main class through your IDE or configure the plugin first.

## Concepts Demonstrated

- **Stack:** Uses last-in, first-out (LIFO) behavior to add and remove fruits.
- **`push()`:** Adds a fruit to the top of the stack.
- **`pop()`:** Removes the top fruit from the stack.
- **`isEmpty()`:** Checks whether the basket contains any fruits.
- **Loops:** Repeats fruit selection and eating operations.
- **Switch statements:** Maps fruit-selection letters to fruit names.
- **Scanner:** Reads user input from the console.

## Limitations

- Commands are case-sensitive and currently recognize lowercase letters only.
- Invalid fruit selections are not validated.
- Entering a non-numeric value for the fruit count can cause an input error.
- The program assumes the basket contains a fruit when `pop()` is called; invalid eating input or an empty basket can cause an exception.
- This is a console-based simulation and does not include a graphical interface.

## Author

**Ichiro Yamazaki**

## License

No license is specified in the repository. Check the repository for licensing information before redistributing or modifying the project.
