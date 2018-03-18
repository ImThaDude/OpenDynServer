
# OpenDynServer
This is an ambitious project to create a hierarchy tree based framework. This framework will let users sync download P2P assets for big files and send UDP data for smaller things. Its a combination of P2P sharing technology with UDP update based interface. My main goal in this project is to create smaller instances of a Server-Client where the clients within that server can P2P transfer files to update the other clients. Likewise, the server will be able to connect to other servers in a P2P fashion through a signaling server that orders on top. Making it a less centralized server. The servers will sync data among the players and to other servers in which the main server has been signaled to communicate to. Likewise, in the future, servers will be able to execute server based logic by receiving the messages from the users. Then server to server will be able to communicate by reflecting the data with each other since the data has already been processed. The extensions will be separated in different ways. There will be, client-client plugins, client-server plugins, server-server plugins, client-main plugins, server-main plugins and they can be easily implemented on the framework through using DLLs to be added on top of the server. Clients will have their client-server, client-client, client-main plugins. Servers will have their server-server, server-client and server-main plugins. Main will have a main-sever and main-client and eventually support main-main to create a tree hierarchy. It will work in that principle and that structure.

Each plugin will have their own dependencies. However it breaks down where main has a manipulation over what dependencies have to exist within each host server and clients. Then host/sevrver can add their own plugins to have dependencies over clients. Clients can only customize themselves only in that fashion.

This creates a more powerful and decentralized and low latency system and approach for an MMORPG.

For server-server interaction.
Say there is a boss. Each server has its own instance of the boss. The servers will sync between state and will try to sync.
The can also negotiate which character is a bigger danger and evaluate between themselves who is the priority.

Quotations is the server communicating, non quotated is server logic.

Monster decision making
Server1
"I was just hit by this much damage by my people"
Server2
Ok, I dont have anybody that does more damage that that so my monster will hit towards him.
"I will attack your guy then"
Server1
Ok I will attack that guy.

Server1
"I was just hit by this much damage by my people"
Server2
Ok, My guy hit me with higher damage.
"No, my guy did more damage to me."
Server1
"Ok, lets attack your guy then"
Lets attack his guy.
Server2
Ok I will attack my guy.

This by itself will be implemented on the framework. It can use something similar to neural networks to finish the logic.
Of course if you loose connection, the AI by itself should be able to self compute.

Or there can be a sync state for both objects.

Create a sync for the AI and the damage where both will try their best to get the closest to both situations and send each other their discrepancies and their actions through a common sync script.

As of client rendering, clients will have to determine by themselves what gets rendered making it fully customizable.

Main can ask for all servers to download their applications and clients. It can be done selectively.

What can end up happening is that this framework can be on top. Therefore when a client or server is created they will download from the server by client and server plugins. All which are contained on this hierarchy.

This unifies the system. And of course there can be a lot of things that can be created with this easy to use framwork. This only creates the structure and a way to sync. The whole content of the game can be downloaded through those p2p services created from the cloud. This including the networking plugins and each can have their own connection. There can also be a creation of multiple channels with different ips through the use of dlls. This would make hierarchical connection really easy through plugins in the interface.

Ex. Server can be created and handled through a nodejs while clients can use unity and their own interfaces.

Each plugin can use the same main channel or create their own. Without the need of leaving the application. Each can also be handled individually standarizing and unyfying. The plugins can be applications that get from this api framework and receive and send messages. It will have a more plug and play type of feel. Maybe whole OSs can be created with this format.
