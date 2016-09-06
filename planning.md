# <img src="https://cloud.githubusercontent.com/assets/7833470/10899314/63829980-8188-11e5-8cdd-4ded5bcb6e36.png" height="60"> Project 1 Planning

This document gives you a little more guidance about the [Project 1 planning deliverables](./readme.md#planning-deliverables) and how to approach them.

### Scope

Software development is about managing complexity. It's easy for code to become a tangled web of tightly coupled functions or data structures if you aren't diligent.

The same applies to the scope of your project. If you're always looking at the top of the mountain, you'll trip on the rocks in front of you.

![iterative-design](https://cloud.githubusercontent.com/assets/7833470/11330092/f76e7c50-9159-11e5-875f-748817e41afc.png)

Figure out the absolutely simplest thing you can build that meets the project requirements, and start with *that* version of your app.

### User Stories

Outline your core user stories. As you build, you'll divide these into clear, smaller steps (sometimes called "development stories"). For example, this user story:

*As a user, I want to create a profile for a dog.*

Might consist of these steps:
```
* Wireframe what a profile page will look like.
* Create HTML and a Handlebars template for a profile page.
* Write a server route to serve the profile page html.
* Create a schema for a dog, defining attributes (e.g. name, age, favorite chew toy, etc.).
* Add a form to get new dog information.
* Make an AJAX call to the server with the form data.
* Fill in the controller for the RESTful route on the server that will create the new dog.  
...
```

You can use a [Trello](https://trello.com) board to track your progress, communicate with each other, and keep focused on the most important goals.

If you make each card a user story, you can make the steps for that user story into a checklist on the card. (You can also make each step an individual card, if you prefer.)

Add comments to your cards as you progress and complete features. By the end of your project you'll have a living log of "gotchas" you debugged and things you learned about the process of iteratively developing an app.

### Wireframes

Sketch out the pages of your app. What will they look like?

![wireframe](https://cloud.githubusercontent.com/assets/7833470/11330149/d84f3e94-915a-11e5-9b7d-31c41492dd6b.jpg)

![wireframe-progress](https://cloud.githubusercontent.com/assets/7833470/11330157/fbfaf388-915a-11e5-927c-1fa228b70f12.jpeg)

Once you have wireframes for the different pages of your site, you can wireframe how the pages will connect to each other by drawing the user flow.

![user-flow](https://cloud.githubusercontent.com/assets/7833470/11330163/1df572f6-915b-11e5-9458-a37dcc670360.png)


### Data Models

Write out the properties for your schema(s). Make sure to answer these questions:

* Will your application have many models or only a few?
* How will the models interact with each other?
* What attributes (properties) will the schemas have, and what kind of data types (string, integer, collection, etc.) will they use?

Consider drawing an entity relationship diagram (ERD) to visually represent related resources.

### Feasibility Check

Before you get started, you might need to do some research to see if what you want to do is possible in the amount of time you have. For example:

* read the documentation for an external api to determine what data you can request. Is it JSON? XML? Is all the information you want included in the response? Will you need to make several different requests to the API?  Do you need to sign up and wait for approval to use the API?

* verify that you can successfully request data from your API with Postman or `curl`.

* research something you want to use that hasn't been taught in class yet, like an external library or module, data store, etc.

#### Example Feasibility Checks

* [ ] Read Yelp API documentation.
* [ ] Use Postman to test Twilio API.
* [ ] Write a script to scrape news data.
