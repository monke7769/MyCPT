---
toc: true
comments: false
layout: post
title: CPT Project Plan
description: Basic Outlines and ideas for our upcoming CPT project.
type: plans
courses: { compsci: {week: 0} }
---

## Overview
Our project idea came from last trimester's joke button page. We found many button CSS designs and modified them to create our own. As a result, we thought that a great idea for our CPT project would be to create a website where users can save and edit designs, with the aim being an online button editor that simplifies complicated parts of CSS such as animations and box shadows. Our website would also have a like/dislike system that collects user data and displays the best designs for users to see. Users would have the option of making designs public and private and sharing designs with others.

## Purpose
In the domain of web design, where the pursuit of aesthetically pleasing layouts intersects with the nuanced
orchestration of cascading style sheets (CSS), the endeavor to efficiently unearth and implement creative
concepts can often resemble a traversal through a convoluted labyrinth. Recognizing the inherent value of
time, our primary objective is to furnish a guiding beacon—a streamlined pathway, if you will—to effortlessly
unveil designs and master the intricacies of CSS, all without the exhaustive investment of protracted periods.
Envision this as a digital compass, directing you towards a seamless fusion of creativity and code, thereby
rendering the process an engaging exploration rather than an arduous enigma.

# Frontend
## Page Designs

Initial Design
![John's Image](../../../images/initial.png)

Canva: 
![canva](../../../images/canva.png)

Main Page
![main](../../../images/mainpage.png)


## HTML + CSS Editor

Our design consists of an HTML and CSS editor in the page. This seems somewhat redundant, since someone can create their design on a local file and upload, however this funtion comes with several benefits.
- Users who don't want to create a new project file can quickly test lines in a pinch
- HTML and CSS editors allow people to visualize code written by helper tools such as animation or box shadow
- When viewing other designs and wishing to implement code, allows for easy reference and copying

> Security
 A potential issue with an HTML editor is that an attacker can easily use the HTML editor to gain access to data stored on our website. While we trust the other people at our school, and are not concerned with people viewing so called private designs while our website is in the testing phase, it is important to ensure that somebody cannot inject code to access private data or destroy our website. This issues arises as if HTML code that is inputted is displayed on our website, anybody essentially has full control over our website. 
 Potential fixes:
 - Find a workaround that doesn't require HTML. This would be difficult but ideal
 - Somehow encapsulate the provided HTML in a separate container that prevents it from having access to the rest of the code and only displays within itself. This might still have loopholes, and requires lots of research, but is what we strive for.
 - other solution: ban javascript, but removes functionality
 ![diagram](../../../images/yes.png)

### Private versus Public designs

Our website will allow users to make public designs for sharing, and private designs as references for themselves later. A diagram of how the database will handle this is show below.
![diagam](../../../images/maybe.png)

#### Animation

- The plan for animations is that the user will be able to select an element, then select the path that the element will travel in the page
- There will also be numerous types of animations to manipulate elements, akin to google slide element animations
- There will also be "mix-and-matchable" buttons and animations -> allows for the use of certain button designs and a different animation

![Image](../../../images/animationDiagram.png)

#### Box Shadow

- Box shadow is pretty complicated, as a result, we plan to use a menu and presets to simplify the process
- Generally, box shadow is a string of 20 numbers or so. This is overly complex so what we plan on doing is having a scrolling menu that indicates each number with its purpose for easier modification

![Image](../../../images/boxShadow.png)

## Finding Designs

- we will tag will the designs with certain words/hashtags in smaller font at the top of each page and create a search function (more specifics will be researched later)

The display page for one design as shown below:

![elprimo](../../../images/ElPrimoDesign.png)

The search page listing will look like this:

![search](../../../images/SearchFunction.png)

## Like and Dislike designs

- CSS button to upvote/downvote designs +/- 1 vote
- score for a single design will be stored in the backend database

#### Others

- Other plans will be placed here as we come up with them


# Backend

## User Accounts, Database

- we will have a mySQL database for the website to hold different user accounts they can log in with
- account login will include username and password
- each account will have certain stored properties in the database such as different profile settings
- include profile picture, DOB, interests, other info that the users can themselves customize

## Database of Designs
- We are going to create a Mysqlite database that will store all the designs and with this we can allow users to acsess public designs that they might want to use for their website
- With the database of designs we can again expand making an AI that will create your custom button based on a wireframe
- We can help people spread their desired designs
- The data that will be stored includes data the design is made, author, likes and dislikes, the actual design code in css and html, ratings, and possibly more

## Public vs. Private design fetch
- We will have the features of public and private designss
- For public designs we will fetch all the buttons from the databse of designs that are public and allow users to use them on their site
- For private designs this will be only be accessible to the author and if other users try to fetch it, it will not work

## Fetching reviews
- We will have a review system on public designs so people can give their valued opinion on each design
- With the review system people can improve their buttons or change it if they wish
- The review system will fetch reviews from a database that will contain date the review was made, the author, likes and dislikes, and more

![Image](../../../images/IdeationAImageDiagramBackend.png)
