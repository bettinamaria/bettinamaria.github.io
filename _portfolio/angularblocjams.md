---
layout: post
title: BlocJams Music Player
thumbnail-path: "img/blocjams.png"
short-description: BlocJams is a digital music player, a Spotify replica where you can find music to play back and listen to online.

---

{:.center}
![]({{ site.baseurl }}/img/blocjams.png)

## Explanation

For this project in the front end web development foundation part, the task was to build Bloc Jams; think of it like a replica of Spotify, a digital music player where you can find music to play back and listen to. After the initial built was done by leveraging Html, CSS and plain Javascript, I had to rebuild the app using the Angular framework.  Requirements were to build the backbone of the application by using Angular, a single web page application framework to serve as the overall structure; with HTML to be used as the backbone of the application layout, CSS and jQuery to add styling, like animations and responsiveness to the web app and to implement interactivity to the music player (e.g. to start and stop playing a song and to jump from one song to the next) with Javascript. 
Angular is a Javascript framework that is mainly used to build CRUD (Create, Read, Update, Delete) dynamic web applications. These dynamic web applications come in the form of single-page applications (SPAs) that do not require page loads when navigating between pages. Examples of SPAs include Gmail and Medium.

## Problem

Now, what does a digital music web player need to actually work? The requirements for Bloc Jams Angular were outlined in user stories i.e. a step by step breakdown of the web app's structure to build all of its functionality. Basically, my homework as a developer was to find a way to solve and implement the following.  
1. Bootstrap Angular to the existing Bloc Jams application and create an Angular module
  * Configure routing and states for the application
  * Implement controllers for the application's views
  * Create a service that controls song playback
  * Write a custom directive that controls song and volume sliders
  * Create a custom time code filter
  * Complete all user stories and ensure web app runs as anticipated

## Solution

With the initial setup of the app - *it was explained that it is better to use a NodeJS server*. *SPAs that change the URLs of an application require a server to intercept their requests and allow the frontend of the application to handle what's displayed in the browser.*
Most web applications refresh when we navigate to a different page on the site. When a user clicks a link, the application sends a request to the server for a new HTML file. The browser then reloads the entire page with the newly received information.

An alternative to this request/response process is to use single-page applications (SPA). They have engineering benefits as well as a snappier user interface that feels like a native desktop application.
he browser also has to load a new HTML document when a user navigates between the pages, which can result in a slow experience. With Angular, we can pull the shared HTML into one global file, and each of the unique fragments into separate templates. Templates, in this context, are HTML documents with Angular markup.

## Results

After working through all user stories, the music player works as requested. 

## Conclusion

This project taught me how to look at a web application by breaking the music player's functionality down into small steps. It made me better understand how each part interacts with each other and how one would look at building play, pause, next and previous song button from scratch. 