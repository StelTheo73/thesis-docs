# Game Conceptual Design

Having explored the available educational games for quantum computers, studied GBL techniques and the basic theory around quantum computers, and chosen the framework and game engine we will use to develop the application, it is time to discuss the process that was followed to design the game up to the creation of the early prototype.

## Game & Mechanics Choice

The first step in designing the game was to determine the gender. Based on the findings in Chapter 2, we decided to make a puzzle game, as it is suitable for increasing information retention while allowing for simple mechanisms.

We then had to define the game mechanics. We reasoned that a 2D shooting game could have simple mechanisms, especially if the effect of gravity or other external factors on the missiles is not taken into account. This thinking led us to the decision to create a game with missiles being launched into space from a spaceship. We immediately thought that there was a similar computer game that we could use as a blueprint: [_Space Invaders_](https://en.wikipedia.org/wiki/Space_Invaders)

We then had to decide which element of the game was appropriate to introduce the concepts of quantum computing. We could control 3 variables, the position of the spaceship, the position of the enemy spaceships and the state of the missiles. In terms of controlling the state of the missiles, we thought the game would be similar to Tetris, which is still a puzzle game, but it can get tedious and eventually distract the players from the learning objective, as they have a limited time to manipulate the state of the missiles, so they may randomly affect them, with no time to recall the knowledge they have gained. After rejecting the missile state control, we considered the spacecraft position control and decided to control our own spacecraft rather than the opposing spacecraft.

Based on the above, we decided to control the spacecraft not with a traditional joystick, but by acting on the spacecraft with quantum gates. We decided to have distinct locations where the spaceship, and therefore the targets, could be found, and to encode each location with quantum bit states. In this way we match the position of the spacecraft to the state of a quantum register.

## Game-Based Learning Elements

We then had to decide which GBL elements to include in our game.

First, we decided to use narratives to introduce the theory and rules of the game, specifically overlays that appear at the beginning of certain levels and give the student the information needed to complete the level.

We then decided to create an incentive system to increase the student's motivation. Based on the games we found in the literature, we decided to introduce a scoring system that awarded 1 to 3 stars for successfully completing a level. To get all 3 stars, the player must complete each level with the least number of moves. We also thought it would be good to give the player new spaceships as they progressed through the game to increase motivation and engagement. We also decided not to use a leaderboard to avoid frustration or discrimination, as discussed in Chapter 3.

Finally, we decided to adopt the graceful failure approach to allow users to experiment and try alternative ways of solving the puzzle. So we decided that there would be no immediate penalty if players made a wrong move, i.e. if they moved the spaceship to the wrong position or if a shot missed. At the end of the level, they will only receive the maximum number of stars if they have used the minimum number of moves to solve the puzzle and if all their missiles hit the target. The opposite scenario will not result in a complete failure, they will simply not receive the maximum number of stars.

## Development Process

After defining the genre, mechanics and GBL elements we would use in the game, we designed the game development process. The process follows a waterfall model. We started with an initial wireframe representing a level of the game that we would implement (application prototype) and evaluate with typical users. Then, based on the user feedback, we would refine the prototype to create the first version of the application.

===========================================================================================================
TODO: In chapter 7 intro, connect with chapter 6. Also, do not forget to mention the loop between prototype and first evaluation round -> Prototype -> Evaluation -> Improve Prototype -> Start Development
