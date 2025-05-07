# Evaluation

Building on the conceptual design and development process described in Chapter 6, this chapter focuses on evaluating the application against the objectives we set in chapter 1, namely:

1. The game to be an effective learning tool and to successfully introduce the basic concepts of quantum computing to university students.

2. The game should be enjoyable and simple so as not to distract the student from the learning objective.

3. The game should be short and require no additional equipment beyond a mobile phone, making it an effective learning tool that can be utilized during a university lecture or when students have limited time.

The evaluation process uses a mix of methods and is divided into two parts: the first part evaluates the learning outcome of the game, while the second part evaluates the interactive system and the game experience. The evaluation of the learning outcome is based on a Pre-Post Tests methodology, while the evaluation of the interactive system and game experience are based on questionnaires and a focus group. To evaluate the application as an interactive system, we used the _System Usability Scale_ questionnaire, while to evaluate the game experience we used the shortened version of the _Game User Experience Satisfaction Scale_ questionnaire, the _GUESS-18_.

In addition to the aforementioned objectives, evaluating the application as an interactive system and as a game will allow us to determine whether the GBL mechanisms and elements we have incorporated into the game, namely:

1. Combination of Puzzle & Shooter mechanics

2. Narratives at the beginning of some levels

3. Incentive system

4. Graceful failure mechanism

are effective and create an enjoyable gaming experience.

Finally, we aimed to examine whether the application enhances information retention. To this end, we repeated the Post Test 2 weeks after the initial tests.

_Figure 7.1_ shows the evaluation process we followed.

![Evaluation Process.](chapter-7/image001_evaluation_flow.png){#fig:fig701 height=50%}

A group of undergraduate university students, totaling 23, volunteered to participate in the evaluation of the game, all of whom claimed to have a strong background in mathematics.

Quiz questions are available in the _Appendix B_ section of this thesis. Both SUS and GUESS-18 questionnaires are available in the _Appendix C_ section of this thesis.

## Evaluation Process Description

### Evaluation of Learning Outcome

The first phase of the evaluation was based on the Pre-Post approach, as described by _Cooksey and Jonsson_ [-@cooksey-jonsson-pre-post] and _Stratton_ [-@stratton-pre-post]. We started by creating a repository of candidate questions to help structure the quiz. These questions were mainly taken from comprehension quizzes given in the _Quantum Computation_ course at the University of Patras (academic year 2023-24, lecturers: Sgarbas, K. and Kounavis, P.). A subset of these questions was then selected and adapted to the content of the game. The quiz consists of 3 theoretical questions and 9 questions regarding quantum gates actions. Each correct answer awards one point, while each incorrect answer gives zero points. The theoretical questions relate to the theory presented to the player via slides. The quantum gates related questions ask the player to calculate the new state of a qubit after the gate has been applied to it, or ask the player to select the appropriate gate to perform a quantum calculation. The questions are designed to prove that the player has learned to use -some of- the gates introduced in chapter 4 and understands the concept of superposition.

As suggested by _Cooksey and Jonsson_ [-@cooksey-jonsson-pre-post] and _Stratton_ [-@stratton-pre-post], participants were asked to complete the Pre Test before interacting with the game to get an overview of their previous knowledge. Then, they were asked to complete the tutorial level and then complete the 30 levels of the game and retake the quiz. Players were given as much time as they wanted and were asked to record how long it took to complete the game, from the moment they started playing the tutorial level until the moment they completed the last level. The time spent on the quiz was not included in this measurement. There was no further guidance on how the game works and no external help was provided to solve the levels. The _Normalized Gain_ metric was used to measure efficiency, as suggested by _Cooksey and Jonsson_ [-@cooksey-jonsson-pre-post] and _McKagan, Sayre and Madsen_ [-@kagan-normalized-gain].

### Evaluation of the Interactive System

The participants who completed the Pre-Post Tests were asked to answer the SUS questionnaire.

SUS is a 10-item, 5-point Likert scale questionnaire that measures the usability of a system. The items are scored on a scale from 1 to 5, with 1 being "strongly disagree" and 5 being "strongly agree". The scores are then converted to a score out of 100. Half of the items are positively worded and half are negatively worded. The positively worded items are scored by subtracting 1 from the score, while the negatively worded items are scored by subtracting the score from 5. The scores for each item are then summed and multiplied by 2.5 to convert them to a score out of 100. The SUS score is not a percentage, but it can be interpreted as a percentage for comparison purposes. A score of 68% is considered average, while a score above 80% is considered excellent. [@brooke-sus; @bangor-sus]

### Evaluation of the Game Experience

After completing the SUS questionnaire, the participants were asked to answer the GUESS-18 questionnaire. The GUESS-18 is a shortened version of the GUESS questionnaire, and is an 18-item, 7-point Likert scale questionnaire that measures the game experience. We chose the shortened version to prevent survey fatigue. The items are scored on a scale from 1 to 7, with 1 being "strongly disagree" and 7 being "strongly agree". The scores are then converted to a score out of 100. The GUESS-18 questionnaire is divided into 9 subscales. Each subscale has its own score, which can be used to measure the overall game experience. [@phan-guess; @keebler-guess-18]

### Focus Group

A subset of 8 participants from the initial 23 players took part in the focus group. The discussion focused on four key areas: _User Interface & User Experience_ (UI & UX), _Game Mechanics_, _Difficulty_, and _Scoring & Rewards_. Participants were also encouraged to share their overall impressions of the application and engage in open discussions with one another. Insights gathered from the focus group will inform future improvements to the game. The questions they were asked to discuss were related to 4 areas; _User Interface & User Experience_ (UI & UX), _Game Mechanics_, _Difficulty_ and _Scoring & Rewards_. They were also free to discuss with each other and comment on their overall experience of the application. The findings from the focus group will be used to improve the game in the future.

The focus group was conducted via Zoom meeting, lasted about 1 hour and was neither recorded nor transcribed. The focus group had no strict structure. The users were free to discuss each of the 4 areas tested for about 10 to 12 minutes per area under the supervision of the researcher who took notes. Follow-up questions were then asked for clarification. In addition, the supervisor encouraged individuals who were not participating as actively to share their views. [@rabiee-focus-group; @wilkinson-focus-group]

### Retention Test

Two weeks after the first evaluation, the participants were asked to complete the same quiz they had completed in the first evaluation. A subset of 10 participants from the initial 23 players took part in this test. The aim of this test was to measure the retention of knowledge acquired through the game. The participants were asked to complete the quiz without playing the game again, and they were not given any additional information about the quiz or the game. The time spent on the quiz was not included in this measurement. The results of this test will be compared with the results of the first Pre Test to determine whether the game has a positive effect on information retention.

## Results

In this section we present the results of the evaluation process described in _Section 7.1_. The results are divided into four sections: _Learning Outcome_, _Interactive System_, _Game Experience_ and _Focus Group_. Each section presents the results of the evaluation process and discusses the findings. Because of the small sample size, we do not perform any statistical analysis of the results. The results are presented qualitatively and also in graphical form, to help visualize the findings.

### Learning Outcome

To measure the effectiveness of the application as a learning tool, we used the _Normalized Gain_ metric. It is calculated as the ratio of the actual average gain to the maximum possible gain.

The _Normalized Gain_ [@cooksey-jonsson-pre-post; @kagan-normalized-gain] for each individual player is calculated as follows:

$$
g = \frac{post\% - pre\%}{100\% - pre\%}
$$

Where:

* $pre\%$: player\'s score in the quiz before playing the game (Pre Test)

* $post\%$: player\'s score in the quiz after playing the game (Post Test)

* $100\% - pre\%$: maximum possible gain, since score is capped at 100%

The _Average Normalized Gain_ is defined as:

$$
\langle g \rangle = \frac{\langle post\% \rangle - \langle pre\% \rangle }{100\% - \langle pre\% \rangle}
$$

Where:

* $\langle pre\% \rangle$: average score of all players in the quiz before playing the game (Pre Test)

* $\langle post\% \rangle$: average score of all players in the quiz after playing the game (Post Test)

![Score Improvement.](chapter-7/image002_scores.png){#fig:fig702 height=40%}

![Correlation between Pre Test and Post Test Scores.](chapter-7/image004_score_scatter.png){#fig:fig703 height=40%}

In _Figure 7.2_ we can see the players\' score in the quiz before playing the game (blue - left bars) and the players\' score after they completed the game (orange - right bars). We can observe a significant improvement in players\' scores after completing the game. For instance, the average player score before the game was about 17% and after the game it was slightly above 75%. This is an encouraging result and an indication that the game is effective as a learning tool.

Participants who scored above 90% had attended university courses in Physics and Computer Science, making them more familiar with concepts such as superposition, gates, and registers. The two participants with the lowest performance in the Post Test had the same level of mathematical knowledge as the others but had not attended courses in Physics or Computer Science. The remaining participants had the same level of mathematical knowledge and had attended Computer Science courses but did not have the same academic background in Physics as those who achieved a Post Test score above 90%.

We can assume that the highest quiz scores were achieved by those with a strong academic background in Physics and Computer Science, as the concepts examined in the quiz are more closely related to those taught in Physics and Computer Science courses. This hypothesis can be supported by the findings of the focus group, where several users asked for additional information on the concept of superposition. Finally, as part of the analysis of the results, we also asked the following question; Does the initial score - and therefore any prior knowledge of the players - affect the final score? In _Figure 7.3_, we attempt to correlate the initial score with the final score. We observe a moderate positive correlation between the two variables, but due to the small number of participants we cannot draw any definite conclusions.

![Correlation between Duration and Post Test Scores.](chapter-7/image005_duration_scatter.png){#fig:fig704 height=40%}

The average time it took the players to complete the game was 18 minutes. We then examined whether the time taken by players to complete the game affected their understanding of the object and thus their final score. In _Figure 7.4_, we observe a weak positive correlation between the two variables, but again, due to the small number of participants and the high level of variance, we cannot draw any definite conclusions.

![Normalized Gain.](chapter-7/image003_gain.png){#fig:fig705 height=40%}

The _Average Normalized Gain_ ($\langle g \rangle$) of 0.7 indicates a substantial improvement in the players\' knowledge after playing the game. According to the literature, an average gain above 0.25 is considered effective [@cooksey-jonsson-pre-post], making this result particularly significant. This demonstrates the game\'s effectiveness as an educational tool and highlights its potential to significantly enhance learning outcomes.


Finally, we performed a t-test^[https://www.statskingdom.com/paired-t-test-calculator.html] to compare the Pre Test and Post Test Scores. The Null Hypothesis ($H_0$) states that there is no significant difference between the two means, while the Alternative Hypothesis ($H_1$) states that there is a significant difference. The t-test results in a $t-value$ of $15.591$ and a $p-value$ of less than $0.001$ for a Significance Level $a = 0.05$, indicating that we can reject the Null Hypothesis with high confidence and conclude that the difference between the means is statistically significant. This further supports the effectiveness of the game as a learning tool.

### Interactive System

As described in _Section 7.1.2_, we used the _SUS_ questionnaire to evaluate the usability of the application. The SUS score for each participant is calculated using the following formula [@lewis-sus]:

$$
SUS = 2.5 (20 + \sum {(w_{01}, w_{03}, w_{05}, w_{07}, w_{09})} - \sum {(w_{02}, w_{04}, w_{06}, w_{08}, w_{10})})
$$

Where $w_{i}$ is the weight of the answer to the _i-th_ question (1-5).

To determine the overall SUS score, we calculate the average SUS score across all participants using the formula:

$$
\langle SUS \rangle = \frac{1}{N} \sum_{i=1}^{N} SUS_{i}
$$

Where $N$ is the number of participants and $SUS_{i}$ is the SUS score of the _i-th_ participant.

The SUS score of our application is 86.33, which is classified as _Excellent_ on the _Bangor adjective rating scale_ [-@bangor-sus] and corresponds to the highest grade, _A+_, on the _Sauro-Lewis curved rating scale_ [-@sauro-sus; -@sauro-lewis-sus]. These results indicate that the application is highly usable and provides a positive user experience. The findings will be compared with the focus group findings.

### Game Experience

As described in _Section 7.1.3_, we used the _GUESS-18_ questionnaire to evaluate the game experience. The ratings within each subscale are averaged to obtain a subscale score, and the composite score of game satisfaction can be calculated by summing subscale scores together. The minimum composite score is 9 and the maximum is 63. The answer to the question _“I feel bored while playing the game” _ in the _Enjoyment_ subscale needs to be reverse coded (i.e. subtract the score from 8). The scores were calculated using the spreadsheet created by _Keebler et al._ [-@keebler-guess-18]. The polygon chart in _Figure 7.7_ was created using the same spreadsheet.

![GUESS-18 Subscale Score.](chapter-7/image008_guess_score.png){#fig:fig706 height=40%}

![GUESS-18 Subscale Score - Polygon Chart.](chapter-7/image009_guess_chart.png){#fig:fig707 height=40%}

The high scores on the _Visual Aesthetics_ (6.4) and _Enjoyment_ (6.2) subscales indicate that the game was enjoyable, fun, and had well-designed and consistent graphics.

The game scored 6 on the _Usability_ subscale, indicates that the game was easy to use and navigate, which is consistent with the SUS questionnaire score.

Furthermore, the score on the _Personal Gratification_ subscale, which is very close to 6, indicates that players felt satisfied playing the game, which is consistent with the high score on the _Enjoyment_ subscale, while indicating that the game\'s incentive system was effective.

The score for the _Creative Freedom_ subscale (5.4) is satisfactory, as players were able to choose how to solve the game\'s problems, which is consistent with the approach of the graceful failure mechanism incorporated into the game. The score for the _Narratives_ subscale (5.3) indicates that players found the stories incorporated into the games useful, but could be more interesting and add more value to the game.

A relatively lower score on _Play Engrossment_ subscale (3.9) indicates that players were not fully immersed or focused on the gameplay. This could be an area for improvement, perhaps by enhancing the challenge or adding more dynamic elements.

A moderate score on the _Social Connectivity_ subscale (3.9) is expected, since the game is a single-player game and does not have any social features. Finally, the lowest possible score on the _Audio Aesthetics_ subscale (1), is expected, since the game does not have any audio features.

These findings will be compared with the focus group findings.

### Focus Group

The focus group findings align closely with the results of the GUESS-18 questionnaire, highlighting both strengths and areas for improvement in the game experience.

The high scores on the _Visual Aesthetics_ and _Enjoyment_ subscales of the questionnaire are consistent with the focus group feedback, where players praised the simplicity of the mechanics and the ease of navigation. Similarly, the _Usability_ subscale score aligns with the focus group’s positive remarks about the flawless state of the application and predictable navigation. The high score on the _Personal Gratification_ subscale indicates that players felt satisfied and motivated by the game\'s reward mechanisms. This is consistent with the focus group findings, where players agreed that the incentive system encouraged them to improve and that unlocking spaceships provided a sense of reward and motivation to continue playing.

On the other hand, the relatively low scores on _Play Engrossment_ and _Audio Aesthetics_ are echoed in the focus group’s suggestions to add background music and sound effects to enhance immersion. Additionally, the request for more challenging puzzles and hints aligns with the moderate score on _Creative Freedom_, suggesting room for improvement in providing more engaging and dynamic gameplay.

In the following sections we will present the focus group findings by area.

#### User Interface & User Experience {.unnumbered}

- One player requested an extra slide in the tutorial or in the first level, explaining how each level\'s score is calculated.

- One player requested that the _Next Level_ button should be a different color to others (on the level completion overlay).

- One player requested to group levels in the level selection menu by difficulty.

- Players agreed that the game menu was easy to use and that the navigation worked well and was predictable.

- Players agreed that the state of the application was flawless and was updating correctly.

- Some players requested to add background music and sounds when launching missiles and hitting the targets.

#### Game Mechanics {.unnumbered}

- Players found the mechanics simple and casual and commented that this simplicity helped them focus on solving the puzzles.

#### Difficulty {.unnumbered}

- Players agreed that the game is easy and intended of users with no quantum computer experience. All of them could complete all 30 levels. They said they would like to try more difficult puzzles.

- Most players said that the hardest level was level 30 (the final one), as it required a combination of 3 gates to solve the puzzle.

- One player did not understand how the Hadamard gate acts on 2 qubits. Half of the players said they would like more information about superposition, but agreed that the theory presented was sufficient to solve the puzzles.

- One player suggested that there should be hints to use in case you find it difficult to solve the puzzle.

#### Scoring & Rewards {.unnumbered}

- Players agreed that having a score system encouraged them to improve. 7 out of 8 players tried to complete all levels with 3 stars.

- Players agreed that they felt rewarded and motivated to keep playing by unlocking new spaceships as they progressed.

### Retention Test

![Retention Test Results.](chapter-7/image010_retention.png){#fig:fig708 height=40%}

The results of the retention test are shown in _Figure 7.8_. As mentioned in _Section 7.1.5_, 10 out of 23 participants took part in the retention test. The average score of the players in the retention test was 55%, which is lower than the average score of 75% in the Post Test. The average score of 55% is significantly higher than the average score of 17% in the Pre Test, indicating that players retained most of the knowledge acquired through the game.

## Conclusions

Based on the feedback and data collected from the Pre-Post Tests, questionnaires and focus group, several conclusions can be drawn:

1. The game is an effective learning tool and successfully introduces the basic concepts of quantum computing to university students. The difference between the Pre and Post test scores and the _Average Normalized Gain_ of 0.7 indicates a substantial improvement in the players\' knowledge after playing the game. The t-test results also indicate that the difference between the means is statistically significant.

2. The average time it took players to complete the game - excluding the quiz - was 18 minutes. This is a good indication that the game is short and can be played during a university lecture (as an educational tool) or when the student has limited time.

3. The game is enjoyable, and the players found the mechanics simple and casual. The navigation works well and is predictable. The state of the application was flawless and was updating correctly.

4. The difficulty was advantageous for the target audience, but some players requested more difficult puzzles. The players agreed that the game is easy, intended for users with no experience around Quantum Computing.

5. The incentive system used in the game was found to be motivating and encouraged players to improve.

6. The game had a positive effect on information retention, as indicated by the retention test results. The average score of 55% in the retention test is significantly higher than the average score of 17% in the Pre Test, indicating that players retained most of the knowledge acquired through the game.

7. The application is highly usable and provides a positive user experience, as indicated by the SUS score of 86.33, which is classified as _Excellent_ on the _Bangor adjective rating scale_ and corresponds to the highest grade, _A+_, on the _Sauro-Lewis curved rating scale_. This finding is also confirmed by the Focus Group feedback and the high score on the _Usability_ subscale of the GUESS-18 questionnaire.

8. The game experience was positive, with high scores on the _Visual Aesthetics_, _Enjoyment_, _Usability_ and _Personal Gratification_ and average scores on _Creative Freedom_ and _Narratives_ subscales of the GUESS-18 questionnaire. The results where confirmed by the Focus Group findings.
