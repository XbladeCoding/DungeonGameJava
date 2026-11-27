# Gridded Dungeoneering

A text-based dungeon crawler I made in Java for my final project. You pick a difficulty, spawn in a random room of the dungeon and fight monsters, grab loot and look for the boss. Watch out for Garfield (1% chance, worth a LOT of points).

**Quick start** (needs Java 17 or newer):
```bash
javac *.java
java tester
```
You move with `north`, `south`, `east` and `west`, and the game tells you what to type in each room.

**Name:** Rohan Balasubramanian

## About the project
This is an original idea dreamt up by myself. I as a kid wanted to build a dungeon crawler game. So I designed a dungeon crawler-style game that consisted of a player fighting monsters and looting dungeons in a n-by-n grid, with a boss fight included in the dungeon as well. The game ends either when a player defeats the Garfield enemy, or when they die, or when they beat the boss of the dungeon.

## How to run
This is a game. In order to run the game, run the following commands:
```bash
javac Game.java
javac Dungeon.java
javac tester.java
java tester
```
This compiles all the classes, including the driver, and executes a single line of code in the tester.java file to start the game.

## Data types
I used the ArrayList data type in order to have an inventory and to have a better way of storing the Monsters in a room, and for loot storage as well.

I chose to not use arrays at all because they really were not needed, but I did use a 2D matrix for the map of the dungeon.

## Methods
There are multiple methods across all ADTs. Here is a list of all of them*:

**Player**
- `pickUpItem(Item item)` - adds an item from the loot on the ground into the player's inventory
- `equip(Item item)` - adds the stats of an Item in the inventory to the current stats of the player
- `heal(Item item)` - uses a healing item in the player's inventory to heal some HP for the player
- `addPoints(int pts)` - adds a certain number of points to the player's point count

**Item**
- getter and setter methods for HP, dmg, and def.

**Dungeon**
- `createDungeon()` - creates the n-by-n grid with Rooms that the player plays inside of.

**Game**
- `mainloop()` - runs the game
- `Battle()` - simulates a battle room
- `Loot()` - simulates a loot room
- `Boss()` - simulates a boss room
- `endGame()` - ends the game

**Room**
- `rollLoot()` - returns a loot pool for the loot room based off of the loot table
- `rollEnemies()` - returns enemies to fight in a battle room

*NOTE: Each class has its own getter and setter methods. I'm not going to list them all; that would take years.

## Data and testing
No data is required to run this project. Each method was tested individually to make sure the entire thing would run properly.

## Known bugs/limitations
No bugs have been discovered. If you find one, let me know.

## Serious problems encountered
When I was writing code, I would move onto the next step of code, only to discover that I needed more code for the code to run (other methods and game mechanics).
