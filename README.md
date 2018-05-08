


# Location Based Quiz

This repository contains the code for the server that is required to run the Location Based Quiz system that was created for the module ['Web and Mobile GIS - Apps and Programming'](https://sp.cege.ucl.ac.uk/study/Pages/Module-Guide.aspx?ModileCd=CEGEG077) at University College London.

This system comprises of two applications:  **a mobile application** and **a web application**. Together, these applications aim to create a functional location-based quiz. The overall purpose of this application is to encourage users to explore new places, whilst also learning something about the locations they visit through the answering of multi choice trivia questions.

## The Mobile Application
[The mobile application](https://github.com/nikscrits/quiz) is the user interface for the system where the user can track their location and answer nearby questions. It can be downloaded to an android phone using [this link](https://build.phonegap.com/apps/3152351/builds). The user help guide for the mobile application can be found  as a html page [here](https://rawgit.com/nikscrits/quiz/master/userguide/Quiz%20User%20Guide.html) or as a PDF file [here](https://github.com/nikscrits/quiz/blob/master/userguide/Quiz%20User%20Guide%20PDF.pdf).

<p align="center"><img src="https://github.com/nikscrits/server/blob/master/screenshots/mobapp.png" width="500"></p>

### Target Audience

This part of the system is designed for an end user with an andorid device who enjoys quizes! The application's simple interface should make it appropriate for users of any age or experience level. 

### Technical Requirements

This mobile application was developed for an Android mobile device with the following specifications ([full spec](https://www.gsmarena.com/motorola_moto_g_(3rd_gen)-7247.php)), therefore running the application on a device with a lower spec may be supported but is not recommended.

>Display size - 5", LCD touchscreen, 720x1280 pixels

>OS  - Android 6.1 (Marshmallow)

>RAM - 1 GB

>GPS - Yes

### Setup and Running the Mobile Application

1. Download the application on a suitable android device using the QR code found [here](https://github.com/nikscrits/server/blob/master/screenshots/QRcode.png) or via the phonegap website using [this link](https://build.phonegap.com/apps/3152351/builds).
2. Navigate to the httpServer.js location or if not already done, clone this server repository:
```
git clone https://github.com/nikscrits/server
cd server
```
3. Run the server in the background:
```
node httpServer.js &
```
4. Open the application on the android device.

## The Web Application
[The web application](https://github.com/nikscrits/questions) is the administrator interface where questions can be set for the users to answer. It can be accessed from [this link](https://http://developer.cege.ucl.ac.uk:31288/) when both the httpServer.js (found in this repository) and the phonegap server (found in the web application repository) are running. The user help guide for the web application can be found as a html page [here](https://rawgit.com/nikscrits/questions/master/userguide/Questions%20User%20Guide.html) or as a PDF file [here](https://github.com/nikscrits/questions/blob/master/userguide/Questions%20User%20Guide%20PDF.pdf).

<p align="center"><img src="https://github.com/nikscrits/server/blob/master/screenshots/webapp.png" width="500"></p>

### Target Audience

This part of the system is designed for the administrator of the quiz to set questions for the users to answer on the mobile application. The webpage's simple interface should make it appropriate for users of any age or experience level. 

### Technical Requirements

This web application was developed using the Google Chrome browser. It was additionally tested using the Safari and Mozilla Firefox browsers. Therefore, running the application on another web browser may be supported but is not recommended.

### Setup and Running the Web Application

 1. Clone the web application repository:
```
git clone https://github.com/nikscrits/questions
```
2. Navigate to the httpServer.js location or if not already done, clone this server repository:
```
git clone https://github.com/nikscrits/server
cd server
```
3. Run the server in the background:
```
node httpServer.js &
```
4. Navigate back to the 'ucesncr' file within questions. Run the phonegap server:
```
cd ucesncr
phonegap serve
```
5. Use [this link](https://http://developer.cege.ucl.ac.uk:31288/) to open the webpage.

## The Server
In order for both the applications to successfully function, a connection to a database is required where the questions and answer data will be saved. The httpServer.js found in this repository facilitates this connection.

### Setup and Run the Server

 1. Clone the repository:
```
git clone https://github.com/nikscrits/server
cd server
```
2. Run the server in the background:
```
node httpServer.js &
```

>*Note: This installation assumes the UCL server and database connection for this module will be used.*

## Technologies Used

This system was build using a number of technologies and templates:

 - [Material design lite](https://getmdl.io/)
 - [Leaflet interactive maps](https://leafletjs.com/)
 - [Leaflet awesome markers](https://github.com/lvoogdt/Leaflet.awesome-markers)
 - [Phonegap](http://phonegap.com)
