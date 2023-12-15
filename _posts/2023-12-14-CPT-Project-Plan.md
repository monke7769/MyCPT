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

ian

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

ryan

## HTML + CSS Editor

ian

### Private versus Public designs

ian

### CSS Helpers - Display

(i.e. padding)
ian

#### Animation

srijan

#### Transition

srijan

#### Box Shadow

srijan

#### Others

srijan

## Finding Designs

hayden

- we will tag will the designs with certain words/hashtags and create a search function (more specifics will be researched later)

## Like and Dislike designs

hayden

- CSS button to upvote/downvote designs +/- 1 vote
- score for a single design will be stored in the backend database

# Backend

## User Accounts, Database

hayden

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


























