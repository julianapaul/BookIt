# BookIt

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
A restaurant reservation app that will let the users book a table at their favorite restaurant.

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:** Social Networking
- **Mobile:** This app would be primarily developed for mobile. Functionality wouldn’t be limited to mobile devices, however mobile version could potentially have more features.
- **Story:** Analyzes users restaurant choices, and begins to show them similar choices. The user can book a table at the restaurant of their choice.
- **Market:** This app would available to any individual.
- **Habit:** This app coould be used as often as the user wanted depending on how much they would like to eat out.
- **Scope:** First we would start with promoting similar resturants based on cusine taste. Large potential for use with Doordash, GrubHub, or streaming applications.

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can search the restaurant of the their choice.
* User can book a table and confirm the reservation.
* User can see the resturants availability.
* User can see the number of seats available at a table.

**Optional Nice-to-have Stories**

* User can see the entire floor map of each restauant.
* User can see information about the restuarant.
* Log of past reservations.
* Profile Add-On: Top restaurant choices, etc.

### 2. Screen Archetypes

* Search Screen
   * Allows user to search up the resturant they to eat at
* Resturant Layout
   * Allows the user to see the layout of the resturant of their choice
* Booking Screen
   * Upon selecting a table within the restaurant layout useers select the amount of guests, reservation date, and preffered time.
   
### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Search
* Resturant Layout
* Booking

**Flow Navigation** (Screen to Screen)

* Search Screen -> Text field to be modified
* Restaurant selection -> Restaurant layout
* Table Selection -> Booking sreen

## Wireframes
<img src="BookIt Wireframes.JPG" width=600>

### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 
### Models
#### User

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | String   | unique id for each user |
   | username      | String   | unique name used for authentication |
   | password      | String   | password used in combination with username for authentication |
   
#### Restaurant Name

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | String   | unique Id for each restaurant |
   | restaurantName| String   | Field stating the name of each restaurant |
   | location      | String   | location of each restaurant |
   
#### Transactions

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | String   | unique ID used to identify each record of a transaction |
   | userBooked    | Pointer to User | points to the user object who booked the table |
   | numOfOccupants| Number   | number of people who will be in attendance |
   | tableType     | Number   | the type of table selected |
   | dateTime      | Date     | the time that the user booked the table for |
   
### Networking
- Restaurant Search Screen
  - (Read/GET) Query all searched or similarly searched restaurants
    ``` Java
    
    ```
- [OPTIONAL: List endpoints if using existing API such as Yelp]
