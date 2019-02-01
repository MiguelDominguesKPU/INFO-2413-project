# INFO-2413-project
client-server poker game implemented in Java using the MVC paradigm. 

Implemented skills:
  - client-server communication using the java TCP-IP API
  - how to wrap and unwrap data for transport across a network
  - multi-threaded programming and synchronization
  - heavy OOP programming practicing dynamic binding, encapsulation, and interfaces
  - implemented using an MVC design pattern, with clients and server-threads having one of multiple States

User starts the client, enters the correct server IP address, and connects to the server with a unique user name

Upon successful connection users are put into the main lobby, where they can: 
  - join hosted games that are waiting for players
  - host a game
  - spectate games in progress
  - chat with other users in the main lobby
  
  The poker game is texas-hold'em for 2 to 4 players. When a player runs out of money, they can continue to spectate that game or 
  return to the main lobby. 
  
  When there is only one player left in a game, the game concludes and all users are returned to the main lobby.
  
  Server maintains client threads and handles inbound/outbound client communication across all the main Models: The main lobby,
  a hosted game waiting for players, and a running game. 
  
  Each client thread on the server has a state which acts as the Controller. The Controller interprets client messages to update the Model
  and change state if nessesary.
  
  Client sends user input to the server, and handles server input by updating the View/GUI appropriatley. 
