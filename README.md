# Run For Life 🏃‍♂️⬛

> A minimalist, physics-based 3D endless runner built in Unity. 

**Run For Life** is a distraction-free, high-speed endless runner designed to test pure mechanical reflexes and spatial awareness. Stripping away the bloated visual noise and microtransactions of modern mobile games, this project focuses entirely on a tight, physics-driven gameplay loop using primitive 3D geometry.

*(Note: Add a screenshot or GIF of your gameplay here later!)*

## ✨ Features
* **Physics-Based Movement:** Fluid, continuous momentum utilizing Unity's Rigidbody system and Vector3 mathematics rather than rigid lane-switching.
* **Procedural Obstacle Generation:** Dynamic spawning algorithms ensure no two playthroughs are ever the same.
* **Dynamic Difficulty Scaling:** * **Easy:** Slower baseline velocity, wider gaps.
  * **Medium:** Standardized arrays, faster reaction times needed.
  * **Hard:** Exponentially scaling speed with dense, overlapping obstacle clusters.
* **Persistent High Scores:** Local data serialization using `PlayerPrefs` to track and save player progress across sessions.
* **Zero Distractions:** A stark, high-contrast visual style (red player, light-grey plane, dark-grey obstacles) engineered to reduce cognitive overload.

## 🛠️ Tech Stack & Architecture
* **Engine:** Unity 3D (2022 LTS+)
* **Language:** C# (.NET Framework)
* **IDE:** Microsoft Visual Studio
* **Core Concepts Demonstrated:**
  * **Singleton Design Pattern:** Used for the central `GameManager` to strictly control game states (Menu, Play, Game Over).
  * **Memory Optimization:** Implementation of Object Pooling and strict `Destroy()` routines to prevent memory leaks during infinite generation.
  * **Collision Integrity:** Utilization of Continuous Dynamic collision detection to prevent the player object from tunneling/phasing through obstacles at extreme velocities.
  * **Frame-Rate Independence:** Physics forces strictly applied inside the `FixedUpdate()` loop using `Time.deltaTime`.

## 🎮 How to Play
**Objective:** Survive as long as possible by dodging the dark-grey blocks. Any collision results in an instant Game Over.

**Controls:**
* `Left Arrow` or `A` - Move Left
* `Right Arrow` or `D` - Move Right

## 🚀 Installation & Setup (For Developers)
To run this project locally in the Unity Editor:
1. Clone the repository:
   ```bash
   git clone [https://github.com/shaiknavedahmed/run_for_life.git](https://github.com/shaiknavedahmed/run_for_life.git)
