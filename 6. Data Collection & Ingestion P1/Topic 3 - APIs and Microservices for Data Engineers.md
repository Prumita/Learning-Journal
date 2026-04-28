
We've already got a working world of APIs all around us. Today we're going to name the working parts associated with it. actually sounds cool.
At lloyds for instance, when you open the banking app:
- She had some serious problems with the banking app. Had to go in to the branch twice actually because of a problem on the app because they couldn't solve it via the phone.
- Also the dog is now on the camera. He is cute. We're now talking about a fussy dog when it comes to eating.

Okay cool moving on, gonna talk about Netflix.
### Netflix - one of the most cited examples of a microservice
Okay, you're watching a show. You want to see your previously viewed so you can continue watching something.
Maybe you recommended shows are working so well, top 10 in the UK right now is inaccurate.
Everything else is working fine, you can stream fine, search fine, click on it and it works.
Idea of how microservices work. So instead of you not being able to load a show, or their entire website being down, or it being stuck on buffering and the end product shows it's broken or not working. With Microservice, one of the components, like top UK watched, that alone will stop working. May not even realise that the service is having trouble.
So with Netflix, every service, content recommendation and so on. All of those are separate.

This allows netflix to:
- Scale individual services as needed
- Enables the deployment of updates without affecting the entire system
- Improves fault tolerance
- Enhances ability to handle high traffic volumes
- Provides a seamless user experience

  By the end of the session we should be able to talk to our colleagues and within our team about APIs? Also speak to why should we break up the monolith, should be able to answer that with specific evidence based reasons. Not just best practise.

Can you recall the key benefits of using microservices architectures?
How does it help with security? What are the benefits?
Faster deployment, independent teams can ship without affecting eachother.

What's the service mesh? It manages the service to service communication.
That's inside the microservice system. So let's say we've got serice discovery, load balancing, retry logic and mutual TLS encryption between services. The key distinction would be, the gateway handles external traffic coming in. The mesh handles internal traffic between services. Imagine a little world with all the cars, and the city and this is your internal world, the mesh handles the internal traffic. External traffic, the gateway, for the other cities, the other places outside of zootopia? Is that what she said? Yes, Zootopia. Zootopia has a service mesh in this idea.

Recap reveal, can you recall the key benefits of using microservieces architecutres?
Nah. Slide has gone, soz.

APIS at a glance! Sweet!

So, client app. There's an API call between the client app and a web server. The web server then directs the API call to the API handler, API handler then interacts with the database, to retrieve the processed data. Then that gets passed back along the change, database back to API handler, back to webserver, back to the client app that made the API call.

Client App <----> Web Server <-----> API <------> DB
Not gonna hand draw it, don't have that ability. 


Okay, APIs at a glance, the why. We now have a pizza version.
We've got a bit of talk about zones in here, not sure if that's official speak or not?
So left zone is the client app making the request, middle zone is the API handler that receives the request and takes it to the database.
Database is the right zone, and it processes the data and returns it.
Middle zone receives what's returned, hands it back to left zone.
This was on an analogy of a waiter etc. Not sure if the zone thing carries over into API life.
We're just flicking between API graphs.

Okay cool, what is a rest API?  

So got the client, goes to HTTP, which HTTP says something below it (Get, post, delete, put) ad then URL to the server. That server then returns a jeson to the client.
Don't totally ge tit? But it's similar to crud on databases apparently.

Post - Creates
Put - Updates
Delete - Removes
Get - Reads

APparently just like CRUD. Create, Read, Update, Delete? Guess that's what they mean.

So with OFGEM for instnace. Your usbmission intake for contractors receives post requests from suppliers. Or Leeds council, have a citizens app and they would send get requests to read planning data. They don't have write access. Get it and read it, but they can't write to make changes. What rest means, it means representational state trends. Let's focus on what it means in practise.
Going to start our practical application apparently when we return from the break! Dunno if I believe that.....
