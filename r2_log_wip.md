### Day 1: June 13, 2020
##### Netlify Identity + protected Functions

**Today's Progress**: I started over my days today since it had been over a week since I last did coding outside of work. Today I figured out Netlify Identity and used that to make a protected serverless Function.

**Thoughts:** Very cool that I am able to authenticate and make secure calls to an api without running my own server. :D

**Link to work:** [Repo](https://github.com/cctechwiz/vanilla_site)

**Tweet:**
[1/100] #100DaysOfCode I started my days over since it has been over a week since I last did any coding outside of work. Today I figured out @Netlify Identity and Functions, to make a protected serverless function call. https://github.com/cctechwiz/vanilla_site

### Day 2: June 15, 2020
##### Started Permafrost: Slide Puzzle Game

**Today's Progress**: I started making a game I thought of recently. It's going to be a puzzle game where you slide the little character to turn all the grass squares into ice squares. So far I've go the TileMap grid working.

**Thoughts:** Fun, I like making games with Godot.

**Link to work:** [Repo](https://github.com/lone-llama-workshop/Permafrost-Slide-Puzzle)

**Tweet:** (forgot to include #100DaysOfCode today... oops)
[2/100] Started my next #GameDev project `Permafrost: Slide Puzzle` using #GodotEngine. The objective is to slide over all the grass and freeze it w/o getting stuck. Got the placeholder assets made in #Aseprite and the TileMap setup in Godot. Repo: https://github.com/lone-llama-workshop/Permafrost-Slide-Puzzle

### Day 3: June 16, 2020
##### Home page listing and linking recipes

**Today's Progress**: Rename project to Simmerdown! I got the home page to list all recipes with links to their respective view page. Also some general refactoring and house keeping.

**Thoughts:** Pretty good progress today, now I can move on to the skeleton of the edit page.

**Link to work:** [Simmerdown](https://github.com/cctechwiz/simmerdown)

**Tweet:**
[3/100] #100DaysOfCode Renamed my wife's recipe app to Simmerdown, it has a nice ring to it. Today I worked on getting all the recipes listed on the Home page with links to their respective View pages. Also did some general refactoring of Services. Repo: https://github.com/cctechwiz/simmerdown

### Day 4: June 17, 2020
##### Basic New Recipe Page

**Today's Progress**: Flushed out all of the New Recipe page execpt the save logic.

**Thoughts:** This went well. I'm going to need to start thinking about where I will needed classes for styling things though.

**Link to work:** [Simmerdown](https://github.com/cctechwiz/simmerdown)

**Tweet:**
[4/100] #100DaysOfCode Created skeleton of "New Recipe" page w/o save logic, everything else is working though. I'm really going to need to start thinking about styling soon, which is definitely not my strong point. Repo: https://github.com/cctechwiz/simmerdown

### Day 5: June 18, 2020
##### Recipe Object from New Page content

**Today's Progress**: Added Recipe class model. Creating newRecipe using that class from contents of New Recipe page. Relinked Netlify deploy to renamed repo... oops.

**Thoughts:** The `document.querySelector` is awesome and made this whole process so much easier.

**Link to work:** [Simmerdown](https://github.com/cctechwiz/simmerdown) [Site](https://simmerdown.netlify.app/) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview)

**Tweet:**
[5/100] #100DaysOfCode Learned how to properly used `document.querySelector()` today to pull all of the inputs from the New Recipe page and create an instance of a Recipe class to pass on to the Repository for saving / caching. Repo: https://github.com/cctechwiz/simmerdown

### Day 6: June 19, 2020
##### New Recipe Page MVP Done

**Today's Progress**: Completed the New Recipe page MVP. It will save the new recipe into the repository local cache (which still goes away on reload for now).

**Thoughts:** This went well, there were a couple of gotcha's like reloading the New Page to add another recipe after saving, with my current setup this wiped the repository.

**Link to work:** [Simmerdown](https://github.com/cctechwiz/simmerdown) [Site](https://simmerdown.netlify.app/) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview)

**Tweet:**
[6/100] #100DaysOfCode Flushed out the rest of the New Recipe Page MVP. Moving on to hooking up FaunaDB to a collection of Netlify serverless functions for DB interactions next. Repo: https://github.com/cctechwiz/simmerdown

### Day 7: June 20, 2020
##### Got Started with FaunaDB and GraphQL

**Today's Progress**: I setup my FaunaDB account and database and created the GraphQL schema. I'm still trying to wrap my head around calling those endpoints from Netlify Functions.

**Thoughts:** It was a large mental overhead learning GraphQL today along with the weirdness around calling them from Netlify Functions. I need to let my brain stew on this for a while and come back to it. The biggest issue so far has been that all the examples are way to complex for what I'm trying to do so they can be hard to follow.

**Link to work:** [Simmerdown](https://github.com/cctechwiz/simmerdown) [Site](https://simmerdown.netlify.app/) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[7/100] #100DaysOfCode I setup my #FaunaDB account/database and created my first #GraphQL schema! Still trying to wrap my head around calling those "endpoints". It was a large mental overhead learning GraphQL, my brain stew on this for a while and come back to it later.

### Day 8: June 22, 2020
##### 

**Today's Progress**: Worked on getting the calls to FaunaDB working. Still getting Index does not exist errors. This will take some more debugging.

**Thoughts:** Not sure what's going on, but I also wasn't completely in it tonight.

**Link to work:** [Simmerdown](https://github.com/cctechwiz/simmerdown) [Site](https://simmerdown.netlify.app/) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[8/100] #100DaysOfCode Worked on getting the calls to FaunaDB working. Still getting Index does not exist errors. This will take some more debugging when my head is more in the game. Repo: https://github.com/cctechwiz/simmerdown

### Day 9: June 23, 2020
##### 

**Today's Progress**: Found that my query works fine on the deployed site. The issue is with my SECRET_KEY somehow not using the correct env var locally. I messed something up setting up fauna during `netlify dev` or something. I'll have to try again tomorrow.

**Thoughts:** This stuff makes me feel so dumb sometimes.

**Link to work:** 

**Tweet:**
[9/100] #100DaysOfCode Found that my query works fine on the deployed site. The issue is with my SECRET_KEY somehow not using the correct env var locally. I messed something up setting up fauna during `netlify dev` or something. This stuff makes me feel so dumb sometimes.

### Day 10: June 24, 2020
##### 

**Today's Progress**: Fixed the auth error I was getting by removing the Fauna Netlify Addon, that wasn't needed if I had the token in env vars. I also converted the API code from using the fauna client to calling the GraphQL endpoint directly with queries. Still need to clean up some code around that change.

**Thoughts:** Using GraphQL is going to make my code much cleaner since I won't need a different function for each CRUD call, just a different query or mutation string.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo) [Site](https://cctw.link/sd) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[10/100] #100DaysOfCode Fixed my SECRET_KEY error by removing the Fauna Netlify Addon. Converted my Netlify function from using the fauna client to calling the GraphQL endpoint directly. This will significantly simplify the code going forward. Repo: https://cctw.link/sd-repo

### Day 11: June 25, 2020
##### 

**Today's Progress**: Cleaned up and renamed fauna graphql serverless function, this one function now handles any graphql passed to it and returns the data. This way I only need this one single serverless function to handle all the database queries from my Api Service. Implemented getRecipeById call. Returning unpacked data from the Api Service now instead of raw GraphQL response.

**Thoughts:** Things went much smoother today interacting with GraphQL. I didn't get all the endpoint in the Api Service implemented like I wanted to, but I'm getting closer. The two queries (get & getAll) are done, now I need to implement the mutations (create, update, & delete).

**Link to work:** [Simmerdown](https://cctw.link/sd-repo) [Site](https://cctw.link/sd) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[11/100] #100DaysOfCode Things went smoother today with #GraphQL. I implemented the two queries (get & getAll) in the Api Service, now I need to implement the mutations (create, update, & delete). Repo: https://cctw.link/sd-repo

### Day 12: June 26, 2020
##### createRecipe Api call working

**Today's Progress**:  Fixed GraphQL schema and implemented createRecipe Api call, recipes are now being saved to the database! Still need to finish update and delete Api calls as well as Repository caching.

**Thoughts:** This was a bit more compicated working with graphql mutations instead of plain queries but eneded up making sense.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo) [Site](https://cctw.link/sd) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[12/100] #100DaysOfCode Fixed #GraphQL schema and implemented the create Recipe Api call, recipes are now being saved to the database! Next is finishing update and delete Recipe Api calls. Repo: https://cctw.link/sd-repo

### Day 13: June 27, 2020
##### MVP Complete!

**Today's Progress**: Finished create and delete calls along with associated view logic. Clean up Api Service and guarded against errors when calling Api when not logged in. This marks the completion of the MVP.

**Thoughts:** This is coming along nicely. I can now have Jess play with it and we can start itterating on design and additional functionality.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo) [Site](https://cctw.link/sd) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[13/100] #100DaysOfCode Finished the create and delete Api calls and their View logic. Cleaned up the app overall. The MVP is now complete! I can now have my wife play with it and I can start iterating on design and additional functionality. Repo: https://cctw.link/sd-repo

### Day 14: June 29, 2020
##### Header & Search MVP

**Today's Progress**: Flushed out basic header with search box and title linked ot home page.

**Thoughts:** Kind of weak effort today, but I coded something, so that's good.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo) [Site](https://cctw.link/sd) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[14/100] #100DaysOfCode Flushed out basic header with search box and title linked to home page. Kind of weak effort today, but I coded something, so that's good. Repo: https://cctw.link/sd-repo

### Day 15: June 30, 2020
##### Moved search to Home from Header

**Today's Progress**: Move the search filtering from the header into the home page where it makes more sense.

**Thoughts:** Today's changes were pretty fun.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo) [Site](https://cctw.link/sd) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[15/100] #100DaysOfCode Moved the search filtering logic from the header into the home page where it makes more sense. I can always use some #CSS magic to float it into the top right if that's where I really want to see it. Repo: https://cctw.link/sd-repo

### Day 16: July 1, 2020
##### Repository Caching

**Today's Progress**: I added caching to the Repository service to speed up navigation after initial load and reduce database calls.

**Thoughts:** This worked out pretty well, now I need to remove some of my `await` calls to help the loading appear even faster.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo) [Site](https://cctw.link/sd) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[16/100] #100DaysOfCode I added caching to the Repository service to speed up navigation after initial load and reduce database calls. Repo: https://cctw.link/sd-repo

### Day 17: July 2, 2020
##### Figured out Content Security Policy meta tag

**Today's Progress**: Figured out Content Security Policy meta tag to allow local scripts and Netlify Identity.

**Thoughts:** I never knew about this header before, it makes a lot of sense and I like it [CSP Info](https://stackoverflow.com/questions/30280370/how-does-content-security-policy-work).

**Link to work:** [Simmerdown](https://cctw.link/sd-repo) [Site](https://cctw.link/sd) [Netlify Dashboard](https://app.netlify.com/sites/simmerdown/overview) [FaunaDB Dashboard](https://dashboard.fauna.com/)

**Tweet:**
[17/100] #100DaysOfCode Learned about Content Security Policy meta tag. Never knew about this header before and as a security professional I like it! Configured it to only allow my locally hosted scripts and the Netlify Identity widget. Repo: https://cctw.link/sd-repo

### Day 18: July 3, 2020
##### Maintenance

**Today's Progress**:
General maintenance today;  
* Played with moving package.json into functions (reverted based on Netlify recommendations)
* Fixed bug of dereference data that was undefined by adding another ? or more opitional chaining
* Added more meta tags to index.html for Description and Author
* Removed old code that I was keeping for reference (everything I wanted to keep has already been superseded)
* Created READMD.md with basic dependencies and install guide
* Crated MIT license file

**Thoughts:** It was nice to clean up some things that were bothering me

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[18/100] #100DaysOfCode Did some general maintenance today; Fixed a bug dereferencing `undefined` while not logged in, created README and LICENSE files, deleted old reference code that has since been superseded. Overall, it was quite therapeutic. Repo: https://cctw.link/sd-repo

### Day 19: July 4th, 2020
##### Grid Snapping

**Today's Progress**: Got basic grid snapping working in the puzzle slider game I'm working on.

**Thoughts:** Doesn't quite work how I want, but I think it's good enough for now to get rolling with. Plus the snapping should only happen on the initial load.

**Link to work:** https://github.com/lone-llama-workshop/Permafrost-Slide-Puzzle

**Tweet:**
[19/100] #100DaysOfCode Got basic grid snapping working in the puzzle slider game I'm working on. Repo: https://github.com/lone-llama-workshop/Permafrost-Slide-Puzzle

### Day 20: July 6th, 2020
##### Login Guarding & Basic CSS Beginings

**Today's Progress**: Prevented most of the content from being rendered if a user is not logged in. Added some very basic flexbox centering to all contnet on the page.

**Thoughts:** An unauthenticated user couldn't make any api requests so the pages were usually half rendered. Now it just looks cleaner before the user logs in. Just adding basic centering to the pages and text makes it look a lot closer to the desired final product already.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[20/100] #100DaysOfCode Prevented site from looking half-rendered, due to an unauthenticated user not getting data from the API. Added basic flexbox / text centering to whole site. This makes it look a lot closer to the final idea already! Repo: https://cctw.link/sd-repo

### Day 21: July 7th, 2020
##### Collapsable category headers and enhanced search 

**Today's Progress**: Created "collapsible" category headers that hide all recipes in that category when collapsed. Added debounce to searching and blur on enter to hopefully help with mobile keyboards. I also added some more basic styling with placeholder colors to start getting a better feel for the final product.

**Thoughts:** This was a more code heavy session working out things I hadn't thought about before. I feel really good after this one.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[21/100] #100DaysOfCode Created collapsible headers that hide all recipes under it. Added debounce to search, and blur on enter to close mobile keyboards.  Tuned CSS and placeholder colors. Lots of new challenges tonight, I feel great after this one. Repo: https://cctw.link/sd-repo

### Day 22: July 8th, 2020
##### Button Footers

**Today's Progress**: Added a buttons footer with a left and right floating button. Did some other CSS styling.

**Thoughts:** It's starting to look pretty good! I still need icons for the buttons so the look more uniform.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[22/100] #100DaysOfCode Added a buttons footer with a left and right floating button. Did some other CSS styling. It's starting to look pretty good! I still need icons for the buttons so the look more uniform. Repo: https://cctw.link/sd-repo


# SKIPPED July 9th :( Making up on July 10th


### Day 23: July 10th, 2020
##### Fixed Footer and added Icons

**Today's Progress**: Fixed the footer click through issues using pointer-events. Added Font Awesome icons to make footer buttons look better.

**Thoughts:** Pretty simple hour tonight, just figuring out how to use Font Awesome icons.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[23/100] #100DaysOfCode Fixed the footer click through issues using pointer-events. Figured out how to use Font Awesome icons to make footer buttons look better. Repo: https://cctw.link/sd-repo

### Day 24: July 11, 2020
##### Fixed mobile sticky hovery, using Icons everywhere now

**Today's Progress**: Fixed the sticky hover on mobile by adding a class to the root when on a non-touch device and predicating all :hover effects with that class in the CSS. I also replaced everywhere on the site with icons where I wanted them. Buttons look and behave much better on mobile.

**Thoughts:** I need to find a better way to test on my device rather than commiting and publishing the code to test it. Maybe the custom viewports stuff in desktop firefox.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[24/100] #100DaysOfCode Fixed mobile sticky hover with  a class on the root when non-touch and predicating all :hover with that class. Replaced everywhere on the site with icons where I wanted them. Buttons look and behave much better on mobile. Repo: https://cctw.link/sd-repo

### Day 25: July 13, 2020
##### Permafrost Playable MVP

**Today's Progress**: Got Permafrost to a playable MVP today with Chris. You can slide around and complete levels. Levels are defined in text files and loaded into a TileMap.

**Thoughts:** This was kind of a jam day, Chris came over to Linette's house and we worked together for several hours.

**Link to work:** [Repo](https://github.com/lone-llama-workshop/Permafrost-Slide-Puzzle)

**Tweet:**
[25/100] #100DaysOfCode Took a break from Simmerdown today to do some #GameDev on a hobby game I've been thinking about for a while. Got it to a playable MVP during a self declared several hour "mini jam" today. [Repo](https://github.com/lone-llama-workshop/Permafrost-Slide-Puzzle)

### Day 26: July 14, 2020
##### Button and Input Styling

**Today's Progress**: Fixed up some buttons and inputs styling to match better between different pages.

**Thoughts:** Pretty basics stuff I guess, but CSS is my weakest area still so the practice was good.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[26/100] #100DaysOfCode Fixed up some buttons and inputs styling to match better between different pages. Pretty basics stuff I guess, but CSS is my weakest area still so the practice was good. Repo: https://cctw.link/sd-repo

### Day 27: July 16, 2020
##### Custom Modal, Clean up, & Bug Fixes

**Today's Progress**: 
    * Created basic custom confirm modal component class
    * Wrapped ingredient unordered list into two columns
    * Added 'All' category to home page, and genericized 'Other' category so it cannot be selected on New/Edit page
    * Pulled common logic/HTML from New/Edit pages out into HtmlBuilder
    * Fixed bug when saving edits that the cached copy wasn't updated correctly

**Thoughts:** It was fun creating a custom modal, and it's always refreshing to refactor code

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[27/100] #100DaysOfCode Built a confirmation modal using an #ES6 class and promises. I also did some clean up, refactoring, and bug fixing; which is always refreshing. Repo: https://cctw.link/sd-repo

### Day 28: July 17, 2020
##### Replaced window.confirm with Modal Confirm

**Today's Progress**: I replaced all the window.confirm dialogs with my custom ModalConfrim dialogs.

**Thoughts:** Pretty basic tonight, but got the time in.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[28/100] #100DaysOfCode Pretty basic tonight, but got the time in by replacing all the window.confirm dialogs with my custom confirm modal dialogs.


# Took a mental health week


### Day 29: July 24, 2020
##### Fixed Alignment of Category Checkboxes

**Today's Progress**: Today I fixed the alignment of the category checkboxes. 

**Thoughts:** It's been bugging me for a while that the checkboxes didn't line up correctly. It looks much better now that those aren't all over the place in the center of the screen.

**Link to work:** [Simmerdown](https://cctw.link/sd-repo)

**Tweet:**
[29/100] #100DaysOfCode After taking a week off for my sanity, today I fixed the alignment of the category checkboxes. It's been bugging me for a while that the checkboxes didn't line up correctly. Repo: https://cctw.link/sd-repo

### Day 30: July 25, 2020
##### Plex Server Setup / Configuration

**Today's Progress**: Today I setup and configured a Plex server. Not really coding today, but finally knocking something off my tech bucket list that I've been wanting to do forever, so I'm counting it.

**Thoughts:** 

**Link to work:** 

**Tweet:**
[30/100] #100DaysOfCode Today I setup and configured a Plex server. Not really coding today, execept for some simple transcoding scripts. I'm happy to finally be knocking something off my tech bucket list that I've been wanting to do forever, so I'm counting it.

### Day 31: July 27, 2020
##### Fixed logout bug

**Today's Progress**: Fixed a bug that appeared when logging out. Turns out it was simply an incorrect CSS selector *facepalm*.

**Thoughts:** 

**Link to work:** 

**Tweet:**
[31/100] #100DaysOfCode Fixed a bug that appeared when logging out. Turns out it was simply an incorrect CSS selector. 🤦‍♂️ With this, Simmerdown is pretty close to being ready to my wife start using it and giving me feedback. Repo: https://cctw.link/sd-repo

---

### Day #: Month DD, 2020
##### SUMMARY

**Today's Progress**: 

**Thoughts:** 

**Link to work:** 

**Tweet:**
[XXXXXXXX/100] #100DaysOfCode
