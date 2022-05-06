## Chatbot_USC

## Steps to Run the chatbot on the local server:- 

1. Create a new Conda environment.
2. Go to the project directory.
3. pip install rasa
4. rasa run -m models --enable-api --cors "*" --endpoints endpoints.yml -p 8001
5. rasa run actions --port 9000 --debug
6. Open the (index) html file in the project directory to connect to the chatbot UI.


#rasa run actions --port 9000 --debug
#nohup   &
#to kill the nohup: ps aux | grep rasa
#


