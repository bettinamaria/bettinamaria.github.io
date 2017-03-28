---
layout: post
title: Blocitoff
thumbnail-path: "img/blocjams.png"
short-description: xxx

---

{:.center}
![]({{ site.baseurl }}/img/blocjams.png)

## Explanation

Bloc Chat is a real-time chat application that sends and receives messages between chat users.

## Problem

For Bloc Chat we also used the AngularJS framework and had to make use of Firebase, an external database to store our users' data in. 

The web chat's functionality had to contain of the following:
*  A list of available chat rooms
*  Ability to create new chat rooms
*  Display of a list of messages in each chat room
*  Ability to set my username to display in chat rooms
*  Ability to send messages associated with my username in a chat room

In addition, we were provided with basic wireframe sketches that suggested a design.

* Register Firebase as a module in an Angular application
* Inject the $firebaseArray service into a controller
* Understand and use the Firebase JavaScript and AngularFire APIs – methods such as *child()* and *$add()*
* Query a Firebase array
* Use UI Bootstrap to create a modal
* Use cookies to store information in the user's web browser

## Solution

First off, I had to understand how to use firebase and set up a back end database to store our Chat rooms data in. After this my Angular app, had to learn how that there was a list of chat rooms (i.e. room related API queries) stored in an external database i.e. in firebase and consequently retrieve the chat rooms and display them on the app interface. We then made use of the UI Bootstrap library to initiate new chat room creation within the app (by clicking on a button 'Create New Chat Room' which triggered a module asking for 'Enter a room name' and then 'Create room' or 'Cancel' submit buttons). The next user story how to see a list of messages in each chat room associated by username was pretty tricky to solve - we first had to create and style a container for holding a list of messages to the right of the list of available chat rooms. Whenever the user jumped between chat rooms, the active room would need to be triggered when clicking/entering from the sidebar. To achieve this, we had to associate an objects with other related objects, in this case we had to associate an active chat room with its user messages; so we had to associate the child data i.e. the room's message with the parent data, in this case the active chat room. The chat message objects were stored in firebase again and had four properties: username, content of message, time it was sent at, and the room Id). The latter room Id was to be generated every time an object got saved to Firebase. The last objective was to display the associated user name to each chat message so we would be able to see who is chatting to whom. A username is a string indentifying a user. To store a string in our browser we use cookies. Angular has an external module for including the services and methods associated with cookies and so we had to integrate this on our Bloc Chat app. In addition to telling Angular to run the cookies method to set a username at the time the app is initialized we also had to create a new pop up module to prompt the web app user to enter his/her user name. Basically, if Angular detected that there was no user, a pop up module would prompt the chat room user to set on. The new user trying to enter a chat room didn't get access to the actual chat until their username has been set. The last step was to verify that messages got sent between each chat room user as requested.

## Results

You can test out Bloc Chat's functionality by accessing it through Github.

## Conclusion

I enjoyed working on this app very much because it forced me to better understand how API requests and retrieval from external databases work. 