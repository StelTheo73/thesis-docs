# Evaluation

In order to measure the learning outcome of the game and to evaluate the user experience, the evaluation process described in the diagram above was designed. More specifically, this process was designed to evaluate the achievement of the objectives set out in Chapter 1, namely:

1. The game to be an effective learning tool and to successfully introduce the basic concepts of quantum computing to university students.

2. The game should be enjoyable and simple so as not to distract the student from the learning objective.

3. The game should be short and require no additional equipment other than a mobile phone, making it suitable to be played during a university lecture or when the student has limited time.

## Evaluation Process Description

![Evaluation Flow](chapter-7/image005_evaluation_flow.png){#fig:fig705 height=50%}

10 university students volunteered to participate in the evaluation of the game, which was carried out in 2 phases. The volunteers claimed to have a strong background in mathematics, with 4 of them having knowledge of complex numbers. The first phase used the pre-post test methodology, for which a quiz was designed and incorporated into the game. The second phase was a focus group with some participants from the first phase.

To support the first phase and the implementation of the quiz, we relied on _Cooksey and Jonsson_ [-@cooksey-jonsson-pre-post] and _Stratton_ [-@stratton-pre-post]. The first step was to create a repository of candidate questions to help structure the quiz. These questions were mainly taken from comprehension quizzes given in the _Quantum Computation_ course at the University of Patras (academic year 2023-24, lecturers: Sgarbas, K. and Kounavis, P.). A subset of these questions was then selected and adapted to the content of the game. The quiz consists of 3 theoretical questions and 9 questions regarding quantum gates actions. Each correct answer awards one point, while each incorrect answer gives zero points. The theoretical questions relate to the theory presented to the player via slides. The quantum gates related questions ask the player to calculate the new state of a qubit after the gate has been applied to it, or ask the player to select the appropriate gate to perform a quantum calculation. The questions are designed to prove that the player has learned to use -some of- the gates introduced in chapter 4 and understands the concept of superposition.

As suggested in the literature, participants were asked to complete the pre-test before interacting with the game to get an overview of their previous knowledge. Then, they were asked to complete the tutorial level and then complete the 30 levels of the game and retake the quiz. Players were given as much time as they wanted and were asked to record how long it took to complete the game. There was no further guidance on how the game works and no external help was provided to solve the levels. The _Normalized Gain_ metric was used to measure efficiency, as suggested in the literature [@cooksey-jonsson-pre-post], [@kagan-normalized-gain]. In addition, we tried to determine whether the knowledge of complex numbers and the time it took each player to complete the game affected the learning outcome.

In the second phase, 8 out of 10 players from the fist phase participated in the focus group. The questions they were asked to discuss were related to 4 areas; _User Interface & User Experience_ (UI & UX), _Game Mechanics_, _Difficulty_ and _Scoring & Rewards_. They were also free to discuss with each other and comment on their overall experience of the application. The findings from the focus group will be used to improve the game in the future.

The focus group took place two days after the completion of the pre-post test. It was conducted via Zoom meeting, lasted about 1 hour and was neither recorded nor transcribed. The focus group had no strict structure. The users were free to discuss each of the 4 areas tested for about 10 to 12 minutes per area under the supervision of the researcher who took notes. Follow-up questions were then asked for clarification. In addition, the supervisor encouraged individuals who were not participating as actively to share their views. [@rabiee-focus-group], [@wilkinsos-focus-group]

## Normalized Gain and Average Normalized Gain

The _Normalized Gain_ metric is used to measure the effectiveness of a learning tool. It is calculated as the ratio of the actual average gain to the maximum possible gain.

The _Normalized Gain_ for each individual player is calculated as follows:

$$
g = \frac{post\% - pre\%}{100\% - pre\%}
$$

The _Average Normalized Gain_ is defined as:

$$
\langle g \rangle = \frac{\langle post\% \rangle - \langle pre\% \rangle }{100\% - \langle pre\% \rangle}
$$

where the brackets indicate the averages. [@cooksey-jonsson-pre-post], [@kagan-normalized-gain]

## Phase 1: Pre-Post Test

In this section we will present the results of the Pre-Post Test. Unfortunately, we do not have that many participants to perform statistical analysis, so we will present the results quantitatively.

![Score Improvement](chapter-7/image001_scores_no_stat.png){#fig:fig701 height=40%}

In the image above we can see the players' score in the quiz before playing the game (blue - left bars) and the players' score after they completed the game (orange - right bars). We can observe a significant improvement in players' scores after completing the game. For instance, the average player score before the game was close to 17% and after the game it was over 70%. This is an encouraging result and an indication that the game is effective as a learning tool.

![Correlation between Initial and Final Scores](chapter-7/image002_score_correlation_no_stat.png){#fig:fig702 height=40%}

As part of the analysis of the results, we asked the following question; Does the initial score - and therefore any prior knowledge of the players - affect the final score? In the plot above, we attempt to correlate the initial score with the final score. We observe a moderate positive correlation between the two variables, but due to the small number of participants we cannot draw any definite conclusions.

![Correlation between Duration and Final Scores](chapter-7/image003_duration_correlation_no_stat.png){#fig:fig703 height=40%}

We then examined whether the time taken by players to complete the game affected their understanding of the object and thus their final score. In the previous plot, we observe a weak positive correlation between the two variables, but again, due to the small number of participants, we cannot draw any definite conclusions.

![Gain of Averages](chapter-7/image006_average_gain.png){#fig:fig701 height=40%}

The average normalized gain ($\langle g \rangle$) of 0.69 indicates a substantial improvement in the players' knowledge after playing the game. According to the literature, an average gain above 0.25 is considered effective [@cooksey-jonsson-pre-post], making this result particularly significant. This demonstrates the game's effectiveness as an educational tool and highlights its potential to significantly enhance learning outcomes.

## Phase 2: Focus Group

In this section we will present the focus group findings by area.

### User Interface & User Experience

- One player requested an extra slide in the tutorial or in the first level, explaining how each level's score is calculated.

- One player requested that the _Next Level_ button should be a different color to others (on the level completion overlay).

- One player requested to group levels in the level selection menu by difficulty.

- Players agreed that the game menu was easy to use and that the navigation worked well and was predictable.

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

1. The game is an effective learning tool and successfully introduces the basic concepts of quantum computing to university students. The difference between the pre and post test scores and the _Average Normalized Gain_ of 0.69 indicates a substantial improvement in the players' knowledge after playing the game.

2. The average time it took players to complete the game - excluding the quiz - was 21 minutes. This is a good indication that the game is short and can be played during a university lecture or when the student has limited time.

3. The game is enjoyable, and the players found the mechanics simple and casual. The navigation works well and is predictable. The state of the application was flawless and was updating correctly.

4. The difficulty was advantageous for the target audience, but some players requested more difficult puzzles. The players agreed that the game is easy, intended for users with no experience around Quantum Computing.

5. The incentive system used in the game was found to be motivating and encouraged players to improve.

Overall, the evaluation process was successful and provided valuable feedback that will be used to improve the game in the future. The research objectives are met, and the game can be considered a successful educational tool. The game should be further expanded to include more levels, more complex puzzles, and additional features to enhance the user experience.
