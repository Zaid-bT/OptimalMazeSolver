# 🧩 Optimal Maze Solver

A C++ maze-solving game built using **Qt Framework** and **Qt Widgets**. The game challenges players to navigate randomly generated mazes across multiple difficulty levels, then uses the **Breadth-First Search (BFS)** algorithm to calculate and visualize the shortest possible path.

The project combines interactive gameplay, maze generation algorithms, graph traversal, and visual animations in a neon-themed graphical interface.

## 🎮 Features

- **Multiple Difficulty Levels:** Choose between Easy, Medium, Hard, and Impossible.
- **Random Maze Generation:** Every game generates a new maze layout.
- **Recursive Backtracking:** Uses Depth-First Search (DFS)-based recursive backtracking to generate maze structures.
- **Multiple Possible Solutions:** Randomly removes selected walls to introduce loops and alternative routes.
- **Keyboard Controls:** Navigate through the maze using the arrow keys.
- **User Path Tracking:** Records the player's movement throughout the maze.
- **Optimal Pathfinding:** Uses Breadth-First Search (BFS) to find the shortest path from start to destination.
- **Animated Solution Reveal:** Displays the optimal path step by step after the player completes the maze.
- **Path Comparison:** Overlays the player's path and the optimal path on the same maze to compare their routes.
- **Neon-Themed Interface:** Dark background with neon green maze walls, cyan player trails, and glowing optimal paths.

## 🛠️ Technologies Used

- **Language:** C++
- **Framework:** Qt 6
- **GUI:** Qt Widgets / Qt Designer
- **Graphics:** QPainter
- **Data Structures:** Vectors, Queues, Matrices
- **Algorithms:**
  - Recursive Backtracking (Maze Generation)
  - Breadth-First Search (Optimal Pathfinding)
- **Development Environment:** Qt Creator

## 🧠 Algorithms Explained

### 1. Maze Generation – Recursive Backtracking

The maze is generated using recursive backtracking.

The algorithm:
1. Starts from the top-left cell.
2. Marks the current cell as visited.
3. Randomly shuffles the possible directions.
4. Checks neighboring cells.
5. Removes the wall between the current cell and an unvisited neighbor.
6. Recursively visits that neighbor.
7. Backtracks when no unvisited neighbors remain.

This produces a connected maze structure.

### 2. Introducing Multiple Solutions

A standard recursive backtracking maze has exactly one path between any two cells.

To introduce alternative routes, additional walls are randomly removed after the initial maze generation. This creates loops and allows the player to reach the destination through multiple possible routes.

### 3. Optimal Pathfinding – BFS

Breadth-First Search is used to calculate the shortest path between the starting and ending cells.

The algorithm:
1. Adds the starting cell to a queue.
2. Explores neighboring cells in four directions.
3. Checks whether movement between cells is allowed.
4. Marks visited cells and stores their parent positions.
5. Continues until the destination is reached.
6. Reconstructs the shortest path using the parent matrix.

Since every movement has equal cost, BFS guarantees a shortest path in terms of the number of cell-to-cell moves.

### 4. Animated Path Visualization

After the player completes the maze:
- The original maze is transferred to the solution page.
- BFS calculates the optimal path.
- The optimal path is revealed step by step.
- Once the animation finishes, the user's path is displayed alongside the optimal path.

This allows players to visually compare their navigation with the shortest possible route.

## 🎨 Visual Design

The game uses a dark, neon-inspired visual theme.

| Element | Color |
|---|---|
| Maze Background | Dark Black |
| Maze Walls | Neon Green |
| Player Trail | Cyan |
| Optimal Path | Neon Yellow |
| Start Marker | Yellow |
| End Marker | Red |

## 🎯 Controls

| Key | Action |
|---|---|
| ↑ | Move Up |
| ↓ | Move Down |
| ← | Move Left |
| → | Move Right |

## ⚙️ Installation and Setup
Prerequisites

Make sure you have installed:

Qt 6

Qt Creator

A compatible C++ compiler (MinGW or MSVC)

CMake or qmake, depending on the project configuration

Running the Project

Clone the repository:

git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

Open Qt Creator.

Select File → Open File or Project.

Open the project's .pro file or CMakeLists.txt, depending on your project setup.

Configure the project using an available Qt 6 kit.

Build and run the application.

📂 Project Structure

The main project files include:

Optimal-Maze-Solver/
│
├── main.cpp
├── mainwindow.cpp
├── mainwindow.h
├── mainwindow.ui
│
├── mazewidget.cpp
├── mazewidget.h
│
├── resources/           
│
└── README.md

🚀 Future Improvements

Potential improvements for future versions include:

Maze completion timer and move counter.

Performance statistics for each difficulty.

More advanced maze generation techniques.

Additional maze customization options.

Sound effects and background music.

Improved animations and visual effects.

Saving and displaying previous game results.

📚 Learning Outcomes

This project provided practical experience with:

Object-Oriented Programming in C++.

GUI development using Qt Widgets.

Recursive algorithms and backtracking.

Graph traversal and BFS.

Queue-based pathfinding.

2D graphics rendering using QPainter.

Event handling and keyboard input.

Signals and slots in Qt.

Working with Git and GitHub.

👨‍💻 Author

Zaid

Developed as a C++ and Data Structures & Algorithms project.

Explore the maze, find your way out, and see how close you get to the optimal solution! 🧩
