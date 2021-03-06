# Build a database-driven Slackbot with IBM Watson™ Assistant (Conversation)
Code to build a Slackbot to create and search Db2 database entries for events and conferences. The Slackbot is backed by the IBM Watson Assistant (Conversation) service. We integrate Slack and Assistant using the [Botkit middleware](https://github.com/watson-developer-cloud/botkit-middleware). 

The tutorial with detailed step-by-step instructions is available at https://console.bluemix.net/docs/tutorials/slack-chatbot-database-watson.html. The tutorial is part of the [IBM Cloud tutorials](https://console.bluemix.net/docs/tutorials/index.html) 

# Files in this repository
The files in this repository have the following purpose:
* [cleanup.sh](cleanup.sh): shell script to drop Db2 table and delete Db2-related Cloud Functions actions
* [conversation-workspace.json](conversation-workspace.json): Workspace file used with IBM Watson Assistant service
* [create-services.sh](create-services.sh): shell script which can be used to create Db2 Warehouse and Assistant services
* [db2-setup.js](db2-setup.js): code for Cloud Functions action which creates a Db2 table, fills it with sample data or cleans it up
* [eventFetch.js](eventFetch.js): code for Cloud Functions action which searches event data by identifier
* [eventFetchDate.js](eventFetchDate.js): code for Cloud Functions action which searches event data by dates
* [eventInsert.js](eventInsert.js): code for Cloud Functions action to insert a new record into a Db2 database
* [setup.sh](setup.sh): shell script to set up Cloud Functions actions, bind credentials, create a Db2 table and fill sample data
* [tables.sql](tables.sql): table schema

The directory [botkit-app](botkit-app) contains the code for the Node.js app based on Botkit. See the tutorial for instructions to deploy it to Cloud Foundry. You can also test and use it locally.

# Related Content
Chatbot-related blog posts:
* [Chatbots: Some tricks with slots in IBM Watson Conversation](https://www.ibm.com/blogs/bluemix/2018/02/chatbots-some-tricks-with-slots-in-ibm-watson-conversation/)
* [Lively chatbots: Best Practices](https://www.ibm.com/blogs/bluemix/2017/07/lively-chatbots-best-practices/)
* [Building chatbots: more tipcs and tricks](https://www.ibm.com/blogs/bluemix/2017/06/building-chatbots-tips-tricks/)

