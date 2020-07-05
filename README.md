# Blogs App
App to Read, Write BLogs. Appreciate other users blogs by giving a like and commenting on their blogs.  
Link to the app - https://mernstackblogsapp.herokuapp.com/  
> **_NOTE:_**  Image are not displayed of previous blogs and users after deploying it onto Heroku. It is because Heroku filesystem is ephemeral - that means that any changes to the filesystem whilst the dyno is running only last until that dyno is shut down or restarted. Each dyno boots with a clean copy of the filesystem from the most recent deploy. - https://help.heroku.com/K1PPS2WM/why-are-my-file-uploads-missing-deleted. Currently working on it however you can still add new image which will be displayed on the app for some time.

## Technologies
**Front End** - React.js, Redux  
**Server Side** - Node.js, Express.js  
**Database** - MongoDB  

## Features
* User SignUp
    * Sign up with unique email id
    * Error if User registers with same email id
    * Password is hashed before saving it to the database
    * Option to add profile picture. If user does not wish to upload, default picture will be uploaded
    * Form validation
* User Login
    * Login with email id and password
    * On successful login creates a JWT which is stored in localstorage for authentication on every API call
    * Form validation
* Blogs Page
    * Contains blogs written by all users on Blogs page
    * Anyone can see and read blogs
    * Filter option to categorise blogs as per selected category. By default is selected to show all
    * Option to display number of blogs on per page. By default is 5
    * Pagination
    * Search to find particular blogs
* Read Blog
    * Shows more content written for particular blogs
    * Information about blog author
    * Logged in users can like and comment on the blog. Guest users cannot
    * Each user can like each blog only once and can add multiple comments.
* Write Blog
    * Logged in users can write a blog
    * Blogs with same title will not be accepted
    * Enter about blog and blog display image
    * Form validation
* Profile
    * Contains logged in user profile
    * All blogs written by user
    * Edit / Delete particular blog
    * Edit / Delete user profile
