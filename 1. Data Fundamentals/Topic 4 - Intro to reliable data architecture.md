
So what would we do if there was a massive increase in data?
If you had AWS it is automated scaling.

Webinar Agenda
Design vs architecture diagrams and flow charts
Monolithic vs microservices and UML component diagrams
Creating architecture diagrams and applying lenses, layers and chunks

An architectural diagram shows you an entire system without showing you the individual components of that.
Think about designing a house. You don't draw the wall brick by brick, you just draw a wall.
Design diagram of each wall, might contain individual components.

ARchitectural diagram contains high level. Design diagram is the parts.

An architecture diagram
- Explains what you're building
- How stakeholders will interact with it
- The constraints of the system
- Is often drawn as layers

A design diagram
- Normally does not have stakeholders, constraints or layers
- Focuses on one part of the system and shows its building blocks

So thinking about the bits I've done in Powerpoint, I've done design diagrams. Well, a rudimentary version.
What Robbie has done, showing a single simple for the server kinda thing, those are more architectural diagrams.

Design focuses on How and Where, might not show the 'what' exactly because we're in nitty gritty, not high level.
Architecture focuses on Where and What but not the details of 'How'
The lecturer thinks these are wrong but I feel like that makes sense to me?

Example diagram hopefully:
![Architecture Diagram](https://raw.githubusercontent.com/Prumita/Learning-Journal/main/1.4.ArchitectureDiagram.png)

and some basic flowcharts here:
![Flowchart icons Diagram](https://github.com/Prumita/Learning-Journal/blob/main/Screenshots/1.4.Flowchart_Symbols.png)


# Misuse deployment system
- This identifies security threats in data architecture
- Shows how attackers exploit weaknesses
- Includes servers, databases, networks and controls
- Aids in proactive risk mitigation
- Ensures data protection and system integrity

  SQL injection? Sending a massive amount of requests which could crash or bring down the system. So interesting, we know that things can do big locks and so on. But we don't do anything about it. For example kill people doing labour intensive tasks or something.

  Captcha is that typical thing to select the zebra crossing and so on or click a box to say I'm not a robot. But AI is making discoveries on how to get through the system so they're needing to come up with new methods of verifying people as human.


  UML Diagram types

  System component diagrams
  How do they work?

  It's another architectural diagram, high level.
  Funky little icons that look like books, or binders with 2 big rings.
  Got a library example and a bank example.
  Not sure what makes these special or what the goal is?
  Shows how the different components interact with eachother. A component can be anything from a book to a transaction or a fee
Component is a working independent application.
e.g. Pipeline will be a component of the entire data architecture.
So there are examples in boxes like Controller, service, DAO, MySQL. But on a previous one with a library example there was fee, transaction, book. So these are...independent? I guess they could be APIs. it's a microservice that charges a fee? Something like that?

Tips for diagrams
- Version Control your diagrams, they will evolve
- Simplify when possible
- Create logical groupings using polygons and colours
- Complement diagrams with descriptions
- Avoid too many acronyms
- You will normally have to explain the symbols you use

# lenses layers and chunks
so I think they mean drawing around different chunks of the diagram to try and split things out and group things up.
Example has a layer and then the structure has changed because 2 layers have become one in effect. Or something,

## Other diagrams!
Data architecure diagram
Application architecture diagram
Integration architecture diagram
DevOps architecture diagram
Deployment architecture diagram

### Integration architecture diagram
so I think there's a lens on a couple of bits here, API Management and Workflow and orchestration.
I think the layer might be backend systems? Not sure
![Integration Diagram](https://github.com/Prumita/Learning-Journal/blob/main/Screenshots/1.4.Integration_architecture_diagram.png)


### Deployment architecture diagram
![Deployment Diagram](https://github.com/Prumita/Learning-Journal/blob/main/Screenshots/1.4.Deployment_architecture_diagram.png)

Shows gitHub, Jenkins, sending to Kubernetes I think, then of to Docker.
Not sure, bit confused in the middle there.


### Data architecture diagram
So most similar to what we do at the minute, like something Robbie would do. High level of where data comes from and goes to.

# Data Mesh
Data Mesh is the concept of where data is managed centrally. Removes central management of data within organization. Allows each unit within an organization to manage their own data. Domain driven. e.g. finance, production, logistics. 
Why is the data mesh philosophy, why is it being pushed rather than ahving the data managed centrally? 

So everything in this diagram isgoing between everything else which is interesting.
Good discussion over this vs data silo. Basically it's similar to a data silo but the idea is that actually things are on a shared system, so for example GCP, and sharing would be possible/easy if needed. So aligned in terms of accessibility, but separate areas are experts of those areas.
Silos, might be on completely different systems, might just be impossible or extremely difficult to share between areas.



