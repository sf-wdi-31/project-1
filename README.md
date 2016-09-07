# <img src="https://cloud.githubusercontent.com/assets/7833470/10423298/ea833a68-7079-11e5-84f8-0a925ab96893.png" width="60"> Project One

## DESCRIPTION

It's time to put everything that you've learned in the past month together! For your first project, you will build a full stack web application using jQuery and AJAX, Express, Node.js, Mongoose, and MongoDB.

Apply the skills you've learned by building a full-stack web application from the ground up, and build a polished, published website you can share in your portfolio.

You will be working in pairs for this project. Remember to communicate, communicate, communicate.  Show us what you've got!


##COMPLETED PROJECT DELIVERABLES

* Completion of the **technical requirements**
* On your personal site:
   - A link to your **website hosted on Heroku**
   - A link to your **source code on GitHub**
* A **brief presentation**, in the company of friends, illustrating:
    - Triumphs
    - Challenges
    - Words of Wisdom
    - And _3_ lines(!) of code you want to share with your classmates, copied into a separate document (probably your readme)

Each developer MUST present half of your presentation.

## TECHNICAL REQUIREMENTS

For this project, there are core technical requirements and flex technical requirements. You must complete all of the core technical requirements and 2 of the 5 flex technical requirements.

### Core Technical Requirements

**Your app should have all of the following:**
* **Express API** Build an Express server that has both HTML and JSON endpoints.
* **RESTful Routes** Design your CRUD routes using the [RESTful routing](http://restfulrouting.com/mappings/resources) convention.
* **AJAX** Leverage AJAX to make requests asynchronously.
* **jQuery** Use jQuery to add interactivity and display data on the client side.  
* **Templating** Render JSON data on the front end using handlebars templates.  
* **MongoDB** Persist at least two resources to a MongoDB database. One resource must have full CRUD.  
* **Visual Design** Make your front-end snazzy by adding custom styling. First impressions matter!
* **Code Style** Write professional-looking code. Use a consistent style. Consider following the [Airbnb Javascript Styleguide](https://github.com/airbnb/javascript/tree/master/es5).
* **Git** 50+ commits. Commit early, commit often. Each commit should touch only a few files. Each message should give a clear idea what you changed. (And don't expose any secret API keys/tokens on GitHub!)
* **Heroku** Deploy your app to Heroku.
* **Documentation** Write a README that would make an employer excited to hire you. See the [example readme](https://github.com/sf-wdi-31/readme-example) for a suggested structure. Your README should include:
   * A brief description or elevator pitch for your project
   * A link to project hosted on Heroku
   * Names of collaborators, with links to their GitHub profiles
   * User stories
   * Technologies used
   * Wireframe and site flow (optional)
   * An Entity Relationship Diagram (optional)
   * APIs used (optional)
   * Screenshots (optional)



### Flex Technical Requirements

**Your app should have 2 of the 5 following features:**
* **Data Validation** On the client side, don't let users submit blank forms -- and give them a visible error message explaining why they weren't allowed to submit.  In your database, use mongoose's validations for at least one attribute for each of your schemas (see <a href="http://mongoosejs.com/docs/validation.html">mongoose validation docs</a>). You can meet this requirement with just mongoose's built-in validations, but you could also take it further with custom validations.
* **External API** Use an external API to integrate rich data into your app.
* **Bootstrap** Use Twitter Bootstrap, Foundation, Skeleton, or another CSS framework throughout your site to create a unified baseline style.
* **Model Relationship** Create a one-to-many or many-to-many relationship between two models using either embedded or referenced data.
* **Sessions or Cookies** Research sessions or cookies and use them to track a visitor.  As a much larger challenge, you can use sessions to enable authentication (user sign up, log in, and log out). Note: This option requires significant independent research, and doing authentication correctly is difficult.


## PLANNING DELIVERABLES

Now that you know the full requirements for your app, carry out more detailed planning.

Prepare the following planning deliverables. (You may find it helpful to reference the [Software Development Best Practices workshop](https://github.com/sf-wdi-31/software-development-best-practices).) Meet with an instructor to have your plan approved.

Once your project has been approved, one member of your group should create a **GitHub Repo** for your project and [add your partner as a  collaborator](https://help.github.com/articles/adding-collaborators-to-a-personal-repository/).

We recommend also setting up a [Trello](https://trello.com) board to track your progress, communicate with each other, and keep focused on the most important goals.


1. **Minimal Scope**

  ![iterative-design](https://cloud.githubusercontent.com/assets/7833470/11330092/f76e7c50-9159-11e5-875f-748817e41afc.png)

  Software development is about managing complexity.  For this project, you probably won't have time to build the "spaceship" version of your project idea.  Figure out the absolutely simplest thing you can build that meets the project requirements, and start with *that* version of your app.  What can you reasonably accomplish in a week?  

2. **User Stories**

  Outline your core user stories. When you start to build, you'll divide these into clear, smaller steps (sometimes called "development stories").  Make sure you track development stories once you start implementing, not just the broader user stories.

3. **Wireframes and Site Flow**

  These don't have to be pretty; just sketch what UI elements the main pages will include and how the user will navigate from page to page.


4. **Database**

  List the schemas you'll need, and list the attributes for each.  Indicate any associations (relationships) you plan to have in your data.

5. **Feasibility Check**

  Research new tools or APIs. For an external API you're thinking of using, find out:
  * Does the API return JSON? XML?
  * Is all the information you want included in the response?
  * Will you need to make several different requests to the API?
  * Do you need to sign up and wait for approval to use the API?
  * Are there API keys you should keep hidden?

## BONUS IDEAS  
If you want to push yourself and learn something new, optionally consider doing some of the following with your app, but *please talk to an instructor* beforehand:

* **More Models or Relationships** Add another model to your project or create a new relationship.
* **Model Methods** Level up your models by adding a method to one of your schemas.  For example, a person schema with `firstName` and `lastName` can have a `fullName` method (see mongoose docs on [instance methods](http://mongoosejs.com/docs/guide.html#methods) and [static methods](http://mongoosejs.com/docs/guide.html#statics)).
* **Sass** Use a CSS pre-compiler to write more imperative CSS.

## TIMELINE

> DO NOT START CODING UNTIL YOU HAVE GONE OVER YOUR PROJECT PLAN WITH AN INSTRUCTOR.

* **Wednesday, September 7th by 3:00pm** - Present your app plan to an instructor to go over your [planning deliverables](./planning.md).
* **Weekdays, September 8th-12th** - Technical interview prep at 9:00AM. Project work time for the rest of the day. Daily check-ins with your team's instructor.
* **Tuesday, September 13th @ 1:15pm** - Project due and presentations!

In addition, we suggest you have a feature freeze sometime on Monday, September 12th - meaning no new features! After a feature freeze, you can focus on re-deploying your code to Heroku, polishing existing features, writing your README.md, and planning your presentation.

## FEEDBACK

**Your project will be evaluated based on the following criteria:**

* **Technical Requirements**: Did you deliver a project that met all the technical requirements?

* **Creativity**: Did you add a personal spin or creative element to your project? Did you deliver something of value to the end user?

* **Code Quality**: Did you follow code style guidance and best practices covered in class, such as spacing, modularity, and semantic naming? Did you comment your code?

* **Problem Solving**: Are you able to defend why you implemented your solution in a certain way? Can you demonstrate that you thought through alternative implementations?

Each of the criteria above will be evaluated as one of **incomplete**, **does not meet expectations**, **meets expectations**, or **exceeds expectations**. You'll be receiving written feedback from your instructors.


###HAPPY CODING :)
