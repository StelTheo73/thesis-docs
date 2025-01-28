# Educational Game Development

TODO: CHANGE INTRO
In the previous chapters, we discussed gamification and presented the basic theory of quantum computing and some of the most well-known quantum gates. Next, we will present the educational game we designed to teach learners the concept of superposition and to familiarize them with the effects of some quantum games.

The game developed is called _Qubity_ and is a variant of the arcade video game _Space Invaders_. It combines the characteristics of a "Shoot 'em Up" game with puzzle solving. The game is aimed at university students, as some levels require knowledge of complex numbers to solve the puzzle. However, the levels present the necessary theory for solving the puzzle, so a player with a flair for mathematics could complete the level without having any knowledge of complex numbers, as demonstrated by the evaluation of the game.

## Game Description

The game consists of 30 levels, in which the player is asked to solve a puzzle using certain quantum gates -a subset of those presented in chapter 6. The player operates a spaceship whose position is determined by the state of a quantum register. The player can change the position of the spaceship by manipulating a qubit with one of the available quantum gates.

The first 17 levels have a single qubit register and the available gates are Pauli-X, Pauli-Y, Pauli-Z and Hadamard. The remaining 13 levels have a 2-qubit register and the available gates are Pauli-X, Pauli-Z and Hadamard. In each level there are 2, 4, or 8 different states in which the spaceship can be in, depending on the number of qubits and the available gates.

![Screenshot from Level 16](chapter-7/image001_level_16.jpg){#fig:fig701 height=50%}

In each level, there are one or more asteroid targets. The player shall move the spaceship under the targets by altering the state of the register. Then, they have to destroy the asteroid by launching missiles. Several levels have more than one solution, but to score maximum points they must use the minimum number of gates and as few missiles as possible.

The game is accompanied by a 12-question quiz that allows players to test their knowledge gained by the game.

## Screens

### Home Screen

![Home Screen](chapter-7/image002_home_screen.jpg){#fig:fig702 height=50%}

From the app's home screen, the user can access the game levels, available spaceships, the quiz, a tutorial level and game settings.

### Levels

![Levels Screen](chapter-7/image003_levels_screen.jpg){#fig:fig703 height=50%}

On this screen the player can select any of the available levels. Each level's card shows the number of qubits, the available gates and the score.

### Spaceships

![Spaceships Screen](chapter-7/image004_spaceships_screen.jpg){#fig:fig704 height=50%}

From this screen the player can select one of the available spaceships. The spaceships are decorative in nature, as they all have the same capabilities, but are a reward for the player's progress in the game. Initially only 3 are available, new spaceships are unlocked after completing more levels.

### Quiz

< image >

![Quiz Screen](chapter-7/image005_quiz_screen.jpg){#fig:fig705 height=50%}

This screen gives access to the knowledge check quiz. The player can answer a short quiz or view their score from previous attempts. Each quiz consists of 12 questions, 3 theoretical and 9 related to quantum gates.

![Quiz Form](chapter-7/image006_quiz_form.jpg){#fig:fig706 height=50%}

![Quiz Results](chapter-7/image007_quiz_results.jpg){#fig:fig707 height=50%}

![Quiz History](chapter-7/image008_quiz_history.jpg){#fig:fig708 height=50%}

### Tutorial

![Tutorial Screen](chapter-7/image009_tutorial.jpg){#fig:fig709 height=50%}

This screen loads a tutorial level, for which no score is calculated. First, a few slides are presented with basic quantum computing theory. In particular, the player is introduced to basic theory around qubits, quantum registers and quantum gates, as well as the concept of superposition. The slides consist of short sentences that summarize the theory discussed in chapter 6. Then there are 4 overlays with instructions, which demonstrate to the player how to use the gates to control the spaceship and how to destroy the asteroids.

### Settings

![Settings Screen](chapter-7/image010_settings_screen.jpg){#fig:fig710 height=50%}

From this screen, the user can choose between the available languages and delete their progress in the game. Available languages are English and Greek, with the former being the default.

## Levels

Each level has a different number of possible states, depending on the available gates and the number of qubits.

At the beginning of some levels, there are some slides with theory about the quantum gates available in this level. The first levels are very simple, requiring only 1 use of a gate to put the register into the target state. As the game progresses, the number of gates and combinations increases. In some levels there are gates that do not to be used. The player needs to use what they have learned to solve the puzzle using the minimum number of gates.

![Theory Slide](chapter-7/image011_theory_slide.jpg){#fig:fig711 height=50%}

The first 9 levels introduce the Pauli Gates (X, Y and Z). In level 10, the theory of superposition is reintroduced to increase information retention. Also, Hadamard Gate (H) is introduced. In the next 7 levels, the player is asked to solve the puzzle by combining his previous knowledge of X and H gates.

From level 18, the number of qubits is increased to 2. From this level, no new theory is introduced; the player is just asked to combine their previous knowledge to solve the puzzles. In addition, the level of difficulty increases as the player has to decide which qubit to apply the gate to.

## Development

Development of the game began in November 2024. Google's [_Material Design 3_](https://m3.material.io/) and [_Flame Game Engine_](https://flame-engine.org/) were user to create the graphical elements of the application. The spaceships, asteroids, gates and several other bitmaps used to create the sprite components of the game are from [_Freepik_](https://www.freepik.com/). The background image was created by [_ChatGPT_](https://chatgpt.com/) and was slightly modified.

The first step was the selection of the quantum gates that would be presented in the game, and 30 scenarios were created to form the levels of the game. Each scenario consists of the initial state of the quantum register (initial position of the spaceship), the target state (positions of the target asteroids), the available gates and the minimum number of gates to be used to solve the puzzle. The scenarios are encoded in a YAML file in a manner that is human-readable while allowing for easy addition of new levels.

![Wireframe](chapter-7/image012_wireframe.png){#fig:fig712 height=50%}

![Screenshot from Level 30](chapter-7/image013_level_30.jpg){#fig:fig713 height=50%}

A prototype level was then designed in [_diagrams.net_](https://app.diagrams.net/), which formed the foundation for creating the game's graphical interface. As shown in the images above, the original approach did not include a graphical element for the quantum register, but rather 2 discrete qubits to which the quantum gate would be applied. There were also two buttons, one for applying the gate and one for launching the missiles. The target state was placed at the top of the screen. Finally, the targets were enemy spaceships, as in the original _Space Invaders_ game.

By the first week of December, the basic elements of the user interface were in place and the spaceship control mechanism was working. Then, user testing was conducted, involving 5 users. Based on their feedback, the following corrections were made:

1. A graphical element was created to represent a quantum register with one or two outputs, replacing the discrete qubits. The outputs of the register represent the first or the second qubit.

2. The apply button has been removed. The gate action is applied to the register as soon as one of the register outputs is selected.

3. Targets were replaced with asteroids.

4. An overlay has been added to show the current level ID, gate used and missiles launched.

5. The target state display has been changed to make it easier of the player to understand where they need to place their spaceship.

In the last week of December, Greek language support was added, the tutorial level was created, and theory slides were added at the beginning of some levels. Also, a help menu was added on each level. Finally, quiz questions were created, as well as the quiz menu, quiz and quiz history screens.

In the following days, several bugs were fixed and UI issues were addresses after the application was tested by 2 regular users.

## Score

In order to avoid the [common pitfall](#scoring-pitfall) that can lead to player frustration, no scoring system has been used to compare the player with other players. For each level, the player receives between half and three stars, with a perfect score of three. The optimal score is achieved by using exactly as many missiles as the targets of each level, and also by using as many gates as the optimal solution of each level requires.

To further motivate players as they progress through the game and complete levels, more spaceships become available as rewards. When a spaceship is unlocked, an informative toast is displayed.

![Level score & spaceship reward](chapter-7/image014_score_and_reward.jpg){#fig:fig714 height=50%}

## Quiz

To measure the educational value of the game, a 12-question quiz was designed. The quiz consists of 3 theoretical questions and 9 questions regarding quantum gates actions. The theoretical questions relate to the theory presented to the player via slides. The quantum gate questions ask the player to calculate the new state of a qubit after the gate has been applied to it, or ask the player to select the appropriate gate to perform a quantum calculation. The questions are designed to prove that the player has learned to use -some of- the gates introduced in chapter 6 and understands the concept of superposition.

## Evaluation

10 university students volunteered to participate in the evaluation of the game, which was carried out in 2 phases. The volunteers claimed to have a strong background in mathematics, with 4 of them having knowledge of complex numbers.

In the first phase, the game was shared with the players, and they were asked to complete the quiz before playing the game. Then, they were asked to complete the tutorial level and then complete the 30 levels of the game and retake the quiz. Players were given as much time as they wanted and were asked to record how long it took to complete the game. There was no further guidance on how the game works and no external help was provided to solve the levels. The results of the first evaluation phase are presented below:

![Statistical Analysis](chapter-7/image015_evaluation.jpeg){#fig:fig715 height=50%}

As shown in the graphs above, the average score on the quiz was 8.33% before playing the game and 85% after completing the game. It is clear that players improved their knowledge of quantum computing by playing the game.

Statistical analysis showed no correlation between the time required to complete the game and the improvement in the quiz score. The average time needed to complete the game was 21 minutes. This makes the game suitable to be played in the context of a college lecture to increase student engagement in the classroom or to allow students to test their knowledge in a fun and interactive way.

In the second phage, 8 out of 10 players from the fist phase participated in a focus group. The questions they were asked to discuss were related to 4 areas; _User Interface & User Experience_ (UI & UX), _Game Mechanics_, _Difficulty_ and _Scoring & Rewards_. They were also free to discuss with each other and comment on their overall experience of the application. Below are the focus group findings by area:

### User Interface & User Experience

- One player requested an extra slide in the tutorial or in the first level, explaining how each level's score is calculated.

- One player requested that the _Next Level_ button should be a different color to others (on the level completion overlay).

- One player requested to group levels in the level selection menu by difficulty.

- Players agreed that the game menu was east to use and that the navigation worked well and was predictable.

- Players agreed that the state of the application was flawless and was updating correctly.

- Some players requested to add background music and sounds when launching missiles and hitting the targets.

### Game Mechanics

- Players found the mechanics simple and casual and commented that this simplicity helped them focus on solving the puzzles.

### Difficulty

- Players agreed that the game is easy and intended of users with no quantum computer experience. All of them could complete all 30 levels. They said they would like to try more difficult puzzles.

- Most players said that the hardest level was level 30 (the final one), as it required a combination of 3 gates to solve the puzzle.

- One player did not understand how the Hadamard gate acts on 2 qubits. Half of the players said they would like more information about superposition, but agreed that the theory presented was sufficient to solve the puzzles.

- One player suggested that there should be hints to use in case you find it difficult to solve the puzzle.

### Scoring & Rewards

- Players agreed that having a score system encouraged them to improve. 7 out of 8 players tried to complete all levels with 3 stars.

- Players agreed that they felt rewarded and motivated to keep playing by unlocking new spaceships as they progressed.

## Conclusions

Based on the feedback and data collected from the initial evaluation and focus group, several conclusions can be drawn:

1. The number of participants is small, only 10 people, so a complementary evaluation phase with a larger number of participants is suggested, for more reliable conclusions. However, the result of the initial evaluation is promising.

2. The duration of the game makes it suitable to be used as a teaching tool in the context of a lecture.

3. The UX should be improved, based on the feedback from the focus group.

4. The theory around superposition should be extended.

5. The game could be extended with more levels and quantum gates.
