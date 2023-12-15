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
ryan
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
## Like and Dislike designs
hayden

# Backend
## User Accounts, Database
hayden
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