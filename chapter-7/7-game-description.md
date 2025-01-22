# Educational Game Development

In the previous chapters, we discussed gamification and presented the basic theory of quantum computing and some of the most well-known quantum gates. Next, we will present the educational game we designed to teach learners the concept of superposition and to familiarize them with the effects of some quantum games.

The game developed is called _Qubity_ and is a variant of the arcade video game _Space Invaders_. It combines the characteristics of a "Shoot 'em Up" game with puzzle solving. The game is aimed at university students, as some levels require knowledge of complex numbers to solve the puzzle. However, the levels present the necessary theory for solving the puzzle, so a player with a flair for mathematics could complete the level without having any knowledge of complex numbers, as demonstrated by the evaluation of the game.

## Game Description

The game consists of 30 levels, in which the player is asked to solve a puzzle using certain quantum gates -a subset of those presented in chapter 6. The player operates a spaceship whose position is determined by the state of a quantum register. The player can change the position of the spaceship by manipulating a qubit with one of the available quantum gates.

The first 17 levels have a single qubit register and the available gates are Pauli-X, Pauli-Y, Pauli-Z and Hadamard. The remaining 13 levels have a 2-qubit register and the available gates are Pauli-X, Pauli-Z and Hadamard. In each level there are 2, 4, or 8 different states in which the spaceship can be in, depending on the number of qubits and the available gates.

< Picture of a level >

In each level, there are one or more asteroid targets. The player shall move the spaceship under the targets by altering the state of the register. Then, they have to destroy the asteroid by launching missiles. Several levels have more than one solution, but to score maximum points they must use the minimum number of gates and as few missiles as possible.

The game is accompanied by a 12-question quiz that allows players to test their knowledge gained by the game.

## Screens

### Home Screen

< image >

From the app's home screen, the user can access the game levels, available spaceships, the quiz, a tutorial level and game settings.

### Levels

< image >

On this screen the player can select any of the available levels. Each level's card shows the number of qubits, the available gates and the score.

### Spaceships

< image >

From this screen the player can select one of the available spaceships. The spaceships are decorative in nature, as they all have the same capabilities, but are a reward for the player's progress in the game. Initially only 3 are available, new spaceships are unlocked after completing more levels.

### Quiz

< image >

This screen gives access to the knowledge check quiz. The player can answer a short quiz or view their score from previous attempts. Each quiz consists of 12 questions, 3 theoretical and 9 related to quantum gates.

From the basic theory presented in the previous chapter and in the game slides, the quiz tests whether the player knows the name of the basic information unit in quantum computers, the definition of superposition and the name of the fate that carries a qubit into a superposition state. All other questions test the user's understanding of how quantum gates work, asking the user to perform a simple quantum calculation or select the correct gate to perform an action.

< image : quiz form >

< image : quiz result >

< image : quiz history >

### Tutorial

< image >

This screen loads a tutorial level, for which no score is calculated. First, a few slides are presented with basic quantum computing theory. In particular, the player is introduced to basic theory around qubits, quantum registers and quantum gates, as well as the concept of superposition. The slides consist of short sentences that summarize the theory discussed in chapter 6. Then there are 4 overlays with instructions, which demonstrate to the player how to use the gates to control the spaceship and how to destroy the asteroids.

### Settings

< image >

From this screen, the user can choose between the available languages and delete their progress in the game. Available languages are English and Greek, with the former being the default.

## Levels

Each level has a different number of possible states, depending on the available gates and the number of qubits.

At the beginning of some levels, there are some slides with theory about the quantum gates available in this level. The first levels are very simple, requiring only 1 use of a gate to put the register into the target state. As the game progresses, the number of gates and combinations increases. In some levels there are gates that do not to be used. The player needs to use what they have learned to solve the puzzle using the minimum number of gates.

< image x3: pause menu + theory slide + gate example slide >.

The first 9 levels introduce the Pauli Gates (X, Y and Z). In level 10, the theory of superposition is reintroduced to increase information retention. Also, Hadamard Gate (H) is introduced. In the next 7 levels, the player is asked to solve the puzzle by combining his previous knowledge of X and H gates.

From level 18, the number of qubits is increased to 2. From this level, no new theory is introduced; the player is just asked to combine their previous knowledge to solve the puzzles. In addition, the level of difficulty increases as the player has to decide which qubit to apply the gate to.

## Development

Development of the game began in November 2024. Google's [_Material Design 3_](https://m3.material.io/) and [_Flame Game Engine_](https://flame-engine.org/) were user to create the graphical elements of the application. The spaceships, asteroids, gates and several other bitmaps used to create the sprite components of the game are from [_Freepik_](https://www.freepik.com/). The background image was created by [_ChatGPT_](https://chatgpt.com/) and was slightly modified.

The first step was the selection of the quantum gates that would be presented in the game, and 30 scenarios were created to form the levels of the game. Each scenario consists of the initial state of the quantum register (initial position of the spaceship), the target state (positions of the target asteroids), the available gates and the minimum number of gates to be used to solve the puzzle. The scenarios are encoded in a YAML file in a manner that is human-readable while allowing for easy addition of new levels.

< image: diagrams.net >

< image: level 30 >

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

Για να αποφευχθεί το common pitfall (κεφ. 3) που μπορεί να οδηγήσει σε απογοήτευση του παίκτη, δεν υλοποιήθηκε point system leaderboard που τον συγκρίνει με άλλους παίκτες. Σε κάθε επίπεδο, ο παίκτης λαμβάνει από μισό έως 3 αστέρια, με άριστα τα 3, ανάλογα με το πλήθος των πυλών και των πυραύλων που χρησιμοποίησε. Το βέλτιστο σκορ το λαμβάνει όταν χρησιμοποιήσει ακριβώς τόσους πυραύλους όσους και οι στόχοι κάθε επιπέδου και επιπλεόν όταν χρησιμοποιήσει τόσες πύλες όσες απαιτεί η βέλτιστη λύση κάθε επιπέδου.

Επιπλεόν, για να αυξηθεί το κίνητρο του παίκτη, όσο προχωράει στο παιχνίδι και ολοκληρώνει επίπεδα, περισσότερα διαστημόπλοια γίνονται διαθέσιμα ως επιβράβευση. Όταν ξεκλειδώσει κάποιο διαστημόπλοιο, εμφανίζεται ένα ενημερωτικό toast.

## Quiz

Προκειμένου να μετρηθεί η εκπαιδευτική ικανότητα του παιχνιδιού, σχεδιάστηκε ένα κουίζ 12 ερωτήσεων. Το quiz αποτελείται από 3 θεωρητικές ερωτήσεις και 9 ερωτήσεις υπολογισμού δράσης κβαντικής πύλης. Οι θεωρητικές ερωτήσεις αφορούν θεωρία η οποία έχει παρουσιαστεί στον παίκτη μέσα από slides. Οι ερωτήσεις υπολογισμού δράσης κβαντικής πύλης ζητάνε από τον παίκτη να υπολογίσει τη νέα κατάσταση ενός qubit / quantum register αφού δράσει επάνω του μία πύλη ή ζητάνε να επιλεχθεί η κατάλληλη πύλη για να ολοκληρωθεί ένας υπολογισμός.

Οι ερωτήσεις αφορούν αποκλειστικά θεωρία που παρουσιάστηκε μέσα από τα slides των επιπέδων ή ζητάνε απλούς κβαντικούς υπολογισμούς, με στόχο να αποδείξουν ότι ο παίκτης έμαθε να χρησιμοποιεί -ορισμένες από- τις πύλες που παρουσιάστηκαν στο κεφάλαιο 6 και κατανόησε την έννοια της υπέρθεσης.

< image from quiz menu, quiz and quiz history >

## Αξιολόγηση Παιχνιδιού

Στην αξιολόγηση του παιχνιδιού, η οποία έγινε σε δύο φάσεις, συμμετείχαν εθελοντικά 10 άτομα. Επιλέχθηκαν 10 φοιτητές Πανεπιστημίου, οι οποίοι δήλωσαν ότι έχουν γνώση προχωρημένων μαθηματικών, με τέσσερεις από αυτούς να έχουν γνώση μιγαδικών αριθμών.

Στην πρώτη φάση, διαμοιράσθηκε το παιχνίδι στους παίκτες και τους ζητήθηκε να ολοκληρώουν το quiz πριν παίξουν κάποιο επίπεδο, στη συνέχεια να παίξουν το επίπεδο επίδειξης και έπειτα να ολοκληρώσουν τα 30 επίπεδα του παιχνιδιού. Οι παίκτες είχαν όσο χρόνο ήθελαν στη διάθεση τους και τους ζητήθηκε να καταγράψουν το χρόνο που απαιτήθηκε για να ολοκληρώσουν τα 30 επίπεδα. Δεν δόθηκαν επιπλέον διευρκινίσεις για τον τρόπο λειτουργίας του παιχνιδιού, ούτε κάποια εξωτερική βοήθεια για την επίλυση κάποιου επιπέδου. Στη συνέχεια παρουσιάζονται τα αποτελέσματα της πρώτης φάσης αξιολόγησης:

< image from stat. analysis here >

Η πρώτη φάση έδειξε ότι...

Στη δεύτερη φάση, 8 από τους 10 παίκτες της πρώτης φάσης, συμμετείχαν σε ένα focus group. Οι ερωτήσεις που κλήθηκαν να συζητήσουν αφορούσαν τέσσερεις τομείς, το User Interface & User Experience (UI/UX), τους Μηχανισμούς του παιχνιδιού, τη Δυσκολία και την Βαθμολόγηση & Επιβράβευση. Επιπλέον, αφέθηκαν ελεύθεροι να συζητήσουν μεταξύ τους και να σχολιάσουν τη συνολική τους εμπειρία για την εφαρμογή.

Focus Group --> 4 τομείς --> UI/UX, Mechanics, Difficulty, Score & Rewards

Focus Group Notes

**UI/UX**

- Ένας παίκτης ζήτησε να υπάρξει ένα επιπλέον slide στο tutorial ή στο πρώτο επίπεδο που να εξηγεί πως γίνεται υπολογίζεται στο σκορ του κάθε επιπέδου

- Ένας παίκτης ζήτησε το _Next Level_ button να έχει διαφορετικό χρώμα από τα υπόλοιπα (στο overlay που εμφανίζεται)

- Ένας παίκτης ζήτησε να υπάρξει ομαδοποίηση των επιπέδων στο μενού επιλογής ανάλογα με το βαθμό δυσκολίας

- Οι παίκτες συμφώνησαν ότι το μενού του παιχνιδιού είναι εύχρηστο και το navigation λειτουργεί σωστά και έχει προβλέψιμη συμπεριφορά.

**Game Mechanics**

- Οι παίκτες βρήκαν τα mechanics απλά και συνηθισμένα και σχολίασαν ότι ο απλός χειρισμός τους βοήθησε να εστιάσουν στην επίλυση των puzzle.

**Δυσκολία**

- Οι παίκτες συμφώνησαν ότι το παιχνίδι είναι εύκολο και προορίζεται για χρήστες που δεν έχουν γνώσεις κβαντικών υπολογιστών. Μπόρεσαν όλοι να ολοκληρώσουν και τα 30 επίπεδα. Είπαν ότι θα ήθελαν να δοκιμάσουν και επίπεδα μεγαλύτερης δυσκολίας.

- Οι περισσότεροι παίκτες είπαν ότι το δυσκολότερο επίπεδο ήταν το 30, καθώς απαιτούσε συνδυασμό 3 πυλών για να λυθεί το puzzle.

- Ένας παίκτης δεν κατανόησε τον τρόπο λειτουργίας της πύλης Hadamard σε 2 qubit. Οι μισοί παίκτες δήλωσαν ότι θα ήθελαν παραπάνω πληροφορία για την υπέρθεση, όμως συμφώνησαν ότι η θεωρία που παρουσιάζεται είναι αρκετή για να επιλυθούν τα puzzle.

- Ένας παίκτης πρότεινε να υπάρχουν hints που μπορούν να χρησιμοποιηθούν εάν κάποιος δυσκολεύεται να λύσει ένα puzzle

**Επιβραβεύσεις**

- Οι παίκτες συμφώνησαν ότι η ύπαρξη του score τους έκανε να επιθυμούν να βελτιωθούν. 7 στους 8 παίκτες προσπάθησαν να ολοκληρώσουν όλα τα επίπεδα με 3 αστέρια.

- Οι παίκτες συμφώνησαν ότι το ξεκλείδωμα νέων διαστημοπλοίων όσο προχωρούσαν στο παιχνίδι και η εμφάνιση του ενημερωτικού toast κατά την ολοκλήρωηση των επιπέδων, τους έδινε μία αίσθηση επιβράβευσης και τους παρακινούσε να συνεχίσουν να παίζουν.
