Lesson 1.1 “Introduction to Swift and Playgrounds”
Excerpt From: Apple Education. “App Development with Swift.” Apple Inc. - Education, 2017. iBooks. https://itunes.apple.com/us/book/app-development-with-swift/id1219117996?mt=11

* “What's a modern language? It's one that's safe, fast, and expressive. As Apple was designing Swift, those three primary goals were at the core of every decision.”
    * “Some of the features that make Swift a modern language include:
        * “Clean syntax, which makes code readable and easier to work with
        * Optionals, a new way of expressing when a value may not exist
        * Type inference, which speeds up development and allows the compiler to help identify common issues
        * Type safety, which enforces code that's less likely to crash your program
        * Automatic Reference Counting (ARC) for memory management, which automatically handles some of the deeper technical challenges of native programming
        * Tuples and multiple return values, which allow smaller units of code to do more
        * Generics, which help developers write code that can be used in multiple scenarios”
        * “Fast and concise iteration over collections, making Swift a fast language
        * Structs that support methods, extensions, and protocols, which allow Swift to optimize for memory use and speed while providing flexibility for developers
        * Map, filter, reduce, and other functional programming patterns, which simplify code and streamline common actions that previously required multiple lines of code
        * Powerful error handling, which helps the developer write fewer bugs and better handle scenarios that could cause apps to crash or perform unexpectedly”
*  Open Source 
    * [swift.org](http://swift.org/ "Title")

Lesson 1.2 “Constants, Variables, and Data Types”
Excerpt From: Apple Education. “App Development with Swift.” Apple Inc. - Education, 2017. iBooks. https://itunes.apple.com/us/book/app-development-with-swift/id1219117996?mt=11
Excerpt From: Apple Education. “App Development with Swift.” Apple Inc. - Education, 2017. iBooks. https://itunes.apple.com/us/book/app-development-with-swift/id1219117996?mt=11

* What You'll Learn
    * How to represent numbers, strings, and boolean values using native Swift data types
    * When to use a constant and when to use a variable
    * How to assign values to constants and variables
    * How type inference helps you write clean code
    * How type safety helps you write safe code
* Vocabulary
    * Naming Rules - There are rules for naming constants or variables. The compiler enforces the rules, so you won't be able to build and run your program if you break them.
        * Names can't contain mathematical symbols.
        * Names can't contain spaces.
        * Names can't begin with a number.
        * But can be unicode symbols 
        * Best Practices
            * “Constant and variable names should be clear and descriptive, making it easy to understand the code when you come back to it later. For example, firstName is better than n and restaurantsNearCurrentCity is better than nearby”
            * “To be clear and descriptive, you'll often want to use multiple words in a name. When you put two or more words together, the convention is to use camel case, which means that you lowercase the first letter in the name and then capitalize the first letter of each new word. You've probably noticed examples of this already: defaultScore is the camel case treatment for the combination of default and score. Camel case is easier to read than all the words mushed together. For example, defaultScore is clearer than defaultscore and restaurauntsNearCurrentCity is clearer than restaurantsnearcurrentcity.”
    * var
    * let - constant
        * First, if you set a value to a constant, the compiler understands that it should never be changed. This means you won't be able to build or run your program if you try to change the constant's value. In this way, the compiler enforces safety.
        * Second, there are special optimizations that the compiler can make for constant values. When you use constants for values that won't change, the compiler can make low-level assumptions about how to store the value. These adjustments allow your program to execute faster.
    * comment
        * use // Comment 
        * or /* Comment */
    * Types - “type definition as a blueprint for how objects should look and function. ”
        * Double
        * Bool
        * Int
            * “ Swift allows you to put underscores in your numbers as a way of formatting for easier reading.”
                * var largeUglyNumber = 1000000000
                * var largePrettyNumber = 1_000_000_000
        * String
        * Collection types...
            * Array
            * Dictionary
    * type safety - “When compiling your code, Swift performs type checks on all of your constants and variables, and flags any mismatched types as errors. If you mismatch types, you won't be able to run your program.”
    * type inference - “Once you assign a value to a constant or variable, the type is set and can't be changed. This is true even for variables. The value of a variable may change, but not its type.”
        * type annotation - “There may be cases when it's useful, or even required, to explicitly specify the type of a constant or variable.”, e.g.  “let cityName: String = "San Francisco".  There are three common cases for using type annotation.
            * “When you create a constant or variable but haven't yet assigned it a value.”
            * “When you create a constant or variable that could be inferred as more than one type”
                * “let middleInitial: Character = "J" // "J" would be inferred as a `String`, but we want a `Character`”
            * “When you write your own type definition.”
                * “struct Car {var make: String, var model: String, var year: Int }”
        * “You can use a type annotation with different number types. The Swift compiler will adjust the value to match the type.”
            * “let number: Double = 3”
    * immutable
    * mutable
    * property
    * variable

    * Related Resources
        * [Swift Programming Language Guide: Constants and Variables](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html#//apple_ref/doc/uid/TP40014097-CH5-ID310 "Title")


Lesson 1.3 Operators
* Numberic type conversion
    * let pi = Double(x) + y where x is int and y is Double
* Vocabulary
    * compound assignment
        * e.g. myScore += 3 
    * operator
* Related Resources  
    * [Swift Programming Language Guide: Basic Operators](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-ID60)

Lesson 1.4 Control Flow
* Boolean values
    
        let isSmallNumber = number < 10
        // number is not less than 10, so isSmallNumber is assigned a `false` value 
* Switch statement
```
        let numberOfWheels = 2
        switch numberOfWheels {
        case 1:
            print("Unicycle")
        case 2:
            print("Bicycle")
        case 3:
            print("Tricycle")
        case 4:
            print("Quadcycle")
        default: 
            print("That's a lot of wheels!")
        }

        let character = "z"
        switch character {
           case "a", "e", "i", "o", "u" :
                print("This character is a vowel.")
            default: 
                print("This character is a consonant.")
        }

        switch distance {
            case 0...9:
                print("Your destination is close.")
            case 10...99:
                print("Your destination is a medium distance from here.")
            case 100...999:
                print("Your destination is far from here.")
            default: 
                print("Are you sure you want to travel this far?")
        }
``` 
* Ternary operator
    * `largest = a > b ? a : b`
* Vocabulary
    * conditional 
        * if statement
        * If-else statement
    * interval matching
    * logical operators 
    * switch
* Related Resources 
    * [Swift Programming Language Guide: Control Flow](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/BasicOperators.html#//apple_ref/doc/uid/TP40014097-CH6-ID60) 

Lesson 1.5 Xcode
* File types
    * .xcodeproj 
        * file, which includes all the settings for your project and its targets.
    * .swift 
        * extension contain Swift code, as you'd expect. 
    * .storyboard 
        * files are unique to Interface Builder. They contain information about the design of each scene within your application, as well as how one screen transitions to another. 
    * .xcassets 
        * file makes it easy to maintain all your assets, without needing to work with individual icons and images. This asset catalog has two advantages: It reduces the list of items in the project navigator; and it shows which images will be used for devices of different screen sizes—helping you quickly identify that you're missing assets for a particular device.
    * Info.plist 
        * file contains a list of properties and settings for your app. In earlier versions of Xcode, you needed to edit this file directly, but newer versions allow you to edit settings—including app version, app icon, and device orientation—using the .xcodeproj file that you learned about earlier
* Keyboard shortcuts
    * Command-B—Build the project
    * Command-R—Build and run the project
    * Command-/—Toggle comments on selected rows of code
    * Command-[—Shift the selected code left
    * Command-]—Shift the selected code right
    * [Xcode Keyboard Cheat Sheet](https://swifteducation.github.io/assets/pdfs/XcodeKeyboardShortcuts.pdf)
