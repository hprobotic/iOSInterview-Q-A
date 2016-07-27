# iOSInterview-Q-A
The top Internet companies iOS interview questions and answers

###Development Basics

---

####Q1. Where can you test Apple iPhone apps if you don’t have the device?

A. iOS Simulator can be used to test mobile applications. Xcode tool that comes along with iOS SDK includes Xcode IDE as well as the iOS Simulator. Xcode also includes all required tools and frameworks for building iOS apps.  However, it is strongly recommended to test the app on the real device before publishing it.

####Q2. Does iOS support multitasking? 

A. iOS 4 and above supports multi-tasking and allows apps to remain in the background until they are launched again or until they are terminated.  

####Q3. Which JSON framework is supported by iOS? 

A. SBJson framework is supported by iOS.  It is a JSON parser and generator for Objective-C. SBJson provides flexible APIs and additional control that makes JSON handling easier.

####Q4. What are the tools required to develop iOS applications? 

A. iOS development requires Intel-based Macintosh computer and iOS SDK.

####Q5. Name the framework that is used to construct application’s user interface for iOS. 

A. The UIKit framework is used to develop application’s user interface for iOS. UIKit framework provides event handling, drawing model, windows, views, and controls specifically designed for a touch screen interface.

####Q6. Name the application thread from where UIKit classes should be used? 

A. UIKit classes should be used only from an application’s main thread.  Note: The derived classes of UIResponder and the classes which manipulate application’s user interface should be used from application’s main thread. 

####Q7. Which API is used to write test scripts that help in exercising the application's user interface elements? 

A. UI Automation API is used to automate test procedures. Tests scripts are written in JavaScript to the UI Automation API.  This in turn simulates user interaction with the application and returns log information to the host computer.


###App States and Multitasking

--- 

####Q8. Why an app on iOS device behaves differently when running in foreground than in background? 

A. An application behaves differently when running in foreground than in background because of the limitation of resources on iOS devices.

####Q9. How can an operating system improve battery life while running an app? 

A. An app is notified whenever the operating system moves the apps between foreground and background.  The operating system improves battery life while it bounds what your app can do in the background. This also improves the user experience with foreground app.

####Q10. Which framework delivers event to custom object when app is in foreground? 

A. The UIKit infrastructure takes care of delivering events to custom objects. As an app developer, you have to override methods in the appropriate objects to process those events.

-----
####Source: http://www.geekinterview.com/Interview-Questions/iOS

