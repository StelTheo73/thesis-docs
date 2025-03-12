# Appendix A: Game Screens Presentation

In the previous chapter, we analyzed the conceptual design of our application, defined the development process and evaluation process, and described the development timeline. This chapter focuses on the visual and functional aspects of the game screens. We will present each screen in detail, explaining its purpose and how it contributes to the overall user experience. By understanding the design and functionality of these screens, readers will gain a comprehensive view of how the application operates and how users interact with it.

## Home {.unnumbered}

![Home Screen.](chapter-8-appendix-A/image002_home_screen.jpg){#fig:fig802 height=50%}

From the app's home screen, the user can access the game levels, available spaceships, the quiz, a tutorial level and game settings.

## Tutorial Level {.unnumbered}

![Tutorial Level Screen.](chapter-8-appendix-A/image009_tutorial.jpg){#fig:fig809 height=50%}

This screen loads a tutorial level, for which no score is calculated. First, a few slides are presented with basic quantum computing theory. In particular, the player is introduced to basic theory around qubits, quantum registers and quantum gates, as well as the concept of superposition. The slides consist of short sentences that summarize the theory discussed in chapter 4. Then there are 4 overlays with instructions, which demonstrate to the player how to use the gates to control the spaceship and how to destroy the asteroids.

## Level Selection {.unnumbered}

![Level Selection Screen.](chapter-8-appendix-A/image003_levels_screen.jpg){#fig:fig803 height=50%}

On this screen the player can select any of the available levels. Each level's card shows the number of qubits, the available gates and the score.

## Level {.unnumbered}

![Level Screen.](chapter-8-appendix-A/image001_level_16.jpg){#fig:fig801 height=50%}

In each level, there are one or more asteroid targets. The player shall move the spaceship under the targets by altering the state of the register. Then, they have to destroy the asteroid by launching missiles. Several levels have more than one solution, but to score maximum points they must use the minimum number of gates and as few missiles as possible. Each level has a different number of possible states, depending on the available gates and the number of qubits.

At the beginning of some levels, there are some slides with theory about the quantum gates available in this level. The first levels are very simple, requiring only 1 use of a gate to put the register into the target state. As the game progresses, the number of gates and combinations increases. In some levels there are gates that do not to be used. The player needs to use what they have learned to solve the puzzle using the minimum number of gates.

![Theory Slide.](chapter-8-appendix-A/image011_theory_slide.jpg){#fig:fig811 height=50%}

The first 9 levels introduce the Pauli Gates (X, Y and Z). In level 10, the theory of superposition is reintroduced to increase information retention. Also, Hadamard Gate (H) is introduced. In the next 7 levels, the player is asked to solve the puzzle by combining his previous knowledge of X and H gates.

From level 18, the number of qubits is increased to 2. From this level, no new theory is introduced; the player is just asked to combine their previous knowledge to solve the puzzles. In addition, the level of difficulty increases as the player has to decide which qubit to apply the gate to.

## Spaceship Selection {.unnumbered}

![Spaceships Seection Screen.](chapter-8-appendix-A/image004_spaceships_screen.jpg){#fig:fig804 height=50%}

From this screen the player can select one of the available spaceships. The spaceships are decorative in nature, as they all have the same capabilities, but are a reward for the player's progress in the game. Initially only 3 are available, new spaceships are unlocked after completing more levels.

## Quiz {.unnumbered}

![Quiz Screen.](chapter-8-appendix-A/image005_quiz_screen.jpg){#fig:fig805 height=50%}

The game is accompanied by a 12-question quiz, used for the evaluation process, as described in the previous chapter. This screen gives access to the quiz. The player can take a quiz or view their score from previous attempts.

![Quiz Form Screen.](chapter-8-appendix-A/image006_quiz_form.jpg){#fig:fig806 height=50%}

![Quiz Results Screen.](chapter-8-appendix-A/image007_quiz_results.jpg){#fig:fig807 height=50%}

![Quiz History Screen.](chapter-8-appendix-A/image008_quiz_history.jpg){#fig:fig808 height=50%}

## Settings {.unnumbered}

![Settings Screen.](chapter-8-appendix-A/image010_settings_screen.jpg){#fig:fig810 height=50%}

From this screen, the user can choose between the available languages and delete their progress in the game. Available languages are English and Greek, with the former being the default.
