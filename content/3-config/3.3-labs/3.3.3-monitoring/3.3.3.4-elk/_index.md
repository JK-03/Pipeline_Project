---
title : "ELK Stack"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 3.3.3.4 </b> "
---

#### Overview
- The ELK Stack stands for Elasticsearch, Logstash, and Kibana, which is a powerful set of open-source tools commonly used for log management and analytics.
    - **Elasticsearch**: This is a distributed, RESTful search and analytics engine designed for horizontal scalability, reliability, and real-time search capabilities. It's providing storage and indexing functionality for logs and other data. It's highly efficient for searching and analyzing large volumes of data in near real-time.
    - **Logstash**: Logstash is a data processing pipeline that ingests, transforms, and enriches data before it's indexed into Elasticsearch. It supports a wide range of input sources, including logs, metrics, events, and other structured or unstructured data formats. Logstash can perform various operations on the data, such as parsing, filtering, and formatting, to make it suitable for analysis.
    - **Kibana**: Kibana is the visualization and user interface component of the ELK Stack. It provides a web interface for users to visualize and explore data stored in Elasticsearch.Kibana offers various visualization options, including charts, graphs, maps, and dashboards, allowing users to create custom visualizations and dashboards to gain insights from their data

#### Configuration
