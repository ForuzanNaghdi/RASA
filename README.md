### README Contents:
- [How to install](#how-to-install)
- [rasa run actions](#rasa_run_actions)
- [To run actions on a web widget](#To_run_actions_on_a_web_widget)

### How to install
```bash
pip3 install rasa==3.5.6
```

### rasa run actions
to run custom actions, run this command:
```bash
rasa run actions
```

### To run actions on a web widget
To run actions on a web widget:
* change `action endpoint` in `endpoints.yml` file to specify the URL where the custom actions server is running.
* Modify the `credentials.yml` file to include the socketio channel with the `webhook_url` parameter set to the URL where your widget is running.
then run this command:
```bash
rasa run -m models --enable-api --cors "*"
```
