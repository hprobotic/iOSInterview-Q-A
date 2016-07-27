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

###App States

####Q11. When an app is said to be in not running state? 

A. An app is said to be in 'not running' state when: 
- it is not launched. 
- it gets terminated by the system during running.

####Q12. Assume that your app is running in the foreground but is currently not receiving events. In which sate it would be in? 

A. An app will be in InActive state if it is running in the foreground but is currently not receiving events. An app stays in InActive state only briefly as it transitions to a different state.

####Q13. Give example scenarios when an application goes into InActive state? 

A. An app can get into InActive state when the user locks the screen or the system prompts the user to respond to some event e.g. SMS message, incoming call etc.

####Q14. When an app is said to be in active state? 

A. An app is said to be in active state when it is running in foreground and is receiving events.

####Q15. Name the app sate which it reaches briefly on its way to being suspended.

A. An app enters background state briefly on its way to being suspended.

####Q16. Assume that an app is not in foreground but is still executing code. In which state will it be in? 

A. Background state.

####Q17. An app is loaded into memory but is not executing any code. In which state will it be in? 

A. An app is said to be in suspended state when it is still in memory but is not executing any code.

####Q18. Assume that system is running low on memory. What can system do for suspended apps? 

A. In case system is running low on memory, the system may purge suspended apps without notice.

####Q19. How can you respond to state transitions on your app? 

A. On state transitions can be responded to state changes in an appropriate way by calling corresponding methods on app's delegate object.

For example: 
`applicationDidBecomeActive` method can be used to prepare to run as the foreground app. 
`applicationDidEnterBackground` method can be used to execute some code when app is running in the background and may be suspended at any time. 
`applicationWillEnterForeground` method can be used to execute some code when your app is moving out of the background 
`applicationWillTerminate` method is called when your app is being terminated.

####Q20. List down app's state transitions when it gets launched. 

A. Before the launch of an app, it is said to be in not running state.
When an app is launched, it moves to the active or background state, after transitioning briefly through the inactive state.

####Q21. Who calls the main function of you app during the app launch cycle? 

A. During app launching, the system creates a main thread for the app and calls the app’s main function on that main thread. The Xcode project's default main function hands over control to the UIKit framework, which takes care of initializing the app before it is run.

###Core App Objects
---

####Q22. What is the use of controller object UIApplication?

A. Controller object UIApplication is used without subclassing to manage the application event loop.
It coordinates other high-level app behaviors. 
It works along with the app delegate object which contains app-level logic.

####Q23. Which object is create by UIApplicationMain function at app launch time?

A. The app delegate object is created by UIApplicationMain function at app launch time. The app delegate object's main job is to handle state transitions within the app.

####Q24. How is the app delegate is declared by Xcode project templates?

A. App delegate is declared as a subclass of UIResponder by Xcode project templates.

####Q25. What happens if IApplication object does not handle an event?

A. In such case the event will be dispatched to your app delegate for processing.

####Q26. Which app specific objects store the app's content?

A. Data model objects are app specific objects and store app’s content. Apps can also use document objects to manage some or all of their data model objects.

####Q27. Are document objects required for an application? What does they offer?

A. Document objects are not required but are very useful in grouping data that belongs in a single file or file package.

####Q28. Which object manage the presentation of app's content on the screen?

A. View controller objects takes care of the presentation of app's content on the screen. A view controller is used to manage a single view along with the collection of subviews. It makes its views visible by installing them in the app’s window.

####Q29. Which is the super class of all view controller objects?

A. UIViewController class. The functionality for loading views, presenting them, rotating them in response to device rotations, and several other standard system behaviors are provided by UIViewController class.

####Q30. What is the purpose of UIWindow object?

A. The presentation of one or more views on a screen is coordinated by UIWindow object.

####Q31. How do you change the content of your app in order to change the views displayed in the corresponding window?

A. To change the content of your app, you use a view controller to change the views displayed in the corresponding window. Remember, window itself is never replaced.

####Q32. Define view object.

A. Views along with controls are used to provide visual representation of the app content. View is an object that draws content in a designated rectangular area and it responds to events within that area.

####Q33. You wish to define your custom view. Which class will be subclassed?

A. Custom views can be defined by subclassing UIView.

####Q34. Apart from incorporating views and controls, what else an app can incorporate?

A. Apart from incorporating views and controls, an app can also incorporate Core Animation layers into its view and control hierarchies.

####Q35. What are layer objects and what do they represent?

A. Layer objects are data objects which represent visual content. Layer objects are used by views to render their content. Custom layer objects can also be added to the interface to implement complex animations and other types of sophisticated visual effects.

--
####Source: http://www.geekinterview.com/Interview-Questions/iOS
