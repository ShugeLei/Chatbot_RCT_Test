## Chatbot_USC

## Steps to Run the chatbot on the Casy server:- 
1. connect to the Casy Server: 
   1.1 if on the school internet
   1.2 if not on the school internet, use Cisco AnyConnect VPN(or other VPN) first, then follow the same step as 1.1. 
2. run chatbots:
    2.1 we need four terminal windows to run two chatbots and two custom actions seperately; all the terminals need to follow step 1 to connect to the server first；
    2.2 run chatbot g0, go to g0 and run the command line: 
          nohup rasa run -m models --enable-api --cors "*" --endpoints endpoints.yml -p 5056 &
    2.3 go to g0, run actions in g0:
          nohup rasa run actions --port 9000 --debug &
    2.4 go to g1, run chatbot g1:
          nohup rasa run -m models --enable-api --cors "*" &
    2.5 go to g1, run the custom action:
          nohup rasa run actions &
3. put the link to a web window to the interface:
    http://casy.cse.sc.edu/chatbot_univ/
    
    
        
#nohup   &      # this is to keep the chatbot running on the server
#to kill the nohup: ps aux | grep rasa

// to check the running tasks:
    ps aux | grep python
//  to kill the task:

    sudo kill -9 35225

Steps to run chatbot on apache

g0_chatbot
1. screen -ls -> you will see list of all screens
2. screen -r g0_chatbot -> Attach to the screen.
3. Click ctrl-z to stop the running model
4. Run the model (rasa run -m models --enable-api --cors "*" --endpoints endpoints.yml -p 5063)
4. Detach the screen -> ctrl + a + d

actiong0
1. screen -ls -> you will see list of all screens
2. screen -r actiong0-> Attach to the screen.
3. Click ctrl-z to stop the running model
4. rasa run actions --port 5057 --debug
4. Detach the screen -> ctrl + a + d

chatbot_g1
1. screen -ls -> you will see list of all screens
2. screen -r chatbot_g1 -> Attach to the screen.
3. Click ctrl-z to stop the running model
4. Run the model (rasa run -m models --enable-api --cors "*" --endpoints endpoints.yml -p 5062)
5. Detach the screen -> ctrl + a + d



actiong1
1. screen -ls -> you will see list of all screens
2. screen -r actiong1-> Attach to the screen.
3. Click ctrl-z to stop the running model
4. rasa run actions --port 5058 --debug
4. Detach the screen -> ctrl + a + d



