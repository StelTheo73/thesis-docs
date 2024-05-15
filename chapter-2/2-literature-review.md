

# 2 Literature Review

## 2.1 Computer Science Games for Higher Education
https://www.researchgate.net/publication/325046233_Games_for_Teaching_Computing_in_Higher_Education_-_A_Systematic_Review

## 2.2 Quantum Physics Games

### 2.2.1 Desktop and Web Games
[List Of Quantum Games](https://kiedos.art/quantum-games-list/)

1) [Finnish Game Jam](https://www.finnishgamejam.com/)
    - Competition for game developers.
    - Desktop games: User must download the source files and build the game.
    - Browser games.
    - Most of the games are available on [itch.io](https://itch.io/):
    - Games created by Finnish Game Jam are not designed for educational purposes.
    - The target of this competition is to create games with limited time and resources but with unlimited creativity [[link](https://www.finnishgamejam.com/about/)].

2) [QPlayLearn](https://qplaylearn.com/)
    - Platform with web-based educational games.
    - Uses interactive tools to make the learning process more effective and entertaining for different target groups [[link](https://qplaylearn.com/about)].

3) [Quantum Games Course by Aalto University](https://quantumgames.aalto.fi/)
    - Course offered by Aalto University
    - Games are not designed for educational purposes.
    - This course is designed to teach students how to design and develop games and also learn the basic concepts of quantum computing.

4) [Science At Home](https://www.scienceathome.org/)
    - Aarhus University
    - Browser and desktop educational games
    - Diverse team of scientists, designers and game developers that create scientific games, aiming at teaching by game-play [[link](https://www.scienceathome.org/about-us/)]

5) github / gitlab
    - Lots of desktop games. Most of them use Jupyter Notebooks.
    - The majority of these games are not designed for educational purposes. They have been developed in the context of competitions or workshops.

6) [Decodoku](https://itch.io/profile/decodoku)
    - Has created a lot of quantum games. The games are hosted on itch.io.
    - The games does not have an educational purpose.
    - Most of them are designed to run on the [IBM Quantum Platform](https://quantum.ibm.com/)
    - Browser and desktop games

Conclusions:
  - Educational or not?
  - Quantum Computing or Particle Physics?
  - Designed by professionals, universities or just for fun?
  - Desktop or web?
  - Programming language - Technologies?
Consider adding table

### 2.2.2 Mobile Games
#### Google Play Store (for android devices)
  - [Quantum](https://play.google.com/store/apps/details?id=brychta.stepan.quantum_en)
    * Educational app
    * 13 chapters
    * 4 tests - 60 different questions
  - [QuantumQ](https://play.google.com/store/apps/details?id=com.ph.quantumq)
    * Puzzle game with theory
    * Quantum gates and quantum circuits
  - [Learn Quantum Physics](https://play.google.com/store/apps/details?id=com.codeworld.learnquantumphysics)
    * Educational app
    * Designed for students and professionals
  - [Quantum Computing](https://play.google.com/store/apps/details?id=hu.hexadecimal.quantum)
    * Educational app
  - [Quantum 3](https://play.google.com/store/apps/details?id=com.gellab.quantum3):
    * Educational game designed by Michigan State University
    * Puzzle game
    * Particle physics

#### App Store (for iOS devices)
  - [Quantum Mechanics](https://apps.apple.com/tr/app/quantum-mechanics-theories/id1159692911?l=tr)
    * Educational app
    * Particle physics
  - [Qika Quantum Game](https://apps.apple.com/tr/app/qika-quantum-game/id1546543567): Qika is a quantum game which you need to apply quantum gates to qubits in the grid. You need to change the states of qubits by applying gates in order to reach the target measurement.
    * Puzzle game
    * Applying quantum gates to qubits on order to reach a target measurement !!! Basic concept of our game !!!
  - [Quantum 3](https://play.google.com/store/apps/details?id=com.gellab.quantum3):
    * Same as android game
    * Educational game designed by Michigan State University
    * Puzzle game
    * Particle physics
  - [Quantum Kate AR](https://apps.apple.com/ae/app/quantum-kate-ar/id1471200027):
    * Educational game
    * Casual -> Simulation -> Adventure game
    * Particle physics

  Conclusions:
    - Educational or not?
    - Quantum Computing or Particle Physics?
    - Designed by professional, Universities or just for fun?
    - Android or iOS?
    - Programming language - Technologies?
Consider adding table

## 2.3 Why a mobile game?

https://www.ncfe.org.uk/all-articles/how-educational-games-are-changing-the-way-we-learn/

https://www.researchgate.net/figure/Core-educational-value-of-mobile-games_fig5_360277617

https://www.linkedin.com/pulse/top-7-reasons-using-mobile-apps-education-e-learning-industry-ved-raj

<!-- - Επιθυμούμε να φτιάξουμε ένα παιχνίδι το οποίο μπορεί να παίζεται εύκολα, χωρίς να
χρειάζεται να είναι ο χρήστης μπροστά στον υπολογιστή του.
- Ένα mobile game μπορεί να παιχθεί από περισσότερα άτομα. -->


## 2.4 Mobile Games Development Technologies
Short description of the technologies.

web based (js) OR android based (?) OR iOS based (consider also developing 3 separate apps for web/android/iOS?)
cross-platform game: Use a cross-platform framework like flutter or react-native



## 2.5 Why Flutter
Why we selected flutter?
- cross-platform: Υπήρχαν πιο πολλές εφαρμογές android. Εμείς θέλουμε όλοι οι χρήστες να μπορούν να παίξουν, ανεξάρτητα από τη συσκευή που έχουν.
- Άλλα πλεονεκτήματα flutter π.χ. απόδοση/ταχύτητα σε σχέση με τις άλλες επιλογές???
- Επιπλέον της υποστήριξης από android και iOS, η εφαρμογή μπορεί εύκολα να διατεθεί και ως desktop ή web app.
- Βιβλιοθήκες για κβαντικούς υπολογισμούς (συμβατές με το Dart version 3)
    * https://pub.dev/packages/qartvm
    * https://pub.dev/packages/quantools
- Βιβλιοθήκες για πίνακες
    * https://api.flutter.dev/flutter/vector_math/vector_math-library.html
    * https://pub.dev/packages/advance_math (supports complex numbers and matrices)
