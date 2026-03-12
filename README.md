 # Bowling_Game

<p align="center">
    <image 
        src="docs/img/bowling.png" 
        alt="Project Cover" 
        idth= "200"
        height = "200"
    >
</p>

## Table of Contents
- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies](#technologies)
- [Author](#Juan\Pablo\Garcia)

## Descripition

Simulates the scoring process in a bowling game for two or more players. The system is capable of obtaining scores for each player's throws in each quadrant.
When all 10 frames are completed, the system sends the scores and the total score for each player.
In each frame, the system takes the score for each ball throw and checks whether it is a strike or a spare. If either of these conditions is met, the following rules apply:
- Strike: this condition is achieved when a score of 10 pins knocked down is obtained. In this case, the player gets the opportunity to add the score of the next two throws to the score of the current frame.
- Spare: to get a spare, the player must knock down all 10 pins in the two attempts per frame. If this condition is met, the player has the opportunity to add the score of the next throw to the score of the current frame.
Following these rules, the maximum score a player can achieve is 300 points.



## Installation
Steps to install Bowling_Game

1. Open your bash and send the following commands:

```bash
> git clone https://github.com/JPablo90/Bowling_Game
> mkdir build
> cd build
> cmake ..
> make
> cd ./../bin/Bowling
```
## Usage

1. At the root of the project, go to the bin folder.
 ```bash
> cd bin
> Bowling
 ```
2. The game start.
3. Set each player's scores up to the last roll.
4. Check that the final score is correct.

## Technologies

- C++.
- CMake.
- GTets.

## Author

**Name**: Juan P. García<br>
**Mail**: jp.garciamurillo@gmail.com <br>