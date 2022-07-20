# iOS-question

# 1. iOS - viewDidLoad is being called BEFORE the didFinishLaunchingWithOptions delegate?
The documentation for application:didFinishLaunchingWithOptions:

> You should use this method to initialize your application and prepare it for running. It is called after your application has been launched and `its main nib file has been loaded`. At the time this method is called, your application is in the inactive state. At some point after this method returns, a subsequent delegate method is called to move your application to the active (foreground) state or the background state.

So the view is lazily loaded for view controllers once the the view property or method is called. When this happens viewDidLoad is called so if your window rootViewController property is set to your root ViewController in the nib then this is expected behavior.

More detail: [#1](https://stackoverflow.com/questions/7030635/ios-viewdidload-is-being-called-before-the-didfinishlaunchingwithoptions-deleg).

# 2. That “return” keyword in guard let statement in Swift
###### Example: Return

    func printMyNames(names: [String?]) {
      for i in 0..<names.count {
        guard let myName = names[i] else {
          print("error: name is not found")
          return
        }
        print(myName)
      }
      print("End of For Loop")
    }
  
> `Return not only breaks out of loop but it also exits the function instantaneously`. So our results should be:

```
Output: // Mumtaz
        // Hussain
        // error: name is not found
```

# Design patterns
Questions about design patterns, code architectures, and other programming approaches.

# 1. How would you explain delegates to a new Swift developer?

# Data
Questions dealing with data and data structures.

# 1. How is a dictionary different from an array?

# Accessibility
Questions that cover making apps easier to use for everyone.

# 1. How would you explain Dynamic Type to a new iOS developer?

# Frameworks
Questions about Apple frameworks and APIs beyond UIKit and SwiftUI.

# 1. How does CloudKit differ from Core Data?

# iOS
General questions about building for iOS itself, or UI questions that apply to both UIKit and SwiftUI.

# 1. How do you create your UI layouts – storyboards or in code?
