# Overview of the Elastic stack

## 1. Kibana

Kibana is an analytics and visualization platform, which lets you easily visualize data from Elasticsearch and analyze it to make sense of it.

You can think of Kibana as an Elasticsearch dashboard where you can create visualizations such as pie charts, line charts, and many others.

Kibana is also where you configure change detection and forecasting that I mentioned

Generally speaking, you can think of Kibana as a web interface to the data that is stored within Elasticsearch.

It uses the data from Elasticsearch and basically just sends queries using the same REST API.

## 2. Logstash

Logstash is a data processing pipeline. It has been used to process logs from applications and send them.

A Logstash pipeline consists of three parts(or stages) - inputs, filters, and outputs. Each stage can make use of a so-called plugin.

### 2.1 input

An input plugin could be a file, for instance, meaning that Logstash will read events from a given file.

It could also be that we are sending events to Logstash over HTTP, or we could look up rows from a relational database, or listen to a Kafka queue.

### 2.1 filter

filter plugins are all about how Logstash should process them. For example, we can parse CSV, XML, or JSON, for instance.

We can also do data enrichment, such as looking up an IP address and resolving its geographical location, or look up data in a relational database.

### 2.3 output

An output plugin is where we send the processed events to.
(Formally, those places are called stashes.)

## 3. X-Pack

X-Pack is a pack of features that adds additional functionality to Elasticsearch and Kibana.

### 3.1 Security

1.  Adds both authentication and authorization to both Kibana and Elasticsearch.

2.  Add users and roles, and configure

### 3.2 Monitoring

1. Monitor the performance of the Elastic Stack, being Elasticsearch, Logstash, and Kibana.

2. ex) CPU and memory usage, disk space, and many other useful metrics

### 3.3 Alerting

### 3.4 Reporting

1. Reports can be generated on-demend or on scheduled
   generate reports when certain conditions are fulfilled

### 3.5 Machine Learning

Enables the machine learning for elasticsearch & kibana

1. abnormality detection
2. forecasting

## 4. graph

- considers the relevance with Elasticsearch
- integrate into applications with an API
- visualize the relationship with kabina

## 5. SQL

- Can query Elasticsearch with SQL
- Elasticsearch queries are written in Query DSL
- It translates the SQL internally

## 6. Beats

- Beats is a collection of so-called data shippers.

- They are lightweight agents with a single purpose that you install on servers, which then send data to Logstash or Elasticsearch.
