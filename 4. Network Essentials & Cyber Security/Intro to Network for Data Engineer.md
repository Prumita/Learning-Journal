Tutor for this module: Peter Akanji

# Agenda

1. Basic Principles of Networks
2. IP Addresses
3. Binary and hexadecimal numbers - a Data Engineer has to be able to read those!
4. Modern networking practices

## Basic Principles of Networks

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

