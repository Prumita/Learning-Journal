Going to really try and reenage my focus today!!
Module 6 of 12, topic 2 of 4.
Like...literally half way through? Nice!
Learned what the difference is between collection and ingestion

so, let's dive into some complexity.
Lloyds, we have dozens of different files, different times, different formats, different qualities. That's what heterogeneous means, it means the reality of the messy, coming from all over.


We had an icebreaker, chatting about what ETL would we do in our personal life.

Chatting through an example, a cataologing problem. Got a report called V3 final, that's not good naming is it.

AirBnB case study
They are huge, lots of processes, including
user interactions
booking details
property listings
employs metadata management to ensure data quality and compliance

impact
Provides personalised user experiences
optimises seach results
maintsin high data quality standards
crucial for business operations

What would be batch, what would be real time?
Gave an example of bookings with AirBnB would need to be real time so there aren't clashes.

Then chatted about what would data be of just somebody looking at a page, not clicking on it. I wasn't sure and said metadata, but realised after that wasn't really right, as it is genuinely data, not data about data.
So instead someone said customer behaviour, and yeah that's spot on.

Benefit of an ETL, what's the primary benfit? Answer:
It ensures data is cleaned and transformed before loading into the data warehouse.

### Session aim and objectives
Completion of this topic supports the following outcomes:

Oh darn, missed it. But we're going to do an AWS lab that includes Glue and what not.

She's maybe about to recap from e-learning, which I raced through a bit.

Summary of elearning:

2 main ways, batch and stream processing.
Batch processing is in bulk at scheduled intervals, while rea`l-time processing handles data as it arrives.

Designing ingestion solutions
Key parameters for designing a data ingestion solution include data formats, volumes, velocity, frequency of ingestion and security.

## Intricacies of heterogeneous data ingestion
So far, we have discussed the following aspects of data ingestion:

- Data wrangling and cleaning
- Data structuring
- Data validation

  However, there is more to heterogeneous data ingestion, and we will now discuss:
  - ETL, ELT and Reverse ETL (that's a new one on me!)
  - Data discovery and cataloguing
  - Matching data sources to the right ingestion service.
 
  So let's start with what an ETL is.
  Happy little lego picture.
  knowing the right tool for the job is really confusing.

## The magic of an ETL

Data sources, we extract from them.
Then we tranform, we can automate routine transformations and also filter out sensitive data and never store it.
Then we load it up, stored data is ready for analysis and complex queries can run more quickly.

## Now the ELT, whoop whoop.
Reflects a more modern, cloud optimised approach for data ingestion apparently.
So basucally a buzz acronym.

So we go Extract still, we always need to extract!
Then we load it up, the ingestion process can run more quickly, and we don't invest effort in guessing what people will use. So nice big dumping ground.
Then we transform.

## Reverse ETL
So this is like the reporting leg, or the bit we do where we transform for reporting!
So it's taking data that's in the data warehouse, and trasnforming it into a format that's suitable for operational use.
So could reshape into customer segments etc, or preparing inventory alerts.
Then reload into transactional or third party system, I'm thinking ehre maybe like Power BI or Looker. But it doesn't explicitly say that. But yeah I guess this could also be happening to push to like an app or a front end for people to see too, not just BI tools.
So ETL and ELT is about landing in a data warehouse, which will be why she didn't react to my answer so good.
Reverse ETL is out of the warehouse, and the stuff you do afterwards. So what I've always thought of as a reporters job.

Okay, reverse ETL, operationalising analytics, which is why we're basically called that aren't we?

So, we're saying here:
Instead of a sales rep running a manual report at the end of the month to see who is struggling, Reverse ETL pushes a "Hugh Churn Risk" alert to their screen on  a Tuesday morning, allowing them to intervene immediately

Reverse ETL is not just moving data; it is operationalising analytics. It transforms the data warehouse from a passive storage unit for historical reporting into an active engine that powers day-to-day business operations in real-time.

So got an image here, she's saying elf but he's definitely a gnome, surrounded by gnomish technology.
So sales clerk is working and there's all these pipes, which I guess is nicely demonstrating who is using the reverse ETL.
I'll be honest, I get this concept. But it's cool to know that's the term for it! Who knew!

Use cases for Reverse ETL
- Identify customers at-risk and potential customer churn before it happens
- Drive new sales by correlating data from the CRM and other interfaces
- Hyper-personalised marketing for cross-selling and upselling to existing customers
- Operational anlytics to monitor the changes in business applications and data faster
- Data replication to modern cloud applications for better reporting capabilities and finding insights

Right let's have a dsicussion
why would you want to maximise transformations on data in motion and minimise data at rest? Is the following appropriate architecture?

I've not a scooby. Apparently a good answer will separate a junior from a well seasoned...gee thanks no pressure.

So diagram. We've got source systems with real-time data.
THere's real-time ingestion also
Then there's real-time processing
after that there's more real-time ingestion into real-time apps and batch data stores.
So all of that is very....well real time.
Got real time transformations on business applications.
Then got data at rest for reporting.

Don't totally get what we're on about here honestly.
Okay so if something isn't at rest, it ccould be queried in an inconsistent state.
Latency has a cost.
So architecture does something smart here. does the fast path for real time streaming for immediate intelligence. Apparently the other path is the deep path, which is for batch storing. I can see that it ends up there, but nothing about the fork sugests that either path is slower than the other.
so doing an example about fraud detection. Fraud detection would get real time signals and batches would get complete, historic datasets.
Risk models would get both.
Ever used anything with acturaries


Importance of Data Cataloguing
So we've tlaked about the dewey decimal system
We've got AWS Glu Data Catalog
So AWS Glue Data Catalog does not have the data but it's like a map, so maybe a bit like Collibra or how GCP holds things in the background, Data Lineage stuff.
There's also AWS Glue Crawlers, which sounds cool.

So we've got a fun picture analogy situation.
On the left, big warehouse with loads of books in boxes that sits off to the side of the library (sticking with dewey decimal system stuff),
The warehouse is big, massive, stores anything. But the entire warehouse is dark, you've o idea where anything is.
So the crawler visits the warehouse, and hen they start to find out what's actually in that warehouse.
The crawler is walking around in the warehouse, reading what's there (scans the data sources so he can update the data catalog), like reading hte book spines to go 'oh btw we have this book'.
Lost the anaogy a bit....but the water cooler looks like a database in the picture so that's fun.
I think basically the crawler helps kinda do indexes (cataloguing) so people can then find what they want.
There's 'lake formation' in AWS land, and there's a librarian with a set of keys stood in front. All relates to everything that needs to happen in the lab....whoop.

Metadata cataloguing. 
So we know lots about this, but one I dont' think about very often is the freshness. How recent is that data.
Oh we're in an NHS example of AI generated images now.
So, I'm a person, I talk to the NHS. When I do, GP, Pharmacy or whatever, someone needs to know my full medical history. Not just my reuslts.
Need a full record, but then there's where it exists, who owns it, who is allowed to access it etc.
So there's the store, the patient data stuff, liek xrays and things. Not blood test reuslt sbecause they would be soemwhere else?
MEtadat service, hospital/admin layer, your new Gp would register you. 
Metadata Ingestion - That's evrey touch point that would update a record. So any apointment, result, perscription, the metadata ingestion is needed here. Can't rely on a manual update.
Leads to a visualisation can search histories, allergies, etc.


