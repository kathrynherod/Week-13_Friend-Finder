# Friend Finder - Node and Express Servers

### Overview

This activity is a compatibility-based "FriendFinder" application -- basically a dating app. This full-stack takes in results from your users' surveys, then compares their answers with those from other users. The app will then display the name and picture of the user with the best overall match. 
Express to handles routing. App is deployed to Heroku using JawsDB.

### Live App
Click [here to launch the application in your browser](https://kh-friend-finder.herokuapp.com/). 


### Instructions Overview

1. Your survey should have 10 questions of your choosing. Each answer should be on a scale of 1 to 5 based on how much the user agrees or disagrees with a question.

![1](https://github.com/kathrynherod/Week-13_Friend-Finder/blob/master/gifs/ex1.gif?raw=true)

![2](https://github.com/kathrynherod/Week-13_Friend-Finder/blob/master/gifs/ex2.gif?raw=true)

2. Your `server.js` file should require the basic npm packages we've used in class: `express`, `body-parser` and `path`.

3. Your `htmlRoutes.js` file should include two routes:

   * A GET Route to `/survey` which should display the survey page.
   * A default, catch-all route that leads to `home.html` which displays the home page. 

4. Your `apiRoutes.js` file should contain two routes:

   * A GET route with the url `/api/friends`. This will be used to display a JSON of all possible friends.
   * A POST routes `/api/friends`. This will be used to handle incoming survey results. This route will also be used to handle the compatibility logic. 

5. You should save your application's data inside of `app/data/friends.js` as an array of objects. Each of these objects should roughly follow the format below.

6. Determine the user's most compatible friend using the following as a guide:

   * Convert each user's results into a simple array of numbers (ex: `[5, 1, 4, 4, 5, 1, 2, 5, 4, 1]`).
   * With that done, compare the difference between current user's scores against those from other users, question by question. Add up the differences to calculate the `totalDifference`.
     * Example: 
       * User 1: `[5, 1, 4, 4, 5, 1, 2, 5, 4, 1]`
       * User 2: `[3, 2, 6, 4, 5, 1, 2, 5, 4, 1]`
       * Total Difference: **2 + 1 + 2 =** **_5_**
   * Remember to use the absolute value of the differences. Put another way: no negative solutions! Your app should calculate both `5-3` and `3-5` as `2`, and so on. 
   * The closest match will be the user with the least amount of difference.

7. Once you've found the current user's most compatible friend, display the result as a modal pop-up.
   * The modal should display both the name and picture of the closest match. 
   
   * #### I added a bonus feature to calculate the % compatibility with the friend match.
   
![3](https://github.com/kathrynherod/Week-13_Friend-Finder/blob/master/gifs/ex3.gif?raw=true)

- - -
## Database updates with user repsonse for matching future entries

![4](https://github.com/kathrynherod/Week-13_Friend-Finder/blob/master/gifs/ex4.gif?raw=true)



# Copyright
Coding Boot Camp (C) 2016. All Rights Reserved.
