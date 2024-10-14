## Data system
### System of records. Place oriented. Mutable.
    + / - integration
    + deduplication

    - slow change
    - no inherent change tracking
    - different needs / cross dep conflicts
    - scalability
    - limited selfservice

### Data as product systems. Data Ids, versioned, immutable data.
    + Governance; policies, data properties
    + Selfservice / Discoverability


*'Interestingly, several organizations claim to have implemented the data mesh “by accident,” perceiving this paradigm as the natural evolution of data management.'*

### Data Mesh
    many arrive here by them self, lowering the barrier for company to publish, find, use data
    domain experts (who ever they might be; publish owning data products)

*'Many data products fail because they are a solution in search of a problem – for example, ingesting a new dataset into the data platform because ‘someone’ will find it useful. Adding more data does not necessarily solve a customer’s problems – or provide them with value. '*

### Data Mesh Principles
    1. **Domain-Oriented Decentralized Data Ownership and Architecture**
    2. **Data as a Product**
    3. **Self-Serve Data Infrastructure as a Platform**
    4. **Federated Computational Governance**

### Data product req
    Discoverable
    Addressable (no place)
    Self describing 
    Owned and taken cared of (cross functional?)

### Thesaurus
    Lineage 
    Quality 
    Governance

### data certainty 
    * Raw data
    * Cureated data. Accuracy, relevant repersentation
    * Authoritative. Relevant, complete, consistent, documented.

    
![Data Mesh Architecture](./pics/data_certitude.svg)


### Components

    Data Governance system
    Data Catalogue
    Storage

    Execution Governance 
    Execution System


### Companies providing platforms/services for complete immersion
[atlan](https://atlan.com/?ref=/p/data-catalog-data-mesh/)
    - data catalog
    - metadata man

[K2View](https://www.k2view.com/)
    - data as product management with domain-oriented ownership
    - self service

[DataBricks](https://www.databricks.com/)
    - lakehouse platform

[Danodo](https://www.denodo.com/)

[Snowflake](www.snowflake.com/)

[Data Mesh Manager](https://www.datamesh-manager.com/)


### Data Catalogues (data, metadata, events)
[Linkedins Datahub](https://datahubproject.io/)

[Apache Atlas](https://atlas.apache.org/#/)

[Amundsen](https://www.amundsen.io/)

[Netflix Metacat](https://github.com/Netflix/metacat)
[info](https://netflixtechblog.com/metacat-making-big-data-discoverable-and-meaningful-at-netflix-56fb36a53520)

### Workflow orchestration systems, execution governance. 


[Airflow](https://airflow.apache.org/)

[Dagster](https://dagster.io/)

[Luigi](https://github.com/spotify/luigi)

[Kubelow](https://www.kubeflow.org/)

[Prefect](https://www.prefect.io/)

[Netflix, meastro](https://github.com/Netflix/maestro)

[Argo workflows](https://argoproj.github.io/workflows/)



[Differential Dataflow](https://github.com/timelydataflow/differential-dataflow/blob/master/differentialdataflow.pdf)