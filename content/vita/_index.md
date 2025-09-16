+++
title = "Vita"
+++

I've had several incredible positions in my career, including multiple household names. It took a few years to really understand where in the stack I'm really the most useful. Recently I've felt most impactful:

* Building and operating backend services
* Subjugating unruly data infrastructure - I find you can often increase performance and accessibility while decreasing costs
* Making teams faster and better

# The Walt Disney Company

A company which perhaps needs no introduction; my team is responsible for protecting the actual video that plays on your screen. We manage integration with various Digital Rights Management (DRM) providers, in addition to licensing and entitlement-based access controls.

**Lead Engineer, Media Security** (March 2020 - present)

* Led Star+ On Disney+ Project
    * Negotiated scope, API contracts, delivery estimates, and legal requirements with technical and nontechnical stakeholders
    * Designed linear license and airing rights checks
    * Led team of 8 engineers to deliver work
    * Delivered implementation of airing checks and handling for live or unrated content
    * Product launched successfully on time and without incident
* Led Shutdown of Legacy key management service
    * Old service handled license calls for some clients, written in Java and end of life
    * Imported encryption keys from legacy service to modern key-service and audited for any discrepancies in response
    * Traffic migration completed without incident, eliminated expensive infrastructure and impediments to upcoming roadmap work
* Launched media-rights-service for evaluating session/entitlement-based access to media, which is now a critical component of all playback requests
* Drive a culture of operational excellence:
    * Proposed automation of service deploys, reducing oncall investment from 3 days of manual effort per week to ~hours
    * Introduced Datadog for HTTP metrics
    * Updated Java versions from ancient history (Java 8) to 15 and beyond, dramatically reducing high-percentile latency
    * Worked with SRE to introduce terraform and infrastructure as code
    * Author and review rigorous post-mortems
* Overhauled Event Infrastructure:
    * TCO reductions of over 50% using Ultrawarm Opensearch, tuning compression, and swapping to Graviton nodes
    * Powerful querying capability and joins of different event types by exporting data as Parquet and reading with Athena
    * Automatically generated Athena schemas from Protobuf schemas, eliminating the need to maintain two separate schemas for events
    * Designed and prioritized event emission in more services, increasing visibility into trends and operational issues

# Asimov
Asimov is a biotech company offering "An integrated suite of cells, genes, and software to power advanced genetic design". My role at Asimov was initialize software deployment and data infrastructure and define the software engineering culture.

**Senior Software Engineer** (April 2018 - February 2020)

* Owned deployment platform based on Kubernetes (GKE)
    * Proposed platform based on Kubernetes using Google Cloud Platform after comparing with competitors such as Mesos, Openshift, and Docker Swarm
    * Developed custom admission controller to automatically apply a set of best practices to deployments and to control placement of workloads on appropriate node types
    * Customized and deployed Prometheus and Grafana operators for collection and monitoring of metrics
    * Integrated LetsEncrypt for wildcard subdomain certificates of internal and external software systems
    * Deployed and operated Elasticsearch, Fluentd, Kibana logging stack
    * Integrated Google Identity-Aware Proxy (IAP) with Ambassador for SSO to internal applications, including in-house authentication service for verifying IAP signatures
* Designed and implemented a Data Warehouse:
    * Used akka-streams to extract and warehouse all entities from Benchling's REST API for querying using BigQuery
    * Created a schema registry and validator using Avro and Google Cloud DataStore
    * Refitted warehouse to route tasks using message queues (PubSub) to isolate scaling, failure, retries
* Responsible for engineering practices and culture:
    * Held talks and interactive labs for engineers and scientists to learn Scala, databases, and SQL
    * Introduced continuous build and deployments using CircleCI
    * Established programming language standards and conventions for code review

# Toast

Toast is a cloud-based restaurant software company. They went public in September 2021! In my time at Toast, I worked on the back of house web application, the Android point of sale codebase, and the front of house systems.

Throughout my time at Toast, I:
* Regularly recruited and interviewed new engineers
* Improved interview processes, designed new standard interview question

**Software Engineer Team Lead** (June 2017 - April 2018)
* Led a team of 6 and then 2 (team split) other engineers working on front of house features
* Responsible for design and task breakdown of features and bugfixes
* Provided career mentorship and technical feedback to junior engineers
* Created year-long technical roadmap for addressing quality and operational technical debt
* (Hackathon) Automated uploading of log files from devices

**Senior Software Engineer** (February 2016 - June 2017)
* Rewrote mock printer from naive loop to full-featured and extensible state machine
* Replaced postgres-based event log with Elasticsearch-backed document storage
* Identified and removed numerous race conditions, memory leaks, `NullPointerException`s, and other code safety issues
* Implemented support for embedding amounts such as weight or prices in barcodes

# Amazon

My first big break was Amazon through, believe it or not, a job posting on Craigslist. I initially was a QA Platform Engineer on a little-known project called "Alexa", though I was soon moved to the data platform team, which became the foundation for my career.

**Software Development Engineer, Digital Products** (April 2012 - January 2016)
* Implemented storage solutions for all language and speech data, supporting launch of several voice-enabled systems, including the Amazon Echo, the FireTV, and the Dash
* Designed and implemented highly scalable aggregation service which groups data in a secure, distributed store in near-realtime for use in research, replacing a cronjob that would take days to run
* Designed and implemented a realtime monitoring framework to avoid errors collecting sample speech data from real spoken phrases
* Rewrote synchronous, single-request workflow to prefetch upcoming tasks, increasing throughput for transcribing and annotation real world data
