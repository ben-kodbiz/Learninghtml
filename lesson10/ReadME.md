
# Lesson 10

Way to go!  You've reached the final lesson in HTML5 Web Applications.  In Lesson 10 we study the Application Development Life Cycle!

Using Chapter 1 of the Wiley HTML5 book, create a small web page with 10 facts about HTML5 and include the Application Life cycle.  You can access your copy of the book at http://computermentors.org/student.  Please ask a mentor for your login information.

Feel free to also use the study guide on our student portal as you prepare to take the certification exam.

You will receive up to 200 points for passing your exam, based upon your score.  For example, A score of 70% would receive 140 points since 140 is 70% of 200.  Or you can multiply your score percentage by 2.  80% = 160, 90% = 180, 100% = 200...

Good luck!


## Important Vocabulary
* App Container
* AppCache
* API - Application Programming Interface
* Application State
* CSS - Cascading Style Sheets
* Cookies
* Debugging
* Gesture
* HTML - Hypertext Markup Language
* HTTP - Hypertext Transport Protocol
* JavaScript
* localStorage
* Media Queries
* Namespace
* Platform-independent
* Scripting Language
* Session State
* sessionStorage
* touchEvent
* validator
* WindowsRT (Windows Runtime)
* W3C - World Wide Web Consortium



HTML, CSS, and JavaScript are interpreted languages, which means they do not require a compiler and are platform independent (they can run on tablets, phones, and computers of all kinds).  To package and deploy your project as an App for the Windows Marketplace you will need to use an App Development Tool such as Microsoft Visual Studio.

## The basic steps for building a web app are as follows:
1. Plan your project - Keep it simple!  You're just learning!!  Consider how you want people to interact with your app, such as size of buttons for touch interfaces, or if you need to store data.  Will that data be stored on their device or on a server?
2. Design a User Interface - Make it intuitive and attractive.  Button positions should make sense.  Consider what feels natural for button placement when you hold a tablet or phone in your hand.  Be sure to design a launcher icon for your app!!!
3. Update the App Manifest - The manifest file includes properties of the app and what is needed to run, such as Display name, description, orientation (landscape/portrait), file path to the app's icon, and the app's capabilities (system features or devices your app is compatible with).
4. Write Code!
5. Build the App, converting it into an actual app, using Visual Studio
6. Debug and Test - check for errors! 
7. Package - Package the app into a container, which holds all the various files required by the app, such as images, pages, JavaScript, etc.  By packaging an app into its own container the Windows Runtime Environment can manage memory and the app can run without possibly corrupting the Windows Operating System.  The App Container also makes the app easy to uninstall, since it's all packaged together as one piece, rather than having to download 100s of files. Packages may contain more packages!
8. Validate the app through a validation program or website to make sure it is not missing any vital markup.
9. Deploy the app to the Windows Store.

## Application States
When you first open an app or website, the session state is created.  The session state ends when you exit the app.

