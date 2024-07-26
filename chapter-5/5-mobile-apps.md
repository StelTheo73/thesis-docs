# Mobile Application Development
https://aws.amazon.com/mobile/mobile-application-development/ **aws**<br>
https://www.ibm.com/topics/mobile-application-development **ibm**<br>

Mobile application development is the process of creating software applications that run on mobile devices **ref to aws**. The software can be preinstalled on the device, downloaded from an app store or accessed through a web browser **ref to ibm**.

Mobile games are digital games designed for mobile devices. They can utilize mobile sensors and hardware (e.g. accelerometers, GPS etc.), or even external peripherals, such as gaming controllers and AR/VR headsets.

## Platforms
There are two dominant operating systems for mobile devices, Google's Android and Apple's iOS. iOS is used only on Apple devices while Android is used by several manufacturers.

Developing applications on each of these platforms requires the use of different software development kits (SDKs). There are four approached to mobile app development, which are compared below.

### Native Applications
https://www.techopedia.com/definition/27568/native-mobile-app **techopedia**<br>

A native mobile application is a software application that is designed for a specific operating system platform **ref to techopedia**. Native mobile apps can only work on the platform that they are designed for, because they use the programming languages, frameworks and interfaces that are platform-specific. They run directly on the operating system, so they tend to perform better than other applications that require interaction with the device's operating system or hardware.

Because native apps are compiled directly into machine code, there have to be a different code base for each version of the same application (i.e. iOS or Android version). This is a requirement that significantly increases the cost and time of development and maintenance **ref to aws and techopedia**.

Native android apps are built with the Android SDK **link to android sdk** and use Java **link to Java** or Kotlin **link to Kotlin**. On the other hand, native iOS apps are built with the iOS SDK **link to iOS SDK** and use Swift **link to Swift** or Objective-C **link to Objective-C**.

### Cross-Platform Applications
https://www.techopedia.com/definition/17056/cross-platform **techopedia**<br>
https://www.jetbrains.com/help/kotlin-multiplatform-dev/cross-platform-frameworks.html#popular-cross-platform-app-development-frameworks **jetbrains**<br>
https://medium.com/@evincedevelop/top-10-cross-platform-app-development-frameworks-for-2024-1d812fdfc776 **medium**<br>

Cross-platform apps have the ability to operate on different operating systems with little to no modification.Because the use universal coding languages and frameworks, cross-platform apps can run on iOS and Android using the same codebase. These coding languages and frameworks hide from developers the underlying differences between operating systems. **ref to technopedia**

Multiplatform apps reduce the cost for building and maintaining an application that targets different platforms. On the other hand, there are some performance issues and the access to device-specific features is limited, because they are not interacting directly with the operating system or the hardware. **ref to techopedia and aws**

Some of the most popular frameworks for multiplatform development are Flutter **link to Flutter**, React-Native **link to React-Native**, Ionic **link to Ionic** and Kotlin Multiplatform **link to KMP** **ref to medium and jetbrains**

### Hybrid-Web Applications
https://www.techtarget.com/searchsoftwarequality/definition/hybrid-application-hybrid-app **techtarget**<br>
https://teskalabs.com/blog/mobile-application-containerization-wrapping **teska labs**<br>

A hybrid-web application combines the elements of native and web apps. They are essentially web apps that have a native app shell. They are build with standard web technologies, like JavaScript **link to JS** and HTML **link to HTML5** and are bundled as native app packages. Hybrid apps are executed inside a container, which wraps the applications and acts as a bridge between the application and the operating system. **ref to techtarget** **ref to teska labs**

Although these apps reduce development and maintenance cost and user experience is very good, their performance is very low, as they cannot take advantage of many native device features. **ref to aws** **ref to techopedia --> native mobile app article**

### Progressive Web Applications
Progressive Web Apps (PWAs) skip App Store delivery and conventional installation processes - they are accessible via a URL. PWAs are web apps that use browser capabilities to provide an app-like user experience, so they are written using web technologies, such as JavaScript **link to JS** and HTML **link to HTML5**.

PWAs are able to overcome certain disadvantages of Hybrid Web Apps, as they have better performance and more extensive access to device features. They also have low development and maintenance cost, but the app capabilities are restricted by the browser the use. **ref to techopedia --> native mobile app article** **ref to aws**

## Languages and Frameworks
https://medium.com/@evincedevelop/top-10-cross-platform-app-development-frameworks-for-2024-1d812fdfc776 **See ##Cross-Platform for reference - Medium**<br>

### Android
https://en.wikipedia.org/wiki/Java_(programming_language) **java**<br>
https://en.wikipedia.org/wiki/Kotlin_(programming_language) **kotlin**<br>
https://www.geeksforgeeks.org/kotlin-vs-java/https://www.geeksforgeeks.org/kotlin-vs-java/ **geeksforgeeks**<br>
https://medium.com/@fhrvri.mmxiv/another-guide-on-performance-java-vs-kotlin-40117fa93560 **medium1**<br>
https://medium.com/@midoripig1009/kotlin-vs-java-a-comparison-of-features-and-performance-fe9eaac8b2c2 **medium2**<br>

#### Java {.unnumbered}
Java is a high-level, class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible. Java applications are compiled in bytecode that can run on any Java virtual machine, meaning that compiled Java code can run on all platforms without the need to recompile. It was initially released in 1995. Although Android is built on the Linux kernel, which is largely written in C, the Android SKD uses the Java language as the basis for its applications. **ref to java**

#### Kotlin {.unnumbered}
Kotlin is a high-level, statically typed, general-purpose programming language with type interference. Kotlin is designed to interoperate fully with Java and the JVM version of Kotlin's standard library depends on the Java class library. Kotlin, released by JetBrains in 2016, aims to address Java’s shortcomings and enhance development productivity. **ref to kotlin, medium 1**

#### Comparison {.unnumbered}
Both Java and Kotlin compile to byte-code for the JVM, offering similar performance. Java applications tend to consume more memory, while Kotlin has more efficient memory management, with inline and extension functions that can reduce memory footprint. Kotlin has better startup time due to type interference, leading to faster initialization. Both languages support multithreading, but Kotlin's co-routines simplify concurrent code handling. Kotlin offers modern features and capabilities for Android development while Java has stronger community support. **ref to geeksforgeeks, medium1, medium2**

### iOS
https://en.wikipedia.org/wiki/Objective-C **objective-c**<br>
https://en.wikipedia.org/wiki/Swift_(programming_language) **swift**<br>
https://medium.com/swiftfy/difference-between-objective-c-and-swift-e53369ee2d4f **medium3**
https://www.netguru.com/blog/objective-c-vs-swift **netguru**

#### Objective-C {.unnumbered}
Objective-C is a high-level, general-purpose, object-oriented programming language that first appeared in 1984. It is influenced by [C](https://en.wikipedia.org/wiki/C_(programming_language)) and [Smalltalk](https://en.wikipedia.org/wiki/Smalltalk) and it was primarily selected by [NeXT](https://en.wikipedia.org/wiki/NeXT) for [NeXTSTEP](https://en.wikipedia.org/wiki/NeXTSTEP) operating system. Apple chose Objective-C as the main programming language for iOS and macOS, because macOS was based on NeXTSTEP. **ref to objective-c**

#### Swift {.unnumbered}
Swift is a high-level, general-purpose, multi-paradigm programming language created in 2010 by Apple. Swift is intended to support the core concepts of Objective-C, but in a safer way. It compiles to byte-code and uses an [LLVM compiler](https://en.wikipedia.org/wiki/LLVM). **ref to swift**

#### Comparison {.unnumbered}
Objective-C has more complex and verbose syntax than Swift. It uses square brackets and has longer syntax for method and property definitions, while Swift is more concise and readable, with a syntax that resembles natural language. Swift is also significantly faster than Objective-C and offers a modern framework ([SwiftUI](https://en.wikipedia.org/wiki/SwiftUI)) to build user interfaces. On the other hand, Objective-C has many well-documented, third-party frameworks and is well-tested and more stable. Also, it is a superset of C, so it works smoothly with C and (C++)[https://en.wikipedia.org/wiki/C%2B%2B] code. **ref to medium3, netguru**

### Cross-Platform Frameworks
(flutter vs react-native vs ionic vs kotlin multiplatform)

#### Flutter {.unnumbered}

#### React-Native {.unnumbered}

#### Ionic {.unnumbered}

#### Kotlin-Multiplatform {.unnumbered}








## Game Engines





## Platform, Framework and Game Engine Choice
--> iOS and Android --> why? --> target all users
--> Cross Platform Approach --> why? --> Single code base, reduced costs of development and maintenance, very good user experience and sufficient performance
--> Flame engine --> why?

https://medium.com/@evincedevelop/top-10-cross-platform-app-development-frameworks-for-2024-1d812fdfc776 **See ##Cross-Platform for reference - Medium**<br>


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
