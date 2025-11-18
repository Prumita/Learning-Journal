### NoSQL (Not Only SQL)
This is awesome for me, I always thought it was literally No SQL. I mean, that's what it sounds like. Why do they name things in such a misleading fashion?
Oh well, so yeah, it's for semi-structured and un-structured data. But frm that eventually you might be generating some structured data you want to do deep analysis on, so there's still a place for SQL!

So we're seeing a json reminder here, wonder if I can put it in a code block...but for nwo let's write it out
```
  {
    "doorsWindows": [
      {
        "ID": "A",
        "style": "roller",
        "height": 3,
        "width": 3,
        "wall": "front",
        "bay": 2,
        "location": [0.3,0],
        "dimensions": false
      },
      {
        "ID": "B",
        "style": "zincPA",
        "height": 0.9,
        "openingSide": "out",
        "hingePost": "right",
        "wall": "intWall_1",
        "bay": 4,
        "location": [4,0],
        "dimensions": false
        }
      ]
    }
```

{ = Curly brackets indicate storage of information in key value pairing. Square backets are a list of items grouped together.
[ = square or brace bracket
( = round bracket.

So can see here how A and B are structured slightly differently. Relational database would require these to have lots of individual columns with nulls to hold all the options. As we can see above, can just hold custom key value pairs for each doorsWindows entity.

Going back to SQL we're saying that a relational database is not called because of the relationships between the tables but because the tables themselves are relations? Or something? 

So NoSQL databases are typically
- Non-relational
- Open source
- cluster friendly
- built from the ground-up to handle 21st centrury data challanges
- schema-less

MongoDB apparently can now join but it's not optimised to do so.

### The business benefits of NoSQL
X cut infrastructure costs by $140 million annually after switching from MySQL database to Apache Cassandra 

LinkedIn reduced query latency from hours to seconds and lowered costs by 80% by adopting Voldemort, a noSQL key-value store for their platform.

Airbnb was able to achieve - something. MongDB. Missed it.

So trying to move away from the tabular side of things. If stuff comes through and it would be hard to fit into a table, what can we do then?
We're a reporting project, so I guess we aren't necessarily the people that are going to be looking at storing this? We would be the SQL that comes out the back of it I guess.
Key Value - Redis
Document based - MongoDB
Column based - Apache Cassandra
Graph Based neofj

Key-value. Very very quick returns. Things are often held in cache. Want to pull from your phone, banking information, want certain information to be readily available, want to pull new things through and keep things in memory that aren't as new. Hold in memory and pull through new information.

Document based takes that same style, and then stores that information in a grouping or a set, known as a 'document'. Like an individual observation. So in the earlier example of doors and windows, I think those are 2 documents...or maybe 1, not sure.

Column based is the nearest looking thing to a table. Table with columns and rows. Row is the information line that is turned, attributes related to are the columns. Rather than say

Idea with a graph, have nodes, points of interest. Restaurant, person, city. Person going to a restaurant might have an interaction, so like review, or rating. Restaurant might be related to a city because they are located in said city. Apparently it's wild, very different way of working. Really simplified, think of a graph itself, if you're travelling somewhere. If you were driving around, points of interest are places we want to go, the roads that connect them, then have to break that down further, so maybe there's multiple roads, and at each junction you might have to go left or right or straight on. 
Very conceptually, facebook. Two people on facebook who aren't friends, no line between them. If they are friends, they have a line.
Graph databases is complicated, amount of information can be vast. GEnerative AI can be powerful but difficult to get your head around.
Without good data underneath it becomes very useless.

### Drawbacks

Merging is difficult. Not optimised for merging. NoSQL can work horizontally across distributed clusters. If you need to join one record to another and they exist on different clusters,  you then need to get them to the same place to join them. Becomes very difficult to manage.
Not normally stored in a normalised way. 

### Redis

popular in-memory key-value database.

Can be viewed as a sort of dictionary. 
There's a key, and a value. Value can be strings, lists, sets. Not sure if it can be images etc?
Makes reading and writing extremely fast  because it's stored in RAM. But therefore can only have a limited amount of data.
Idea is data can also be written to disc frequently.

Kinda confused honestly.

So an example. an application with different user sessions using that application. Each of the different sessions are cached, the disk storage exists and redis sits between the user and the storage. The sessions are in redis, in RAM, nice and quick. And then changes can be pushed to disc.
So when is that useful? FOr very fast read and write, for very simple data. Integrity is important but not critical.
So maybe ConnectView, fast retrieval of metrics? 

### Column-based NoSQL databases
I think I spent a while trying to figure these out. MEtadata is really key for these. 
I don't fully understand, but example shows where not every column has a value for a given partition (or kinda like a row). So because it's stored by columns you won't get a blank column back, thre just isn't a column value for that particular partition. What I find so crazy about column storing is that they still visualise it the same and have to work overtime to make clear why it's not the same. just weird.
Effective for sparse data management though, which I can kind of see I guess. 
Not great at joining, but better than other NoSQL options.

### Graph databases.
Finding all friends of my friends is a hard task in RDMBS (recursive CTE?)
But apparently graphs are great at sorting that.
Kinda reminds me of the algorithm thngs I did in Uni, but I guess it's not actually like that at all.
Got nodes, and relationships between those nodes.
Can be used for recommendation systems. So think in a classic table, if you wanted to join customers to products to try and find out which customers are buying what and what else have htey bought, but with a graph database that would be great, just links between customers and the products they bought and nothing else. So then you could see that 100 customers but item 1 and 75 of them also bought item 2, so maybe the other 25 want item 2 and just don't know about it yet.
He's mentioned maps twice, so I wonder if Waze, google maps etc actually use these to find out how to go places? Not sure. I mean that really is the algorithm thing I used to do.

### MongoDB

What is a document?
It is like an observation, like a row in a classic table, instead here is a document. It's a NoSQL equivalent of a row.
We then call a collection, a grouping of documents, so kinda like your table.
It is not a word document, a pdf, or anything like that. It's like the JSON above. 

So why use it?
Great if the schema is unclear. Potentially changing schemas, or we don't know that they'll change.
Great if you just want to search for one specific record.
Not so great if you want to do complicated queries, aggregations etc.
Terminology

|SQL|No SQL|
|------|---------|
|Database|Database|
|Table|Collection|
|Row|Document|
|Column|Field|
|Index|Index|

Max document size of 16MB. 

Uses binary JSON. It's slightly different to JSON. Exactly the same structure as JSON. Saved in a computer readable format. Enhances the speed. Means more data types can be stored. Includes length prefixs which can help with the searching of particular terms. Slightly larger than JSON Files due to extra metadata but performance gains make it worthwhile.

|SQL Statement|MongoDB Commands|
|---|---|
|Select * from Table|db.collection.find()|
|Select * from Table where artist = 'Nirvana'|db.collection.find({Artist:"Nirvana"})|
|Select * from table order by Title|db.collection.find().sort(Title:1)|
|distinct|.distinct()|
|group by|.group()|

And a last one I missed.

Some example code:
```
db.users.find({'last_name': 'Smith'})
// retrieve ssn field for documents where last_name == 'Smith':
```

And missed the rest of that.
Let's just have a go!


