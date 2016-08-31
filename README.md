# romxz.github.io

##Introduction

Our code creates a 3D render of a human bust which can be controlled using serial data (from Arduino) and a graphical user interface control panel. Features include: zoom in/out, lighting control, camera control. 

##Definitions

####Serial Communication and Serial Ports

Serial communication refers to the transportation process in which data is transferred one bit at a time sequentially. Serial ports are interfaces that allow for data transfer through serial communication, and have many important usages today in the fields of automation, scientific instrumentation, and commercial product development.

####Arduino

Arduinos are microcontroller boards that have the ability to read digital/analog data, write digital/analog data, and communicate with a computer using serial communication with its serial port, among other functions. 

####HTTP/Request/Response/GET

HTTP(Hypertext Transfer Protocol) allows for communication and data transfer between clients and servers. This communication occurs via a request-response protocol between a client and a server. GET is one system of this request-response protocol that requests data from the specified resource. 

####Node.js/ Express.js

Node.js is a runtime-environment for server-side Web applications. Most modules are developed in the Javascript language, and events are run in asynchronous I/O.  Express.js is a web framework application for Node.js that is the general standard for developing server-based applications. 

####Localhost

Localhost is the standard hostname that is assigned to the computational device in use (always with IP address 127.0.0.1. )

##File Explanations

####index.js

•	Initializes communication with the serial port and opens up a server. 

•	Gets an analog reading from the serial port and writes it to a client.


####public/index.html

•	Renders a 3D model that can be controlled using serial data. 

•	Imports the relevant JS modules and CSS styling used in the webpage.

•	Runs a script to make a looping request to the server. 

•	Makes a call to src/mesh_import_woman2.


####public/src/mesh_import_woman2.js

•	On startup, a woman’s 3D mesh is loaded, and the initial render, draw conditions (camera/light), and GUI control panel are enabled in the init() function. 

•	The render() function is looped that constantly collects serial data through making requests to the server, which is used to alter the orientation of the shapes on the webpage. 


##Requirements

	- Arduino Software
	- Node.js
	- Web Browser

##Additional Learning Resources

####Node.js


####Arduino

https://www.amazon.ca/Arduino-Starter-Official-170-page-Projects/dp/B009UKZV0A - a starter kit one can purchase to get started with Arduino, includes various electronics devices and a book with 15 projects in increasing difficulty. 

https://www.arduino.cc/en/Tutorial/HomePage - the official Arduino website for tutorials and references. 

https://learn.adafruit.com/category/learn-arduino - offers a plethora of examples for the user's viewing pleasure. 

http://forefront.io/a/beginners-guide-to-arduino/ - a tutorial to absolute beginners wanting to learn Arduino. 

####HTML/CSS

https://www.codecademy.com/learn/web - a basic tutorial to the syntax and general elements of HTML and CSS, and the relationship between the two languages. 

https://www.codecademy.com/learn/javascript - a tutorial that teaches basic Javascript, which can later be used in conjunction with HTML and CSS to influence certain elements on the webpage. 

https://www.codecademy.com/learn/jquery - a tutorial that teaches JQuery, a common Javascript library that makes it simple to create interactive websites that run functions on various event occurences. 

http://www.w3schools.com/ - an online reference that outlines and demonstrates both basic and advanced techniques and scripts regarding web development, including HTML/CSS/Javascript, as well as various Javascript libraries and server-side development. 

https://www.coursera.org/learn/html-css-javascript - an online course that teaches the basics of HTML/CSS and Javascript. 

####General Web Development

https://www.coursera.org/specializations/full-stack - a comprehensive online specialization consisting of 6 courses (5 of which can be obtained for free without the assignments). Covers HTML/CSS/JS, and moves into frameworks like AngularJS and running JS scripts using node.js, and finally covers server-side development using the express JS module and MongoDB. 

####Others

http://www.color-hex.com/ - an online reference for quickly finding HEX colour codes. 

http://stackoverflow.com/ - an online forum where one can publicly answer and ask questions. 

https://www.reddit.com/r/learnprogramming/ - another online forum for asking and answering questions. 

##Instructions

1.	Upload Arduino code that prints to serial. 
2.	Change constants in public/index.html (delimiters, axes, etc. depending on your Arduino code)
3.	Run index.js (through node.js), by typing “node index.js portname” in the command line. 
4.	Open your browser to the webpage “localhost:8080/index.html” to visualize the code at public/index.html.
