This README provides an overview of the **Asteroids** clone developed using Python and Pygame. This project focuses on object-oriented programming (OOP) principles, vector mathematics, and game loop architecture.

---

## ## Project Overview

This is a modern take on the classic arcade game. The player controls a triangular spaceship in a 2D environment, tasked with shooting and destroying asteroids that split into smaller fragments upon impact.

### ### Key Features

* **Physics-Based Movement:** Frame-rate independent movement using delta time () and 2D vectors.
* **Object-Oriented Design:** A clean class hierarchy starting from a base `CircleShape` to specific `Player`, `Asteroid`, and `Shot` classes.
* **Collision Detection:** Accurate circle-to-circle collision logic for gameplay interactions.
* **Asteroid Splitting:** Dynamic logic that shatters large asteroids into smaller, faster shards.
* **Automated Event Logging:** Integrated logging system to track game events like shots fired and asteroid destruction.

---

## ## Architecture

The project is built on several core modules to maintain a clean separation of concerns:

| Module | Responsibility |
| --- | --- |
| **`main.py`** | Entry point; manages the game loop, clock, and sprite groups. |
| **`player.py`** | Handles player input, rotation, thrust, and shooting cooldowns. |
| **`asteroid.py`** | Manages asteroid behavior and the recursive splitting logic. |
| **`circleshape.py`** | The base class for all circular game objects, handling position, velocity, and collisions. |
| **`constants.py`** | Centralized configuration for screen size, speeds, and radii. |


---

## ## Getting Started

### ### Prerequisites

* **uv**: A fast Python package installer and resolver.
* Python 3.12+ (managed automatically by uv).

### ### Installation & Setup

Instead of manual virtual environment management, this project uses `uv` for a seamless experience:

1. **Clone the repository:**
```bash
git clone <your-repo-url>
cd asteroid-game

```


2. **Sync the project:**
This command will automatically create a virtual environment and install all dependencies (including Pygame CE) as defined in the `pyproject.toml` or `requirements.txt` file:
```bash
uv sync

```



### ### Running the Game

You can run the game without manually activating the environment by using `uv run`:

```bash
uv run main.py

```

---

## ## Development with uv

* **Adding new dependencies:** `uv add <package-name>`
* **Running tests:** `uv run python -m pytest` (if applicable)
* **Updating tools:** `uv self update`


---

## ## Controls

* **A / D:** Rotate Left / Right
* **W / S:** Move Forward / Backward
* **SPACE:** Shoot
