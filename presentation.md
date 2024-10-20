---
theme: sky  


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

**Bounded context**:
Data is organized around specific business domains, each with its own clearly defined boundaries. This approach helps in managing complexity by breaking down large systems into smaller, more manageable parts.

--

**Unambigious language** 
Domain-Oriented data emphasizes using a common language shared by both technical and business teams within a specific domain. This language is reflected in the data models, naming conventions, and metadata.

--

**Domain Experts:**
Domain-Oriented data relies heavily on the knowledge and input of domain experts, ensuring that data models and structures accurately reflect the business reality


--

##### 1. Domain-Oriented Data Cont

- **Decentralized Ownership**: Each business domain takes responsibility for its own data.
- **Domain Expertise**: Domain teams, with their deep understanding of the business context, manage and provide data.
- **Alignment with Business Structure**: This approach mirrors how modern businesses employ specialized teams for specific operations.
- **Improved Decision-Making**: By placing data ownership closer to the source, it enhances data-driven decision-making.

---

#### 2. Data as a product
'*This principle treats data as a valuable asset, applying product thinking to data management.*'

--

- **Product thinking** Data gets a vision, strategy, and roadmap. Ownership enhances stewardship, innovation and experimentation. 
- **Push vs pull** record of change. Cultural shift;  Ownership gets claimed - not assigned. Deliver value; not complete assignments.
- **Strategic asset**: Core product. Not a byproduct of operations. Data products gets a vision, strategy and roadmap.
- **Quality focus**: Usable, understandable, correct, on-time, complete.
- **Lifecycle Management**: Data products are managed through their entire lifecycle, from creation to retirement
    
---

#### 3.Self-Serve Data Infrastructure 

*'This principle aims to provide a platform that enables domain teams to easily create, maintain, and use data products.'*

--

- **One Platform**: Unified platform provides domain-agnostic tools and systems. Empowering users to autonomously develop and manage products.

--

- **Ease of Use**: Low barrier for adoption, allowing to find, understand and manage data products. Affordance build in.

--

- **Virtualization**: Data is virtualized rather than centralized. Adressable, decentralized. Not a place. 

--

- **Flexibility**: The platform evolves based on domain requirements, balancing centralized infrastructure with domain-specific needs.

---

#### 4.Federated Computational Governance

'*This principle ensures interoperability and consistency across the decentralized data ecosystem.*'

--

- **Global Standards**: Establishes organization-wide standards for data. Required metadata and conventions.
        
        context: prod | preprod | test
        owner
        linage
        structured | unstructured,         
        simple | complex 
        lot | set | appendstructure
        life time events
        tombstoning | inits
        authorization/authentication

--

- **Automated Enforcement**: Governance rules are computationally enforced, reducing manual oversight.

--

- **Balance**: Strikes a balance between centralized control and domain autonomy

---

#### Summary:
'*These principles work together to create a data ecosystem that is scalable, flexible, and aligned with business needs. The domain-oriented approach (Principle 1) and data as a product mindset (2) address issues of data quality and relevance. The self-serve infrastructure (3) enables efficient data product creation and consumption. Finally, federated governance (4) ensures that this decentralized system remains cohesive and compliant.'*

---

#### DataMesh vs Data Lakes
*   **Shifting data ownership**: From centralized teams to domain experts who understand 
the data best, leading to better data quality and governance.

*   **Data Modeling:**: From generic data models that try to accommodate all use cases.
   to specific data models that reflect the unique needs and language of each domain.


--

#### DataMesh vs Data Lakes cont
*   **Decoupling data pipelines**: From centralized control and generic approaches into smaller, domain-specific units, allowing for more agile development and deployment of data products. Allowing for more domain-specific innovation and experimentation

*   **Emphasizing data as a product**: From central team responsible for data quality to  domain teams focusing on delivering value to data consumers through high-quality, discoverable data products.

--

#### DataMesh vs Data Lakes cont

*   **Providing self-service infrastructure**: Empowers domain teams to manage their data products independently. 

---


#### Organisational and cultural shifts
*'A distributed approach promotes scalability, agility, and data quality by empowering domain teams and fostering a data-driven culture. Data mesh recognizes that data is not a monolithic entity but rather a collection of interconnected, domain-specific datasets that can be best managed by those closest to them.*'


- not only a system architectical shift. Far from it. Everyone participates. Benifits and contributes.

---

#### Data Certitude
    Raw data
    Cureated data: Accuracy, relevant representation. 
    Authoritative data: Relevant, traceble, complete, consistent, documented. 
![Data Mesh Architecture](./pics/data_certitude.svg)

---

### Success stories

JP Morgan | Saxo Bank | Intuit | Paypal

[many](./sources/)

--

Paypal;

    '*Scalability: PayPal started with 6 data products and rapidly expanded to about 40, with plans to add many more. This demonstrates the scalability of the data mesh approach*'

    '*Better regulatory compliance and data security: The decentralized nature of data mesh allowed for improved compliance and security measures*'

    '*Autonomy for data domains: The data mesh provided greater autonomy for different data domains within PayPal, allowing them to manage their own data pipelines*'

---

### Culture Mind shift

*'It's important to note that data mesh adoption is an evolving process. While the technology is largely available, the greater challenge lies in the cultural and organizational shifts required to implement a successful data mesh. Many organizations are taking an incremental approach, starting with specific data products and gradually expanding their mesh over time'*

--

*'The transition from a traditional system of records to a data pipeline/data product system is a significant undertaking that requires a holistic approach to organizational change. It involves not just technological shifts but also fundamental changes in how people think about, manage, and use data. Success in this transition depends on strong leadership, clear communication, and a sustained commitment to building a data-driven culture across the entire organization.'*

--

1. **Mindset Shift:**
   - From viewing data as a byproduct to treating it as a valuable product
   - Embracing decentralization and domain ownership

2. **Skill Development:**
   - Data literacy across the organization
   - Domain teams need to develop data management and engineering skills
   - Platform teams need to shift focus from control to enablement

--

3. **Leadership Support:**
   - Executive sponsorship for the transition
   - Clear communication of the vision and benefits

4. **Cross-functional Collaboration:**
   - Breaking down silos between system research and business units
   - Encouraging knowledge sharing and collaboration across domains

--

5. **Agile and Product-Oriented Thinking:**
   - Adopting agile methodologies for data product development
   - Focusing on user needs and continuous improvement

6. **Data Governance Evolution:**
   - Shifting from centralized control to federated governance
   - Developing new policies and standards for decentralized data management

--

7. **Continuous Learning Culture:**
   - Encouraging experimentation and learning from failures
   - Providing ongoing training and support for new tools and methodologies

8. **Change Management:**
   - Implementing a robust change management program
   - Addressing resistance to change and fostering buy-in across the organization

--

9. **New Roles and Responsibilities:**
   - Creating new roles such as data product owners and data domain leads
   - Redefining existing roles to align with the new data-centric approach

10. **Metrics and Incentives:**
    - Developing new KPIs that align with data product thinking
    - Adjusting incentive structures to encourage data sharing and quality

---


### Future is here
'*Every member will be limited only by discovery, vision, taste, curiosity, creativity.*'

---

If data products are not available when AI-powered tools become commonplace and potentially customized for specific companies, several significant challenges and missed opportunities could arise:

--

Inefficient AI implementations: Without proper data products, AI tools may struggle to access and utilize relevant information, resulting in suboptimal performance and less accurate insights.

--

Increased data silos: The absence of data products could exacerbate existing data silos, making it difficult for AI tools to provide a comprehensive view of the organization's data landscape.

--

Missed innovation opportunities: AI-powered tools often uncover unexpected insights and patterns. Without accessible data products, companies may miss out on these potential innovations.

--

Reduced agility: The inability to quickly access and analyze data through AI tools could slow down a company's ability to respond to market changes or customer needs.

--

Compliance and governance risks: Without structured data products, ensuring data quality, lineage, and compliance with regulations could become more challenging when using AI tools.

--

Difficulty in scaling AI initiatives: As AI tools become more sophisticated, the lack of data products could limit a company's ability to scale its AI initiatives across different departments or use cases.

--

Talent retention issues: Data scientists and AI specialists may be frustrated by the lack of accessible, high-quality data, potentially leading to retention problems.

--

Missed cross-functional opportunities: The absence of data products could limit the ability of AI tools to identify and leverage cross-functional insights and opportunities within the organization.

--



- [NoteboolLM](https://notebooklm.google.com/notebook/4f655dcf-38ad-4646-9b39-b5c7d16f24c4?original_referer=https:%2F%2Fblog.google%23&pli=1)

- [Generated podcast](https://notebooklm.google.com/notebook/4f655dcf-38ad-4646-9b39-b5c7d16f24c4/audio)

---

### Appendix; components

Data Governance systems

Data Catalogue

Storage

Execution Governance 

Execution System

--

#### Companies providing platforms/services for complete immersion

[Starburst](https://www.starburst.io/)
    - built on OS. 

[atlan](https://atlan.com/?ref=/p/data-catalog-data-mesh/)
    - data catalog
    - metadata man

[K2View](https://www.k2view.com/)
    - data as product management with domain-oriented ownership
    - self service
--

[DataBricks](https://www.databricks.com/)
is a unified data analytics platform built on Apache Spark.
Key features:
Lakehouse architecture combining data lake and data warehouse capabilities
Strong support for data engineering, data science, and machine learning workflows
Delta Lake for ACID transactions on data lakes
Collaborative notebooks for data analysis and visualization
        
--

[Danodo](https://www.denodo.com/)

[Data Mesh Manager](https://www.datamesh-manager.com/)

--

[Snowflake](www.snowflake.com/)
    -   Snowflake is a cloud-based data warehousing platform.
        Key features:
        Separation of storage and compute for scalability
        Support for structured and semi-structured data
        Easy data sharing and collaboration
        Strong SQL support and optimization for analytics queries
        Target users: Business analysts, data analysts, and organizations focused on business intelligence and data warehousing

---


#### Data Catalogues (data, metadata, events)
[Linkedins Datahub](https://datahubproject.io/)

[Apache Atlas](https://atlas.apache.org/#/)

[Amundsen](https://www.amundsen.io/)

[Netflix Metacat](https://github.com/Netflix/metacat)
[info](https://netflixtechblog.com/metacat-making-big-data-discoverable-and-meaningful-at-netflix-56fb36a53520)

---

#### Workflow orchestration systems, execution governance. 
[Estuary](https://estuary.dev/) is a real-time data operations platform.
Real-time data integration and ETL
Support for streaming and batch data processing
Schema evolution and data quality management
Open-source core (Flow) with cloud-hosted option
Target users: Data engineers and organizations dealing with real-time data streams and complex data pipelines

--

[Airflow](https://airflow.apache.org/)

[Dagster](https://dagster.io/)

[Luigi](https://github.com/spotify/luigi)

[Kubelow](https://www.kubeflow.org/)

[Prefect](https://www.prefect.io/)

[Netflix, meastro](https://github.com/Netflix/maestro)

[Argo workflows](https://argoproj.github.io/workflows/)


---

# FIN




