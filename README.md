# RASA shopping bot
This is a shopping chatbot based on the RASA platform. The chatbot is capable of communicating with users and taking their orders. To train the model, run this command:
```bash
rasa train
```
Then, to run custom actions, run this command:
```bash
rasa run actions
```
To run actions on a web widget:
* change `action endpoint` in `endpoints.yml` file to specify the URL where the custom actions server is running.
* Modify the `credentials.yml` file to include the socketio channel with the `webhook_url` parameter set to the URL where your widget is running.
then run this command:
```bash
rasa run -m models --enable-api --cors "*"
```
# API
After making the rest input channel available, you can POST messages to `http://<host>:<port>/webhooks/rest/webhook`, with the following format:
```bash
{
  "sender": "test_user",  // sender ID of the user sending the message
  "message": "سلام" // message
}
```
