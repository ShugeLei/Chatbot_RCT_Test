Steps to run chatbot on apache

g0_chatbot
1. screen -ls -> you will see list of all screens
2. screen -r g0_chatbot -> Attach to the screen.
3. Click ctrl-z to stop the running model
4. Run the model (rasa run -m models --enable-api --cors "*" --endpoints endpoints.yml -p 5061)
5. Detach the screen -> ctrl + a + d

actiong0
1. screen -ls -> you will see list of all screens
2. screen -r actiong0-> Attach to the screen.
3. Click ctrl-z to stop the running model
4. rasa run actions --port 5057 --debug
5. Detach the screen -> ctrl + a + d

chatbot_g1
1. screen -ls -> you will see list of all screens
2. screen -r chatbot_g1 -> Attach to the screen.
3. Click ctrl-z to stop the running model
4. Run the model (rasa run -m models --enable-api --cors "*" --endpoints endpoints.yml -p 5062 ）
5. Detach the screen -> ctrl + a + d



actiong1
1. screen -ls -> you will see list of all screens
2. screen -r actiong1-> Attach to the screen.
3. Click ctrl-z to stop the running model
4. rasa run actions --port 5060 --debug
4. Detach the screen -> ctrl + a + d
