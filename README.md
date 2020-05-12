## How to run
* Open terminal and run ``Git clone https://github.com/aryansingh12/cs326-final-omega.git``
* cd into the repository and run ``npm i @types/node`` 
* Run ``node backend/server-main.js``
* Go to http://localhost:8080/ 
* Heroku website: https://cs-326-final-omega.herokuapp.com/

## Changes
* If you make any changes in the typescript file - ``tsc backend/*.ts``

# Team Omega
## CodeTogether
## CS 326 Spring 2020  

## Overview:  
Our application is designed to allow people to come together to create and improve upon independent projects in an efficient way. Our site allows users to create an account to showcase their skills and previous experience to others in order to create an effective project team. Similarly, users can create public projects for people to browse. The projects will have all relevant info like a description, necessary skills, github page, etc. This way, users are able to see which project most interests them or fits well with their skillset. This site is not only for programmers, however. People who think that they have “the next big app idea” can come onto the site and create a project in the hopes that some programmers will see it and hop on board. This is what makes our site unique. The combination of programmers and entrepreneurs into one space to discuss and work on projects will facilitate the creation of more applicable and well thought out projects.   

## Team Members: 
Ron Arbo: https://github.com/ron-arbo  
Aryan Singh: https://github.com/aryansingh12  
TJ Goldblatt: https://github.com/tjgoldblatt  

# Screenshots
## Welcome screen, Featured projects
<img width="1436" alt="Screen Shot 2020-05-07 at 7 19 13 PM" src="https://user-images.githubusercontent.com/31454667/81354004-84765e00-9098-11ea-9717-bab4211289a5.png">

## Browse projects - from the Database
<img width="1433" alt="Screen Shot 2020-05-07 at 7 21 43 PM" src="https://user-images.githubusercontent.com/31454667/81354008-850ef480-9098-11ea-99bc-5c9b40b37899.png">

## Create project 
<img width="1437" alt="Screen Shot 2020-05-07 at 7 19 23 PM" src="https://user-images.githubusercontent.com/31454667/81354005-84765e00-9098-11ea-968b-0469ba877a13.png">

## Project Description 
<img width="1432" alt="Screen Shot 2020-05-07 at 7 22 37 PM" src="https://user-images.githubusercontent.com/31454667/81354016-8b04d580-9098-11ea-8675-fe067f749cf8.png">

## Feedback section
<img width="1432" alt="Screen Shot 2020-05-07 at 12 25 26 AM" src="https://user-images.githubusercontent.com/31454667/81354018-8b9d6c00-9098-11ea-9698-b8e2678c2095.png">

## Edit project
<img width="1431" alt="Screen Shot 2020-05-07 at 7 33 25 PM" src="https://user-images.githubusercontent.com/31454667/81354482-b1774080-9099-11ea-8949-fc31858f5d38.png">

## Profile
<img width="1431" alt="Screen Shot 2020-05-07 at 7 21 56 PM" src="https://user-images.githubusercontent.com/31454667/81354009-850ef480-9098-11ea-9357-530f7f445c6d.png">

## Edit profile
<img width="1437" alt="Screen Shot 2020-05-07 at 7 33 11 PM" src="https://user-images.githubusercontent.com/31454667/81354481-b0deaa00-9099-11ea-91b6-407c0282fc56.png">

## Login
<img width="1429" alt="Screen Shot 2020-05-07 at 7 19 31 PM" src="https://user-images.githubusercontent.com/31454667/81354007-850ef480-9098-11ea-820c-a5ce060d5d29.png">

## Sign Up
<img width="1438" alt="Screen Shot 2020-05-07 at 7 29 52 PM" src="https://user-images.githubusercontent.com/31454667/81354308-4463ab00-9099-11ea-899d-2f15f4a9a448.png">

## API
### All endpoints

* Project Endpoints: Assuming you are deploying the server on localhost with port 8080<br/>

   * The create endpoint is:<br/>
   ``localhost:8080/codetogether/users/:userID/createProject``

   * The read endpoint is:<br/>
   ``localhost:8080/codetogether/users/:userID/readProject``

   * The update endpoint:<br/>
   ``localhost:8080/codetogether/users/:userID/updateProject``

   * The delete endpoint:<br/>
   ``localhost:8080/codetogether/users/:userID/deleteProject``

* Profile Endpoints: Assuming you are deploying the server on localhost with port 8080 <br/>

   * The create endpoint is: <br/>
   ``localhost:8080/codetogether/users/:userID/createProfile``

   * The read endpoint is:<br/>
   ``localhost:8080/codetogether/users/:userID/readProfile``

   * The update endpoint:<br/>
   ``localhost:8080/codetogether/users/:userID/updateProfile``

   * The delete endpoint:<br/>
   ``localhost:8080/codetogether/users/:userID/deleteProfile``
   
* Other Endpoints:

  * Find all projects endpoint: <br/>
  ``localhost:8080/codetogether/users/:userID/allProjects``
  
  * Project searching endpoint: <br/>
  ``localhost:8080/codetogether/users/:userID/projectSearch``


### Responses

<img width="651" alt="Screen Shot 2020-05-07 at 8 06 34 PM" src="https://user-images.githubusercontent.com/31454667/81356123-76c3d700-909e-11ea-8749-4cc5f5b12ca3.png">
<img width="642" alt="Screen Shot 2020-05-07 at 8 06 46 PM" src="https://user-images.githubusercontent.com/31454667/81356126-76c3d700-909e-11ea-8eff-b68c72209c20.png">
<img width="649" alt="Screen Shot 2020-05-07 at 8 06 59 PM" src="https://user-images.githubusercontent.com/31454667/81356128-76c3d700-909e-11ea-8099-daa696a20a4a.png">
<img width="643" alt="Screen Shot 2020-05-07 at 8 07 05 PM" src="https://user-images.githubusercontent.com/31454667/81356130-775c6d80-909e-11ea-8d3e-9d5840efc31a.png">


## Database Documentation
Our database is a collection containing two types of documents: Projects and Profiles. They are described below 
```Typescript
   project document { 
       _id: <ObjectId>,            //ObjectId provided by MongoDB 
       projectName: String,        //Name of the project 
       projectButtons: String[],   //Array of all languages used to create the project (Ex: ["Java", "HTML", "CSS"]) 
       projectDescription: String, //Description of the project 
       projectLinks: String,       //A string of helpful links related to the project (Githubs, guides, url, etc.) 
       projectNumWorkers: String,  //The number of people you're looking for to help with the project 
       projectProgress: String,    //The amount of progress made on the current project 
       projectWorkers: String,     //The current people working on the project
   }
``` 
 
```Typescript
   profile document { 
       _id: <ObjectId>,           //ObjectId provided by MongoDB 
       profileID: String,         //ID used to identify specific profile 
       firstName: String,         //First name of user 
       lastName: String,          //Last name of user 
       profileAbout: String,      //The 'About' section for the user's profile page 
       profileBio: String,        //The user's bio section 
       profileEmail: String,      //The user's email used to sign and log in  
       profileLinks: String,      //The user's links for things like github, linkedin, facebook, etc. 
       profilePassword: String,   //The password used by the user to sign and log in 
       profileProjects: String,   //The 'projects' section for the user's profile page
       skills: Strings[],   //An array of the skills a user has 
   }
```

## Conclusion
We thoroughly enjoyed the project as a whole, for some of us this was the first time we had done a complete project on our own basically from scratch. Our group didn’t really have any prior knowledge regarding web programming so every step of the way was a learning process. The hardest parts of the project were definitely creating the server and databases, while the easiest parts were HTML and CSS. One thing we wish we had a better understanding of prior to starting the project was the backend portion of the project, we relied a lot on stack overflow to answer questions we had. One decently sized technical hurdle was connecting Heroku to our project which took some time to figure out what we needed to do.
