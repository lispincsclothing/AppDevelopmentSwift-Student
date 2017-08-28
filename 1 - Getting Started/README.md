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

Lesson 1.6 - Building, Running, Debugging an App
* After Simulator has launched, you should see a device image with a white background. To rotate the image from portrait to landscape orientation, use the keyboard shortcuts Command-Left Arrow and Command-Right Arrow.
* The Simulator image may appear quite large, depending on the screen resolution of your Mac and the device you chose to simulate. From inside the Simulator application, you can use keyboard shortcuts, from Command-1 to Command-5, to scale the device image up or down. If you're using an older Mac, you may want to select an older lower-resolution device, such as an iPhone SE, to reduce the total impact of Simulator on your system.
* “To quit Simulator, use the keyboard shortcut Command-Q.”
* “Simulator doesn't work for all portions of an app. Certain interactions depend on the actual physical device to run. For example, if you try to use Simulator to test an interaction with the Camera app, the program will crash. If your code depends on other hardware components that don't exist on a Mac—maybe an accelerometer, a gyroscope, or a proximity sensor—you'll want to test with an actual device”
* “There are also some software limitations with Simulator. For example, push notifications can be delivered to physical devices, and the MessageUI framework—which helps compose email and text messages—is incompatible with Simulator. If you're running into a lot of issues in Simulator, you might try testing the code on your iPhone or iPad. Your issues may be resolved.
* “issues: warnings, compiler errors, and bugs.”
    1. Try to understand the problem
    2. Brainstorm a potential solution
    3. Try the solution
    4. Verify it worked, repeat as necessary

1.7 Documentation
* Option-click the viewDidLoad() method name, and Xcode displays a popover with a brief description of the function and the OS versions that support it. It also shows which framework the function belongs to. In this case, the framework is UIKit.
* Within the Quick Help popover, click Method Reference to access Xcode documentation, which includes more thorough explanations and references to related functions. (You can also access this window from the Xcode Help menu or by using the shortcut Command-Shift-0.)
* You can also download all the guides and sample code to your computer—making them searchable from the documentation browser. Open Xcode Preferences (Command-Comma) and click Components. Select the Documentation section, near the top of the window, then click "Check and Install Now" to download the guides and sample code.
* You can also download all the guides and sample code to your computer—making them searchable from the documentation browser. Open Xcode Preferences (Command-Comma) and click Components. Select the Documentation section, near the top of the window, then click "Check and Install Now" to download the guides and sample code.

1.8 Interface Builder Basics

* Interface Builder opens whenever you select an XIB file (.xib) or a storyboard file (.storyboard) from the project navigator.
    * An XIB file contains the user interface for a single visual element, such as a full-screen view, a table view cell, or a custom UI control. XIBs were used more heavily before the introduction of storyboards. They're still a useful format in certain situations, but this lesson will focus on storyboards.
    * In contrast with an XIB, a storyboard file includes many pieces of the interface, defining the layout of one or many screens as well as the progression from one screen to another. As a developer, you'll find that the ability to see multiple screens at once will help you understand the flow within your app.

* Inspectors
    * In addition to the File and Quick Help inspectors (which are always available), the top of the utilities area displays four context-sensitive inspectors when you're in Interface Builder. To explore these different inspectors and how they can help you customize the objects in your view, select the button you just added—either in the Document Outline or in the scene itself.
    * The Identity inspector  allows you to edit the properties related to an object's identity, such as what class it belongs to. In this example, the button belongs to the UIButton class. If you'd defined a custom button class elsewhere, you could use the Identity inspector to change the class of the button you just added. You'll learn more about classes in a future section.
    * The Attributes inspector  provides a list of adjustable visual properties for the selected item. In the case of a UIButton, you can change attributes such as the button's text, text color,background, and alignment. Try changing the look of your button.
    * “The Size inspector  allows you to adjust the size and position of the selected element within the scene. You'll use the X and Y fields—where the top left of the screen corresponds to (0,0)—to change the position. The X value gets larger as you move the element farther to the right, and Y gets larger as you move down the screen. For UIButton, the Size inspector includes additional fields for adjusting the padding around the button's title or image.
* Many objects that you can configure in Interface Builder have properties that can only be set programmatically. For example, UIScrollView has a contentSize property that does not have a matching option in the Attributes inspector.  When you need to adjust one of these settings, you can do so programmatically by setting up an IBOutlet and updating the properties using dot notation.
    * `scrollView.contentSize = CGSize(width: 100, height: 100)`
* In fact, everything that you can do in Interface Builder can also be done programmatically, including setting up all child views and adding them to the screen.
```
let label = UILabel(frame: CGRect(x: 16, y: 16, width: 200,
height: 44))
view.addSubview(label) // Adds label as a child view to `view 
```