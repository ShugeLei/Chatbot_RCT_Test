## Chatbot_USC

## Steps to Run the chatbot on the Casy server:- 
1. connect to the Casy Server: 
   1.1 if on the school internet, use the command line: 
         ssh -p222 student-user@casy.cse.sc.edu 
         PWD: passw0rd!
         then go to the directory: demos/chatbot_univ/
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
3. put the link to an web window to the interface:
    http://casy.cse.sc.edu/chatbot_univ/
    
    
        
#nohup   &      # this is to keep the chatbot running on the server
#to kill the nohup: ps aux | grep rasa


