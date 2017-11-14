## INSTRUCTION TEXT FOR WEBSITE

### FACEBOOK SETUP

1. Set up a facebook [page](https://www.facebook.com/pages/create/).

2. Go to the Facebook Developer’s Quickstart Page and click “Skip and Create App ID” at the top right. Then create a new Facebook App for your bot and give your app a name, category and contact email.
    
	![create-fb-app](https://blog.hartleybrody.com/wp-content/uploads/2016/06/create-fb-app-1024x604.png "")
    
    You’ll see your new App ID at the top right on the next page. Scroll down and click “Get Started” next to Messenger.
    
    ![setup-fb-messenger-app](https://blog.hartleybrody.com/wp-content/uploads/2016/06/setup-fb-messenger-app-1024x613.png "")


3. Now you’re in the Messenger settings for your Facebook App. There are a few things in here you’ll need to fill out in order to get your chatbot wired up to the Heroku endpoint we setup earlier.

	![setup-fb-messenger-app](https://blog.hartleybrody.com/wp-content/uploads/2016/06/page-access-token-generation-1024x346.png "")
    
    Using the Page you created earlier (or an existing Page), click through the auth flow and you’ll receive a Page Access Token for your app.
        
	Click on the Page Access Token to copy it to your clipboard. 
   
4. Paste the page access token into its field in the config.py file.

5. Head over to Messenger under products in you projects facebook developer page and click on settings. Navigate to the webhooks section, click on edit events and select messages and messaging_postbacks as shown below.
	
	![setup-fb-messenger-app](https://blog.hartleybrody.com/wp-content/uploads/2016/06/page-access-token-generation-1024x346.png "")


### NGROK SETUP

1. Download your desired bot template from the website


2. Dowload ngrok from their [page](https://ngrok.com/download).


3. On Linux or OSX you can unzip ngrok from a terminal with the following command. 

	```
	unzip /path/to/ngrok.zip

	```
	On Windows, just double click ngrok.zip.


4. Navigate to the folder containing the unzipped contents of ngrock and run it with the command ./ngrok . You should see something similar to the image below on your terminal.

	![ngrok](https://cdn-images-1.medium.com/max/1600/1*LtnvanCk2-ZVJY1kA0cMfQ.png "")


5. Copy and replace the facebook token and server url in the config.py file and replace FACEBOOK_TOKEN_HERE with the facebook page token selected as in the instructions above and SERVER_URL_HERE with the url displayed after running ngrok:

	```
	CONFIG = {
     'FACEBOOK_TOKEN': 'FACEBOOK_TOKEN_HERE',
     'VERIFY_TOKEN': 'my_verify_token',
     'SERVER_URL': 'SERVER_URL_HERE'
 	}

	```

6.
