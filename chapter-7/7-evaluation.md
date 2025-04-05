# Evaluation

![Evaluation Flow](chapter-7/image005_evaluation_flow.png){#fig:fig701 height=50%}

In order to measure the learning outcome of the game and to evaluate the user experience, the evaluation process described in _Figure 7.1_ was designed. More specifically, this process was designed to evaluate the achievement of the objectives set out in Chapter 1, namely:

1. The game to be an effective learning tool and to successfully introduce the basic concepts of quantum computing to university students.

2. The game should be enjoyable and simple so as not to distract the student from the learning objective.

3. The game should be short and require no additional equipment other than a mobile phone, making it suitable to be played during a university lecture or when the student has limited time.

In order to assess these objectives, we will use a mix of methods, which will be discussed below. To assess the first objective, we need to measure the learning outcome of the game. To assess the other two objectives, we need to evaluate the application as an interactive system and as a game.

To measure the learning outcome, we decided the integration of a quiz in the game with common questions about quantum computing. To evaluate the application as an interactive system we used the _System Usability Scale_ questionnaire, while to evaluate the game experience we used the shortened version of the _Game User Experience Satisfaction Scale_ questionnaire, the _GUESS-18_. Finally, we decided to conduct a focus group in order to evaluate the structure, usability and difficulty of the game and get more in-depth feedback in general.

## Evaluation Process Description

### Evaluation of Learning Outcome
< TODO: add # participants > undergraduate university students volunteered to participate in the evaluation of the game, which was carried out in 2 phases. The volunteers claimed to have a strong background in mathematics and were aged 19-24. The first phase used the Pre-Post test methodology, for which a quiz was designed and integrated into the game.

To support the first phase and the implementation of the quiz, we relied on _Cooksey and Jonsson_ [-@cooksey-jonsson-pre-post] and _Stratton_ [-@stratton-pre-post]. The first step was to create a repository of candidate questions to help structure the quiz. These questions were mainly taken from comprehension quizzes given in the _Quantum Computation_ course at the University of Patras (academic year 2023-24, lecturers: Sgarbas, K. and Kounavis, P.). A subset of these questions was then selected and adapted to the content of the game. The quiz consists of 3 theoretical questions and 9 questions regarding quantum gates actions. Each correct answer awards one point, while each incorrect answer gives zero points. The theoretical questions relate to the theory presented to the player via slides. The quantum gates related questions ask the player to calculate the new state of a qubit after the gate has been applied to it, or ask the player to select the appropriate gate to perform a quantum calculation. The questions are designed to prove that the player has learned to use -some of- the gates introduced in chapter 4 and understands the concept of superposition.

The version of the application used in this phase of the evaluation had one difference from the final version available on Github. The quiz results screen had been modified to show only the final score and not the correct or incorrect answers. To automate the process of collecting results, the results were sent to a remote database. The collection of results was anonymous; when the application was first started, a random UUID was generated and sent along with the score for each quiz attempt, making it possible to group the results by user without knowing who each attempt belonged to.

As suggested in the literature, participants were asked to complete the pre-test before interacting with the game to get an overview of their previous knowledge. Then, they were asked to complete the tutorial level and then complete the 30 levels of the game and retake the quiz. Players were given as much time as they wanted and were asked to record how long it took to complete the game. There was no further guidance on how the game works and no external help was provided to solve the levels. The _Normalized Gain_ metric was used to measure efficiency, as suggested in the literature [@cooksey-jonsson-pre-post; @kagan-normalized-gain].

### Evaluation of the Interactive System
The participants who completed the Pre-Post Tests were asked to answer the SUS questionnaire.

SUS is a ten-item, 5-point Likert scale questionnaire that measures the usability of a system. The items are scored on a scale from 1 to 5, with 1 being "strongly disagree" and 5 being "strongly agree". The scores are then converted to a score out of 100. Half of the items are positively worded and half are negatively worded. The positively worded items are scored by subtracting 1 from the score, while the negatively worded items are scored by subtracting the score from 5. The scores for each item are then summed and multiplied by 2.5 to convert them to a score out of 100. The SUS score is not a percentage, but it can be interpreted as a percentage for comparison purposes. A score of 68% is considered average, while a score above 80% is considered excellent. [@brooke-sus; @bangor-sus]

The SUS score is calculated as follows:

$SUS = 2.5 (20 + \sum {(SUS01, SUS03, SUS05, SUS07, SUS09)} \newline - \sum {(SUS02, SUS04, SUS06, SUS08 SUS10)})$

### Evaluation of the Game Experience
Then, the participants were asked to answer the GUESS-18 questionnaire. The GUESS-18 is a shortened version of the GUESS questionnaire, and is an 18-item, 7-point Likert scale questionnaire that measures the game experience. We chose the shortened version to prevent

 The items are scored on a scale from 1 to 7, with 1 being "strongly disagree" and 7 being "strongly agree". The scores are then converted to a score out of 100. The GUESS-18 questionnaire is divided into 9 sections. Each section has its own score, which can be used to measure the overall game experience. The sections and question are presented in Figure 7.1_.




[@tondello-guess; @tondello-guess-18]






### Focus Group
8 out of < TODO: add # participants> players from the fist phase participated in the focus group. The questions they were asked to discuss were related to 4 areas; _User Interface & User Experience_ (UI & UX), _Game Mechanics_, _Difficulty_ and _Scoring & Rewards_. They were also free to discuss with each other and comment on their overall experience of the application. The findings from the focus group will be used to improve the game in the future.

The focus group took place two days after the completion of the pre-post test. It was conducted via Zoom meeting, lasted about 1 hour and was neither recorded nor transcribed. The focus group had no strict structure. The users were free to discuss each of the 4 areas tested for about 10 to 12 minutes per area under the supervision of the researcher who took notes. Follow-up questions were then asked for clarification. In addition, the supervisor encouraged individuals who were not participating as actively to share their views. [@rabiee-focus-group; @wilkinsos-focus-group]

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

where the brackets indicate the averages. [@cooksey-jonsson-pre-post; @kagan-normalized-gain]
