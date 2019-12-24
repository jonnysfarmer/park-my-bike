# Park My Bike

## Overview

My second project was a React web app giving you all surrounding bike park locations around a London postcode, with an additional feature of cycling directions from a 2nd postcode.

This was the second project from General Assembly Software Engineering Immersive, and was a 48 hour paired programming project.

Launch on [GitHub Pages](https://jonnysfarmer.github.io/park-my-bike/).  Check out the GitHub [Repo](https://github.com/jonnysfarmer/park-my-bike).

## Brief

- Pair program
- Create a react app that talks to an API and displays some data
- Use any API you like
- Deploy on Github pages

## Technologies Used
 - React
 - Axios
 - Bulma
 - Mapbox
 - React Router
 - CSS
 - JavaScript (ES6)
 - GitHub Pages
 - Webpack

### APIs used:
- [Postcode API](https://postcodes.io/)
- [TFL API](https://api.tfl.gov.uk/)

## Approach Taken

We had approximately 48 hours to plan, code and present our projects.  We investigated multiple free APIs which gave good quality data.  Once of our team was a keen cyclist and we came across the cycle park API from TFL.  We were also keen to use Mapbox as neither of us had used this before.

### Features
The key features was that a user could input their postcode.  This would then display all cycle-parks in a 250m radius of them on a map.  You can get more information about the specific cycle park when clicking on point of interest.  The user can then input another postcode giving directions cycling directions to that specific cycle park.

### Information Flow

A lot of this project was converting postcodes to Longitude / Latitude co-ordinates and vice-versa.  

 - User inputs destination postcode.  This is then converted to Long / Lat via the Postcode API and put into MapBox & the TFL cycle park API with the various locations posted on the map as pins.
 - The Long / Lat is passed via the URL.  If the user moves the map, to stop constant TFL API calls, there is a refresh button which re populates the map with parking points.
 - On pin click, the parking point information is displayed as a pop up including image, distance and number of parking points.
 - On Pop up click, it gives the user the ability to input a 'starting location' postcode for navigation.
 - On input, the park point location is converted from Long / Lat to a postcode via the Postcode API, and both postcodes are inputted into a TFL cycling directions API.
 - These directions are then mapped into a table and displayed.
 - The user starting postcode for the directions is saved so the user can find directions by clicking on additional pop ups without re inputing your starting location unless you click the rest button.

 ### Images
 
![Front-page](images/1.png)
![Map-View](images/2.png)
![directions-1](images/3.png)
![directions-2](images/4.png)