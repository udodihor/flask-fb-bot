# flask-fb-bot
Basic Facebook bot (chats with you using random phrases) using Flask and Python.
You can start with this bot as a basic staff to build something more difficult and useful.

### What do you need to run this bot?
1. Sublime + Terminal
2. Heroku free account and Heroku CLI
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
#### Create app
Go to: https://developers.facebook.com/apps
Create a new application with a random name. Next, when prompted on the next page for the type of product you are building, click the “Set Up” button on the Messenger option.

![Image of step_1](https://i.imgur.com/fhV34om.png)

#### Generate Access token
After you were redirected on the Settings page, you need to select or create a specific Facebook Page (Public ommunity or other) to assign to your bot.

![Image of Step_2](https://i.imgur.com/4dWhMMD.png)

![Image of Step_3](https://i.imgur.com/qns9PZ6.png)

Now, you need to Generate Token for your app and actually paste this FB token to your application in `app.py` find `ACCESS_TOKEN = 'GENERATED_TOKEN_FROM_FACEBOOK'` and change value with your generated token.

Next, in the `VERIFY_TOKEN` value put any variable you want. To protect your bot, Facebook requires you to have a verify token. When a user messages your bot, Facebook will send your bot the message along with this verify token for your Flask app to check and verify the message is an authentic request sent by Facebook. Choose a string you want to use for your verify token and replace the placeholder in the app.py file with your code (ex. “TESTINGTOKEN” could be your verify token, but I’d recommend something harder for someone to guess) and place the same token (minus the quotation marks) in the Verify Token field.

### Create a Heroku account
Register on [Heroku](https://heroku.com). It's free.

### Setup Heroku CLI
Go to your terminal, and paste follwing command:

`$ brew tap heroku/brew && brew install heroku`
or

download and install automatically [here](https://cli-assets.heroku.com/heroku.pkg).

After Heroku CLI successfully installed, we could create our first application! :clap:


#### Set up Webhook
