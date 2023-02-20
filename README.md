# Chatbot
Build Chat-bot using google dialog flow

# How to Build Basic Chatbot Without Coding and Deploy to Websites

Build best automated AI chat bot using Google Dialog flow
Introduction:
A chat-bot is , a robotic self learning and talking bot which imitate human conversation through text chats and voice commands (a good example being Siri or Amazon Alexa).

Different Chatbots:

1.Task Handling Chat-bot where you ask something and it execute that task in more easy manner For example if you ask to book a table at a restaurant ,or open website than it will perform the operation on your mobile,laptop and lands you at the page you ask ,order the pizza for you

2.A.I. based chat bots (learn over a period of time using Machine Learning techniques) — dialog flow is an example of that
  
  Chat bots are mostly used for businesses will only increase as time goes by.
   No programming prior experience is required because Google Dialogflow is the platform where all the Machine learning algorithm get trained in back-end


Google Dialogflow Working Diagram :
![](https://miro.medium.com/max/678/0*JSeiIVmCQWPNMA1O.png)


# OK Now ! Lets Build our First Chatbot
# Create a Dialogflow Agent
Agents are your number of chatbots you will create will show in agent section for different uses varies upon your applications
Go to the Dialogflow Console.
Sign-in, if your new to interface sign up using google login
Accept the terms and conditions and you will be in the console
Create an Agent. To create, click on the dropdown menu in the left pane in order to see “Create new agent”

![](https://miro.medium.com/max/877/0*MDIofQ8pATjuE2pP.png)

Call this “AppointmentScheduler”
Dialogflow creates a GCP project for you to access logs, cloud functions etc. You can select an existing project as well.
When you’re ready, click Create.
Dialogflow creates two default intents as a part of the agent.
Default Welcome intent helps greet your users
Default Fallback intent helps catch all the questions that your bot does not understand.
At this point, we have a functional bot that greets the users.

# Test the Agent!
On the right hand side of the Dialgflow console, you can see the testing panel that looks like this:

![](https://miro.medium.com/max/644/0*9zkKNS5ykdKQQIxf.png)

To test the agent, in the “Try it now” box type “Hi”. The agent should respond back with the default greeting defined in the “Default Welcome Intent”. This could be “Greetings! How can I assist?” You can also modify the response.

Now, if you try “set an appointment” it does not know what to do so it initiates the fallback intent. This is because we have not created any intent to catch that particular question!

# Intent creation-from here you start training about the Q&A
![](https://miro.medium.com/max/635/0*NrEgjoeFZ-qpeH3A.png)

# First step Create Intent
For this first of all click the intent, click on “Intent” within the “Agent” you can see on left of your side where you can see your agent name
then click on the “CREATE INTENT” button on the right. Name the intent as “Schedule Appointment”
![](https://miro.medium.com/max/1296/0*qi3JupDmTiBDfbDD.png)

Forgot about context and event functionality for now cause we are building basic conversational chatbot.
GO and click on “Add Training phrases” tab .Now here you can use your own custom training Q&A For demonstration we can use the following phrases for this. Try them out individually.
“Set an appointment on Wednesday at 2pm”
“Need an appointment for 4pm tomorrow”
“I would like to set an appointment for 3pm on Tuesday”
Now these are your training phrases assuming that how the person will ask questions to bot.
Select the time ie 3pm and date ie tommorow or it can be date like 23,34,10 hover it and select the part to triggered ie select 3pm it will color change and you will select enitity @sys.time similarly for data select the “tomorrow” and you will get the diffrent color and select it as @sys.date by this action system can learn that tommorw is for date ,3pm is for time i hopes you got the idea of entity in action
As you are putting these in, you will see “date” and “time” are automatically identified as system entities @sys.date and @sys.time.
![](https://miro.medium.com/max/1091/0*z8yhU-03ZZbnJF2_.png)


To make this functional we need to respond back to the user. Let’s add a response. Scroll down to the “Response section and actually click on “Add Response”. You could just say — “You are all set. See you then!” or you could make it more interesting and say “you are all set for $date at $time. See you then!” Dollar($) sign here helps you access the entity values.
![](https://miro.medium.com/max/1296/0*pCNIrO-fa_3Eh3Fy.png)

At this point you can click “Save” and test the agent with “set an appointment for 4pm on Thursday.” and as expected, you get the response with the right date and time.

# Slot Filling:

Now, try to test “set an appointment”, since that is not very specific and we have not currently handled that scenario, it should be handled by Fallback intent. To support this, we use something called Slot-filling.
Slot filling allows you to design a conversation flow for parameter value collection within a single intent.This is useful when an action can’t be completed without a specific set of parameter values. To learn more about slot-filling refer to this documentation.
Next, let’s set up Slot-filling.
Click on “Actions and Parameters”.
Make the entities as required and Dialogflow will make sure to ask for both date and time before it responds back.
For time add “what time would you like to come in”
For the date add “what date”. You can add other variants too.
When you’re finished, click Save.
Voila ! Test Your Chatbot!
Now its time for testing the chatbot, the Dialogflow should be set up (right side). Test it in the Try it now panel on the right by entering the following conversation:
User: “Hi”
User: “Set an appointment”
Chatbot response: “What date?”
User: “May 23”
Chatbot response: “What time would you like to come in?”
User: “10am”
Chatbot response: “you are all set for 2019–05–23 at 10:00:00. See you then!”
Finally Integration:
Enable One-Click Web Integration
Dialogflow provides many types of integration for your chatbot. Let’s take a look at a sample web user interface for the chatbot.
Click on Integrations in the Dialogflow left panel.

Enable the Web Demo integration by flipping the switch

![}(https://miro.medium.com/max/693/0*r70PGhGe1_5fppdz.png)

Click on the URL link to launch Web Demo
![](https://miro.medium.com/max/963/0*sWZmbZ3yLzt0ndG5.png)

Start using the chat user interface by typing in the Ask something… section! If you are using a Chrome browser, if you click the microphone icon and you can speak your questions to the chatbot. Start chatting with the chatbot using the following conversation:
Type “Hi” and hit Enter. The chatbot should respond as before.
Then enter/say “set an appointment for 4pm tomorrow”. The bot should respond back with the confirmation of the appointment.

Congratulation on you First Chatbot without any coding experience Google dialogflow is doing on its own . If you LIKE PLEASE SHARE AND COMMENT

Deployment on Website
Create Account on Kommunicate
Open link https://www.kommunicate.io
2. Now once you Login or Signup to your Kommunicate dashboard and navigate to towards . If you do not have an account, you can create one here. Locate the Dialogflow section and click on Integrate Bot.

![](https://miro.medium.com/max/1134/1*RJNGEO9LzrZ0tzUifV3saw.png)


Set up Dialogflow API Credentials
3.After clicking on the setting of your agent one popup box will open. You will be asked for Dialogflow credentials.You can get them by logging into your Dialogflow console.
4.Click on the Settings icon (gear icon on the left panel)and select V2 API as the preferred API version.and copy the Service account key in blue text

![](https://miro.medium.com/max/1242/1*AMif9SqftHwjiqyXiQ5fMQ.png)

# Link Dialogflow Bot into Kommunicate

5. Go back to Dialogflow settings screen of Kommunicate, feed in your credentials, then click on next to save and progress.
In the bot profile section that follows, you will be able to give your bot a name. The name will be visible to your customers whenever the bot interacts with them.

![](https://miro.medium.com/max/1221/1*EQRQV35Pe6DyBNP3DT0cwA.png)

To completely finalize the setup, save and proceed to the next steps. You can set up your bot profile and automatic chatbot to human handoff in the next steps.

![](https://miro.medium.com/max/1228/1*dpDcVJJcCG5JPsu-7GQUQA.png)


Now You can check your newly created bot in two places:
Dashboard →Bot Integration → Manage Bots: You can check all your integrated bots here
Dashboard → Bot Integration: Your Dialogflow icon should be green with the number of bots are you have successfully integrated.
The final step is to connect Dialogflow bot into your website. Before that, to use the bot in customer conversation, you need to assign all the incoming conversations to the bot. You can do that from the Conversation rules section under Settings.
Enable Assign new conversations to bot and select your newly configured bot from the Select a bot dropdown. Learn more about conversation rules here.

![](https://miro.medium.com/max/1273/0*0aqDAQ9BlDG4g7RL.png)

Navigate to Dashboard →Settings. Click on Install under the Configuration section
Copy the JavaScript code add it to your website code. The Kommunicate chat widget will appear and you can now see your bot live in action.
Now you can easily see the chatbot running live into your website

# For WordPress Chat bot integration please see the plugin and guide

I.Install header footer plugin in wordpress
II.Go to settings in Wordpress Dashboard — .>Insert Header And Footer
III.GO to kommunicate.io s— ->click on settings icon >Install TAB>copy java code
IV.Put javascript code from Kommunicate.io that you generated and paste that code in footer section Of wordpress

![](https://miro.medium.com/max/1229/1*TlrYF0GNm0zxkhYZ5g4bRw.png)

Click Save !
Finally CONGRATS you finally build chatbot by yourself

https://wordpress.org/plugins/chatbot/#description


