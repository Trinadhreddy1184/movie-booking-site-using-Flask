# movie-booking-using-Flask
This project is Movie-booking Site based on  Python Flask using  some AWS services sych as RDS and Elastic Beanstalk for deployment.
If you clone it or to use it there are some important points to notice and some changes to be made.
The instructions to be followed are:-
  ->Inorder to run this you need to import all the libraries specified in 'requirements.txt' file.
      $ pip install -r requirements.txt
    Above command installs all the required libraries to run the project.
  ->Use 'wsgi.py' to run the project instead of 'application.py'.
  ->Network connection is needed in order to run the project.
  ->Html files are in /template folder and CSS & Js files are in /static folder.
  ->We use flask-mail to send mail for otps and booking details , some code  must be changed inorder to send mail 
    1.In 'application.py' 
