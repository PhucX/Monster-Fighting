# Monster-Fighting

Monster-Fighting is an action RPG game developed with Pygame, featuring AI-controlled Non-Player Characters (NPCs) that utilize various pathfinding and decision-making algorithms, including Q-Learning.

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Technologies Used](#technologies-used)
* [How AI Works (NPCs)](#how-ai-works-npcs)
* [Algorithms Implemented (for NPCs)](#algorithms-implemented-for-npcs)
* [Getting Started](#getting-started)
* [How To Play](#how-to-play)
* [Future Improvements](#future-improvements)
* [Authors](#authors)

## Overview

This project is a 2D game inspired by the classic "The Legend of Zelda" series. The core focus is on creating an interactive game world where NPCs exhibit intelligent behavior through various AI algorithms. Players can explore, fight enemies, and interact with these AI-driven characters.

The project aims to:
* Implement a functional top-down action RPG.
* Explore and showcase different AI pathfinding and decision-making techniques for NPCs.
* Provide a platform to experiment with algorithms like A*, BFS, DFS, and Reinforcement Learning (Q-Learning) in a game context.

## Features

* **Interactive Gameplay:** Control a player character, explore maps, engage in combat with enemies.
* **Intelligent NPCs:** NPCs with selectable AI algorithms determining their movement and behavior.
* **Multiple AI Algorithms for NPCs:** Including A*, BFS, DFS, Backtracking, UCS, Forward Checking, MinConflict, Hill Climbing, Beam Search, and Q-Learning.
* **Dynamic Algorithm Switching:** Ability to change NPC pathfinding algorithms during gameplay via an in-game UI.
* **Partial Observability Mode:** NPCs can operate with limited or full knowledge of the game world.
* **Q-Learning NPCs:** NPCs that can learn behaviors through a reward-based system.
* **Basic Combat System:** Player and enemies can attack and take damage.
* **Graphical Interface:** Built with Pygame, featuring tile-based maps and sprite animations.

## Technologies Used

* **Python:** Version 3.12+
* **Pygame:** For game engine, graphics, sound, and input handling.
* **(Potentially) NumPy:** For Q-Learning calculations or other numerical tasks.

## How AI Works (NPCs)

* **Game World Representation:** The game map is tile-based, with obstacles and entities defined.
* **NPC State & Perception:**
    * **Non-QL NPCs:** Utilize pathfinding algorithms to navigate towards targets (player, enemies, patrol points). Can operate under full or partial observability (simulating sight range and line-of-sight).
    * **Q-Learning NPCs:** Observe a discretized state of the environment (e.g., distance/direction to player/enemy, own health) and choose actions based on a learned Q-table. Rewards are given for desirable actions (e.g., attacking enemies, reaching player, surviving).
* **Pathfinding:** Algorithms like A*, BFS, DFS are used by non-QL NPCs to find paths around obstacles.
* **Decision Making:**
    * **Non-QL NPCs:** Use a state machine (`get_status`, `actions`) to decide between idling, moving, attacking, patrolling, or following specific logic like POE's Last Known Positions.
    * **Q-Learning NPCs:** The Q-agent selects actions to maximize expected future rewards.

## Algorithms Implemented (for NPCs)

* **Breadth-First Search (BFS):** Explores level by level, finds the shortest path in terms of steps.
* **Depth-First Search (DFNhã** ([@vothnha26](https://github.com/vothnha26))
* **Nguyễn Trọng Phúc** ([@PhucX](https://github.com/PhucX))
