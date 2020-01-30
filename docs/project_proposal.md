# Project Proposal

## Overview

Food trucks often have applications that customers can download to see their schedule, menu and even place online orders for pick-up. There is a need for a quality mobile application that makes finding new food trucks easier. We plan to fix this problem by creating an app that encapsulates the whole process. The customer will use the app to find food trucks, decide what kind of food they would like and order it. The truck manager will then be able to see this activity from the app, and then begin preparing the food that the customer ordered.

## Goals

1. Provide customers a service that helps them easily find a satisfactory food truck.
2. Provide business owners with a way to help inform customers of their food trucks.
3. Create an all in one app for food truck businesses.

## Features

We have discussed and drafted the following list of features we plan to implement for our application:

- Ability to sign on using third party services or the platform&#39;s built in authentication
- Transactions handled inside app or leveraging built in payment methods such as Google pay or Apple pay
- Food truck owners can manage their menu and accept orders through the app
- Customers can place orders through the app
- Find nearby food trucks on a map based on distance or any other metric
- Various search criteria to filter based on taste or dietary preferences
- Ability to verify that a user owns a food truck

!!! warning
    These are the main features that planned to be completed by the end of the semester. More features may be added if time permitting.

## Timeline

| Objective   | Date  |
|---|---|
|Requirements Specification and Deliverables   |**==Jan 31==**   |
|User Interface Design Completed   |**==Feb 3==**   |
|Architecture Designs Completed   |**==Feb 17==**   |
|Implementation Completed   |**==Mar 23==**   |
|Testing Completed   |**==Apr 16==**   |


## Specifications

Our project will be composed of a couple development environments responsible for displaying information to the end user, and another for managing data given by users and food truck owners, processing payments, and delivering information to the clients and food truck owners. The back-end will be implemented with the ==Spring-Boot java framework== to handle information, queries, and payments. The front-end will be implemented with ==React-Native== to provide portability and cross-compatibility for the user-interface providing a simple platform for food-truck owners to list their products and location, accept payments, etc. and for end-users to locate food trucks in a map-style view, peruse menus, query for different genres of food-trucks, and possibly make purchases.