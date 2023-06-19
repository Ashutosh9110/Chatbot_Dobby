

For the chatbot will be using Dialogflow which is Google product which is a chat bot building framework. Using this
we can easily make chatbots.

Architecture:

We will build our chatbot via dialogflow. The user will talk to the chatbot like what is the weather today or will
it rain today. This query which is asked from the chatbot in chatbot's parlance is called INTENT (Intents are mappings
between a user's queries and actions fulfilled by your software). From INTENT we
extract ENTITY. Eg: If a user asks will it rain today? Here the rain word is ENTITY. 2: If a user asks to convert 500
US $ into INR, then 500 US $ and INR are the ENTITY here.

BASICALLY, our chatbot extract entities from intent. FULFILMENT: This is the most important stage. Here we what we
does is that we make a python/flask app/api/website and this api is responsible for the conversion. after conversion
the api will send the result to the chatbot as reply. This is how this entire thing works.

User will connect with the chatbot --> we extract the intent from that--> From INTENT we will extract ENTITY -->
We will send those entities to our webapp --> WebApp will complete the required task and will return the result
to the chatbot and the chatbot will present the result as reply to the user.

In Dialogflow, every chatbot is called an agent.

What is Dialogflow?
It used to be a company called api.ai which google acquired and changed it's name to dailogflow. This company
gives you an NLU (natural language understanding) platform using which anyone can create chatbots easily without
training the model from scratch (this is the best part about dialogflow).

A Dialogflow agent is a virtual agent that handles concurrent conversations with your end-users. It is a natural
language understanding module that understands the nuances of human language. Dialogflow translates end-user text
or audio during a conversation to structured data that your apps and services can understand.

Are there other platforms/framework like this?

Yes, there are multiple platforms available... Amazon's aws lex, facebook's wit.ai, IBM 's watson


Training phrases: once you are done with giving similar phrases, the NLU of the dialogflow will start training
the chat with these phrases



We are able to send the json that we had in chatbot to our server (system). We will be extracting the parameter
from the json response that we have got from the chatbot.

Requests module  is used to hit urls