#Definitions:

Node: A individual node from withn a NodeRED Flow

Flow: A collection of nodes

HockEOS: The specific flow for this solution



#Data Flow:

1) User sends /nhl/get/team=XXX to HockEOS incoming UDP Node, where XXX is the three letter code of an NHL team.

2) HockEOS Incoming UDP node passes data to OSC node, which returns the three digit code

3) The three digit code passes through a switch node to determine which team ID# it corresponds to (number is neede for API Call)

4) EOS Screen is Updated / Old values are cleared

5) ID is put into the API URL and a call is initiated to the NHL API

6) NHL API returns details about the next game for that particular team, and sets a number of variables used throughout

7) A "Game ID" variable from step 6 is passed into another API URL, and then a call is initiated every X seconds (currently 5, but eventually user-definable)

8) Live game data comes back from the NHL, all kinds of variables are sets

9) Some calculations are made for power play status and other Things

10) Data from variables is converted to OSC messages

11) OSC messages are sent to Eos

12) Magic Sheet objects of type "command" are updated as needed
