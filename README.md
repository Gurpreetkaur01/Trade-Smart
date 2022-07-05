This document explains all the files on the server and their functions for this application. The folders and files are listed below:
•	CSS folder: The folder contains all the stylesheets used for the application, they includes the stylesheets for the forms, footer and the pages.
•	Images: the folder contains the images used in the application
•	Node_modules: this folder contains the library that generates the word cloud that displays the most popular searches. The library is a built using JavaScript and it’s called jqcloud.
•	PHPMailer: This folder is a library that is used to send mails to the email address of everyone that signs up with a conestoga email address ( @conestogac.on.ca )
•	phpMyAdmin: This folder is a library that is used to manage the database as a graphical user interface (GUI) instead of using the command line. 
•	Change Password: This is a php file that is used to change password for the user, it reads the SESSION variable and the old password the user entered. If there is a match, the new password entered by the user is accepted and if there is no match, password change is not allowed.
•	Confirmation: this is a php file that reads the confirmation code that is sent to the user’s email address through a get method and confirms if it is the same as the one on the database. If the two numbers match, the user is fully registered by saving the name into another table called (registeredusers)
•	Delete: this is a php file that handles the deleting of a post, the file reads the id of the url using the get method and changes the status from active to deleted in the database.
•	Deletemyaccount: this file reads the SESSION name of the user, checks the database and removes the users record from the registeredusers table and adds the record into the deletedusers table.
•	Homepage: this file reads all the data in the post database where the status is active and displays them. It also includes links to chat with the poster of each ads. Signed-in users are registered to chat using their email address and users that are not signed-in are registered to chat using a randomly created ID.
•	Image_check and imgpost: these are used to check the size of the images uploaded in the posts.
•	Indexjav: this is the javascript file that does all the validation on the homepage.
•	Json: this is a php file that reads all the posts in the database where the status is active and converts all the data into json, the mobile app uses this json file to display all the posts.
•	Logout: this is a php file that logs out the user. The file unsets and destroys the Session saved on the browser.
•	Mobilesearchjson: This serves the same purpose as the json file, this only queries the database based on the search from the mobile app. The result of the query is converted into a json file.
•	Populardemand: this is a php file that reads all the saved searches from the searchlog table and makes the word cloud by using the jqcloud library.
•	Postpage: this is a php file that displays the form to make a post. If the user is not signed in, the page displays “you are not logged in” but if the user is signed in, a form is displayed.
•	Profile: this is a php file that displays all the posts posted by a user, the page enables users to change their password, delete their account and delete their posts.
•	S3 and s3_config: this is a library that is used to save images into the amazon S3 cloud and the url to the image is only saved into the database.
•	Savepost: this is a php file that reads all the information posted by the user and saves the information into the database (posts table). It handles saving the images into the amazon S3 cloud. It saves the url of the images into the database and also saves the QRcode url into the database.
•	Screenpost: this is a php file that reads all the data from the posts table in the database where the status is active. It displays the ID, qrcode, one image, title of the posts and it is displayed for the monitor placed on the hallway.
•	screenpostBooks, screenpostElectronics, screenpostOthers, screenpostRents and screenpostTutorial: These works exactly like the screenpost file but each of the file displays the category in their names.
•	Searchresult: this is a php file that queries the posts table in the database based on what the user is searching for. (It searches for posts with a status of active).
•	Showqr: this is a php file that displays the search result from the qr code. It reads the id of the url using the get method and queries the database with that id read from the url.
•	Sign-up: this is a php file that displays a form for the user for signing up an account. The email accepted must end with “@conestogac.on.ca”.
•	Signuptest: this is a php file that validates the sign-in form and saves the users information into the temp_users table. It also sends a mail to the email address provided by the user.
•	Sign-in: this is a php file that displays a form to the user for signing in. 
•	Signintest: this is a php file that reads the sign-in form and queries the database if the email address and the password matches. If there is a match, the user would be able to make a post and view their profile.
•	UUID_creator: this is a php file that is used to create a random ID that is used to register guest for the chat functionality.
