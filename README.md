# Code Together

## Todo

What is done and who did it: (If I missed something you did just add it in, mostly been keeping track of myself)  
Database:  
Note that we have two methods for each operation. One for projects, and one for profiles. Their implementation is very similar.  
Creation and connection in code: Aryan  
put() Method: Mostly Aryan, Small Part Ron 
get() Method: Mostly Ron, Small Part Aryan  
del() Method: Ron  
Incorporation of Radio Buttons into DB: TJ  
find() Method: Mostly Aryan, Small Part TJ  
  
HTML Connection/Output:  
Project CRUD Operations work with DB and Output in HTML:  
Create: Aryan, I think  
Read: Ron  
Update: Ron  
Delete: TJ  
Profile CRUD Operations Work with DB and Output in HTML:  
Create: Aryan/Ron?  
Read: Ron  
Update: Ron (Need tweaks with HTML though)  
Delete: TJ  
  
Other:  
Searching Functionality: Ron  
Minor Index.html layout changes: Ron  
Hyperlink projectName in index.html to appropriate project description: Aryan  
Hyperlink lastName in index.html to appropriate profile page: Ron, but largely based off Aryan's work  
Feedback section: Aryan  
  
Things that need to be done:  
* Finish above HTML connections with DB (Try to change the need for input for delete, update)
* Some HTML might be weird with our inputs (Contact section in profile, Project section in profile, etc.)
* Add radio buttons to profiles? Either this, or we need to delete the skills section in profile

## How to run
* Open terminal and go to the project directory
* Run ``npm i @types/node`` 
* Everytime you make a change in a typescript file - ``tsc backend/*.ts``
* Run ``node backend/server-main.js``
* Go to http://localhost:8080/ 
* website: https://cs-326-final-omega.herokuapp.com/

* Project - 
    * project_id: int
    * name: string
    * description: string
    * already_working: string
    * helpful_links:[string]
    * programming_languages: [string]
    * developers_working: int (or could be an array of develop ids?)
    * developers_needed: int

* Developer
    * developer_id: int
    * name: string
    * email: string
    * skills: [string]
    * resume (maybe parse this using something in the future): pdf
    * weekly_hours: int

* Investor
    * investor_id: int
    * name: string
    * email: string
    * job_description: string
    * funding: int
    * weekly_hours: int

# Screenshots

## Welcome screen, all projects
<img width="1430" alt="Screen Shot 2020-04-08 at 5 49 23 PM" src="https://user-images.githubusercontent.com/31454667/78837203-8f6a9f80-79c1-11ea-95ac-3e9f55ecd21b.png">

## Project Description 
<img width="1432" alt="Screen Shot 2020-04-08 at 5 49 11 PM" src="https://user-images.githubusercontent.com/31454667/78837199-8da0dc00-79c1-11ea-8eb8-bd7e50c74a71.png">

## Create a new Project page
<img width="1430" alt="Screen Shot 2020-04-08 at 5 49 42 PM" src="https://user-images.githubusercontent.com/31454667/78837206-90033600-79c1-11ea-9168-b1e71cff05fe.png">

## Profile Section
<img width="1431" alt="Screen Shot 2020-04-08 at 5 50 18 PM" src="https://user-images.githubusercontent.com/31454667/78837211-909bcc80-79c1-11ea-9940-50e10eac26e4.png">

## Login
<img width="1414" alt="Screen Shot 2020-04-08 at 5 49 52 PM" src="https://user-images.githubusercontent.com/31454667/78837207-90033600-79c1-11ea-9338-b8428fb3206e.png">

## Sign Up
<img width="1429" alt="Screen Shot 2020-04-08 at 5 50 03 PM" src="https://user-images.githubusercontent.com/31454667/78837209-90033600-79c1-11ea-92ca-1c1f54a06e5b.png">
