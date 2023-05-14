# RASA
a bot for shopping
This chatbot is able to communicate with the user and take their order.
to train the model run this command:
```bash
rasa train
```
then to run custom actions run this command:
```bash
rasa run actions
```
To run actions on a web widget , 
* change `action endpoint` in `endpoints.yml` file to specify the URL where the custom actions server is running.
* Modify the `credentials.yml` file to include the socketio channel with the `webhook_url` parameter set to the URL where your widget is running.
then run this command:
```bash
rasa run -m models --enable-api --cors "*"
```
