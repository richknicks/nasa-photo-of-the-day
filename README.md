# Module Project: Component Side Effects- NASA APOD

## Description

In this project I built out an application to show the nasa photo of the day.

## Project Set Up

---

This project was put together using create-react-app (CRA). You will not need to install CRA in order to make this project work.

# _Project - NASA APOD 

- This is a really fun project, and one to show your family and friends when you've finished.
- You will be starting from scratch and building the entire app
- You don't have any design specs to follow for this project, so you may want to start by building a basic wireframe first. Make it simple at the beginning, since you don't know what data you'll be getting back from NASA
- Once you get the data back, there may be more than you expected, or less than you expected, so your design plans may change. That's totally fine, and very normal in the real world. Just make the proper adjustments and move forward!

## Directions

**Step 1 - Planning**

- [ ] If you want, this is the time to make a simple design spec (look up ["simple wireframes"](https://www.google.com/search?q=simple+wireframes) to find resources & examples). **A pen & paper sketch (or outline) is often the fastest way to start your planning.**
- [ ] Once you have a design plan in mind, break down the designs into individual components.
- [ ] Plan which components will hold state, what data each needs from props (if any), and where you will be making your data fetch.
- [ ] Now it's time to jump into the code!

**Step 2 - File structure**

- [ ] Take a look at your planned components. Create the folders and files you need for each component.
- [ ] Leave most of them blank for now - you need to get your data from the API before you can really get these built.

**Step 3 - Fetching the Data**

- [ ] In `App.js` (or where ever you wanted to fetch the data) add state for the data you'll be getting from NASA.
- [ ] Add an effect hook to handle the API call side effect.
- [ ] Go to the [NASA APOD API docs](https://api.nasa.gov/#apod) and read through the docs to see how to make the API call.
- [ ] You don't _need_ an API key. However you may need one if you exceed the API request limits.
- [ ] Using the endpoint given, fetch the data using `axios`.
- [ ] In your `.then()` make sure to `console.log` the response so you can look at the shape of the data. 😃
- [ ] Before you add your data to state, make sure your effect hook has a dependency array (probably empty, since we don't want this effect synced up to any state/props), otherwise you will start an **infinite loop, and you will exceed the API rate limits of the DEMO_KEY and need to use a real API_KEY.**

DEMO KEY rate limits:

> Hourly Limit: 30 requests per IP address per hour

> Daily Limit: 50 requests per IP address per day

_Note: if the photo url is NOT a photo, you will need to learn how to display a video in a React app on your own, OR just fetch the APOD from a different date by adding this to the back of the API endpoint: `&date=2012-03-14`_

**Step 4 - Adding the Data to State**

- [ ] Once you have made the call correctly, and logged the data, add the data to the state property you built.

**Step 5 - Display the Data**
Now is the time to build out your other components. Compose your UI, and then pass the data to your children components via props so you can render it on the DOM.


## Pro Tips:

- You may run into an error where your components try to access object properties before your data is finished being fetched - ie. `Cannot read property 'url' of undefined`. This means that the data you passed as props is undefined, when you were expecting it to be an object. You can fix this by simply adding something like this to any component that needs to read data from your state object:

```js
// Display a loading message while the data is fetching
if (!props.photoOfTheDay) return <h3>Loading...</h3>;

// Display your component as normal after the data has been fetched
return (
  {* your normal JSX here *}
);
```

- Read through the API docs carefully. 

## Functionality
Working

## Tech Stack

React, Axios, JSX

## How to use

Simply just go to your terminal and type in nmp start and you can run it locally on your browser or you can deploy it and see through a webpage. 




