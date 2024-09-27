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

According to Statista, the most popular frameworks for multiplatform development are [Flutter](https://docs.flutter.dev/) and [React-Native](https://reactnative.dev/) and [Kotlin Multiplatform](https://kotlinlang.org/docs/multiplatform.html). [@statista_cross_platform]

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

#### Flutter {.unnumbered}
Flutter is a user interface (UI) SDK developed and released by Google in 2017. It can be used to create natively compiled mobile, web and desktop apps from a single codebase. It uses its own rendering engine to draw widgets on the screen, unlike other UI frameworks that rely on the platform's rendering engine or manipulate the platform's built-in UI stack. Flutter also provides access to native APIs. The [Dart](https://en.wikipedia.org/wiki/Dart_(programming_language)) programming language is used to write applications in Flutter and the applications are compiled ahead-of-time (AOT) on all platforms except the web, where the code is transpiled to JavaScript or WebAssembly. [@wikipedia_flutter], [@jetbrains_cross_platform], [@medium_cross_platform]

#### React-Native {.unnumbered}
React-Native is a UI SDK released by Meta Platforms (formerly Facebook Inc.) in 2015 and can be used to develop apps for mobile devices, Android TV, tvOS, web applications and desktop applications. Its components wrap existing native code and can interact with native APIs. React-Native apps are written in JavaScript or TypeScript. [@wikipedia_react_native], [@jetbrains_cross_platform], [@medium_cross_platform]

#### Comparison {.unnumbered}
React-Native is easier to learn, because it uses JavaScript as a programming language and has greater community support. On the other hand, Flutter has better documentation and its command line interface (CLI) offers tools that allow Continuous Integration (CI) and Continuous Development (CD) to be created more easily than React-Native. Flutter's CLI also offers the ability to automate application deployment in the app stores. Both frameworks feature hot-reload functionality, which allows developers to see changes instantly while modifying their code, without having to recompile.

Flutter uses its own on widgets and libraries and its own rendering engine and compiles directly to native code, while React-Native depends on the underlying platform and uses multiple JavaScript layers before compiling to native code. Also, React-Native requires the developers to use third-party libraries, both for development and testing. These facts make Flutter significantly faster than React-Native, while allowing Flutter to use less CPU and memory, have a smaller package size and have more consistent UI across platforms. [@radix_flutter_vs_react_native], [@medium_flutter_vs_react_native]

## Platform, Framework and Game Engine Choice
The application that will be developed will be a cross-platform mobile application, in order to target users using both Android and iOS. We chose to develop a cross-platform application to get optimal performance, not rely on browser limitations and have a single codebase. This choice also reduces development and maintenance costs and provides a great user experience.

Between Flutter and React-Native, we chose to use Flutter, because it is lighter, faster, produces smaller packages and automates the application deployment in the stores. Also, Flutter has its own game engine, the Flame engine, which will make the development of our game easier.

In addition, Flutter has libraries (e.g. [qartvm](https://pub.dev/packages/qartvm), [quantools](https://pub.dev/packages/quantools)) for performing quantum calculations and simulating quantum circuits, which may be useful in the game development process, while there are no corresponding libraries in React-Native.
