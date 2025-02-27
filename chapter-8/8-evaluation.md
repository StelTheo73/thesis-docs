# Evaluation

In order to measure the learning outcome of the game and to evaluate the user experience, the evaluation process described in the diagram above was designed. More specifically, this process was designed to evaluate the achievement of the objectives set out in Chapter 1, namely:

1. The game to be an effective learning tool and to successfully introduce the basic concepts of quantum computing to university students.

2. The game should be enjoyable and simple so as not to distract the student from the learning objective.

3. The game should be short and require no additional equipment other than a mobile phone, making it suitable to be played during a university lecture or when the student has limited time.

## Evaluation Process Description

![Evaluation Flow](chapter-8/image005_evaluation_flow.png){#fig:fig805 height=50%}

10 university students volunteered to participate in the evaluation of the game, which was carried out in 2 phases. The volunteers claimed to have a strong background in mathematics, with 4 of them having knowledge of complex numbers. The first phase used the pre-post test methodology, for which a quiz was designed and incorporated into the game. The second phase was a focus group with some participants from the first phase.

To support the first phase and the implementation of the quiz, we relied on _Cooksey and Jonsson_ [-@cooksey-jonsson-pre-post] and _Stratton_ [-@stratton-pre-post]. The first step was to create a repository of candidate questions to help structure the quiz. These questions were mainly taken from comprehension quizzes given in the _Quantum Computation_ course at the University of Patras (academic year 2023-24, lecturers: Sgarbas, K. and Kounavis, P.). A subset of these questions was then selected and adapted to the content of the game. The quiz consists of 3 theoretical questions and 9 questions regarding quantum gates actions. Each correct answer awards one point, while each incorrect answer gives zero points. The theoretical questions relate to the theory presented to the player via slides. The quantum gate questions ask the player to calculate the new state of a qubit after the gate has been applied to it, or ask the player to select the appropriate gate to perform a quantum calculation. The questions are designed to prove that the player has learned to use -some of- the gates introduced in chapter 4 and understands the concept of superposition.

As suggested in the literature, participants were asked to complete the pre-test before interacting with the game to get an overview of their previous knowledge. Then, they were asked to complete the tutorial level and then complete the 30 levels of the game and retake the quiz. Players were given as much time as they wanted and were asked to record how long it took to complete the game. There was no further guidance on how the game works and no external help was provided to solve the levels. The _Normalized Gain_ metric was used to measure efficiency, as suggested in the literature [@cooksey-jonsson-pre-post], [@kagan-normalized-gain]. In addition, we tried to determine whether the knowledge of complex numbers and the time it took each player to complete the game affected the learning outcome.

In the second phase, 8 out of 10 players from the fist phase participated in the focus group. The questions they were asked to discuss were related to 4 areas; _User Interface & User Experience_ (UI & UX), _Game Mechanics_, _Difficulty_ and _Scoring & Rewards_. They were also free to discuss with each other and comment on their overall experience of the application. The findings from the focus group will be used to improve the game in the future.

## Phase 1: Statistical Analysis of Quiz Results

In this section, we analyze the quiz results using statistical methods to evaluate the effectiveness of the game as a learning tool. Key metrics used in this analysis include the p-value, Pearson correlation coefficient, and Average Normalized Gain.

- **P-value**: The null hypothesis in this context is the assumption that there is no significant difference between the initial and final quiz scores of the participants. It suggests that any observed difference in scores is due to random chance rather than the effectiveness of the game as a learning tool. The p-value is used to test this hypothesis, with a lower p-value indicating stronger evidence against the null hypothesis.

- **Pearson Correlation Coefficient (Pearson r)**: A measure of the linear correlation between two variables, ranging from -1 to 1. A value closer to 1 indicates a strong positive correlation, while a value closer to -1 indicates a strong negative correlation. A value close to 0 indicates that there is little to no linear correlation between the two variables.

- **Average Normalized Gain ($\langle g \rangle$)**: A metric used to measure the effectiveness of an educational process, calculated as the ratio of the actual average gain to the maximum possible average gain. A higher value indicates greater effectiveness.

The normalized gain for each individual player is calculated as follows:

$$
g = \frac{post\% - pre\%}{100\% - pre\%}
$$

The Average Normalized Gain is defined as:

$$
\langle g \rangle = \frac{\langle post\% \rangle - \langle pre\% \rangle }{100\% - \langle pre\% \rangle}
$$

where the brackets indicate the averages. [@cooksey-jonsson-pre-post], [@kagan-normalized-gain]

![Significance of Score Improvement](chapter-8/image001_scores.png){#fig:fig801 height=40%}

![Correlation between Initial and Final Scores](chapter-8/image002_score_correlation.png){#fig:fig802 height=40%}

![Correlation between Duration and Final Scores](chapter-8/image003_duration_correlation.png){#fig:fig803 height=40%}

![Impact of Knowledge of Complex Numbers on Final Scores](chapter-8/image004_complex_numbers.png){#fig:fig804 height=40%}

![Gain of Averages](chapter-8/image006_average_gain.png){#fig:fig801 height=40%}

1. **Significance of Score Improvement (p-value: 0.0)**:
    The p-value of 0.0 indicates that the difference between the initial and final scores is extremely statistically significant. This means that the observed difference in scores is highly unlikely to have occurred by chance, and there is strong evidence to suggest that the intervention or factor being tested had a significant impact on the scores.

2. **Correlation between Initial and Final Scores (Pearson r: 0.51)**:
    The Pearson correlation coefficient of 0.51 indicates a moderate positive correlation between the initial and final scores. This suggests that players who had higher initial scores also tended to have higher final scores, but the relationship is not very strong. There are other factors that might be influencing the final scores.

3. **Correlation between Duration and Final Scores (Pearson r: 0.16)**:
    The Pearson correlation coefficient of 0.16 indicates a weak positive correlation between the duration and final scores. This suggests that the amount of time spent on the task has a minimal impact on the final scores. Other factors are likely more influential in determining the final scores.

4. **Impact of Knowledge of Complex Numbers on Final Scores (p-value: 0.0648)**:
    The p-value of 0.0648 is slightly above the common significance threshold of 0.05. This means that there is not enough evidence to conclude that there is a statistically significant difference in the average final scores between those who know complex numbers and those who don't at the 5% significance level.

5. **Average Normalized Gain ($\langle g \rangle$) of 0.69**:
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

## Final Conclusions

Based on the feedback and data collected from the initial evaluation and focus group, several conclusions can be drawn:

1. The difference between the initial and final scores is extremely statistically, as indicated by the p-value of 0.0.

2. There is a moderate positive correlation between initial and final scores, suggesting that initial performance is somewhat predictive of final performance.

3. The duration of the task has a weak correlation with final scores, indicating that time spent is not a strong predictor of performance.

4. Knowledge of complex numbers does not show a statistically significant difference in final scores at the 5% significance level, but the result is close to being significant and might be considered at a higher threshold.

5. The average time needed to complete the game was 21 minutes. This makes the game suitable to be played in the context of a college lecture to increase student engagement in the classroom or to allow students to test their knowledge in a fun and interactive way.

6. The average normalized gain ($\langle g \rangle$) of 0.69 demonstrates the game's effectiveness as an educational tool.

7. The number of participants is small, only 10 people, so a complementary evaluation phase with a larger number of participants is suggested, for more reliable conclusions. However, the result of the initial evaluation is promising.

8. The duration of the game makes it suitable to be used as a teaching tool in the context of a lecture.

9. The theory around superposition should be extended.

10. The game could be extended with more levels and quantum gates.
