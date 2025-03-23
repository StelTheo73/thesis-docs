# Conceptual Design & Development

Having explored the available educational games for quantum computers, studied GBL techniques and the basic theory around quantum computers, and chosen the framework and game engine we will use to develop the application, it is time to discuss the process that was followed to design the game up to the creation of the early prototype. Furthermore, in the last section of this chapter we will present the development timeline. _Figure 6.1_ shows the process of conceptual design and implementation of the application prototype.

![Design & Prototype Creation Flow.](chapter-6/image001_design_flow.png){#fig:fig601 height=50%}

According to _Kalmpourtzis_ [-@kalmpourtzis_edu_game_design], the five components of educational game design are: Mechanics, Narrative, Aesthetics, Technology and Pedagogy. These components are interconnected and should be considered when designing a game. The mechanics are the rules and procedures that guide the player's actions and the game's response to them. The narrative is the story that the game tells, the aesthetics are the visual and auditory components that make up the game's look and feel, the technology is the hardware and software that the game runs on, and the pedagogy is the educational theory that the game is based on.

As for the technological part, we discussed it in the previous chapters and decided that we would build a cross-platform application using the Flutter framework and the Flame game engine. We will then present the analysis of the remaining 4 game components. As shown in _Figure 6.1_, the analysis of these elements was done in parallel and led us to define the development process we followed.

## Genre Selection & Mechanics Definition (Mechanics)

The first step in designing the game was to determine the gender. Based on the findings in Chapter 2, we decided to make a puzzle game, as it is suitable for increasing information retention while allowing for simple mechanisms.

We reasoned that a 2D shooting game, combined with a puzzle game, could have simple mechanisms, especially if the effect of gravity or other external factors on the missiles is not taken into account. This thinking led us to the decision to create a game with missiles being launched into space from a spaceship. We immediately thought that there was a similar computer game that we could use as a blueprint: _Space Invaders_^[https://en.wikipedia.org/wiki/Space_Invaders]

We then had to decide which element of the game was appropriate to introduce the concepts of quantum computing. We could control 3 variables, the position of the spaceship, the position of the enemy spaceships and the state of the missiles. In terms of controlling the state of the missiles, we thought the game would be similar to Tetris, which is still a puzzle game, but it can get tedious and eventually distract the players from the learning objective, as they have a limited time to manipulate the state of the missiles, so they may randomly affect them, with no time to recall the knowledge they have gained. After rejecting the missile state control, we considered the spaceship position control and decided to control our own spaceship rather than the opposing spaceship.

Based on the above, we decided to control the spaceship not with a traditional joystick, but by acting on the spaceship with quantum gates. We decided to have distinct locations where the spaceship, and therefore the targets, could be found, and to encode each location with qubit states. In this way we match the position of the spaceship to the state of a quantum register. The player chooses the gate they want and places it at a specific location. Placing the gate at the specific location will change the value of the register, thus affecting the position of the spaceship.

Finally, once the ship is in the correct position, the player must launch missiles to destroy the targets. That requires implementing a moving graphical element and defining the equations of motion in two-dimensional space.

## Game-Based Learning Elements Selection (Narratives, Aesthetics)

First, we decided to use narratives to introduce the theory and rules of the game, specifically overlays that appear at the beginning of certain levels and give the student the information needed to complete the level.

We then decided to create an incentive system to increase the student's motivation. Based on the games we found in the literature, we decided to introduce a scoring system that awarded 1 to 3 stars for successfully completing a level. To get all 3 stars, the player must complete each level with the least number of moves. We also thought it would be good to give the player new spaceships as they progressed through the game to increase motivation and engagement. We also decided not to use a leaderboard to avoid frustration or discrimination, as discussed in Chapter 3.

Finally, we decided to adopt the graceful failure approach to allow users to experiment and try alternative ways of solving the puzzle. So we decided that there would be no immediate penalty if players made a wrong move, i.e. if they moved the spaceship to the wrong position or if a shot missed. At the end of the level, they will only receive the maximum number of stars if they have used the minimum number of moves to solve the puzzle and if all their missiles hit the target. The opposite scenario will not result in a complete failure, they will simply not receive the maximum number of stars.

## Educational Content Selection (Pedagogy)

Together with the definition of the mechanics and the choice of the GBL elements to be used in the game, it was decided which aspects of the basic theory of quantum computing - introduced in Chapter 4 - would be presented in the game. We decided to introduce the concepts of qubit, quantum register and quantum gate at a tutorial level, as these are the most basic concepts. Next, we decided to introduce Pauli gates (Pauli-X, Pauli-Y and Pauli-Z). We decided that the first levels should have registers with one qubit. After the player has become familiar with the operation of these gates, we will introduce the concept of superposition for one-bit registers. Later, when the player also understands superposition, we will use registers with two qubits. There, the player will have to combine their previous knowledge to solve the puzzles.

## Evaluation Process Definition (Pedagogy)

We also wondered how we could assess the learning outcomes of the game. After reviewing the available literature [@cooksey-jonsson-pre-post; @stratton-pre-post], we decided that a Pre-Post test study would be appropriate to evaluate the game. For the purposes of this study, a quiz was designed and integrated into the game. At this stage, we simply collected some candidate questions as suggested in the literature. The final selection of questions was made after the construction of the game had been completed and before the quiz screen had been created. In addition, we decided to conduct a focus group to evaluate the structure, usability and difficulty of the game. Finally, we decided to conduct a usability test to evaluate the game's performance and user experience, using _System Usability Scale_ (SUS) [@avouris-sus, p: 458] and _Game Experience Questionnaire_ (GEQ) [@ijsselsteijn-geq].

 The structure and content of the two phases (Pre-Post tests and focus group) are presented in detail in Chapter 7.

## Application Structure

_Figure 6.2_ shows the structure that was chosen for the application.

![Application Structure & Navigation Flow.](chapter-6/image002_app_structure.png){#fig:fig602 height=50%}

The 'Home' screen will consist of 5 buttons which will navigate the user to the level selection screen, the ship selection screen, the quiz menu, the tutorial level or the settings. It will not be possible to navigate between these screens without returning to the home menu, in order to keep navigation as simple as possible and avoid too much depth.

The 'Level Selection' screen will allow the user to select one of the available levels. Each level is preceded by a tile showing the level number, the portals available and the score the player has achieved in that level.

The 'Level' screen and the 'Tutorial Level' screen will be the only screens managed by the Flame game engine and will have Flame widgets. When the user leaves these screens, the game engine will shut down.

The 'Spaceship Selection' screen will allow the user to select which spaceship to operate. Spaceships are initially locked and rewarded to the User as described in Section 6.3.

The 'Quiz' screen will provide the ability to navigate to two sub-screens, the 'Quiz Form' screen, where the user can take the quiz we have created for the evaluation needs, and the 'Quiz History' screen, where the user can view previous quiz attempts. In this way, they can see for themselves if they have improved their knowledge. After completing a quiz, the application will proceed to the 'Quiz Results' screen, where the score for that particular attempt will be displayed.

Finally, the 'Settings' screen should allow the user to change the language and to reset the progress of the game.

The final layout and functionality of the screens will be presented in Appendix A.

## Level Wireframe

![Wireframe](chapter-6/image003_wireframe.png){#fig:fig603 height=50%}

A prototype level (wireframe) was then designed in _diagrams.net_^[https://app.diagrams.net/], which formed the foundation for creating the game's graphical interface. As shown in _Figure 6.3_, the original approach did not include a graphical element for the quantum register, but rather 2 discrete qubits to which the quantum gate would be applied. There were also two buttons, one for applying the gate and one for launching the missiles. The target state was placed at the top of the screen. Finally, the targets were enemy spaceships, as in the original _Space Invaders_ game.

## Development Timeline

![Development Timeline.](chapter-6/image004_development_timeline.png){#fig:fig604 height=80%}

Development of the game began in November 2024. The game developed is called _Qubity_ and, as mentioned before, is a variant of the arcade video game _Space Invaders_. Google's _Material Design 3_^[https://m3.material.io] and _Flame Game Engine_^[https://flame-engine.org/] were user to create the graphical elements of the application. The spaceships, asteroids, gates and several other bitmaps used to create the sprite components of the game are from _Freepik_^[https://www.freepik.com/]. The background image was created by _ChatGPT_^[https://chatgpt.com/] and was slightly modified.

The first step was the creation of 30 scenarios (puzzles) to form the levels of the game. The first 17 levels have a single qubit and the available gates are Pauli-X, Pauli-Y, Pauli-Z and Hadamard. The remaining 13 levels have a two qubits and the available gates are Pauli-X, Pauli-Z and Hadamard. In each level there are 2, 4, or 8 different states in which the spaceship can be in, depending on the number of qubits and the available gates, as described in the previous sections. Each scenario consists of the initial state of the qubits (initial position of the spaceship), the target state (positions of the target asteroids), the available gates and the minimum number of gates to be used to solve the puzzle. The scenarios are encoded in a YAML file in a manner that is human-readable while allowing for easy addition of new levels.

![Screenshot from Level 30.](chapter-6/image005_level_30.jpg){#fig:fig605 height=50%}

By the first week of December, the basic elements of the user interface were in place and the spaceship control mechanism was working. Then, user testing was conducted to refine the prototype, involving 5 users. Based on their feedback, the following corrections were made:

1. A graphical element was created to represent a quantum register with one or two outputs, replacing the discrete qubits. The outputs of the register represent the first or the second qubit.

2. The apply button has been removed. The gate action is applied to the register as soon as one of the register outputs is selected.

3. Targets were replaced with asteroids.

4. An overlay has been added to show the current level ID, gate used and missiles launched.

5. The target state display has been changed to make it easier of the player to understand where they need to place their spaceship.

Also, the quiz-related screens and the 'Tutorial' screen were partially implemented, theory slides were added at the beginning of some levels and help overlays were added on each level.

In the last week of December, Greek language support was added and the 'Tutorial' screen was finalized. Also, quiz questions were created, and the 'Quiz', 'Quiz Form', 'Quiz Results' and 'Quiz History' screens were finalized. The alpha version of our application was ready.

In the following days, several bugs were fixed, and UI issues were addressed after the application was tested by 2 regular users. In addition, the 'Settings' screen was finalized, and some missing translations were added. Finally, the project was restructured a bit, and some performance issues were fixed.

The application code has been published in the following GitHub repository: https://github.com/StelTheo73/qubity/. The application is available as an APK (for installation on Android devices) at the following link: https://github.com/StelTheo73/qubity/blob/main/release/qubity-1.0.0.apk.
