---
author:
 - Θεοφίλου Στυλιανός
author-genitive: Θεοφίλου Στυλιανού
author-mnr: 1072791
subject: Διπλωματική
title: Σχεδιασμός και Ανάπτυξη Ψηφιακού Παιχνιδιού Μάθησης
title-en: Design and Development of Digital Learning Game
date: Μάρτιος 2025
place: Πάτρα
school: Πολυτεχνική Σχολή
department: Ηλεκτρολόγων Μηχανικών \& Τεχνολογίας Υπολογιστών
supervisor: Σιντόρης Χρήστος, Ε.ΔΙ.Π.
commitee:
    - Σγάρμπας Κυριάκος, Καθηγητής
    - Φείδας Χρήστος, Καθηγητής
director:
abstract-el: |+
    Η Κβαντική Υπολογιστική είναι ένας αναδυόμενος τομέας που απαιτεί βαθιά κατανόηση των θεμελιωδών αρχών της Κβαντομηχανικής, όπως τα qubits, η υπέρθεση και οι κβαντικές πύλες. Η παρούσα διατριβή παρουσιάζει το σχεδιασμό και την ανάπτυξη ενός εκπαιδευτικού παιχνιδιού για κινητά τηλέφωνα με στόχο την εισαγωγή των φοιτητών πανεπιστημίου στα βασικά στοιχεία της Κβαντικής Υπολογιστικής, ως εναλλακτική λύση στις παραδοσιακές εκπαιδευτικές μεθόδους. Το παιχνίδι χρησιμοποιεί τεχνικές μάθησης βασισμένης στο παιχνίδι για να ενισχύσει την ενασχόληση, την κατανόηση και τη διατήρηση πληροφορίας μέσω διαδραστικών puzzle. Το παιχνίδι αναπτύχθηκε με το  Flutter framework και παρέχει μια προσιτή και ευέλικτη μαθησιακή εμπειρία σε διαφορετικές πλατφόρμες κινητών συσκευών. Η διαδικασία αξιολόγησης, η οποία περιελάμβανε στατιστική ανάλυση αποτελεσμάτων μίας Pre-Post Test μελέτης και ένα Focus Group, έδειξε ότι το παιχνίδι βελτίωσε με επιτυχία την κατανόηση των αρχών της Κβαντικής Υπολογιστικής από τους εκπαιδευόμενους. Τα ευρήματα αναδεικνύουν τις δυνατότητες της μάθησης βασισμένης στο παιχνίδι να κάνει τις αφηρημένες επιστημονικές έννοιες πιο προσιτές και ευχάριστες.
abstract-en: |+
    Quantum Computing is an emerging field that requires a deep understanding of fundamental principles of Quantum Mechanics, such as qubits, superposition, and quantum gates. This thesis presents the design and development of an educational mobile game aimed at introducing university students to the basics of Quantum Computing, as an alternative to traditional educational methods. The game employs Game-Based Learning (GBL) techniques to enhance engagement, retention, and comprehension through interactive puzzles. Developed using the Flutter framework, the game provides an accessible and flexible learning experience across different mobile platforms. The evaluation process, which included statistical analysis of a Pre-Post Test study and a Focus Group, demonstrated that the game successfully improved learners' understanding of quantum computing principles. The findings highlight the potential of Game-Based Learning in making abstract scientific concepts more approachable and enjoyable.
keywords-el:
    - Μάθηση Βασισμένη στο Παιχνίδι
    - Εκπαιδευτικό Παιχνίδι
    - Κβαντική Υπολογιστική
    - Κβαντική Μηχανική
    - Παιχνίδι για Κινητές Συσκευές
    - Flutter
keywords-en:
    - Game-Based Learning
    - Educational Game
    - Quantum Computing
    - Quantum Mechanics
    - Mobile Game
    - Flutter
acknowlegements: |+
    I would like to thank all the users who participated in the User Testing, Pre-Post Testing and the Focus Group,
    for their time and valuable feedback.
    I would also like to thank my friends and fellow students, Arachovitis Georgios and Giannakis Myron,
    for their important contribution in editing the texts and images used in the game and their valuable advice in general.
    Finally, I would like to thank my supervisor, Mr. Sintoris Christos, for his guidance and support throughout the thesis.
# Θα ήθελα να ευχαριστήσω όλους τους χρήστες που συμμετείχαν στο User Testing, το Pre-Post Testing και το Focus Group,
# για το χρόνο που μου διέθεσα και για την πολύτιμη ανατροφοδότηση που παρείχαν.
# Επίσης θα ήθελα να ευχαριστήσω τους φίλους και συμφοιτητές μου, Γιαννάκη Μύρωνα και Αραχωβίτη Γεώργιο, για τη σημαντική αρωγή τους
# στην επιμέλεια των κειμένων και των εικόνων που χρησιμοποιούνται στο παιχνίδι και τις πολύτιμες συμβουλές τους εν γένει.
# Τέλος, θα ήθελα να ευχαριστήσω τον επιβλέποντα καθηγητή μου,
# κ. Σιντόρη Χρήστο, για την καθοδήγηση και την υποστήριξή του καθ' όλη τη διάρκεια της διπλωματικής.
lang: en-US
book: true
toc-own-page: true
toc: true
classoption:
    - twoside
titlepage: true
colorlinks: true
indent: true
header-includes:
    # - |
    #     ```{=latex}
    #     \usepackage{awesomebox}
    #     ```
    - |
        ```{=latex}
        \usepackage{cleveref}
        % pandoc-fignos: change the caption name
        \renewcommand{\figurename}{Image}
        ```
# \usepackage{caption}

pandoc-latex-environment:
    noteblock: [note]
    tipblock: [tip]
    warningblock: [warning]
    cautionblock: [caution]
    importantblock: [important]
titlepage-text-color: 0A0A0A
logo: images/uplogo.png
logo-stamp: images/logo-up-4color-stamp.jpg
signature: images/student-signature.png
listings-disable-line-numbers: false
disable-header-and-footer: false
# header-center: header-center
header-left: "\\hspace{1cm}"
header-right: "\\rightmark"
first-chapter: 1
biblatex: true
bibliography: bibliography/bibliography.bib
# reference-section-title: 'Βιβλιογραφία'
mainfont: "Linux Libertine O"
CJKmainfont: Noto Serif CJK SC
sansfont: "Linux Biolinum O"
monofont: "Ubuntu Mono"
lof: true # List of figures
lot: true # List of tables
# geometry: [a4paper, bindingoffset=0mm, inner=20mm, outer=20mm, top=20mm, bottom=20mm] # See https://ctan.org/pkg/geometry for more options
fignos-cleveref: False
fignos-plus-name: Figure
fignos-star-name: Figure
fignos-caption-name: Figure
fignos-caption-separator: period
fignos-number-by-section: False
secnos-plus-name: Section
secnos-star-name: Section
caption-labelformat: original
tablenos-plus-name: Table
tablenos-star-name: Table
tablenos-caption-name: Table
---