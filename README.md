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
### Core/Central Game Variables
drones: array

particles: array

hitcount: integer counter for how many times the player has been hit (max 5)

health: for player display, tells the player's life

gamveOver: ends game once player reaches 5 hits

### Player Class Variables
position: tracks player position

gravity: gravity constant

allForce: determines all forces on the player

jump: When the player hits the "w" button, a vertical jump force is applied to the player

onGround: used to check whether the player can jump

### Drone Class Variables
position: tracks drone position

force: calculates all forces on the drone

maxSpeed: limits speed to prevent overspeed
radius: used for collision

### Maze Class Variables
wall_x, wall_y: define the wall positioning of the maze to determine collision for the drone and the player

### Particle Class Variables
position: tracks the position of particles

gravity: gravity for particles

lifespan: fades the particles away

color: random colors for particles

### WaveManager Class Variables
currentWave: current wave number

activeDrones: tracks the number of drones currently on screen

spawnCheck: Sometimes, p5js has issues with ticks. So, this variable sets a delay for a second to prevent code from 'spawning' more drones than required.

## Code Setup
* Create multiple .js files for different classes
* 
