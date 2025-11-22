# Chess Game — Advanced Programming Project

This project was developed as the Practical Assignment for the **Advanced Programming (PA)** course in the **Bachelor’s in Computer Engineering** at **ISEC — Polytechnic Institute of Coimbra**, during the **2024/2025 academic year**.

The goal was to build a complete and robust implementation of a chess game, emphasizing strict use of design patterns and a clear separation of responsibilities across the system.

---

## ✨ Implemented Features

The chess game includes a comprehensive and fully functional set of mechanics, along with accessibility and learning-oriented tools:

### ♟️ Core Game Logic
- **Full Chess Rules**: All basic movement and capture rules, plus special moves:
  - Castling  
  - En Passant  
  - Pawn Promotion  
- **Game State Management**:
  - Check  
  - Checkmate  
  - Stalemate  

### 🎓 Learning Tools
- **Undo/Redo** functionality through Command Pattern  
- **Move Highlighting**: Visual display of all legal moves for the selected piece  

### 💾 Data Persistence
- **Import/Export** of complete game state (`.dat` files) via Java Serialization  

### 🔊 Accessibility & Feedback
- **Sound feedback** for moves and captures  

### 🖥️ Graphical User Interface (GUI)
- Fully implemented using **JavaFX**

---

## 💻 Technical Highlights & Design Patterns

A core strength of this project is the rigorous application of **Software Design Patterns**, demonstrating solid skills in modular and scalable architecture.

| Design Pattern | Main Classes | Description |
|----------------|--------------|-------------|
| **Model–View–Controller (MVC)** | `ChessGame` (Model), `BoardView` (View), `RootPane` (Controller) | Enforces strict separation between game logic and UI for clean, maintainable code. |
| **Facade** | `ChessGameManager` | Provides a simple, safe interface to the internal game logic, shielding external components from low-level details. |
| **Observer** | `PropertyChangeSupport`, `BoardView`, `RootPane` | Automatically updates UI components whenever the model changes (e.g., after each move). |
| **Command** | `MoveCommand`, `CommandManager` | Implements Undo/Redo by encapsulating each move as a command with a reversible action. |
| **Factory Method** | `PieceFactory` | Creates chess pieces flexibly based on type or string representation (e.g., for pawn promotion or game import). |
| **Singleton** | `ModelLog`, `SoundManager`, `ImageManager` | Ensures only one shared instance of key managers exists (logs, sounds, images). |

---

## 🛠️ Technologies Used
- **Language:** Java  
- **GUI:** JavaFX  
- **Design Patterns:** MVC, Facade, Observer, Command, Factory Method, Singleton  

---

## ⚙️ How to Run the Project

You may adapt these steps to match your repository structure:

1. Clone the repository:  
   ```sh
   git clone <repository-url>
```
Open the project in IntelliJ IDEA or another Java IDE
Ensure the correct Java SDK version is selected (e.g., Java 17 or Java 21)
Run the main class: ChessMain
```
