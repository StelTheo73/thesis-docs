# Evaluation

Building on the conceptual design and development process described in Chapter 6, this chapter focuses on evaluating the application against the objectives we set in chapter 1, namely:

1. The game to be an effective learning tool and to successfully introduce the basic concepts of quantum computing to university students.

2. The game should be enjoyable and simple so as not to distract the student from the learning objective.

3. The game should be short and require no additional equipment other than a mobile phone, making it suitable to be played during a university lecture or when the student has limited time.

The evaluation process uses a mix of methods and is divided into two parts: the first part evaluates the learning outcome of the game, while the second part evaluates the interactive system and the game experience. The evaluation of the learning outcome is based on a Pre-Post tests methodology, while the evaluation of the interactive system and game experience are based on questionnaires and a focus group. To evaluate the application as an interactive system used the _System Usability Scale_ questionnaire, while to evaluate the game experience we used the shortened version of the _Game User Experience Satisfaction Scale_ questionnaire, the _GUESS-18_.

_Figure 7.1_ shows the evaluation process we followed.

![Evaluation Process](chapter-7/image001_evaluation_flow.png){#fig:fig701 height=50%}

< TODO: add # participants > undergraduate university students volunteered to participate in the evaluation of the game, who claimed to have a strong background in mathematics.

## Evaluation Process Description

### Evaluation of Learning Outcome
To support the first phase and the implementation of the quiz, we relied on _Cooksey and Jonsson_ [-@cooksey-jonsson-pre-post] and _Stratton_ [-@stratton-pre-post]. The first step was to create a repository of candidate questions to help structure the quiz. These questions were mainly taken from comprehension quizzes given in the _Quantum Computation_ course at the University of Patras (academic year 2023-24, lecturers: Sgarbas, K. and Kounavis, P.). A subset of these questions was then selected and adapted to the content of the game. The quiz consists of 3 theoretical questions and 9 questions regarding quantum gates actions. Each correct answer awards one point, while each incorrect answer gives zero points. The theoretical questions relate to the theory presented to the player via slides. The quantum gates related questions ask the player to calculate the new state of a qubit after the gate has been applied to it, or ask the player to select the appropriate gate to perform a quantum calculation. The questions are designed to prove that the player has learned to use -some of- the gates introduced in chapter 4 and understands the concept of superposition.

The version of the application used in this phase of the evaluation had one difference from the final version available on Github. The quiz results screen had been modified to show only the final score and not the correct or incorrect answers. To automate the process of collecting results, the results were sent to a remote database. The collection of results was anonymous; when the application was first started, a random UUID was generated and sent along with the score for each quiz attempt, making it possible to group the results by user without knowing who each attempt belonged to.

As suggested in the literature, participants were asked to complete the Pre-test before interacting with the game to get an overview of their previous knowledge. Then, they were asked to complete the tutorial level and then complete the 30 levels of the game and retake the quiz. Players were given as much time as they wanted and were asked to record how long it took to complete the game. There was no further guidance on how the game works and no external help was provided to solve the levels. The _Normalized Gain_ metric was used to measure efficiency, as suggested in the literature [@cooksey-jonsson-pre-post; @kagan-normalized-gain].

### Evaluation of the Interactive System
The participants who completed the Pre-Post Tests were asked to answer the SUS questionnaire.

SUS is a 10-item, 5-point Likert scale questionnaire that measures the usability of a system. The items are scored on a scale from 1 to 5, with 1 being "strongly disagree" and 5 being "strongly agree". The scores are then converted to a score out of 100. Half of the items are positively worded and half are negatively worded. The positively worded items are scored by subtracting 1 from the score, while the negatively worded items are scored by subtracting the score from 5. The scores for each item are then summed and multiplied by 2.5 to convert them to a score out of 100. The SUS score is not a percentage, but it can be interpreted as a percentage for comparison purposes. A score of 68% is considered average, while a score above 80% is considered excellent. [@brooke-sus; @bangor-sus] In _Figure 7.2_ we present the SUS questionnaire.

![SUS Questionnaire](chapter-7/image002_sus.png){#fig:fig702 height=50%}

### Evaluation of the Game Experience
After completing the SUS questionnaire, the participants were asked to answer the GUESS-18 questionnaire. The GUESS-18 is a shortened version of the GUESS questionnaire, and is an 18-item, 7-point Likert scale questionnaire that measures the game experience. We chose the shortened version to prevent survey fatigue. The items are scored on a scale from 1 to 7, with 1 being "strongly disagree" and 7 being "strongly agree". The scores are then converted to a score out of 100. The GUESS-18 questionnaire is divided into 9 sections. Each section has its own score, which can be used to measure the overall game experience. [@phan-guess; @keebler-guess-18] The sections and questions of the GUESS-18 questionnaire are presented in _Figure 7.3_.

![GUESS-18 Questionnaire](chapter-7/image003_guess.png){#fig:fig703 height=50%}

### Focus Group
8 out of < TODO: add # participants> players from the fist phase participated in the focus group. The questions they were asked to discuss were related to 4 areas; _User Interface & User Experience_ (UI & UX), _Game Mechanics_, _Difficulty_ and _Scoring & Rewards_. They were also free to discuss with each other and comment on their overall experience of the application. The findings from the focus group will be used to improve the game in the future.

The focus group was conducted via Zoom meeting, lasted about 1 hour and was neither recorded nor transcribed. The focus group had no strict structure. The users were free to discuss each of the 4 areas tested for about 10 to 12 minutes per area under the supervision of the researcher who took notes. Follow-up questions were then asked for clarification. In addition, the supervisor encouraged individuals who were not participating as actively to share their views. [@rabiee-focus-group; @wilkinsos-focus-group]

## Results

### Learning Outcome
To measure the effectiveness of the application as a learning tool, we used the _Normalized Gain_ metric. It is calculated as the ratio of the actual average gain to the maximum possible gain.

The _Normalized Gain_ for each individual player is calculated as follows:

$$
g = \frac{post\% - pre\%}{100\% - pre\%}
$$

Where:

* $pre\%$: player's score in the quiz before playing the game (Pre test)

* $post\%$: player's score in the quiz after playing the game (Post test)

* $100\% - pre\%$: maximum possible gain, since score is capped at 100%

The _Average Normalized Gain_ is defined as:

$$
\langle g \rangle = \frac{\langle post\% \rangle - \langle pre\% \rangle }{100\% - \langle pre\% \rangle}
$$

Where:

* $\langle pre\% \rangle$: average score of all players in the quiz before playing the game (Pre test)

* $\langle post\% \rangle$: average score of all players in the quiz after playing the game (Post test)

[@cooksey-jonsson-pre-post; @kagan-normalized-gain]

### Interactive System
As described in _Section 7.2_, we used the _SUS_ questionnaire to evaluate the usability of the application. Yhe SUS score for each participant is calculated using the following formula:

$$
SUS = 2.5 (25 + \sum {(w_{01}, w_{03}, w_{05}, w_{07}, w_{09})} - \sum {(w_{02}, w_{04}, w_{06}, w_{08}, w_{10})})
$$

Where $w_{i}$ is the weight of the answer to the _i-th_ question (1-5).

To determine the overall SUS score, we calculate the average SUS score across all participants using the formula:

$$
\langle SUS \rangle = \frac{1}{N} \sum_{i=1}^{N} SUS_{i}
$$

Where $N$ is the number of participants and $SUS_{i}$ is the SUS score of the _i-th_ participant.

### Game Experience
TODO: how to score the GUESS-18 questionnaire
https://www.ruxresearch.com/_files/ugd/c357c3_06d8d7c0416c439ebbf7f25c3c1971c5.pdf


### Focus Group

## Conclusions
