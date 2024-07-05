this is a practice application for the youtube video
https://www.youtube.com/watch?v=Z1RJmh_OqeA

** read it for clarification **

@CreativGaming
1 year ago (edited)
Hello all. I figured out why this doesn't work. SQL alchemy has been updated since this video Tutorial. The problem is nobody explains it properly, but I will give you a quick fix. Instead of Running the db.create_all() command in the terminal Initialize the Database in your code after your Database Models classes have been setup:

`with app.app_context():

        db.create_all()

`

Basically, put this in your Flask app under the Db.Model classes. Make sure to indent properly and run your flask app one time. It should create the database (also check your instance folder for the db file). Then comment it out. You can run other SQL commands under the with statement if you need info on what's in your database file.
102
@mohitvashisht9259
1 year ago
This is not working for me. Can you share your code please. Thanks!
@CreativGaming
1 year ago
 @mohitvashisht9259  What error message are you getting?
@mohitvashisht9259
1 year ago
The database file is not creating while running the app.py file
@CreativGaming
1 year ago (edited)
 @mohitvashisht9259  Yes, but what error message are you getting in the terminal when you run the app.py file?
@mohitvashisht9259
1 year ago
 @CreativGaming  No error in itself, it is executing and giving no error but my database file is not created, as shown here.
@rogerchan548
1 year ago
I find it useful to just type it in the terminal. It creatd the datebase under the instance folder
@CreativGaming
1 year ago (edited)
 @mohitvashisht9259  I think I know why you were having this issue. If you run the file and didn't get an error, odds are the database file was created in the instance folder. Turns out in flask when the file is created a copy of that file is sent to the instance folder. They is where python looks for it in.
6
@tech-n-data
1 year ago (edited)
 @CreativGaming  Thank you!!!!!!!!!!
@p_deges
1 year ago
thank you for the info :)
@Coff33_Break
1 year ago
thank you so much @Creativematrix1 that actually worked 
