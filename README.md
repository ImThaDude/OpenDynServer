
# OpenDynServer
This is an ambitious project to create a hierarchy tree based framework. This framework will let users sync download P2P assets for big files and send UDP data for smaller things. Its a combination of P2P sharing technology with UDP update based interface. My main goal in this project is to create smaller instances of a Server-Client where the clients within that server can P2P transfer files to update the other clients. Likewise, the server will be able to connect to other servers in a P2P fashion through a signaling server that orders on top. Making it a less centralized server. The servers will sync data among the players and to other servers in which the main server has been signaled to communicate to. Likewise, in the future, servers will be able to execute server based logic by receiving the messages from the users. Then server to server will be able to communicate by reflecting the data with each other since the data has already been processed. The extensions will be separated in different ways. There will be, client-client plugins, client-server plugins, server-server plugins, client-main plugins, server-main plugins and they can be easily implemented on the framework through using DLLs to be added on top of the server. Clients will have their client-server, client-client, client-main plugins. Servers will have their server-server, server-client and server-main plugins. Main will have a main-sever and main-client and eventually support main-main to create a tree hierarchy. It will work in that principle and that structure.

Each plugin will have their own dependencies. However it breaks down where main has a manipulation over what dependencies have to exist within each host server and clients. Then host/sevrver can add their own plugins to have dependencies over clients. Clients can only customize themselves only in that fashion.

This creates a more powerful and decentralized and low latency system and approach for an MMORPG.

For server-server interaction.
Say there is a boss. Each server has its own instance of the boss. The servers will sync between state and will try to sync.
The can also negotiate which character is a bigger danger and evaluate between themselves who is the priority.

Quotations is the server communicating, non quotated is server logic.

Server1
"I was just hit by this much damage"
Server2
Ok, I dont have anybody that does more damage that that so my monster will hit towards him.
"I will attack your guy then"
Server1
Ok I will attack that guy.

