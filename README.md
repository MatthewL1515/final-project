# Final Project

## Project Description
This project will be a wave-based survival game, where a player navigates a maze while avoiding a growing swarm of drones. Drones will follow and seek the player (Chapter 5: Autonomous Agents), but are destroyed on collision with a wall or mouse clicks, creating particle bursts with the player's limited number of lives.

## Modelling Classes
**Player**: For controlling player position, gravity, health, drawing, and collision detection with drones and walls.

**Drone**: The autonomous agent class (chapter 5) that tracks and seeks the player. It will also have mouse click detection and will do a particle animation upon any collision (except with other drones).

**Maze**: Draws a maze and stores it in this class. I'd like to do further research to see whether it's feasible to randomly generate a maze. 

**Particle**: Visual effect(no collision checks for this). Acts as a result of an if, on detection of a drone collision. Has motion and fading of particles.

**Wave Manager**: Counts the number of waves, controls spawning more waves, and keeps count of all drones present(if none, spawn next wave).

## Other Variables and Data Structures
