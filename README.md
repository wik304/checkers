# Checkers (Warcaby) - JavaFX

A classic checkers game written in Java using the JavaFX graphics library. The application features local two-player gameplay with a built-in chess clock system.

## 🌟 Key Features

- **Local multiplayer (1vs1):** Hot-seat gameplay on a single computer.
- **Full checkers mechanics:** Implementation of forced captures, backward movement during multiple captures, and promotion of regular pieces to Kings.
- **Chess clocks:** Each player has a default time limit of 10 minutes per game. The time is counted down in real-time.
- **Move log:** A side panel displaying the history and duration of individual moves for both white and red players.
- **LAN mode preparation:** The interface includes a menu with a planned LAN mode (currently under development).

---

## 🛠 Technologies

The project was built using a modern technology stack for Java desktop applications:

- **Language:** Java 23
- **GUI:** JavaFX 17.0.6 (Controls & FXML)
- **Build Tool:** Maven (with built-in Maven Wrapper)
- **Testing:** JUnit 5.10.2 (configured in `pom.xml`)

---

## ⚙️ System Requirements

To compile and run the project on your computer, you will need:

- **Java Development Kit (JDK)** version **23** or newer installed.
- The `JAVA_HOME` environment variable pointing to your JDK installation folder.
- You do **not** need to install Maven – the project uses the included Maven Wrapper (`mvnw`) script.

---

## 🚀 Installation and Usage

Use the built-in `javafx-maven-plugin` to automatically download dependencies, compile the code, and run the game.

### For Windows

Open the terminal (Command Prompt or PowerShell) in the project's root directory and run:

```cmd
mvnw.cmd clean javafx:run
```

### For Linux / macOS

Open the terminal in the project's root directory, grant execute permissions to the script (only required the first time), and run the game:

```bash
chmod +x mvnw
./mvnw clean javafx:run
```

---

## 📂 Project Structure

The main application logic is divided into clean, readable classes and packages:

| File / Class | Description |
|-------------|-------------|
| `CheckersApp.java` | The main starter class for the JavaFX application. |
| `CheckersGame.java` | Manages the graphical user interface (GUI), menu, board, and clocks. |
| `GameLogic.java` | The game engine. Responsible for move validation, captures, promotion, and win conditions. |
| `Piece.java` | Visual and state representation of the game pieces. |
| `Tile.java` | Visual and state representation of board tiles. |
| `MoveResult.java` | Helper class for handling move results. |
| `MoveType.java` | Enum describing move types (`NORMAL`, `CAPTURE`, `NONE`). |
| `pom.xml` | Maven configuration file containing JavaFX dependencies. |

---

## 🎮 Gameplay Rules Implemented

- Mandatory captures.
- Multiple captures in a single turn.
- Backward movement during multi-capture sequences.
- Promotion to King upon reaching the opponent's back row.
- Win detection when a player has no valid moves or no remaining pieces.
- Real-time chess clocks with a 10-minute limit per player.

---

## 🚧 Future Development

Planned features include:

- LAN multiplayer mode.
- Improved game settings.
- Enhanced UI and animations.
- Game saving and loading.
- Additional game statistics.

---
