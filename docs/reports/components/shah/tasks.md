#### Creating the app and organization

I began working on the app, taking Sophie’s UI design and putting it into effect. In the progress of building the UI diagrams I worked on the apps structure.

1. Tools
      1. s
      2. As stated before we are using **React-Native** in combination of Expo as it allows us to build for both iOS/Android with a single code base. Additionally Expo helps with some inconsistencies between both platforms such as fonts and icons as well as providing a system to show live development builds and build the production app.
      3. The first notable main package that we are using is called **react-navigation** which provides for the overall navigation of our app. It provides for the animation on page transition as well as navigation with back buttons across both platforms since they have different methods of navigation (buttons vs swiping on iOS)
      4. The next notable library is **react-native-paper** as it will provide for the visual aesthetics. It is a material design library so the design principles are that of Google’s Material Design specification .
2. App file structure
      1. Currently the file structure is as follows
         1. The  main area to look at is src as it contains the code
         2. Components would contain standalone items such as a colored button or the mean appBar
         3. Constants contain global constants such as page names, or ports for api calls
         4. Context contains a list of variables that change page to page, for example the changeTheme function changes depending on what page its on (in this case its either defined or not, context provides a default value incase its not defined)
         5. Navigation is the react-navigation parts that setup the drawer/tabs/stack and what page links to what, as well as basic design features
         6. Pages is where code for individual pages will be, for example the map page or myOrders page
      2. Image of structure  
        ![fileStructure](../../images/shah/fileStruct.png)
3. Navigation structure
      1. As of now the navigation structure is not set in stone, but this is what we have now
      2. The main navigation is a drawer, a side nav that swipes from the left. This determines what set of tabs you see at the bottom
      3. The tabs at the bottom determine what page you see, for example if you're in the home drawer, you get to see the home tab which has 3 buttons, a my order tab, map tab and favorite tab. For example clicking the map tab will show the map page
      4. Pages are determined by the tab selected, they are the smallest form of navigation since they are at the top of the stack
4. Next steps
      1. The next thing to do is get the navigation finalized. Right now its in a prototype phase where it was being made before we all had 100% agreed on what the layout should be just to figure out how things look and organization of files
      2. After that I will work on the user login/signup
      3. Then app permissions for GPS/Camera



