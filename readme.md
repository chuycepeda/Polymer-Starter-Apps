###Getting started

This is a repo to get a fast-track approach into progressive web apps using Polymer Starter Kit, plus Android and iOS deployments using Cordova.

#####Dependencies
* <a href="https://nodejs.org/en/download/">Install Node </a>
* Install Cordova <code>$ sudo npm install -g cordova</code>
* Install Yeoman <code>$ sudo npm install -g yo</code>
* Install Gulp and Bower <code>$ sudo npm install -g gulp bower</code>
* Install Polymer generator 
<code>$ sudo npm install -g generator-polymer</code><br>

---

#####Guidelines

Follow this guidelines to understand how these git files where generated and develop on your own instead of just cloning the repo. The following steps are done in terminal.
<br>
<br>

######1 - SETTING UP THE POLYMER FOLDER STRUCTURE
<code>$ mkdir polymer-app</code><br>
<code>$ cd polymer-app</code><br>
<code>$ yo polymer</code><br>

<br>

######2 - SETTING UP THE CORDOVA PLATFORMS
<code>$ cordova create polymerapp com.wtc.polymer.polymerapp PolymerAPP</code><br>
<code>$ cd polymerapp </code><br>
<code>$ cordova platform add android</code><br>
<code>$ cordova platform add ios</code><br>
<code>$ cd .. </code>

<br>

######3 - BUILDING YOUR WEB APP
<code>$ gulp</code> <br>
At this point your progressive web app is ready.

<br>

######4 - BUILDING YOUR ANDROID & IOS APPS
- Now, go to your /polymer-app/dist/ folder and copy all its files and folders.<br>
- Then, go to your /polymerapp/www/ folder, delete its contents and paste all your copied files.<br>
- Next do the following:<br>
<code>$ cd polymerapp </code><br>
<code>$ cordova build android</code>
<code>$ cordova build ios</code>

<br>

######5 - IT'S DONE !
- You can find your Android Studio project at /polymerapp/platforms/android/, where you can change default icon for example. Also .apk is at /polymerapp/platforms/android/build/outputs/apk/.
- You can find your XCode project at /polymerapp/platforms/ios/.


---

#####Developing on your own 

If you have either cloned the repo or followed the guidelines, now you must have a web app with its equivalent version for android and ios. Now, everytime you want to make some changes follow the next steps:
<br>

1. Edit your app at /polymer-app/app/ folder. To see live changes you can run <code>$ gulp serve</code>.
2. Once you finish, repeat steps 3 and 4 from the guidelines to build your distributable and get your updated android and ios versions.


---

###Deploying to Google App Engine or Firebase

For the ease of having your web app available on the web, I've included an <code>app.yaml</code> file in the root of this repo. After building your web app with <code>$ gulp</code> command, you can copy this file into the /dist/ folder and make deploy to Google App Engine.

<br>
<a href="https://www.polymer-project.org/1.0/start/toolbox/deploy">Detailed instructions can be found here.</a>
