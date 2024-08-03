# Mobile Application Development
Mobile application development is the process of creating software applications that run on mobile devices. The software can be preinstalled on the device, downloaded from an app store or accessed through a web browser. [@aws_mobile_app_development], [@ibm_mobile_app_development]

Mobile games are digital games designed for mobile devices. They can utilize mobile sensors and hardware (e.g. accelerometers, GPS etc.), or even external peripherals, such as gaming controllers and AR/VR headsets.

## Platforms
There are two dominant operating systems for mobile devices, Google's Android and Apple's iOS. iOS is used only on Apple devices while Android is used by several manufacturers.

Developing applications on each of these platforms requires the use of different software development kits (SDKs). There are four approached to mobile app development, which are compared below.

### Native Applications
A native mobile application is a software application that is designed for a specific operating system platform [@techopedia_native_mobile_app]. Native mobile apps can only work on the platform that they are designed for, because they use the programming languages, frameworks and interfaces that are platform-specific. They run directly on the operating system, so they tend to perform better than other applications that require interaction with the device's operating system or hardware.

Because native apps are compiled directly into machine code, there have to be a different code base for each version of the same application (i.e. iOS or Android version). This is a requirement that significantly increases the cost and time of development and maintenance.  [@aws_mobile_app_development], [@techopedia_native_mobile_app]

Native android apps are built with the [Android SDK](https://developer.android.com/studio) and use [Java](https://dev.java/learn/getting-started/) or [Kotlin](https://kotlinlang.org/docs/getting-started.html). On the other hand, native iOS apps are built with the [iOS SDK](https://developer.apple.com/develop/) and use [Swift](https://developer.apple.com/swift/) or [Objective-C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html).

### Cross-Platform Applications
Cross-platform apps have the ability to operate on different operating systems with little to no modification.Because the use universal coding languages and frameworks, cross-platform apps can run on iOS and Android using the same codebase. These coding languages and frameworks hide from developers the underlying differences between operating systems. [@techopedia_cross_platform]

Multiplatform apps reduce the cost for building and maintaining an application that targets different platforms. On the other hand, there are some performance issues and the access to device-specific features is limited, because they are not interacting directly with the operating system or the hardware. [@techopedia_cross_platform], [@aws_mobile_app_development]

Some of the most popular frameworks for multiplatform development are [Flutter](https://docs.flutter.dev/), [React-Native](https://reactnative.dev/), [Ionic](https://ionicframework.com/docs) and [Kotlin Multiplatform](https://kotlinlang.org/docs/multiplatform.html) [@medium_cross_platform], [@jetbrains_cross_platform].

### Hybrid-Web Applications
A hybrid-web application combines the elements of native and web apps. They are essentially web apps that have a native app shell. They are build with standard web technologies, like [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) and [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) and are bundled as native app packages. Hybrid apps are executed inside a container, which wraps the applications and acts as a bridge between the application and the operating system. [@techtarget_hybrid_app], [@teska_containerization]

Although these apps reduce development and maintenance cost and user experience is very good, their performance is very low, as they cannot take advantage of many native device features. [@aws_mobile_app_development], [@techopedia_native_mobile_app]

### Progressive Web Applications
Progressive Web Apps (PWAs) skip App Store delivery and conventional installation processes - they are accessible via a URL. PWAs are web apps that use browser capabilities to provide an app-like user experience, so they are written using web technologies, such as JavaScript and HTML.

PWAs are able to overcome certain disadvantages of Hybrid Web Apps, as they have better performance and more extensive access to device features. They also have low development and maintenance cost, but the app capabilities are restricted by the browser the use. [@aws_mobile_app_development], [@techopedia_native_mobile_app]

## Languages and Frameworks

### Android

#### Java {.unnumbered}
Java is a high-level, class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible. Java applications are compiled in bytecode that can run on any Java virtual machine, meaning that compiled Java code can run on all platforms without the need to recompile. It was initially released in 1995. Although Android is built on the Linux kernel, which is largely written in [C](https://en.wikipedia.org/wiki/C_(programming_language)), the Android SKD uses the Java language as the basis for its applications. [@wikipedia_java]

#### Kotlin {.unnumbered}
Kotlin is a high-level, statically typed, general-purpose programming language with type interference. Kotlin is designed to interoperate fully with Java and the JVM version of Kotlin's standard library depends on the Java class library. Kotlin, released by JetBrains in 2016, aims to address Java’s shortcomings and enhance development productivity. [@wikipedia_kotlin], [@medium_kotlin_vs_java_1]

#### Comparison {.unnumbered}
Both Java and Kotlin compile to byte-code for the JVM, offering similar performance. Java applications tend to consume more memory, while Kotlin has more efficient memory management, with inline and extension functions that can reduce memory footprint. Kotlin has better startup time due to type interference, leading to faster initialization. Both languages support multithreading, but Kotlin's co-routines simplify concurrent code handling. Kotlin offers modern features and capabilities for Android development while Java has stronger community support. [@geeksforgeeks_kotlin_vs_java], [@medium_kotlin_vs_java_1], [@medium_kotlin_vs_java_2]

### iOS

#### Objective-C {.unnumbered}
Objective-C is a high-level, general-purpose, object-oriented programming language that first appeared in 1984. It is influenced by [C](https://en.wikipedia.org/wiki/C_(programming_language)) and [Smalltalk](https://en.wikipedia.org/wiki/Smalltalk) and it was primarily selected by [NeXT](https://en.wikipedia.org/wiki/NeXT) for [NeXTSTEP](https://en.wikipedia.org/wiki/NeXTSTEP) operating system. Apple chose Objective-C as the main programming language for iOS and macOS, because macOS was based on NeXTSTEP. [@wikipedia_objective_c]

#### Swift {.unnumbered}
Swift is a high-level, general-purpose, multi-paradigm programming language created in 2010 by Apple. Swift is intended to support the core concepts of Objective-C, but in a safer way. It compiles to byte-code and uses an [LLVM compiler](https://en.wikipedia.org/wiki/LLVM). [@wikipedia_swift]

#### Comparison {.unnumbered}
Objective-C has more complex and verbose syntax than Swift. It uses square brackets and has longer syntax for method and property definitions, while Swift is more concise and readable, with a syntax that resembles natural language. Swift is also significantly faster than Objective-C and offers a modern framework ([SwiftUI](https://developer.apple.com/xcode/swiftui/)) to build user interfaces. On the other hand, Objective-C has many well-documented, third-party frameworks and is well-tested and more stable. Also, it is a superset of C, so it works smoothly with C and [C++](https://en.wikipedia.org/wiki/C%2B%2B) code. [@medium_swift_vs_objective_c], [@netguru_swift_vs_objective_c]

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

see [@medium_cross_platform]

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
