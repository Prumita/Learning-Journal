### Covered by Aysan

Going to focus in on Kafka today. Going to focus on how it works and what it is mainly used for.
81% of companies use Kafka for data pipelines and 66% use it for stream processing.
Where would you see stream processing in the wild?

Internet of Things. Netflix, Social Media, fraud detection in banking etc.

One of the best ways to understand Kafka is to look at where it's being used. Look at the problems that companies could not do well.

## Audi
They use kafka for predictive maintenance. Monitor vehicle health in real time and predict failures before breakdowns even happen.
Modern vehicles generate a huge amount of sensor data, data from engines, brakes, battery systems. A lot of the components are generating data. Producing events. Kafka help process that data continuously.
Instead of being reacive after a failure happens, the maintenance becomes proactive. Fixing before the failure happens.
This data is going to be processed by something.
So why do we want it quickly?
If we're not processing the predictions quickly then we could lose that data and lose the event that provides that prediction. The scenario could have changed by the time a batch update is done at the end of the day, for example.
Kafka is very scalable, it's their superpower. 
Ultimately this approach will reduce maintenance costs. Big saying in medical field like prevention is better than the cure, same is true here.

## Knowledge check discussion
Imagine you are a data eingeer at an automotive company that uses Kafka to monitor vehicle health data in real-time. Recently, you noticed that some sensor data is delayed, leading to inaccurate predictive maintenance alerts.

What steps would you take to identify and resolve the issue of a delayed sensor data in your Kafka system?

## Cloud-Based Event Streaming Services

Event streaming in big data

Big Data Landscape:
- Real-time data processing is essential
- Event streaming platforms are crucial

Apache Kafka:
- Leader in high-throughput streaming
- Widely adopted open-source solution

Cloud providers:
- Azure, AWS, GCP offer managed services
- Benefits: managed infrastructure, seamless integration, scalability

Cloud companies realise that companies struggle to use Kafka by thsemelves. So Kafka is open-source, can do whatever the heck you like, but the cloud ones come more in the box, package, ready to go.

## Azure Event Hubs and Event Grid

Big Data and Real-Time Processing

| Comparison | Azure Event Hubs | Azure Event Grid |
|---|---|---|
| Definition | Managed, real-time data ingestion service. | Managed event routing service. |
| Use cases | Telemetry ingestion, log collection, real-time analytics, big data pipelines | Serverless applications, workflow automation, event integration |
| Key Features | - Supports AMQP 1.0 and Kafka protocols.<br>- Partitioning and offset management.<br>- Capture feature for storing data in Azure Blob Storage or Data Lake. | - Low latency event delivery.<br>- Advanced filtering and routing.<br>- Supports custom events and integrates with Azure services. |

## Comparing Azure Event Hubs with Kafka

| Feature | Kafka | Azure Event Hubs |
|---|---|---|
| Management | Self-managed clusters, infrastructure provisioning and maintenance | Fully managed service, abstracts cluster management complexities |
| Protocol support | Uses its own protocol; extensive client libraries | Kafka-compatible endpoint; no client code changes needed |
| Ecosystem and integration | Rich ecosystem with many connectors and community support | Deep integration with Azure services; may have limitations outside Azure |
| Scalability | Highly scalable with fine-grained performance control | Scales automatically with less control over infrastructure |
