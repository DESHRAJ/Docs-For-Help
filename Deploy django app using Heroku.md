How to deploy django application using HerokuApp?

10 steps to follow and you will have your django app hosted  online : 

1. Signup on Heroku at https://signup.heroku.com/signup/dc

2. Login on Heroku at https://devcenter.heroku.com/login

3. Download the Heroku Toolbelt:
	A) If you are using Windows: 	

			https://s3.amazonaws.com/assets.heroku.com/heroku-toolbelt/heroku-toolbelt.exe

	B) If you are using Ubuntu, Run the command in the terminal(open terminal using Alt + Ctrl + T ):

			wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh

4. Once installed, you can use the heroku command from your command shell. Log in using the email address and password you used when creating your Heroku account.
Run this command to login in the shell :

			heroku login

5. Create a requirements.txt file in your project's root directory. Mention the requierments that you need to run you django app on Heroku Server.
For example, open the following link: https://github.com/DESHRAJ/Youtube-Downloader/blob/master/ytd/requirements.txt

6. If your project is not a git repository, then make it a Git repository by running this command in the root directory of your project: 

			git init 

6.a. create your first commit by running:

  			git add requirments.txt
  			git commit -m "Initial commit."
		
if you do not create first commit then later on running git push heroku master command you get following error:

			error:src refspec master does not match any
			error:failed to push some refs
			
You now have a functioning git repository that contains a simple application as well as a requirements.txt file, which is used by Python’s dependency manager, Pip.

7. then run the following command in the projects root directory : 
			
			heroku create yourAppName

(NOTE : The app name you will provide will be checked by heroku and if it is not used by anyother user, you will get you django app running at http://yourAppName.herokuapp.com ).

8. Finally, run the following command to deploy the application : 
			
			git push heroku master

9. To check if the django app has been hosted or not, run the following command: 

			heroku open

10. If you encounter any error in deploying you app, then see the logs using the command : 
			
			heroku logs --tail

and try to figure it out that where the error occured. If you encounter error in log then by googling the question, you can easily figure out what needs to be changed. Its pretty easy to deploy app using heroku. 
