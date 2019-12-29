# flask-fb-bot
Basic Facebook bot using Flask and Python.

### What do you need to run this bot?
1. Sublime + Terminal
2. Heroku free account
3. Facebook account (to use Facebook Developer Center)
4. 30 min of your time

### Bot app
You can just clone the source code from this repo. Only few things you will need to change (Tokens Variables).
After copying current code, go to your Terminal, open the project folder and run the following command:

`$ pip install -r requirements.txt`

So now, you can run a flask app using terminal (in project folder):

`$ python app.py`

If all goes well, you might see a URL to the Flask App. To test it, copy and paste this link to the browser or just type:
http://localhost:5000

You will see an error: Invalid verification token. 

### Set up a Facebook Application
Go to: https://developers.facebook.com/apps
Create a new application with a random name. Next, when prompted on the next page for the type of product you are building, click the “Set Up” button on the Messenger option.

![Image of step_1](https://i.imgur.com/fhV34om.png)

