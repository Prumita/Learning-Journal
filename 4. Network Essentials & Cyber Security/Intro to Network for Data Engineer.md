Tutor for this module: Peter Akanji

# Agenda

1. Basic Principles of Networks
2. IP Addresses
3. Binary and hexadecimal numbers - a Data Engineer has to be able to read those!
4. Modern networking practices

# Basic Principles of Networks

Common network devices are:

### Hub
Most organisations don't tend to use Hubs anymore because they are too open and too simple. For most replaced by Switch.

### Switch
Modern hub.

R### outer
We have this in our own house.

### Firewall
Stateful packet inspection

### VPN concentrator
VPN termination point

Some of these are physical devices, and sometimes you can find a physical device that has all of these. So our home internet router from Vodafone etc would tend to be all of these at once.

Usually in an organisation we separate them fo rmanagement, maintainence and so on.

### Switch
We use this to group devies together. In my home I'll have a mobiel hone, laptop, desktop etc. Home is like a unix? Unit? In order to service all those devices, need to connect them to a switch. Helps you distribute data from one device to another. So my virgin router is the switch that lets me connect to Virgin. He's the middle man that brings in the data and distributes it to everyone. Does it in an inteligent way. 
So reason why we can all access different things on our devices at the same time, is because the switch is supplying data to different devices on different channels. So my phone doesn't stop my laptop from working etc. 
Fancy term, collision domain.
You are a separeate entity, a domain. So switch makes sure each of the domains are okay.
So how does the switch enable this? With IP addresses! So it knows all of the devices IP addresses, so when the device requests dta, the switch knows where to send that data back to.
All devices in my home are a unit, it's kinda like one domain. So data comes from the web via the switch, so the switch distributes within one unit. 

### Router 
Imagine working from home. So work has its own network and you link to your workplace via the internet.
So I represent a network of my own, and my workplace represents a network of its own. 
Think of a network like a house, within a house, no problem, no permission. But with 2 different networks, that's 2 houses, you need permission. The internet is how you get between houses.
So the router helps you communicate between these houses. Switch helps communicate within the house.
The router uses a gateway. Gateway is like the front door to the houses, it gives access to those networks.

### Firewall
Literally a wall. Can have a firewall within the network. Definitely have firewall moving from one network to another. It's a way of ensuring what you allow is what you allow. Can configure what you want to allow. Do you want to allow the particular traffic? Firewalls can be configured differently to allow different things.

### VPN Concentrator
Come back to it later! He wants us to build a beautiful story.

### Networking models
How do we arrange our components to ensure they communicate? Two main ones:

Peer - to - peer
Client - server model.

#### Peer to peer
Used at home. All of the previously covered devices are spoken. Peer just means equal. We are together. Nobody controls anybody, but we share things, printer shares resources with the PC and so on. Important in peer to peer, there's no one device that is a controller. There is no centralised administration. No one determines when I should log in, no one determines when I should log out, how I should do it, no one is a controller.

|Advanges | Disadvantages|
|---|--|
|Easy ot set up| No centralised administration|
|Scalable| Not as secure|
|Lower cost| Limited reliability|
|Used for simple tasks: transferring files and sharing printers| Slower performance|

So this is not secure, there's no one in charge of who gets into here. So main reason for peer to peer is for exchange, it's for sharing. If I have 5 users, I don't have to attach a printer to each of them. Can have one printer and all will share the printer. I cannot control how much they print, how they print, no administration.

#### Client/Server

Client means, those who are using the environment. Might be devices, might be human, the ones that are being served.
Server means, the entity that provides the service. Whatever that service might be.  Common services include:

|Server Type| Description|
|--|--|
|Email|Email server runs email server software. Clients use client software to access email|
|Web|WEb server runs web server software. Clients use browser software to access web pages.|
|File|File server stores corporate and user files. The client devices access these files.|

So the server becomes the controller. Thinking a restaurant, the server there is in control of the table. A good restaurant will make sure that the server is empowered to serve the table very well. Not going all over the place, only have 3 tables that they are serving, but they are serving those 3 tables really well. Other tables are fighting? Not their business. Ensures what they are responsible are well taken care of. 

Security is the main reason for this, need to have control. 

## Network components

How to read topology, how to read a network map.

Wireless Router
Well we know what a router is, lets the networks talk to eachother. this one is wireless.

LAN Switch
Local Area Network. In your home you have your own LAN, can be small or big. Can have LAn with 5 devices, or 500. It's a switch, so it's managing and distributing data within that LAN.

Router
This would be a physical or cabled router. Not wireless, so connected physically by cable.

Multilayer Switch
Will look at this one more later on. Advanced set up for data engineering world.
It means it's a switch that coordinates LANs together. For multi-LAN apparently.

Firewall Appliance
There are different ways of establishing firewalls. Firewalls that are like devices. Like a lock.There are also firewalls that are software based. Different firewall, different way of thinking.

Not an architect, don't need to learn the complexity of the map.

Also need to be aware of connectors. 
So in topology:
Solid line: Cable
Dashed line: Wireless
There's not one type of cable. Cables are connectors but they are also medium.
Consider a cable or a medium. So think like our roads, they are roads, but we have single carriageway, dual carriageway and motorway. 
Type of cable that you use, whether you use copper, fibre optic (or even wireless connection), will depend on the amount of data to be conveyed within the network.

# IP Addresses

Sending data. So computers numbered 1 through 4 are sending to a switch, numbered 5. 
If 5 wanted to send to 1-4, we could send a broadcast. So for example, need to do an update, could warn everyone to save work before shutdown.
MAC Address is globally unique, it's the fingerprint of the card. MAC means Media Access Control.

IP address is the address the device has because it belongs to the network. If it is static, permanent, then the administrator has allocated that address and decides to give it to you permanently. If it is dynamic, then every time you come online you might have a fresh ip address, that is called dynamic.
Dynamic is more secure. So for example when you're staying in a building you always stay in the same room, vs every time you are in that building you change room, you're harder to find, so harder to hack.
Some devices are constant, part of working tools, so their ip addresses remain the same. When it comes to users, client etc, dynamic is preferred.

Switch has the detail of all the ip addresses that are connected to it. All data, we have the source address, and the destination address.

How does the computer figure it out?
Every device has an address in decimal. So it has the length of that address is 32 bits. Each of the sections is 8 bits.
We put the address on the device. When you put the devie on the network you insert the address there.
THe address we use is IPv4, for version 4. There is also v6, but v4 is what I'm used to seeing.
Total length is 32, but broken into 4 blocks. Each block is called an octet.
|8|8|8|8|
|-|-|-|-|

So you have about 5 classes of the address blocks.
|Class|Definition|First block values|Number of devices|
|-|-|-|-|
|A|1st block, network address. Last 3 blocks is host address|1-126|16,777,214|
|B|First 2 blocks, network address is. Last 2 blocks is what host will receive|128-191|65,534|
|C|First 3 blocks is the network, last 1 block is host|192-223|254|
|D| Mostly not used, for TV people? Multimedia people?|||
|E| Reserved (tutor hasn't said, but maybe htis is military, top secret stuff??)|||

Why is 127 skipped? it is reserved for something else.

So mostly in the organisation they take between A, B and C.

So how do we know what class of IP address is the typical device?
Following the above table, check the value of the first block in the ip address. e.g.
163.40.1.31 Class B (between 128-191)
102.1.1.5 Class A (between 1 and 126)
205.11.13.14 Class C (between 192-223)

So how do you choose the class? It depends how many devices you want on your network, so you pick the class that will give you the appropriate number of devices. Again above table shows the number of devices the various classes can support.

When you have an ip address you would usually put it in decimal. So when you say 192.168.1.1 that is decimal. In 4 blocks, separated by dots.
Need to know how to convert from decimal to binary. What is the binary representation of 192? What's the binary representation of 168? Of 1?

So let's do a little 8 block table:
So basically you get a number and you take the biggest you can from it every time, and put a 1 when you can:

So starting with 192, biggest umber to take from that is 128, so put a 1 there.
|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|1||||||||

192-128 leaves 64, so that can go in 64.

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|1|1|||||||

Leaves 0, so that's the binary for 192.

Try again, start with 203, again goes in 128.
|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|1||||||||

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|1||||||||
203-128 = 75. So that goes into 64 too.

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|1|1|||||||

75-64 = 11. So that's bigger than 8.

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|1|1|||1||||

11-8 = 3:
|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|1|1|||1||1||

3-2 = 1
|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|1|1|0|0|1|0|1|1|

And 1-1=0, so we have our final binary number.

Another way to express this is

1x2^7 + 1x2^6 + 0x2^5 + 0x2^4 + 1x2^3 + 0x2^2 + 1x2^1 + 1x2^0

So that becomes:
128 + 64 + 0 + 0 + 8 + 0 + 2 + 1

He's moved off the notes but I hope that's good.

Let's do another one.

107.10.1.5

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0||||||||
107 is smaller than 128, so 0 there.

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0|1|||||||

107 bigger than 64, so 1 there. 107-64 = 43
|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0|1|1||||||
43 is bigger than 32 so 1 there. 43 - 32 = 11

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0|1|1|0|||||

11 smaller than 16, so put 0.

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0|1|1|0|1||||

11 bigger than 8, so put 1. 11 - 8 = 3

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0|1|1|0|1|0|1|1|

Finishing up, 4 bigger so 0, 2 smaller than 3, so 1, 1 and 1, so 1.

So that's 107. Let's do 10.

|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0|0|0|0|1|0|1|0|

Now 1.
|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0|0|0|0|0|0|0|1|

Now 5.
|128|64|32|16|8|4|2|1|
|-|-|-|-|-|-|-|-|
|0|0|0|0|0|1|0|1|

So together we have

01101011.00001010.00000001.00000101
