# Legacy Code Is "The Best"

![](https://s-media-cache-ak0.pinimg.com/236x/c7/b5/e1/c7b5e1827478b8f703a74371e6f2b214.jpg)

## The Task

You are currently interviewing for a new development team, and they are planning on releasing their new product in 3 months.  There's only one problem: their lead dev, Trevor, just left to travel around Southeast Asia and "find himself" and has been unreachable for weeks.  We have no idea when he will be back.

Fortunately, one of your consultants was closely involved in the coding earlier.  He will introduce the code base and the problems he would like you to solve.  Since this would be your job for the next 3 months, he wants to make sure you can solve these problems.  If you do well on these problems, you may find yourself with a job offer.

Solve as many of these problems as you can in whatever order you feel comfortable with.  Just like in any interview process, you should feel free to ask the consultants any questions you have, but they reserve the right to not answer them or answer them as cryptically as an interviewer would.

This exercise is competitive.  We will announce winners, so we recommend not asking your fellow devs for help.  However, Professor Google and Captain Stackoverflow's doors are always open, and you are encouraged to use any and all notes from them or from your former projects.

## The Code

Below is a basic rundown of the files in the app, and what they do.  This is mostly exhaustive of the code you will have to touch in this coding challenge, but perhaps not completely.  For any questions on file organization, please ask your consultants.  For any questions on what a line of code in a file is doing, follow the Read-Search-Ask pattern.

1. Basically all code you need is in `ionic/senseus/www/`
2. `index.html` includes all the outside resources and kicks off the show
3. All default Ionic/Angular CSS is in `www/css`
4. All custom CSS for this app is in `www/static/css`
4. Images are located in both `www/img` and `www/static/images`
5. Most external tools are located in `www/libs`
6. All the actual HTML on screens are located in `www/templates` with a name similar to that of the title of the screen in the browser
7. All front-end functionality for this app is in `www/static/js`
8. Most of the Angular functionality for this app is in `www/static/js/controllers.js`

## The Problems

### There Is No "I" in UI...ummm, Nevermind

1. The text is incredibly small on the Event Details screen.  Please make it bigger.  Bonus points if you can make it even bigger for mobile.
2. The rows on the Event Review page are pretty squished.  Make them a consistent height, and separate them with a better border or margin.
2. Why is there a random modal on the Event Details screen?  We should probably get rid of that.
3. There is a similar problem on the Event Guests screen.
3. The Event Times screen on Mobile looks like a lion ate a zebra and threw it back up.  Please untangle this mess.
4. There are a bunch of buttons 

### The Code We Deserve, but Not the Code We Need

There are a bunch of features the product has decided to abandon, but we still have the code for them.  Make sure you clean them out entirely if you start work on them, but be careful not to break other features.  Please get rid of these relics:

1. The "Find an Event" button on the landing page, and the modal it pops up.
2. The "Enable location sharing?" toggle button.
3. We have two dot-progress bars at the bottom of the screen.  Probably only need one of those.  Pick the one that makes sense to you.
4. The "Event Type" section on the "Event Details" screen.

### Squashing Bugs

Some things are just not working right.  See if you can make these things work.

1. There is no map on our "Event Location" screen.  There should be.
2. The text input on "Event Location" does not autoComplete with the Google Places API.  It should.

### All the Features!

1. There is no way to get back to other screens (like Event Location and Event Invite) from the Event Review page.  Add some buttons to each of our summary rows that redirects to the respective screen on our ui-router.
2. It is OK that "Create Event" does not currently save to the Database, but we need to test that all the information *can* be saved.  Rewire the "Create Event" button so it displays all the eventInfo in an alert dialog.  Bonus points if you can wire it up with a modal.

### A Note on Refactoring

This company cares a lot about sustainable code.  So if you see a place to make things more scalable, or cleaner, please improve the code.  However, remember two things:

1. **Separate** refactoring commits from commits for feature implementation, bug squashing etc.  You should *only refactor* in the commit, not change functionality.
2. Before you commit, test that the feature you're touching still works as expected.

## Set Up

To get this project started, you will need to do a few things first.

1. Fork and clone this repo
2. Install Ionic globally with `npm`
3. In the `legacy-code` directory, navigate to `ionic/senseus` and start your web server.
  4. Check this [documentation](http://ionicframework.com/docs/guide/testing.html) for advice on this.
5. If this does not open a version of the app, please ask a consultant for help.
6. Navigate around the landing page, and the "Create an Event" workflow.  All of the problems to solve will be in those places.

## General Advice

1. Open up Dev Tools, and don't close it ever.
2. Check the Terminal for any errors with your web server.
3. Commit early, and commit often.  You can always revert a small change, but a big change could be very messy.
