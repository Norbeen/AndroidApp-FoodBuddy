Original App Design Project - README Template
===

## Table of Contents

## Authors		
Élisée D. <=> Nabin B.

## Overview

This food recipe app will let users find varieties of food recipes, user can click on the food they would like, and they can view a video or get details on that food.

### Description
[Recipe finder app]
We created this app with an intention of giving power to the end user to pick and choose from varieties of ingrediets and cuisine. Trending section is where a user can see 28 different recipe, search section is where a user can see hundreds of recipes based on the most rated ingredients for food, and we have a joke section, you can enjoy while your food is cooking. Login and signup made possible using firebase and API fetched via Spoonacular api. 


### App Evaluation
[Evaluation of your app across the following attributes]
- **Category: Food and Drinks (Google Play store)**
- **Mobile: It will be convinient for a user to just look up various food without knowing what to look for**
- **Story: A user can get a great recipe idea they never knew and then try it**
- **Market: Any person who don't know how to make a food can enjoy our recipe app**
- **Habit: Maybe once a week when people want to try something on their own while feeling bored**
- **Scope:We will begin by implementing minor things and gradually add features over time**

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* [x] User can register for an account
* [x] User can see food buddy(app) logo
* [x] User can login
* [x] User can see three navigation buttons
* [x] Each navigation button contains search bar, random food recipe and profile
* [x] User can logout
* [x] User can click recipe for detail
* [x] User can see varieties of recipies
* [x] User can see random food recipes
* [x] User can see the title, image and description of items
* [x] User can automatically see random recipes
* [x] User can click on the recipes to see detail screen
* [x] User can see a detail page on the recipe
* [x] User can see random jokes
* [x] User can see the recipe for the item in detailed view

**Optional Nice-to-have Stories**

* [User can add their own recipes] 
* [User can upload thier vides on how to make recipes]
* [User can like and share other peoples recipe]
* [User can search for a recipe]
* [User can click search button]
* [User can type in food name]
* [User can save their favorite recipe]


## Video Walkthrough

Here's a walkthrough of implemented user stories:

* Gif 

<img src='https://github.com/https-github-com-elisee10/FoodBuddy/blob/main/sprint4.gif' title='Video Walkthrough' width='' alt='sprint 4' />




### 2. Screen Archetypes

* Registration Screen
    * User signs register for an account
    * User can see food buddy(app) logo
    
* Login Screen
    * User can login
    * User can see food-buddy logo
    * User can click on register button
    
* Home Screen
    * User can search for a recipe
    * User can click search button
    * User can click recipe for detail
    * User can see varieties of recipies
    * User can see random food recipes
    * User can see three navigation buttons
    * Each navigation button contains search bar, random food recipe and profile

* Search Screen
    * User can see a search bar at the top
    * User can type in food name
    * User can click search button
    * User can see varities of recipe 
    * User can see the title, image and description of items
    * User can click the items to see a detailed view

* Trending Screen
    * User can automatically see random recipes
    * User can click on the recipes
    * User can see a detail page on the recipe

* Profile Screen
    * User can see their own profile
    * User can save their favorite recipe
    
* Detail Screen
    * User can click an item to see the details
    * User can see the title, image and description of the items
    * User can see the recipe for the item 
    
### 3. Navigation

**Tab Navigation** (Tab to Screen)
* Search for food
* Logout


**Flow Navigation** (Screen to Screen)

* Login Screen
     => Home
* Registration Screen
    => Home
* Search Screen
    => List of food items 
* Trending Screen
    => List of food items
* Profile Screen
    => List of saved items
* Detail Screen
    => Detailed view of items

## Wireframes

![wireframe](https://github.com/Norbeen/source/blob/main/Screen%20Shot%202020-11-09%20at%206.54.24%20PM.png?raw=true "wireframe")


![wireframe](https://github.com/Norbeen/source/blob/main/Screen%20Shot%202020-11-09%20at%206.54.36%20PM.png?raw=true "wireframe")

![wireframe](https://github.com/Norbeen/source/blob/main/Screen%20Shot%202020-11-09%20at%206.54.42%20PM.png?raw=true "wireframe")


### Models

  | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | Username     | String   |  Text to store the name of the user |
   | title | String| title of the recipe |
   | image         | String    | image of selected recipe|
   |description    | String    | description of recipe|
   
### Networking

* Search Screen (create/GET) 
    * (GET) the recipe image, title and description of searched item
    * (GET) the how to make description of searched food item
    * (POST) the title, image and detailed description of how to make recipe

* Trending Screen (create/GET)
    * (GET) the title, image and description of the recipe randomly
    * (GET) the how to make description of random recipe displayed
    * (POST) the title, image and detailed description of how to make recipe
     
* Profile Screen(create/GET )
    * (GET) the title, image and description of saved items


* Saving the title, image and description 
   

    * private void savePost(String title, String image, ParseUser currentUser, String ingredient, String description) {
    * Post post = new Post();
    * post.setUser(currentUser);
    * post.setTitle(title);
    * post.setDescription(description);
    * post.setImage(image);
    * post.setIngredient(ingredient);
    * post.saveInBackground(new SaveCallback() {
                

