# 1051-Final-Project

## Difficulties Faced and Overcame
&ensp;&ensp;The largest challenges I faced while completing the project can be broken down into three categories: coding issues, misjudgement of time, and difficulties in web design. First, touching on my coding difficulties, I come from a programming background of AP Computer Science. I became comfortable with addressing hypothetical situations through code, and my only true application outside of this realm was a final game project completed at the end of the course. As a result this, I never had to rely on existing documentation before, as there was not the concern of spending unnecessary time building a feature that someone else had already constructed and thoroughly tested. However, this is not the case when building a website with HTML, JavaScript, and CSS, as there is an abundance of tutorials and element documentation online. The project was my first introduction to taking the framework of someone else's base and applying it to my own needs. A few specific of these unique difficulties was often online documentation assumed that static html pages were going to be used. However, as I was using Flask to dynamically generate my pages I had to format my code with this structure which required in-depth editing to ensure that my web pages would be able to find my pictures in the correct directories and I would be able to utilize for and if statements to avoid hardcoding information that was already stored in my database tables. 

&ensp;&ensp;My second difficulty came with the timing of the project. I originally had planned to integrate a registration system for fake photography classes, as well as a shop page, into my website design. However, I miscalculated how long it would take me in order to learn the required SQLite3 commands to make my gallery and photo tags possible while working by myself. Much of my work time went into creating these features, as I had to expand on the teachings of CS50 to learn and implement calls such as 'SELECT * FROM pictures WHERE name IN (SELECT Name FROM tags WHERE tag="' + tag + '")', in order to only return the information of photos with a specific tags by referencing data from more than one table, and SELECT tag, count(\*) AS Tagcount FROM tags GROUP BY tag, in order to count the number of times a tag was used in order to build my tag option page (where the font size of tag depends on the number of photographs with that tag).

&ensp;&ensp;My third difficulty that I had to overcome was I had never before completed a project so dependent on web design and creating appealing visual aesthetics in an online medium. I misjudged how long it would take testing out different fonts, sizes, and colors in order to make a webpage look professional and avoid looking tacky. This required learning about a wide variety of CSS properties such as 'cursor', 'width', 'height', 'box-shadow', and 'position', in addition to learning how to apply css only when an element is hovered over and how to establish the dimensions of pictures so they resize when the browser size changes. Also, although I was able to get through all of the photos, the task of transferring photos from my computer to my laptop took longer than expected (due to the incompatible .HEIC Apple photo file format).


# What was learned
Some features I had to learn about for this project was to ability for two routes to render the same html page (I needed a special case so that a message could be generated if a person attempted to search for a tag that had no corresponding images), new HTML tags, how to edit existing code in order to fit my purposes, the syntax differences between JavaScript, Java, and Python, as well as how to properly integrate for and if statements into HTML code using Jinga syntax. The ability to alter code for my own purposes was a skill I progressively improved at as I worked on the project, as I became comfortable with looking at the skeleton of the code, understanding how it functioned, and adding or removing classes, changing HTML tags, or picking apart the JavaScript (this came into play in particular with the CSS for the resizable photo gallery, as I changed the location of the photo caption, how many photos I wanted on each line, and the desired reaction when the photo was hovered over). Furthermore, specific to SQLite3 and databases, I learned how to create more than one table within a database, how to select all or some of the information from a given table, how to import .csv files into a SQLite3 database table, and tricks such as using .schema to see how a table was constructed (in the cases of my tables, I had one named tags that stored a Name with a varchar(40) and a tag associated with the name that also had varchar(40), and another named pictures that stored Name with varchar(40), Caption with varchar(255), and the file directory path as Filename varchar(255)) and .mode columns in order to make my table data easier to read when a variation of SELECT * FROM was used on a table. In the design front, I learned about Bootstrap and the elements that go into allowing the features to function (such as some, like the NavBar, requiring JavaScript) and about a wide breadth of css properties for my stylesheet.

# What I enjoyed
Although I thoroughly enjoyed this project and the opportunity to learn new programming frameworks, as well as continue to develop my Python knowledge through flask, my favorite part of the assignment was being able to learn about SQLite3 and how to integrate it with Flask. I find the capabilities and search queries for tables extremely powerful, and I became excited every time I discovered a new command to assist my coding or a new key word to combine with my SELECT queries. Furthermore, I also really enjoyed being able to search the internet for different HTML tags and CSS properties to use for my website in order to help it look as professional as possible.

# Quick overview of files

## app.py
Includes the Python Flask framework that deals with my database queries and dynamically builds my HTML

## layout.html
The framework for all other HTML pages on the site, includes the code for the top navigation bar

## index.html
The code for the homepage, including the rotating photo slideshow

## gallery.html
The code for the photo selection, able to be used for cases where all photos are shown or only some are shown based on tags

## tags.html
The code for the page that includes links (actually buttons due to links not have a POST method) to reach the photo collections that match that category, also the page the user is redirected to if a tag with no corresponding pictures is searched

## about.html
The code for the page detailing the founders of Dramartsy

## history.html
The code for the page detailing the journey of Dramartsy

## styles.css
The stylesheet that I created for the project

## tags.js
Includes the Javascript that allows the tags on tags.html to increase in size given the number of pictures associated with that tag

## gallery.js
Includes the Javascript that makes the lightboxes on gallery.html possible

## index.js
Includes the Javascript that makes the slideshow on index.html possible

## final.db
Includes the two tables used for the website, pictures (which stores a picture's name, caption, and file location) and tags (which stored a picture’s name and all of the associated tags for that name)




