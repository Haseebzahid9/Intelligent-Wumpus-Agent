# Wumpus Intelligence Analytics Dashboard

A high-fidelity, web-based simulation of a **Knowledge-Based Agent** navigating the classic "Wumpus World" environment [cite: 3]. This project demonstrates the application of **Propositional Logic**, **Resolution Refutation**, and automated reasoning in a partially observable grid [cite: 4, 12].

## 🚀 Overview
The Wumpus Logic Agent is a single-page application (SPA) that integrates a logical reasoning engine with a real-time visualization layer [cite: 6, 7]. The agent must navigate an $N \times N$ grid to find gold while avoiding deadly pits and the predatory Wumpus [cite: 9, 31].

### Key Features
* **Resolution Refutation Engine:** Performs automated inference to prove cell safety [cite: 12].
* **Dynamic World Generation:** Randomly places hazards with a 20% pit density; cell (0,0) is always safe [cite: 9, 10].
* **Real-time Telemetry:** Visualizes percepts such as Breeze, Stench, and Glitter [cite: 17, 18].
* **Knowledge Base (KB) Visualizer:** Displays active CNF clauses and logical steps in real-time [cite: 12, 28].
* **Adjustable Clock Speed:** Control simulation velocity for detailed analysis.

---

## 🛠️ Technical Architecture

### The Reasoning Engine
The engine maintains a Knowledge Base consisting of clauses in **Conjunctive Normal Form (CNF)** [cite: 12]. It follows a "Sense-Think-Act" cycle [cite: 21]:
1.  **Sense:** Detects environmental percepts at the current location [cite: 21].
2.  **Think:** Updates the KB and uses resolution to identify safe cells in the frontier [cite: 13, 22].
3.  **Act:** Moves to the nearest safe, unvisited cell using pathfinding logic [cite: 22, 24].

### Core Logical Axioms
The agent's world model is built on propositional variables for Pits ($P$), Wumpus ($W$), and Safety ($S$) [cite: 15]:
* **Breeze:** $Breeze(x, y) \iff Pit(Adj_1) \lor Pit(Adj_2) \lor \dots$ [cite: 17]
* **Stench:** $Stench(x, y) \iff Wumpus(Adj_1) \lor Wumpus(Adj_2) \lor \dots$ [cite: 18]
* **Safety:** $Safe(x, y) \iff \neg Pit(x, y) \land \neg Wumpus(x, y)$ [cite: 19]

---

## 📊 Analytics & Metrics
The dashboard provides transparency into the agent’s internal state through several metrics [cite: 26]:
* **Inference Count:** Total number of resolution attempts made [cite: 27].
* **Trajectory Steps:** The total number of moves in the agent's path [cite: 24].
* **Active Clauses:** The current size of the Knowledge Base [cite: 28].
* **System Log:** A chronological trace of actions and deductions [cite: 29].

---

## 🚦 Getting Started
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/wumpus-logic-agent.git
    ```
2.  **Open the application:**
    Simply open the `23F-0644-Haseeb-6f.html` file in any modern web browser.
3.  **Configure & Run:**
    * Set your desired **Grid Size**.
    * Adjust the **Clock Speed**.
    * Click **Initialize**, then **Start Execution**.

## 💻 Tech Stack
* **Frontend:** HTML5, CSS3 (Zinc/Slate Dark Palette), JavaScript (ES6+).
* **Logic:** Propositional Logic / Resolution Refutation.
* **Fonts:** Inter & JetBrains Mono.

---

*This project serves as a robust platform for testing reasoning algorithms and visualizing AI behavior.* [cite: 32]
