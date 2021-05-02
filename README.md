# movie-booking-using-Flask
#### This project is Movie-booking Site based on  Python Flask using  some AWS services sych as RDS and Elastic Beanstalk for deployment.
#### If you clone it or to use it there are some important points to notice and some changes to be made.
#### The instructions to be followed are:-
    
   1. Inorder to run this you need to import all the libraries specified in 'requirements.txt' file.
      $ pip install -r requirements.txt
      Above command installs all the required libraries to run the project.
    2. Use 'wsgi.py' to run the project instead of 'application.py'.
    3. Network connection is needed in order to run the project.
    4. Html files are in /template folder and CSS & Js files,Images are in /static folder.
    5. We use flask-mail to send mail for otps and booking details , some code  must be changed inorder to send mail 
        * In 'application.py' change the value of '#sendermail' to sender email address.(line 14,48,104,196)
        * Change the value of '#sendermailpassword' to sender email password.(line 15)
        * The sender must enable 'less secure app access' in their gmail settings inorder to send mail.[Click here to enable](https://myaccount.google.com/lesssecureapps)
    6. We used AWS RDS service for database to our website. So it is preferable if you use your own database in your test as I am not providing any of my                 details.So inorder to establish database connection there are some changes to be made and some instructions to be followed.
        * First thing to do is if you don't know about AWS RDS [Click here to the official documentation](http://aws.amazon.com/documentation/rds)
        *Create a Mysql database instance if not exist.[Click here to create db instance](https://ap-south-1.console.aws.amazon.com/rds/home)
        * In 'application.py' file line 20 change the value of 'host=' to your database instance endpoint by replacing '#yourdatabaseinstance' with your endpoint.
        * And also change the values of 'user=' and 'password=' by admin credentials you used while creating database instance.
        * Use database editors such as 'sqlelectron' to edit your database  to create and edit your database tables etc.
        * The schemas and data for tables in database are shown as     
            Userdata:    

               | Field    | Type         | Null | Key  | Default | Extra |
               | :------: | :----------: | :--: | :--: | :-----: | :---: |
               | Name     | char(20)     | YES  |      | NULL    |       |
               | Email    | varchar(30)  | NO   | PRI  | NULL    |       |
               | Phone    | bigint       | YES  |      | NULL    |       |
               | Password | varchar(100) | YES  |      | NULL    |       |       

            movies:
            
               |Field | Type | Null | Key | Default | Extra|
               ----------------------------------------
               Moviename  varchar(30)  YES    NULL  
               Language  char(20)  YES    NULL  
               Description  varchar(5000)  YES    NULL  
               Imdb  float  YES    NULL  
               image  varchar(200)  YES    NULL  

            recommended_movies:
   
               Field  Type  Null  Key  Default  Extra
               ----------------------------------------
               Moviename  varchar(30)  YES    NULL  
               Language  char(20)  YES    NULL  
               Description  varchar(5000)  YES    NULL  
               Imdb  float  YES    NULL  
               image  varchar(200)  YES    NULL  

            booking:
              
               Field  Type  Null  Key  Default  Extra
               ---------------------------------------      
               Name  varchar(30)  YES    NULL  
               Email  varchar(30)  YES    NULL  
               Moviename  varchar(30)  YES    NULL  
               Theatre  varchar(30)  YES    NULL  
               Date  varchar(30)  YES    NULL  
               Timing  varchar(30)  YES    NULL  
               Number  int  YES    NULL  
               Seats  varchar(100)  YES    NULL  

   7. We used Fast2sms API for sending otp to phone.There are few changes to be made.
      * Create a Fast2sms account and use your authentication key to send otp from your account.For more information and to use this API [Click here.](https://docs.fast2sms.com/?python#post-method10)
      * In 'application.py' in line 66 replace '#yourauthorizationkey' with your Fast2sms authorization key.

#### After changes use ide such as 'Pycharm' for better visualization and interface.
#### Important thing:-
   1. Create database naming 'users' and create tables in those database.Use 'Sqlelectron' for this. This tool provide you interface to create tables and insert data into it.
   2. This project has some functionality limitations and some pages are still in progress, and we are trying hard to fix those things.


## -------------------------------Thank You-------------------------------------
