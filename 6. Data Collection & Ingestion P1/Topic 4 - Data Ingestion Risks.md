
## Case Study

Facebook doing some dodgy stuff! So even if you weren't logged into Facebook they were still stealing your data from you. Ick.
So they had Implemented SLAs to manage the ingestion adn mitigate data ingestion risks. In 2018, Cambridge Analytica scandal. 18 million users data harvested without consent.
Facebook were fined 5 million US dollars....okay that's not much. Not for Facebook anyway.

Okay so we're chatting SLAs. They help ensure timely data collection and address potential risks.

SLA is kinda a contract. Not just a 'do this work in this amount of hours'. It's a set of rules that says what good data looks like and who owns it when it goes wrong. Agreed downtime etc, who is going to get things fixed in what time and so on. 

So what's an SLA? It must answer three questions

1. What does good look like?
  - The quality threshold, the latency target, the uptime percentage.
2. How do we know when it's broken?
  - The monitoring, the alerting, the measurement method.
3. What happens next?
  - The escalatoin path, the fix timeline, the owner.
  - Without all three, it's not an SLA. It's a wish.

## Data Ingestion Risks
Even with properly designed SLAs, data ingestion risks will still exist.
These include:
- Ingestion system failing and needing troubleshooting (SLA will specify timelines and escalation)
- Ingestion system not behaving optimally and falling below sustainable standards
- Security vulnerabilities of the ingestion system.
- Ingested data quality deteriorating systematically in an unplanned manner.
- PII an sensitive data being ingested and handled improperly.
- Unused ingested data may keep clogging up our infrastructure
- Data ingestion frequency may be inadequate due to changing environment
- Ingested data having licencing restrictions that changed or are not properly managed
- Upstream schema changes breaking downstream systems and metadata becoming stale

## Troubleshooting Practical

Okay so I've got her on the left, me on the right, notes on my other screen, let's do this.

It opens with a little top header, so we have ingestion risks. I typed them out above. We're going to talk about those, and this ntoebook is going to put me in the seat of trying to figure out what's going on. When a pipeline breaks, the SLA only specifies the timelines and escalation. It's not going to tell you what the problem is.

So there's 4 python mistakes below, and they map to the 9.

I did the first one, it was a suddenly missing email. We put a 'no email present' backup value when there was no email.



