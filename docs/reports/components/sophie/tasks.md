#### UI Design & Preemptive Troubleshooting

First, I’d like to give a brief overview of the few obstacles that I encountered and how I dealt with them. Additionally I have laid out any issues I imagine could arise later on in the project and how I may approach solving them.

1. Obstacle: Learning React Native 
    1.  The first part of this project before I began designing the UI was to look at React Native as in-depth as possible to judge what was feasible given our time frame. After going through documentation and tutorials, with React Native’s abilities and structure in mind, I was able to better plan out the interface and navigation for our application.
2.  Obstacle: Setting Up Work Environment 
    1. I actually had a ridiculously hard time installing and setting up expo to be able to compile and demo our code on an iOS device. I could not use homebrew and ended up going through yarn instead. As things are currently, npm start will run normally and open expo if run in Visual Studio Code, but otherwise it will not.
3.  Obstacle: Accomodating for Truck-Manager View and Customer View  
    1.  We realized that we had overlooked whether or not we would treat the Truck-manager as a user account with different privileges and pages, or have a seperate app just for them. We decided to treat truck-manager accounts as a type of users. When a person creates their account or   
4.  Potential Issue: Canceling a previously placed order   
    1.  We will account for this by adding a feature If a user 

My approach to the project so far has been to balance visual, aesthetic with an accessible, straightforward design while maintaining a sense of the organization of our data and what is feasible to present to users. The line between flashy features and clutter is a delicate one, but by keeping to a refined list of functionalities our app should fulfill I think things turned out very well.

#### Initial Design and Model

I did several installments of sketches. The first few were of the main (landing) page and several other pages that showcased main functions of the application. I used this as a way to get the team talking about a variety of topics:

- Which features were reasonable and which needed to be trashed or maybe saved for later to implement if we had enough time
- What kind of layout was appropriate for our application
- “Where” (how) we should allow pages to be accessed, and how (swiping a certain direction, tapping an area versus a specific icon...etc)

These discussions often branched off into other important areas and helped us foresee and tackle issues before they arose in the implementation stage, ultimately saving us a lot of time. 

The following are  few images of the hand-drawn UIs for our application, including the loading screen, login screen, and display for creating an account. Following are the landing page, from which the user can view the surrounding trucks, search for trucks by name or cuisine type, then see profiles, add menu items to their cart and place orders.

![ui1](../../images/sophie/ui1.jpg)
![ui2](../../images/sophie/ui2.jpg)
![ui3](../../images/sophie/ui3.jpg)

#### Feature Design & Adjustments
 
- We are hoping to have a stationary, constant navigation menu on the bottom of the screen that will allow access to the three main pages of our app, and a fourth icon to open a drawer that will show less frequented pages like a user’s profile, settings, and a logout option.

- I also did a use case design as part of the planning process which can be found [here](#use-case).
