# Jeff Souza's ePortfolio

This portfolio includes two programs designed and enhanced while a student in the Computer Science program at Southern New Hampshire University.  It includes a self-assessment, a code-review and two artifacts with enhancements and narratives explaining each enhancement.  The first program is a Campsite Locator application developed during my CS-360 Mobile Architecture course.  The enhancements for this program are in software design/engineering and databases.  The second program is a simple python-based listing application that covers enhancements in it’s algorithms and data structure.

## Self-Assessment

## Code Review

<iframe width="560" height="315" src="https://www.youtube.com/embed/aqCf2m3RZMs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Campsite Locator Enhancements

### The GitHub repository for the Campsite Locator application can be found here: [Campsite Locator](https://github.com/listen2speak/CampsiteLocator)

For the software design/engineering aspect of the ePortfolio, I have decided to go with the Campsite Locator application that I had developed in CS-360 Mobile Architecture.  This application takes a total of 30 pre-selected campgrounds throughout the New England area and allows the user to browse them by state.  A weather API was integrated into the application to allow for the user to check on current weather conditions in the area of the selected campground, a favorites list that originally allowed the user to only manually add in new favorites, and also allows the user to post a link to the campground’s website directly to FaceBook.  

I have chosen this artifact as I feel that this has been one of the greatest accomplishments of my time as an undergraduate.  This was the first time where I felt I had actually created a useful product and could see the outcome of my work physically (or at least emulated) on a phone.  There was no pre-designed code that had blank lines to fill in or other lines of code to edit.  I was given a task and a blank screen and built this from nothing.  I feel the component overall showcases my skills in the software development field.  Specifically, working between classes and methods, and manipulating data from the internal “set” database to the user’s “favorites” database.  

I improved upon this work by adding a favorites checkbox to the campsite activity screen.  When selected, a few things occur.  First, I added a star that toggles from a black outline to a golden star when selected.  When the user selects this item, the shared preferences editor remembers that the box was checked, ensuring that when the user returns to the information page about the campsite, the favorite star is still gold.  It also adds the name, location and star rating to the favorites list.  This can now be seen when the user clicks on the favorites button in the main menu and they can then manipulate the name and location as well as give the campsite a user rating.  This data manipulation will only affect the favorites list and will leave the original searched item untouched.  

I chose to use the shared preferences tool as it is a great way of passing shared information throughout the program using a xml file (Aggarwal, 2019).  This was perfect for wanting to ensure that the favorites star stays checked after exiting the application by saving this data as a key/value pair to device storage.  

I was able to accomplish what I set out to do for my enhancement to this item.  I will further allow for manipulation the favorites database for the third enhancement, but the goal was to enable a favorites checkbox from the campsite information screen and I accomplished that goal.  

When I originally wrote the program, I failed miserably at commenting my code.  Coming back to it now after 8 months I was very much lost.  Trying to remember what activities fed into each other and what activities manipulated the SetLibrary database and the Favorites Database got very tricky.  This was poor coding on my part and I am suffering for it now.  I, at first, attempted to re-write a lot of my code to move information from within the CampsiteActivity to the favorites list.  Then I stepped back and realized that sometimes the simplest solution is the best.  I already had a database helper class written and all I needed was to utilize that and send over the information that was required.  I also learned how to edit shapes for checkboxes as well and that, though more for aesthetics, was interesting as well.

For my databases enhancement I continued to work on my Campsite Locator application. This time, I have manipulated the user’s “Favorites” database using SQLite.  This takes the software design enhancement and gives the user further access to change the information in their own database without affecting the programs internal database.  The user can now add their own comments, which will be displayed in the list, as well as give their own star rating, and edit the site name and location if it suits them.  There is also the ability to go directly to the campsite website when they select the campsite from their favorites list.  I felt that this was the next step in the process of advancing this program and would fit well with the requirements set forth for this type of enhancement project.
	
I chose to use SQLite for this application as it is open source and does not require a separate server.  The program we are running is a small program with not a tremendous amount of data being added to either the internal database or the user’s favorite database.   The fact that we are using this for a mobile application, with the possibility of the database ever reaching the 140-terabyte maximum that SQLite supports being very minute, makes SQLite a very good choice for the Campsite Locator application (Hans, 2020).  

I was able to meet my course objectives as I had laid them out in module one.  The core of what I wanted to accomplish was met, manipulating the database to allow the user to copy all information from the internal database to their own favorite database.  Allow the user to edit information and put in their own star rating, and then proceed to the campsite’s website for further research.  

Lastly, as was the case in the first enhancement, the most difficulty I had was having to go back and comment my previous work.  After going through all of the classes and layouts I was able to see what classes worked with which database.  Once that was accomplished, ensuring that I was only allowing the user to manipulate their own database and not the internal database was easier to understand.  The only other issue that really held me up was a whitespace error in creating new columns in the favorites database.  This was seen when using DB Browser for SQLite and see how the column names were not correctly labeled.  Two whitespace errors caused a few hours or head scratching and rework before it was caught. 

References:

Aggarwal, P. (2019, October 14). Shared Preferences in Android with Examples. GeeksforGeeks. https://www.geeksforgeeks.org/shared-preferences-in-android-with-examples/

Hans, J. (2020, September 23). SQLite vs MySQL vs PostgreSQL (Detailed Comparison). https://blog.ssdnodes.com/blog/sqlite-vs-mysql-vs-postgresql/

## Companions.py Enhancment

### The GitHub repository for the Companions.py can be found here: [Companions](https://github.com/listen2speak/Companions)

For this artifact I had chosen to use a simple program that I was originally using to familiarize myself in both Python and JSON files.  Python was the first language that I received training in at the start of my computer science education, but I only ever had that one course in it.  I wanted to familiarize myself with its structure and syntax again since java and C++ had been the main coding languages that I had been using since that first class.  In one other class, Systems Architecture, we were introduced to JSON files but I never recalled actually learning about how they were used or for what purpose they served.  Again, I wanted to familiarize myself a bit better with them.  This program is a simple list program.  It asks for the user’s name and then allows the user to create two lists, one for friends’ names and another for pets.  Here they can print the list, delete from it and then save it to a JSON file.  Those files will then be read at the start of the program to keep the data the user stored.  I first started this during the winter break that brought in this year.  
	
I chose this artifact as a way to incorporate my knowledge of search algorithms.  Originally, when deleting a name from either list, the program would follow a linear pattern while searching for the name. Dealing with a small list, a linear pattern would be fast enough, however should that list grow to a much larger amount, linear search becomes a less viable solution.  I have chosen to insert a binary search.  Here, we split an ordered list and search the middle element.  We then continue to half split the list in the direction that our query lies until we find the list.  This way we are not individually looking at each element of the list but always splitting our list in half and looking to the center (Leech, 2018).

Originally, I had thought to make an adjustment to the list allowing for it to be made up of arrays of strings using both name and age and to order them using either of the two variables.  Instead I focused more on the search aspect and tied it into my delete function.  This way we can search for the name to be deleted using the binary search method and if found, it is removed from the list.  If it is not found, it is stated and then the user is allowed to continue with the program.  

My biggest challenge in getting this to work was to recall my algorithm data.  I had lost all the work I had from my algorithms class due to a system crash on my computer so trying to recall these methods and get them to function was a bit of a challenge.  Once I sat down and remembered how the binary search function works, I was on my way.  I did forget about subtracting “1” from my total length of the list and subtracting and adding “1” to and from my “mid” variable.  This was causing my program to crash whenever I was attempting to delete an element that wasn’t in the list.  Fortunately, that has been remedied and the method is working as intended now.  

References:

Leech, C. (2018, July 13). Implement linear and binary search algorithms with Javascript. Medium. https://medium.com/employbl/implement-linear-and-binary-search-algorithms-with-javascript-2149997588f0
