Nidia is back, I missed last week due to being on holiday and haven't had chance ot catch up yet.

So thinking about fraud detection, looks super similar to legit transactions, but isn't, how in real time do these get identified?

The challenge - High transaction volumes in financial institutions
Need - to prevent system issues and detect fraud
Implementation - Isolation Forest, time series models, striim integration.

Isolation Forest - Looks for outliers and notices the outliers
Time series, arena, ceremax?? Looks for what normal looks like over time. So if Monday mornings are always busy, then that becomes normal, but if it's extra busy, well that's less normal.
Striim integration, it's real time streaming ingestion platform that captures changes in data. As they happen. As it feeds into the detection engine.

What's the outcome of implementing these?
To catch the fraudulent transaction earlier, and to have fewer outages. better security.
Three benefits, everyone wants that.

think about patient observation feeds. Data changes, challenge is the same, find the unexpected and find it fast.

## Session aim and objectives

- Automate monitoring processes for data ingestion services using industry-standard tools
- Implement forecasting and anomoly detection techniques, including ARIMA, SARIMAX, and other methods.
- Integrate monitoring with incident management systems to enhance operational responsiveness
- address real-world use cases and typical ingestion issues in Kafka and cloud environments.

### Monitoring in data engineering

Monitoring data ingestion pipelines is essential to:

- Ensure Data Integrity - Detecitng corruption or loss e.g. patient records ariving incomplete
- Maintain Performance - Performance. Spotting bufferings?? SLA compliance. 
- Enhance Reliability - Fast detection and response to failures.
- Support Compliance - Audit trails and reporting.

So say something drops, an alarm would go off. So a data pipeline needs the same, needs the same monitoring. If there's no alarm of paging system then we'd only find out something went wrong when downstream users start complaining.
What monitoring is the most relevant to my employer?

Data Integrity - detecting corruption or loss

### Industry-standard monitoring tools

Prometheus and Grafana

These tools are essential for monitoring and visualising data pilines:

#### Prometheus
- Open-surce monitoring toolkit
- Collects metrics at intervals
- Time series data model
- PromQL for data analysis
- Alertmanager for alerts

#### Grafana
- Open-source visualisation platform
- Supports multiple data sources
- Customisable dashboards
- Integrated alerting

Prometheus and Grafana appear in the EPA assessment criteria. If you implement these at work ever, even in a test environment they can be documented as portfolio evidence.

### Monitoring Kafka with Prometheus and Grafana
How is - I missed this section sorry.

### Automating monitoring processes
Alerting with Prometheus Alertmanager

Beyond metrics collection and visualisation, it automates responses to potential issues.

Alertmanager Setup:
- Define alerting rules
- Configure noritication channels

Example alerting rule:
- HighConsumerLag alert for Kafka
- Expression: kafka_consuemr_lag > 10000
- Duration: 5 minutes
- Severity: Critical
- Annotations: Summary and description

code 
``` 
groups:
  -  name : kafka_alerts
      rules:
         - alert: HighConsumerLag
            expr: kafka_consumer_lag > 10000
            for: 5m
            labels:
              severity: critical
            annotations:
              summary: "Hugh Consumer Lag Detected"
              description: "Consumer lag is {{ $value }} for group {{ $labels.group }}"
```

5 minute duration is typical here because a transient spike is very normal. So making sure it's a sustained problem is important.

### Case study scenario
Monitoring a healthcare data pipline
How would you approach this task?

Implementation steps:
1. Deploy prometheus and Grafana
2. Set up Kafka Exporter
3. Create Dashboards
4. Define Alerting Rules
5. Integrate with Incident Management
    
