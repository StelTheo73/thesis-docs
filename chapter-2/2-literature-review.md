

# 2 Literature Review

## 2.1 Computer Science Games for Higher Education
https://www.researchgate.net/publication/325046233_Games_for_Teaching_Computing_in_Higher_Education_-_A_Systematic_Review

## 2.2 Quantum Physics Games

### Desktop and Web Games
Platforms: Decodoku, QPlayLearn, finnishgamejam / itch.io, quantumgames.aalto, ibm

1) [finnishgamejam](https://www.finnishgamejam.com/):
    - Game jam for game developers.
    - Desktop games: User must download the source files and build the game.
    - Web games.
    - Most of the games are available on [itch.io](https://itch.io/):
    - Games hosted on finnishgamejam/itch.io are not designed for educational purposes.
    The target of this jam is to create games with limited time and resources but with unlimited creativity [[link](https://www.finnishgamejam.com/about/)].

3) [QPlayLearn](https://qplaylearn.com/about)
    - Platform with web-based educational games.

### Mobile Games
1) Google Play Store (for android devices)
    - Quantum: Εκπαιδευτική εφαρμογή με 13 κεφάλαια θεωρίας. 4 τεστ - 60 ερωτήσεις.
    - QuantumQ Circuit Puzzle: Επίλυση puzzle με κβαντικά κυκλώματα και κβαντικές πύλες. Περιέχει θεωρία.
    - Learn Quantum Physics: Εκπαιδευτική εφαρμογή με θεωρία. Απλά και προχωρημένα θέματα. Όμορφο design.
    - Quantum Computing: Εκπαιδευτική εφαρμογή με θεωρία. Απλά θέματα. Όχι ελκυστική.

2) App Store (for iOS devices)
    - [Quantum Mechanics](https://apps.apple.com/tr/app/quantum-mechanics-theories/id1159692911?l=tr) - Theories: Εκπαιδευτική εφαρμογή με θεωρία. Δεν εμβαθύνει στους κβαντικούς υπολογιστές. Θίγει και άλλα θέματα κλασσικής ή/και σωματιδιακής φυσικής
    - [Qika Quantum Game](https://apps.apple.com/tr/app/qika-quantum-game/id1546543567): Qika is a quantum game which you need to apply quantum gates to qubits in the grid. You need to change the states of qubits by applying gates in order to reach the target measurement.
    - [Quantum 3](https://apps.apple.com/ae/app/quantum-3/id1406630529): Quantum 3 is an educational match-3 game for all ages where fun meets quantum physics! Build subatomic particles, learn about the mysteries of fundamental physics and deploy antimatter to clear the way! You'll match and swap quarks to make (and learn about) the baryons you need for each objective. Puzzle out the quantum properties of color, flavor and spin. So get in there and start your quantum-venture! Quantum 3 is puzzle-matching at its finest and a great intro to the world of particle physics!
    - [Quantum Kate AR](https://apps.apple.com/ae/app/quantum-kate-ar/id1471200027):


## 2.3 Why a mobile game?
- Σύμφωνα με τα παραπάνω, βρήκαμε μόνο ένα παιχνίδι για κινητές συσκευές. Τα περισσότερα ήταν θεωρητικά και μη αλληλεπιδραστικά.
- Επιθυμούμε να φτιάξουμε ένα παιχνίδι το οποίο μπορεί να αξιοποιηθεί από περισσότοερους χρήστες, να παίζεται εύκολα, χωρίς να
χρειάζεται να είναι ο χρήστης μπροστά στον υπολογιστή του.
- Ένα mobile game μπορεί να παιχθεί από περισσότερα άτομα.


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
