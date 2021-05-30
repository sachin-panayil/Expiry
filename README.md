Original App Design Project - README Template
===

# Expiry

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
Our app, Expiry, will allow users to track the expiration date of their food items. The user can manually enter food items or possibly, through a QR Code Scanner, can enter it that way. It would then ask for the expiration date and log it. Custom reminders can be set days prior to the expiration date. This app will help people be less wasteful.

### App Evaluation
- **Category:** Utilities / Productivity
- **Mobile:** Entering food expiration dates on the computer is a hassle when compared to entering it on your smart phone where the food can be right next to you while entering it. Our app produces a mobile first experience and makes use of the camera and convenience of a smartphone. 
- **Story:** Over 80 billion pounds of food is thrown away in the US alone which causes food to be the largest component taking up space in US landfills. This app provides people with the opportunity be less wasteful of their food products.
- **Market:** Anyone that wants to alleviate less waste and be more mindful of the environment would love this app. More people are turning to eco-friendly ideas and this is one that can stand out amongst all of them. We believe that the size and scale of this app is huge. 
- **Habit:** A user can use this app multiple times throughout the day. Whether it be to add more food items or to check on previously added ones. This can be very habit forming as whenever a user gets a food item, an instinct can be made to enter it into the app.
- **Scope:** This app should not be too technically challenging. A lot of it follows the frameworks of the apps we have previously built. This app will be interesting to build regardless of what version it is. We feel as if this product is extremely defined. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User logs into their account to access their food lists and preference settings - ( Finished )
* User can view the foods they have listen and click into it to get more specific details - ( Finished )
* User can view the foods that are going to expire soon (time depends on user preference) - ( Started )
* Profile pages for each user that can track various things - ( Finished )
* Settings for notifications, general, etc - ( Half Way Completed )

**Optional Nice-to-have Stories**

* Points system that increases every time the user is non wasteful
* User can connect with friends to see who has more points
* Can connect user with local food donation centers

### 2. Screen Archetypes

* Login Screen - User can login to their account
   * User logs into their account to access their food lists and preference settings
   * User is asked for username and password
* Register Screen – User can sign up for an account
   * User is not required to re-login every time app is closed. 
   * Asks for username, email, and password 
* Food Screen
   * User can view the foods they have listen and click into it to get more specific details
   * User can view the food in a 4x4 view
   * Expiration date and name of item are both viewable
* Detailed Food Screen
   * User can click into an item in the food screen
   * Expiration date and other information can be viewed here
* Calendar Screen
   * User can view the foods that are going to expire soon (time depends on user preference)
* Settings Screen
   * User can change notification settings, time for calendar, etc
* Profile Screen
   * User can upload a profile picture and view their profile information

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Settings
* Profile
* Calendar
* Food List

Optional:
* Friends


**Flow Navigation** (Screen to Screen)

* Profile -> Profile screen where profile picture can be uploaded
* Settings -> Settings screen where settings can be toggled
* Log-in -> If log-in is incorrect, log-in screen will be brought to user / if correct, food screen appears
* Register -> Register screen where if registration is successful, login screen is shown
* Calendar -> Calendar screen
* Food Screen -> When food item is tapped, detailed food screen is shown

## Wireframes
<img src="wireframe.jpeg" width=600>

## Schema 

### Models

#### User

| Property | Type | Description |
| :----------- | :-----------: | -----------: |
| UserId   | string | unique id for user |
| FirstName | string | the user's first name |
| LastName | string | the user's last name |
| UserName | string | the user's username |
| EmailAddress | string | the user's email address |
| Password | string | the user's password |

#### Post

| Property | Type | Description |
| :----------- | :-----------: | -----------: |
| ObjectId | string | unique id for post |
| author | Pointer to User | UserId |
| foodItem | string | the food uploaded by user manually |
| CreatedAt | DateTime | date when post is created  |
| UpdatedAt | DateTime | date when post is last updated  |
| ExpirationDate | DateTime | date when foodItem expires |


### Networking
* Login Screen
   * (Login/POST) Login information
* Register Screen  User can sign up for an account
   * (POST/Create)  New user information 
* Food Screen
   * (Read/GET) Query all food items where user is author
* Detailed Food Screen
   * (Read/GET) Dates of expiration
   * (Create/POST) New dates of expiration
   * (Delete) Existing expiration
* Calendar Screen
   * (Read/GET) Dates of expiration
* Settings Screen
   * (Read/GET) Existing notification and calendar settings
   * (Update/PUT) New calendar settings
* Profile Screen
   * (Update/PUT) Update profile image
   * (Read/GET) Query logged in user info


### GIF

![Part 4](https://github.com/The-deciders/Expiry-Sprint-4/blob/sprint/Part%204.gif)

### Walkthrough Link

https://drive.google.com/file/d/147RPcvtBfU_ApN4hMbFRbCfVxwzqZHb_/view?usp=sharing

