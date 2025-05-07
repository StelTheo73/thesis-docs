# Mobile Application Development

Having completed the presentation of game-based learning and the basic theory around quantum computing, it is time to evaluate the options available for the development of the application, that is, the programming language, the framework and the game engine. First, we will define mobile game development and present the available application types, and then we will review the different programming languages and available frameworks.

Mobile application development is the process of creating software applications that run on mobile devices. The software can be preinstalled on the device, downloaded from an app store or accessed through a web browser. [@aws_mobile_app_development; @ibm_mobile_app_development]

Mobile games are digital games designed for mobile devices. They can utilize mobile sensors and hardware (e.g. accelerometers, GPS etc.), or even external peripherals, such as gaming controllers and AR/VR headsets.

## Platforms

There are two dominant operating systems for mobile devices, Google\'s Android and Apple\'s iOS. iOS is used only on Apple devices while Android is used by several manufacturers.

Developing applications on each of these platforms requires the use of different software development kits (SDKs). There are four approaches to mobile app development, which are compared below.

### Native Applications

A native mobile application is a software application that is designed for a specific operating system platform [@techopedia_native_mobile_app]. Native mobile apps can only work on the platform that they are designed for, because they use the programming languages, frameworks and interfaces that are platform-specific. They run directly on the operating system, so they tend to perform better than other applications that require interaction with the device\'s operating system or hardware.

Because native apps are compiled directly into machine code, there have to be a different code base for each version of the same application (i.e. iOS or Android version). This is a requirement that significantly increases the cost and time of development and maintenance. [@aws_mobile_app_development; @techopedia_native_mobile_app]

Native android apps are built with the _Android SDK_^[https://developer.android.com/studio] and use _Java_^[https://dev.java/learn/getting-started/] or _Kotlin_^[https://kotlinlang.org/docs/getting-started.html]. On the other hand, native iOS apps are built with the _iOS SDK_^[https://developer.apple.com/develop/] and use _Swift_^[https://developer.apple.com/swift/] or _Objective-C_^[https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html].

### Cross-Platform Applications

Cross-platform apps have the ability to operate on different operating systems with little to no modification. Because the use universal coding languages and frameworks, cross-platform apps can run on iOS and Android using the same codebase. These coding languages and frameworks hide from developers the underlying differences between operating systems. [@techopedia_cross_platform]

Multiplatform apps reduce the cost for building and maintaining an application that targets different platforms. On the other hand, there are some performance issues and the access to device-specific features is limited, because they are not interacting directly with the operating system or the hardware. [@techopedia_cross_platform; @aws_mobile_app_development]

According to Statista, the most popular frameworks for multiplatform development are _Flutter_^[https://docs.flutter.dev/], _React-Native_^[https://reactnative.dev/] and _Kotlin Multiplatform_^[https://kotlinlang.org/docs/multiplatform.html]. [@statista_cross_platform]

### Hybrid-Web Applications

A hybrid-web application combines the elements of native and web apps. They are essentially web apps that have a native app shell. They are build with standard web technologies, like _JavaScript_^[https://developer.mozilla.org/en-US/docs/Web/JavaScript] and _HTML_^[https://developer.mozilla.org/en-US/docs/Web/HTML] and are bundled as native app packages. Hybrid apps are executed inside a container, which wraps the applications and acts as a bridge between the application and the operating system. [@techtarget_hybrid_app; @teska_containerization]

Although these apps reduce development and maintenance cost and user experience is very good, their performance is very low, as they cannot take advantage of many native device features. [@aws_mobile_app_development; @techopedia_native_mobile_app]

### Progressive Web Applications

Progressive Web Apps (PWAs) skip App Store delivery and conventional installation processes - they are accessible via a URL. PWAs are web apps that use browser capabilities to provide an app-like user experience, so they are written using web technologies, such as _JavaScript_ and _HTML_.

PWAs are able to overcome certain disadvantages of Hybrid Web Apps, as they have better performance and more extensive access to device features. They also have low development and maintenance cost, but the app capabilities are restricted by the browser the use. [@aws_mobile_app_development; @techopedia_native_mobile_app]

## Languages and Frameworks

### Android

#### Java {.unnumbered}

_Java_ is a high-level, class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible. _Java_ applications are compiled in byte-code that can run on any _Java_ Virtual Machine (JVM), meaning that compiled _Java_ code can run on all platforms without the need to recompile. It was initially released in 1995. Although Android is built on the Linux kernel, which is largely written in _C_^[(https://en.wikipedia.org/wiki/C_(programming_language)], the _Android SKD_ uses the _Java_ language as the basis for its applications. [@wikipedia_java]

#### Kotlin {.unnumbered}

_Kotlin_ is a high-level, statically typed, general-purpose programming language with type interference. _Kotlin_ is designed to interoperate fully with _Java_ and the JVM version of _Kotlin\'s_ standard library depends on the _Java_ class library. _Kotlin_, released by JetBrains in 2016, aims to address _Java’s_ shortcomings and enhance development productivity. [@wikipedia_kotlin; @medium_kotlin_vs_java_1]

#### Comparison {.unnumbered}

Both _Java_ and _Kotlin_ compile to byte-code for the JVM, offering similar performance. _Java_ applications tend to consume more memory, while _Kotlin_ has more efficient memory management, with inline and extension functions that can reduce memory footprint. _Kotlin_ has better startup time due to type interference, leading to faster initialization. Both languages support multithreading, but _Kotlin\'s_ co-routines simplify concurrent code handling. _Kotlin_ offers modern features and capabilities for Android development while Java has stronger community support. [@geeksforgeeks_kotlin_vs_java; @medium_kotlin_vs_java_1; @medium_kotlin_vs_java_2]

### iOS

#### Objective-C {.unnumbered}

_Objective-C_ is a high-level, general-purpose, object-oriented programming language that first appeared in 1984. It is influenced by _C_^[https://en.wikipedia.org/wiki/C_(programming_language] and _Smalltalk_^[https://en.wikipedia.org/wiki/Smalltalk] and it was primarily selected by _NeXT_^[https://en.wikipedia.org/wiki/NeXT] for _NeXTSTEP_^[https://en.wikipedia.org/wiki/NeXTSTEP] operating system. Apple chose _Objective-C_ as the main programming language for iOS and macOS, because macOS was based on _NeXTSTEP_. [@wikipedia_objective_c]

#### Swift {.unnumbered}

_Swift_ is a high-level, general-purpose, multi-paradigm programming language created in 2010 by Apple. _Swift_ is intended to support the core concepts of Objective-C, but in a safer way. It compiles to byte-code and uses an _LLVM compiler_^[https://en.wikipedia.org/wiki/LLVM]. [@wikipedia_swift]

#### Comparison {.unnumbered}

_Objective-C_ has more complex and verbose syntax than _Swift_. It uses square brackets and has longer syntax for method and property definitions, while _Swift_ is more concise and readable, with a syntax that resembles natural language. _Swift_ is also significantly faster than _Objective-C_ and offers a modern framework (_SwiftUI_^[https://developer.apple.com/xcode/swiftui/]) to build user interfaces. On the other hand, _Objective-C_ has many well-documented, third-party frameworks and is well-tested and more stable. Also, it is a superset of _C_, so it works smoothly with _C_ and _C++_^[https://en.wikipedia.org/wiki/C%2B%2B] code. [@medium_swift_vs_objective_c; @netguru_swift_vs_objective_c]

### Cross-Platform Frameworks

#### Flutter {.unnumbered}

_Flutter_ is a user interface (UI) SDK developed and released by Google in 2017. It can be used to create natively compiled mobile, web and desktop apps from a single codebase. It uses its own rendering engine to draw widgets on the screen, unlike other UI frameworks that rely on the platform\'s rendering engine or manipulate the platform\'s built-in UI stack. _Flutter_ also provides access to native APIs. The _Dart_^[https://en.wikipedia.org/wiki/Dart_(programming_language)] programming language is used to write applications in _Flutter_ and the applications are compiled ahead-of-time (AOT) on all platforms except the web, where the code is transpiled to _JavaScript_ or _WebAssembly_. [@wikipedia_flutter; @jetbrains_cross_platform; @medium_cross_platform]

#### React-Native {.unnumbered}

_React-Native_ is a UI SDK released by Meta Platforms (formerly Facebook Inc.) in 2015 and can be used to develop apps for mobile devices, Android TV, tvOS, web applications and desktop applications. Its components wrap existing native code and can interact with native APIs. _React-Native_ apps are written in _JavaScript_ or _TypeScript_. [@wikipedia_react_native; @jetbrains_cross_platform; @medium_cross_platform]

#### Comparison {.unnumbered}

_React-Native_ is easier to learn, because it uses JavaScript as a programming language and has greater community support. On the other hand, _Flutter_ has better documentation and its command line interface (CLI) offers tools that allow Continuous Integration (CI) and Continuous Development (CD) to be created more easily than _React-Native_. _Flutter\'s_ CLI also offers the ability to automate application deployment in the app stores. Both frameworks feature hot-reload functionality, which allows developers to see changes instantly while modifying their code, without having to recompile.

_Flutter_ uses its own on widgets and libraries and its own rendering engine and compiles directly to native code, while _React-Native_ depends on the underlying platform and uses multiple _JavaScript_ layers before compiling to native code. Also, _React-Native_ requires the developers to use third-party libraries, both for development and testing. These facts make _Flutter_ significantly faster than _React-Native_, while allowing _Flutter_ to use less CPU and memory, have a smaller package size and have more consistent UI across platforms. [@radix_flutter_vs_react_native; @medium_flutter_vs_react_native]

## Platform, Framework and Game Engine Choice

The application that will be developed will be a cross-platform mobile application, in order to target users using both Android and iOS. We chose to develop a cross-platform application to get optimal performance, not rely on browser limitations and have a single codebase. This choice also reduces development and maintenance costs and provides a great user experience.

Between _Flutter_ and _React-Native_, we chose to use _Flutter_, because it is lighter, faster, produces smaller packages and automates the application deployment in the stores. Also, _Flutter_ has its own game engine, the _Flame Game Engine_^[https://flame-engine.org/], which will make the development of our game easier.

In addition, _Flutter_ has libraries (e.g. _qartvm_^[(https://pub.dev/packages/qartvm], _quantools_^[https://pub.dev/packages/quantools]) for performing quantum calculations and simulating quantum circuits, which may be useful in the game development process, while there are no corresponding libraries for _React-Native_.
