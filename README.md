# HybridApp_JS

#### Explain the concept of: Hybrid Mobile App Development.
* Hybrid Apps make it possible to embed HTML5 and JavaScript app's inside a mobile application (IO, Android), still being able to use phone functions, combining the best (and worst) elements of Native and HTML5 apps.  
* Native Apps are specific to a given mobile platform (iOS or Android) using the development tools and language that the respective platform supports. Native apps look and perform the best.  
* HTML5 Apps use standard web technologies, like JavaScript and CSS to create cross platform mobile applications. Limitations from this strategy is: session management, no secure offline storage, no access to native device functionality (camera, calendar, etc).  

![alt tag](https://cloud.githubusercontent.com/assets/16150075/24773151/4a880236-1b14-11e7-82a5-b72112b67b37.PNG)
![alt tag](https://cloud.githubusercontent.com/assets/16150075/24773135/3cb931d4-1b14-11e7-90d0-ef1724fa46f6.PNG)

To get native-like functionality in HTML apps, we can use a tool such as Cordova.  
Apache Cordova enables software programmers to build applications for mobile devices using CSS3, HTML5, and JavaScript instead of relying on platform-specific APIs like those in Android, iOS, or Windows Phone.  
It enables wrapping up of CSS, HTML, and JavaScript code depending upon the platform of the device.  
It extends the features of HTML and JavaScript to work with the device. The resulting applications are hybrid, meaning that they are neither truly native mobile application (because all layout rendering is done via Web views instead of the platform's native UI framework) nor purely Web-based (because they are not just Web apps, but are packaged as apps for distribution and have access to native device APIs).


#### Explain the Pros & Cons of using Hybrid Mobile App Development compared to Native App Development.
Pros for Hybrid:  
* Much cheaper than Native apps which makes it good for startups.
* It can be used across platforms like IOS and android.
* It is faster to develop and make a demo of the app.  

Cons for Hybrid:
* Performance isn't as good and not as fast as Native
* Can miss out on extra native api’s that are not supported by Cordova
* Doesn't utilize native features (like the camera) as good as Native applications.
* Does not support newly arrived features as quickly as Native.


#### Explain about the "building blocks" involved in an Ionic Hybrid Application.
Ionic framework is an free and open source library for building highly interactive apps. Ionic apps are made of high-level building blocks called components.  
Components allow you to quickly construct an interface for your app.
Components are primarily Angular directives with HTML and CSS and also can include JavaScript functionality.  
* AngularJS framework on javascript for front-end presentation layer.
* Cordova/Ionic for communication with phone hardware and a test server (Ionic serve).
* HTML5 & Sass for styling and display of components.
* ADB(Android Debug Bridge) to communicate with phone and enables debugging. It’s a “bridge” for developers to work out bugs in their Android applications.
* Node.js to bring all the code together using middleware, ionic, express and so on.

#### Explain and demonstrate ways to debug Hybrid Mobile Applications Running on a real device.
With Ionic you can debug your app through your browser using the sockets and ports that the phone uses to communicate with the browser, this enables you to see the console and debug live.  
Open Chrome and navigate to: "chrome://inspect/#devices"


#### Explain how and why, it is possible for a Hybrid Application to access native phone devices like location, calendar etc. 
Accessing native phone features, like location and the calendar, is possible through the use of Cordova plugins, it can act as an interface that can be used to expose native functionality.


#### Explain using an example how your Hybrid Application communicates with a backend.
In our case to make Hybrid Application to communicate with the back end we need database and we used Mongodb for that.  
After installing Mongodb, we run it by typing “mongod”.  

* Running on the server or an emulater/device. 
When you run the application on the browser you write "ionic serve", this means a local web server is started up and that your browser is opened to point at the local server address.  
This starts you up, looking at your app loaded in a browser on your computer with the address (if you chose localhost).  
When running on an emulator or a device you type "ionic emulate android" for the emulator or "ionic run" for a device.  
This brings you over to the index.html front-end view.  
* data setup. 
When you run it first time it's empty, so to know that a db is connected and that the backend communicates.  
We can insert some test data like this: Test Data This will show the test data on the started webpage.


#### Explain, using an example you have implemented, the "fundamentals" of an Ionic application.
Ionic uses AngularJS and Cordova to create Hybrid Apps, for the styling of this app Ionic uses CSS and JavaScript like BootStrap does. When creating the HTML for a the app, Ionic specific directives is used like this.
```html
<ion-side-menu side="left">
    <ion-header-bar class="bar-dark">
      <h1 class="title">Projects</h1>
      <button class="button button-icon ion-plus" ng-click="newProject()">
      </button>
    </ion-header-bar>
    <ion-content scroll="false">
      <ion-list>
        <ion-item ng-repeat="project in projects" ng-click="selectProject(project, $index)" ng-class="{active: activeProject == project}">
          {{project.title}}
        </ion-item>
      </ion-list>
    </ion-content>
  </ion-side-menu>
```
#### Explain, with focus on location, technologies related to locations used on:
Your app (client side). 
Your backend. 
TODO
