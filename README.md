# Flask Facebook chat-bot
Basic Facebook bot (will chat with you using random phrases you set up) using Flask and Python.
You can start with this bot as a basic app to build something more difficult and useful.

### What do you need to run this bot?
1. Sublime + Terminal
2. Heroku free account and Heroku CLI
3. Facebook account (to use Facebook Developer Center)
4. 30 min of your time

### Bot app
You can just clone a source code from this repo. Only few things you will need to change (Token Variables).
After copying current code, go to your Terminal, open the project folder and run the following command:

`$ pip install -r requirements.txt`

So now, you can run a flask app using terminal (in project folder):

`$ python app.py`

If all goes well, you might see a URL to the Flask App. To test it, copy and paste this link to the browser or just type:
http://localhost:5000

You will see an error: Invalid verification token. 

### 1. Set up a Facebook Application
#### 1.1. Create app
Go to: https://developers.facebook.com/apps
Create a new application with a random name. Next, when prompted on the next page for the type of product you are building, click the “Set Up” button on the Messenger option.

![Image of step_1](https://i.imgur.com/fhV34om.png)

#### 1.2. Generate Access token
After you were redirected on the Settings page, you need to select or create a specific Facebook Page (Public community or other) to assign to your bot.

![Image of Step_2](https://i.imgur.com/4dWhMMD.png)

![Image of Step_3](https://i.imgur.com/qns9PZ6.png)

Now, you need to Generate Token for your app and actually paste this FB token to your application in `app.py` find `ACCESS_TOKEN = 'GENERATED_TOKEN_FROM_FACEBOOK'` and change value with your generated token.

#### 1.3. Create Verify Token
Next, in the `VERIFY_TOKEN` value put any variable you want. To protect your bot, Facebook requires you to have a verify token. When a user messages your bot, Facebook will send your bot the message along with this verify token for your Flask app to check and verify the message is an authentic request sent by Facebook. Choose a string you want to use for your verify token and replace the placeholder in the app.py file with your code (ex. “TESTINGTOKEN” could be your verify token, but I’d recommend something harder for someone to guess) and place the same token (minus the quotation marks) in the Verify Token field.

### 2. Create a Heroku account
Register on [Heroku](https://heroku.com). It's free.

### 3. Setup Heroku CLI
Go to your terminal, and paste following command:

`$ brew tap heroku/brew && brew install heroku`

or

download and install automatically [here](https://cli-assets.heroku.com/heroku.pkg).

After Heroku CLI is successfully installed, we could create our first heroku application! :clap:

### 4. Heroku app creation
In your terminal, run next command:

`$ heroku login` and push any button.

You'll be redirected to default browser app and asked for login to your heroku account. After successful login, go back to your terminal window. Now you're logged in.
To create new app, run command:

`$ heroku create`

If all goes well, you will see something similar to:
![Image for step_5](https://i.imgur.com/yUb1Gyp.png)

Heroku will automatically create a new application instance in your account. After creation, you will see a git URL to your heroku app (we will deploy our bot there).

Finally, to deploy the app, paste next command in your terminal:

`$ git push heroku master`

##### :warning: NOTE: If you cloned this repo, it will work fine. If you just downloaded the files from GitHub, you will need to initiate git repo, and create first commit and only then start to push your code to heroku: 

`$ git init.`

`$ git add -A && git commint -m "First commit"`

After that, copy the URL of your heroku web-app you previously created. You can check it in your heroku account (go into the created application, and find an "Open" button). 

### 5. Set up Webhook
In Facebook Developer Center, in your Messenger settings, add a Callback URL to Webhooks section:
![Image of step_6](https://i.imgur.com/X9g2NdM.png)

Here, you will need to paste URL to your heroku app (we copied it in previous step), and into another field put the value (VERIFY_TOKEN = YOUR_CREATED_VALUE) you've created in step 1.3. 

If you've did all right, Facebook will test this callback and add this to the app. After that, for the subscription fields, be sure to check the messages, messaging_postbacks, message_deliveries, messaging_pre_checkouts boxes:
![Image of Step_7](https://i.imgur.com/KQ32ztw.png)

So, it was a final step. Go to your messages in Facebook, create a new message and send it to previously created community/group. 

![Image of final](https://i.imgur.com/eZ1fytL.png)

Enjoy & Thank you! :clap: :raised_hands:

Alternative deployment, using ngrok is [here](https://www.twilio.com/blog/2017/12/facebook-messenger-bot-python.html)

Feel free to ask me here or on [reddit](https://www.reddit.com/user/ssb_beast)