# argus-accidents
Real-time accident monitoring and reporting.

https://devpost.com/software/argus-dfgv04

## Inspiration
Following the news of a Tesla Model 3 colliding with a crashed tow truck in Moscow, Telsa claimed that there was a problem with the software in regards to detecting accidents.

## What it does
A web-app that uses object detection to monitor for accidents in CCTV cameras and report them immediately to a user's phone and browser client.

## How I built it
-Uses TensorFlow's object detection model for accident "detection".
-Google Maps API with custom interface. :0
-Server set up in Node.js. npm install nodemon server/server.js To run (see dependencies in package.json... there are some python dependencies but I forgot): python crash_detection_model.py
-Express.js because it makes things easier.
-Socket.io used to update the client with accident details.
-Twillio API to send SMS to the user at the moment of an accident.
-Google Geocoding API used to convert the unique markers' longitude and latitude to human-readable addresses.

## Challenges I ran into
Google does not like to be spammed with 100s of API calls in less than a second.

## Accomplishments that I'm proud of
Making a work-around for the above.

## What I learned
To move from static webpages to client-server web-applications. This includes: Node.js, Express.js, and Socket.io

## What's next for Argus
To use real live footage from CCTV cameras around the globe.
