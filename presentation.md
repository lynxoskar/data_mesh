---
theme: black  


title: "Data Mesh"

---

# Data Mesh

> *'Interestingly, several organizations claim to have implemented the data mesh “by accident,” perceiving this paradigm as the natural evolution of data management. [1](https://blog.owulveryck.info/2024/04/09/data-as-a-product-and-data-contract-an-evolutionary-approach-to-data-maturity.html)'*

---

## Systems
**System of records** :'*transactional operational systems*'

**Data Lake** : '*traditional data pipelines systems*'

**Data Mesh** : '*decentralized domain (cross system) data products*'

--

### Thesaurus data

**Place Oriented** : Mutable state. Place associed with value. Updates records in place. 

**Value Oriented** : Immutable values. Separated from place. Creates new version or appends new data. Allows for decentralized use and value based governance. 

*'ex; version controll systems; git vs svn.'*  

[rich hickey on plop](./sources/perplexity_placeoriented_vs_immutable.md)

---

### System of records [SOR] 
Systems of records (SOR) are traditional, centralized systems that serve as the authoritative source for specific data and/or functions within an organization. **Operative flow**

--

**SOR cont.**
* Place oriented
* Mutable - Deduplicated data
* Atomic operations - transactional 
* Consistency - single source of thruth   
* Slow change - limited agility, system modeling creates bottlenecks
* No inherent change tracking 
* Scalability.
* Limited selfservice, discoverebility. 

---

### Data Lakes 
Traditional pipelines with centralized data platform. Data flowing through a series of ingestion, cleansin and transformative stages.

--

**Lakes cont.**
*  Centralized repository storing RAW data in as native format as possible. 
*  Decupled place from data. 
*  Centralized team maintains and manages data repository
*  Excel at handling large volumes of data
*  Struggles with diversity of data sources (ingress) and shifting use cases

---

### SOR vs Pipelines

--

### Representation
- **Systems of Record:** Data as mutable objects or records in fixed locations
- **Data Pipelines:** Data as immutable values flowing through transformations

--

### Historical Context:
- **Systems of Record:** Often only maintain current state
- **Data Pipelines:** Naturally preserve historical data and changes over time

--

### Processing Model:
- **Systems of Record:** Often rely on in-place updates and transactions
- **Data Pipelines:** Use functional transformations on immutable data streams

--

### Data Quality and Governance:
- **Systems of Record:** May require complex mechanisms to ensure data integrity
- **Data Pipelines:** Can leverage immutability and functional transformations for better data quality control


---

## Data Mesh

*'Many data products fail because they are a solution in search of a problem – for example, ingesting a new dataset into the data platform because ‘someone’ will find it useful. Adding more data does not necessarily solve a customer’s problems – or provide them with value. '*

--

### Data Mesh Principles
1. *Domain-Oriented* Decentralized Data Ownership and Architecture
2. Data as a *Product*
3. *Self-Serve* Data Infrastructure 
4. Federated Computational Governance

--

![System](./pics/4_principles.webp)

--

#### 1. Domain-Oriented Data 'Tackling complexity in the heart of data...'
*'The Domain-Oriented approach, rooted in DDD principles, aims to create a business-aligned data architecture. Empowering domain teams to take ownership of their data, leading to more accurate, relevant, and usable data products across the organization. This approach addresses many of the challenges faced by traditional, centralized data management systems, particularly in large, complex organizations with diverse data needs.'*
--

### 1. DDD - cont.

- **Eric Evans book** [domain driven design](https://fabiofumarola.github.io/nosql/readingMaterial/Evans03.pdf)

--

**bounded context**
Data is organized around specific business domains or subdomains, each with its own clearly defined boundaries. This approach helps in managing complexity by breaking down large systems into smaller, more manageable parts.
ex; same id might have different associated data depending on context. (resize time in mimer...)

--

**unambigious language** 
Domain-Oriented data emphasizes using a common language shared by both technical and business teams within a specific domain. This language is reflected in the data models, naming conventions, and metadata.

--

**Domain Experts:**
Domain-Oriented data relies heavily on the knowledge and input of domain experts, ensuring that data models and structures accurately reflect the business reality

--

- Expert Teams (not systems) with deep understanding of domain and data
- Aligns with problem solving and change. 
- Improves decision making. 
- Decentralized; ownership not centralized.

--

| Aspect | Traditional Approach | Domain-Oriented Approach |
|--------|----------------------|--------------------------|
| Data Ownership | Centralized IT or data team | Distributed across domain teams |
| Data Model | Often generic, one-size-fits-all | Specific to each domain's needs |
| Data Governance | Centralized policies | Federated, domain-specific policies |
| Data Quality | Managed by central team | Responsibility of domain teams |
| Scalability | Can become a bottleneck | More scalable due to decentralization |
| Innovation | Often slower due to centralization | Faster, domain-specific innovation |

--

#### 2.Data as a product
    - **push vs pull** -> record of change. Cultural shift;  Ownership gets claimed - not assigned. Deliver value, produce value. Not complete assignments. 
    - **strategic asset** -> Core product. Not a byproduct of operations. Data products gets a vision, strategy and roadmap.
    - **quality focus** -> Usable, understandable, correct, on-time, complete.
    

--
#### 3.Self-Serve Data Infrastructure 
    - Producers; Unified platform, empowering domain teams (not system teams) to   autonomously develop and manage data products.
    - Data is addressable rather then in place.
    - Consumers; Discoverebility and affordance build.

--
#### 4.Federated Computational Governance
    - Establishes standards for data product properties and lifecycle
        - structured, unstructured
        - complex or simple
        - linage 
        - set, lot or appendstucture (deduplicated)
        - life times events
        - 
        - tombstoning / inits
    - Automated enforcement
    - Access and security
    - Balance between centralized control and domain autonomy
    
---

# Organisational and cultural shifts

    - not only a system architectical shift. Far from it. Everyone participates. Benifits and contributes.

---



### DataMesh vs Data Lakes

Data mesh aims to address the limitations of traditional data management approaches by:

*   **Shifting data ownership**: From centralized teams to domain experts who understand 
the data best, leading to better data quality and governance.

*   **Data Modeling:**: From generic data models that try to accommodate all use cases.
   to specific data models that reflect the unique needs and language of each domain.

*   **Decoupling data pipelines**: Into smaller, domain-specific units, allowing for more agile development and deployment of data products.

*   **Emphasizing data as a product**: From central team responsible for data quality to  domain teams focusing on delivering value to data consumers through high-quality, discoverable data products.

*   **Providing self-service infrastructure**: Empowers domain teams to manage their data products independently, promoting agility and innovation.

*   **Innovation:**

This distributed approach promotes scalability, agility, and data quality by empowering domain teams and fostering a data-driven culture. Data mesh recognizes that data is not a monolithic entity but rather a collection of interconnected, domain-specific datasets that can be best managed by those closest to them.

---


--






### Data as product systems. Data Ids, versioned, immutable data.
    + Governance; policies, data properties
    + Selfservice / Discoverability
    + Focus on value

---



### Data Great devide
    Operational data, accuracy consistency availability for real-time use
     [signals orders trades]

    Data Products - data-driven system

    
| Feature | System of Records | Data Product |
|----------|----------|----------|
|    Data Types     |  Transactional, in place, unique operations        | Analytical series historical data          |
|    Purpose     |  Operational efficienty, transactional        | Data driven insights,  Quality(value) descisions          |
|    Structure     |  Structured, relational        | Polyglot, diverse formats          |
|Ownership|Centralized, place oriented| Decentralized adressable domain-driven
|Accessibility|Limited to operational users| Broad, self-service access

---

*'It's important to note that data mesh adoption is an evolving process. While the technology is largely available, the greater challenge lies in the cultural and organizational shifts required to implement a successful data mesh. Many organizations are taking an incremental approach, starting with specific data products and gradually expanding their mesh over time'*

---

### Organisations Great devide
    System departments vica vie domain teams. 






---

# Future
- Data from id:links. Data + metadata interpreted by ai. Every consumer will be limited only by finding, vision,  taste, curiosity, creativity.

- [NoteboolLM](https://notebooklm.google.com/notebook/4f655dcf-38ad-4646-9b39-b5c7d16f24c4?original_referer=https:%2F%2Fblog.google%23&pli=1)

- [Generated podcast](https://notebooklm.google.com/notebook/4f655dcf-38ad-4646-9b39-b5c7d16f24c4/audio)

---

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

[Starburst](https://www.starburst.io/)
    - built on OS. 

[atlan](https://atlan.com/?ref=/p/data-catalog-data-mesh/)
    - data catalog
    - metadata man

[K2View](https://www.k2view.com/)
    - data as product management with domain-oriented ownership
    - self service

[DataBricks](https://www.databricks.com/)
    -   Databricks
        Databricks is a unified data analytics platform built on Apache Spark.
    Key features:
        Lakehouse architecture combining data lake and data warehouse capabilities
        Strong support for data engineering, data science, and machine learning workflows
        Delta Lake for ACID transactions on data lakes
        Collaborative notebooks for data analysis and visualization
        Target users: Data engineers, data scientists, and analysts in organizations dealing with big data and advanced analytics
        Snowflake

[Danodo](https://www.denodo.com/)

[Snowflake](www.snowflake.com/)
    -   Snowflake is a cloud-based data warehousing platform.
    Key features:
        Separation of storage and compute for scalability
        Support for structured and semi-structured data
        Easy data sharing and collaboration
        Strong SQL support and optimization for analytics queries
        Target users: Business analysts, data analysts, and organizations focused on business intelligence and data warehousing

[Data Mesh Manager](https://www.datamesh-manager.com/)


### Data Catalogues (data, metadata, events)
[Linkedins Datahub](https://datahubproject.io/)

[Apache Atlas](https://atlas.apache.org/#/)

[Amundsen](https://www.amundsen.io/)

[Netflix Metacat](https://github.com/Netflix/metacat)
[info](https://netflixtechblog.com/metacat-making-big-data-discoverable-and-meaningful-at-netflix-56fb36a53520)

### Workflow orchestration systems, execution governance. 
[estuary](https://estuary.dev/)
        - Estuary is a real-time data operations platform.
    Key features:
        Real-time data integration and ETL
        Support for streaming and batch data processing
        Schema evolution and data quality management
        Open-source core (Flow) with cloud-hosted option
        Target users: Data engineers and organizations dealing with real-time data streams and complex data pipelines

[Airflow](https://airflow.apache.org/)

[Dagster](https://dagster.io/)

[Luigi](https://github.com/spotify/luigi)

[Kubelow](https://www.kubeflow.org/)

[Prefect](https://www.prefect.io/)

[Netflix, meastro](https://github.com/Netflix/maestro)

[Argo workflows](https://argoproj.github.io/workflows/)



[Differential Dataflow](https://github.com/timelydataflow/differential-dataflow/blob/master/differentialdataflow.pdf)


[Future](https://notebooklm.google.com/notebook/4f655dcf-38ad-4646-9b39-b5c7d16f24c4/audio?pli=1)