# MS3---Grubs' Up!
Third Milestone Project for Code Institute

 ![](assets/images/devices.PNG)

I wanted to design a website for users to be able to share their own recipes and view recipes from other users. I used MongoDB 
for the database and I used Flask to facilitate building the bulk of the website with templates.

[The live project can be viewed here.](https://jgibson90.github.io/MS3/)

---
# Contents
- [UX](#ux)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Testing](#testing)
- [Bugs](#bugs)
- [Deployment](#deployment)
- [Credits](#credits)
- [Special Thanks](#special-thanks)
---

# UX
## User Stories
- User goals 
    - As a user, I want to immediately understand what is offered by the website
    - As a user, I want to be able to seamlessly navigate through the site to easily find
     more information
    - As a user, I want to be able to easily interact with the site and the applications within
    - As a user, I want to be able to view all the recipes that are uploaded
    - As a user, I want to be able to sign up so that I can upload my own recipes
    - As a user, I want to be able to edit/update/delete my own recipes

    I made the wireframe using Balsamiq which you can view the wireframe [here.](assets/images/Wireframe.png)

## Design Choices
---
When designing this website I looked at existing recipe sites such as [this one for Hello Fresh](https://www.hellofresh.co.uk) 
for inspiration. I opted for a multi page website with certain pages only being accessible if a registered user is logged in.

## Fonts
I chose [Hepta Slab](https://fonts.google.com/specimen/Hepta+Slab) for my logo for something eye catching and unique. 
I chose [Catamaran](https://fonts.google.com/specimen/Catamaran) for my headings as I wanted something that
would immediately stand out and be noticeable. I chose 
[Roboto](https://fonts.google.com/specimen/Poppins?preview.text_type=custom#standard-styles)
for my main font for its' excellent readability and clean look.

## Icons
I used [Font Awesome](https://fontawesome.com/) for my form icons as well as my button icons and the social media links in the footer.

## Colours
I used the built in CSS colour styling in Materialize to choose my colour scheme and apply it to all necessary HTML element classes. 

![](assets/images/colours.png)

# Features
- Responsive on all device sizes
- Ability to sign up and become a registered user
- CRUD Functionality
- MongoDB database linked to the website
- Hashed passwords for user security
- Admin privileges to edit/delete any recipes 
- Social media links

## Future Features
Due to time constraints I was unable to implement these features but will include them in the future
- Modal popup to confirm recipe deletion 
- Ability to see if a recipe is vegetarian or vegan

# Technologies used
## Languages used
- [HTML5](https://en.wikipedia.org/wiki/HTML)
- [CSS3](https://en.wikipedia.org/wiki/CSS)
- [Python](https://www.python.org/)

## Tools, Frameworks and Libraries used
- [Git](https://git-scm.com/) 
    - Git was used for version control, using the Terminal to commit and push to GitHub.
- [Font Awesome](https://fontawesome.com/)
    - Font Awesome was used to add icons to the footer for better UX amd aesthetics.
- [Materialize](https://materializecss.com/)
    - Materialize was used to aid with prebuilt classes and the responsiveness of the website across multiple devices.
- [JQuery](https://jquery.com/)
    - JQuery was used in conjunction with the respective Materialize elements for responsiveness
- [Flask](https://flask.palletsprojects.com/en/2.0.x/)
    - Flask was used to easily create a multi page website through the use of templates 
- [MongoDB](https://www.mongodb.com/)
    - MongoDB was used to create a database to store a collection of users and recipes
- [Google Fonts](https://fonts.google.com/)
    - Google Fonts were used to import the Hepta Slab, Catamaran and Roboto fonts into the style.css file for the main logo, headings and the main body respectively.
- [Balsamiq](https://balsamiq.com/) 
    - Balsamiq was used to create the wireframes for the project.

# Testing
I used the [CSS Validator](https://jigsaw.w3.org/css-validator/) which brought up two errors which can be seen [here](assets/images/CSSTest.PNG). I also 
used the [HTML Validator](https://validator.w3.org/) which brought up these three warnings which can be seen [here.](assets/images/HTMLTest.PNG)
### Fixes
- I simply removed the comma in the middle of the two `margin:0, auto` declarations in the `.btn` and `#form-button` sections of my style.css.
- Given that the Map is a section in it's own right I don't feel the need to add a heading as I think it will detract from the flow of the page.
- With regards to the two warnings about the type attribute being unnecessary for JavaScript resources, I removed the `type` attribute and it caused the code to fail so I have left them in place.

## JSHint Testing
I ran my JavaScript through [JSHint](https://jshint.com/) and it displayed these warnings for my [maps.js file.](assets/images/JSHint1.PNG)
    - After reviewing these I added the missing semicolons in the maps.js file.

I also ran my sendEmail.js file through JSHint and it returned no warnings or errors which can be seen [here.](assets/images/JSHint2.PNG)

## Testing User Stories from UX 
1. As a user, I want to immediately understand what is offered by the website

    1. Upon entering the website, the user is greeted with a navbar with three dropdown options to go to anywhere on the page 
    2. The user has two options, to either select a link from the navbar or to scroll down, both of which lead to the same location

2. As a user, I want to be able to seamlessly navigate through the site to easily find more information

    1. The site has been designed to be fluid being made up of a single scrolling page. At the top of the page is a fixed navbar so the user can always find their way around the website

3. As a user, I want to be able to easily interact with the site and the applications within

    1. The Google Maps API has 3 seperate dropdown menus to choose from. Each one contains a different set of locations with corresponing markers and info windows which appear on the map with a Drop animation when they are selected
    2. The sign up form has EmailJS integration and will notify the user if the inputs are not entered correctly. Upon successfully submitting the form, an auto reply is sent to the user confirming that they have signed up to the newsletter successfully.


## Further Testing 
- The project was tested on Google Chrome, Mozilla Firefox, Safari for iOS and Microsoft Edge.
- The project was viewed on a variety of different devices such as Desktop, Laptop, iPhone 7, iPhone 8, iPhone 11, and iPad.
- I asked friends and family to view the project and give feedback on any user experience issues and/or bugs. 

## EmailJS Testing
- Firstly I set up my two templates for my emails, one being the auto reply to the user and the other being the one sent to the London Life email which can be seen [here](assets/images/EmailJSTemplate2.PNG) and [here](assets/images/EmailJSTemplate1.PNG) respectively.
- Then I filled in the form with my details and checked to see if I recieved both the auto reply and the confirmation that there was a new sign up to the newsletter. Proof of which can be seen [here](assets/images/EmailJSTest-3.PNG), [here](assets/images/EmailJSTest-4.PNG) and [here.](assets/images/EmailJSTest-5.PNG)

# Bugs
Following on from Testing I also encoutered these bugs.
## During development
- Signup form refused to center despite Bootstrap grid and CSS styling
    - Shift + f5 to clear the cache 
- Google Maps markers and info windows not appearing in the map
    - Tutor Support, my mentor and Stack Overflow helped me decipher where I was going wrong
- On iPhone the phone input on the form could not be entered correctly due to the pattern I had specified
    - I removed the hyphens from the pattern to fix the issue


# Deployment

**London Life** was developed on Gitpod, using GitHub to host the repository.
These were the steps taken to successfully deploy the website.
- Open [**GitHub**](https://github.com/) and log in
- Select the **repository**
- Click the **Settings** button from the top menu
- Scroll down to the **GitHub pages** section
- Click the **Source** dropdown menu and select **Main Branch**
- After the page has refreshed the link to the website can now be found 
under the **GitHub pages** section

## Cloning the Website
- Open [**GitHub**](https://github.com/) and log in
- Select the **repository**
- Click the **Code** drop down button next to the green GitPod one
- Select **"Clone with HTTPS"** and copy the link
- Open your **IDE** and the **Terminal**
- Specify a new **path directory** where you want to put the clone
- Type `git clone` and then **paste** the previously copied url from before

# Credits

## Code
- I used [Bootstrap 4](https://getbootstrap.com/) to make the site
responsive on different devices.

- I used the EmailJS tutorial from Code Institutes course to help write my EmailJS function.

- I was provided the fix to add infoWindows to my Markers on Stack Overflow, you can view it [here.](https://stackoverflow.com/questions/66689094/how-can-i-add-info-windows-to-a-marker-event-listener)
 
## Images
- The hero background image came from
[Pexels.](https://www.pexels.com/photo/sunset-river-london-thames-34632/)

## Websites

- I used [ResizeImage](https://resizeimage.net/) to help get the hero image
to display properly.

# Special Thanks
Special thanks to the Slack community, Stack Overflow, Tutor Support and my Mentor for all their advice and guidance on this project.
