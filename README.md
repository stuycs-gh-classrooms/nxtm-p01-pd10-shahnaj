[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Mfyqb_T6)
# NeXtCS Project 01
### thinker0: Shahnaj Rahman 

---

### Overview
Your mission is create either:
- Life-like cellular automata [life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life), [life-like](https://en.wikipedia.org/wiki/Life-like_cellular_automaton), [demo](https://www.netlogoweb.org/launch#https://www.netlogoweb.org/assets/modelslib/Sample%20Models/Computer%20Science/Cellular%20Automata/Life.nlogo).
- Breakout/Arkanoid [demo 0](https://elgoog.im/breakout/)  [demo 1](https://www.crazygames.com/game/atari-breakout)
- Space Invaders/Galaga

This project will be completed in phases.  
The first phase will be to work on this document. 
* Use markdown formatting.
* For more markdown help
  - [click here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) or
  - [here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)


---

## Phase 0: Selection, Analysis & Plan

#### Selected Project: Breakout/Arkanoid 

### Necessary Features
What are the core features that your program should have? These should be things that __must__ be implemented in order to make the program useable/playable, not extra features that could be added to make the program more interesting/fun.
    A user controlled paddle that moves left and right (keyboard and/or mouse).
    A ball that moves and bounces off:
    - the paddle 
    - the side walls
    - the top wall
    - the bricks 
    A grid of bricks arranged in rows and columns 
    Bricks disappear when hit by the ball
    The player loses a "life" if the ball goes past the paddle.

In addition to basic gameplay, if you choose breakout your program must have the following:
    A set number (more than one) of "lives".
    The ability to play/pause the game.
    The ability to reset the game.
    Some continuation of the game if all the bricks have been destroyed.


### Extra Features
What are some features that are not essential to the program, but you would like to see (provided you have time after completing the necessary features. Theses can be customizations that are not part of the core requirements.

A decorative background made with simple shapes. 
Changing the ball's color or shape.
Different brick colors for each row.

### Array Usage
How will you be using arrays in this project?

1D Array:
- I will use a 1D array for player's lives. 

2D Array:
- I will use a 2D array to store all bricks in the game. 


### Controls
How will your program be controlled? List all keyboard commands and mouse interactions.

Keyboard Commands:
- Left arrow: move paddle left
- Right arrow: move paddle right
- Spacebar: Play/Pause
- R: Reset the game

Mouse Control:
- Mouse movement: Paddle follows the mouse's x position 
- Mouse pressed: Could be used to restart 


### Classes
What classes will you be creating for this project? Include the instance variables and methods that you believe you will need. You will be required to create at least 2 different classes. If you are going to use classes similar to those we've made for previous assignments, you will have to add new features to them.

CLASS NAME0 - Ball 
- Instance variables:
  int x, y: // position of the ball 
  int dx, dy; // velocity / how fast the ball is moving in each direction 
  int r; // radius of the ball 
- METHODS
Ball(int startX, int startY)
- sets up the ball's starting spot and speed 
void display()
- draws the ball on the screen 
void bounceX()
- inverts dx, flips the ball horizontally when it hits a wall or brick 
void bounceY()
- inverts dy, flips the ball vertically when it hits the paddle, top wall, or brick 

CLASS NAME1 - Brick
- Instance variables:
int x,y; // position of the brick 
int w,h; // width and height of the brick 
boolean active; // true if the brick hasn't been hit yet 
- METHODS
Brick(int x, int y, int w, int h)
- sets up the brick 
void display()
- draws the brick if it is still active
boolean isHit(int ballX, int ballY)
- check if the ball overlaps this brick / if the ball hits the brick 
