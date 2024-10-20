---
theme: league  


title: "Data Mesh"

---

# Data Mesh

> *'Interestingly, several organizations claim to have implemented the data mesh “by accident,” perceiving this paradigm as the natural evolution of data management. [1](https://blog.owulveryck.info/2024/04/09/data-as-a-product-and-data-contract-an-evolutionary-approach-to-data-maturity.html)'*

---

## Systems
**System of record** :'*transactional operational systems*'

**Data Lake** : '*traditional data pipelines systems*'

**Data Mesh** : '*decentralized domain (cross system) data products*'

--

### Thesaurus data

**Place Oriented** : Mutable state. Place associed with value. Updates records in place. 

**Value Oriented** : Immutable values. Separated from place. Creates new version or appends new data. Allows for decentralized use and value based governance. 

*'ex; version controll systems; git vs svn.'*  

[rich hickey on plop](./sources/perplexity_placeoriented_vs_immutable.md)

---

### System of records 
Systems of Record (SOR) are traditional, centralized systems that serve as the authoritative source for specific data and functions within an organization. **Operative flow**

--

**SOR cont.**
*   Place oriented
*   Mutable - Deduplicated data
*   Atomic operations - transactional 
*   Consistency - single source of thruth   
*   Slow change - system modeling creates bottlenecks
*   No inherent change tracking 
*   Limited selfservice, discoverebility.  

---

### Data Lakes 
Traditional pipelines with centralized data platform. Data flowing through a series of ingestion, cleansin and transformative stages.

--

**Lakes cont.**
*  Centralized repository storing raw data in generic format. 
*  Decouples data from its place of origin 
*  Centralized team maintains and manages the data repository
*  Excel at handling large volumes of data
*  Struggles with diversity of data sources and shifting use cases

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
- **Systems of Record:** Rely on in-place updates and transactions
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
*'The Domain-Oriented approach, aims to create a business-aligned data architecture. Empowering domain teams to take ownership of their data, leading to more accurate, relevant, and usable data products across the organization. This approach addresses many of the challenges faced by traditional, centralized data management systems, particularly in large, complex organizations with diverse data needs.'*
--

### 1. DDD - cont.

- **Eric Evans book** [domain driven design](https://fabiofumarola.github.io/nosql/readingMaterial/Evans03.pdf)

--

**Bounded context**:
Data is organized around specific business domains, each with its own clearly defined boundaries. Managing complexity by breaking down large systems into smaller, more manageable parts.

--

**Unambigious language** 
Domain-Oriented data emphasizes using a common language shared by both technical and business teams within a specific domain. This language is reflected in the data models, naming conventions, and metadata.


--

#### 1. Domain-Oriented Data Cont

- **Decentralized Ownership**: Each business domain takes responsibility for its own data.
- **Domain Expertise**: Domain teams, with their deep understanding of the business context, manage and provide data.

--

- **Alignment with Business Structure**: This approach mirrors how modern businesses employ specialized teams for specific operations.
- **Improved Decision-Making**: By placing data ownership closer to the source, it enhances data-driven decision-making.

---

#### 2. Data as a product
'*This principle treats data as a valuable asset, applying product thinking to data management.*'

--

#### Data as a product cont
- **Product thinking** Data products have a vision, strategy, and roadmap. Ownership enhances stewardship, innovation, and experimentation. 
- **Cultural Shift:** Ownership gets claimed, not assigned. Focus on delivering value, not completing assignments.

--

#### Data as a product cont
- **Strategic asset**: Data is a core product, not a byproduct of operations.
- **Quality focus**: Data products are usable, understandable, correct, timely, and complete.
- **Lifecycle Management**: Data products are managed through their entire lifecycle, from creation to retirement.
    
---

#### 3. Self-Serve Data Infrastructure 

*'This principle aims to provide a platform that enables domain teams to easily create, maintain and use data products.'*

--

- **Unified Platform:** Provides domain-agnostic tools and systems, empowering users to autonomously develop and manage products.

--

- **Ease of Use:** Low barrier for adoption, allowing users to find, understand, and manage data products with built-in affordance.

--

- **Virtualization:** Data is virtualized rather than centralized—addressable and decentralized.

--

- **Flexibility**: The platform evolves based on domain requirements, balancing centralized infrastructure with domain-specific needs.

---

#### 4. Federated Computational Governance

'*This principle ensures interoperability and consistency across the decentralized data ecosystem.*'

--

- **Global Standards**: Establishes organization-wide standards for data. Required metadata and conventions.
        
        namespace: prod | preprod | test
        owner: group | person
        linage: data & execution
        format: structured | unstructured,         
        complexity: simple | complex 
        structure:  lot | set | appendstructure
        lifecycle events
        tombstoning | inits
        authorization/authentication

--

- **Automated Enforcement**: Governance rules are computationally enforced, reducing manual oversight.

--

- **Balance**: Strikes a balance between centralized control and domain autonomy

---

#### Summary:
*These principles work together to create a data ecosystem that is scalable, flexible, and aligned with business needs. The domain-oriented approach and data-as-a-product mindset address issues of data quality and relevance. The self-serve infrastructure enables efficient data product creation and consumption. Federated governance ensures that this decentralized system remains cohesive and compliant.*

---

#### DataMesh vs Data Lakes
*   **Shifting data ownership**: From centralized teams to domain experts, leading to better data quality and governance.

*   **Data Modeling**: From generic models accommodating all use cases to specific models reflecting each domain's unique needs and language.


--

#### DataMesh vs Data Lakes cont
*   **Decoupling data pipelines**: From centralized control into smaller, domain-specific units, allowing for agile development and domain-specific innovation.

*   **Emphasizing data as a product**: From central team responsible for data quality to domain teams focusing on delivering high-quality, discoverable data products.

--

#### DataMesh vs Data Lakes cont

*   **Providing self-service infrastructure**: Empowers domain teams to manage their data products independently. 

---


#### Organisational and cultural shifts
*'A distributed approach promotes scalability, agility and data quality by empowering domain teams and fostering a data-driven culture. Data mesh recognizes that data is not a monolithic entity but rather a collection of interconnected, domain-specific datasets that can be best managed by those closest to them.*'

--

### Nb
Not only an architectical shift. Far from it. Everyone participates. Benifits and contributes.

---

#### Data Certitude
    Raw data
    Cureated data: Accuracy, relevant representation. 
    Authoritative data: Relevant, traceble, complete, consistent, documented. 
![Data Mesh Architecture](./pics/data_certitude.svg)

---

### Success stories

JP Morgan | Saxo Bank | Intuit | Paypal

[many](https://github.com/lynxoskar/data_mesh/blob/main/sources/perplexity_success_stories.md)

--

[Paypal](https://github.com/lynxoskar/data_mesh/blob/main/sources/perplexity_success_paypal.md)

'*Scalability: PayPal started with 6 data products and rapidly expanded to about 40, with plans to add many more. This demonstrates the scalability of the data mesh approach*'

--

'*Better regulatory compliance and data security: The decentralized nature of data mesh allowed for improved compliance and security measures*'

'*Autonomy for data domains: The data mesh provided greater autonomy for different data domains within PayPal, allowing them to manage their own data pipelines*'

---

### Culture Mind shift

*'Data Mesh adoption is an evolving process. While the technology is largely available, the greater challenge lies in the cultural and organizational shifts required for successful implementation. Many organizations are taking an incremental approach, starting with specific data products and gradually expanding their mesh over time.'*

--

*'The transition from a traditional system of records to a data pipeline/data product system is a significant undertaking that requires a holistic approach to organizational change. It involves not just technological shifts but also fundamental changes in how people think about, manage, and use data. Success in this transition depends on strong leadership, clear communication, and a sustained commitment to building a data-driven culture across the entire organization.'*

--

### Key Factors for Successful Transition:
1. **Mindset Shift:**
    - From viewing data as a byproduct to treating it as a valuable product
    - Embracing decentralization and domain ownership

--

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
'*Every member will be limited only by curiosity, vision, taste, and creativity.*'


--

### Importance of Data Products in the Age of AI:

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






---

### Appendix; components


**Key Components:**

- **Data Governance Systems**
- **Data Catalogs**
- **Storage Solutions**
- **Execution Governance**
- **Execution Systems**

--

#### Companies Providing Comprehensive Platforms

[Starburst](https://www.starburst.io/)
    - Built on open-source technologies
    - Provides analytics engine for Data Mesh 

[atlan](https://atlan.com/?ref=/p/data-catalog-data-mesh/)
    - Data catalog and metadata management
    - Facilitates data discovery and collaboration

[K2View](https://www.k2view.com/)
    - Data-as-product management with domain-oriented ownership
    - Offers self-service capabilities

--

[DataBricks](https://www.databricks.com/)
    - Unified data analytics platform built on Apache Spark 
    - Lakehouse architecture combining data lake and data warehouse capabilities
    - Supports data engineering, data science, and machine learning workflows
    - Delta Lake for ACID transactions on data lakes
    - Collaborative notebooks for data analysis and visualization
        
--

[Danodo](https://www.denodo.com/)
    - Data virtualization and integration platform
    - Enables real-time data access without replication

[Data Mesh Manager](https://www.datamesh-manager.com/)
    - Specialized tools for managing Data Mesh architectures
    - Focuses on governance and domain management

--

[Snowflake](www.snowflake.com/)
    - Cloud-based data warehousing platform
    - Separation of storage and compute for scalability
    - Supports structured and semi-structured data
    - Easy data sharing and collaboration
    - Strong SQL support optimized for analytics queries

---


#### Data Catalogues (data, metadata, events)
[Linkedins Datahub](https://datahubproject.io/)
    - Open-source metadata platform
    - Facilitates data discovery and lineage tracking

[Apache Atlas](https://atlas.apache.org/#/)
    - Open-source metadata management and governance
    - Integrates with Hadoop ecosystem

[Amundsen](https://www.amundsen.io/)
    - Data discovery and metadata engine
    - Developed by Lyft for data cataloging


[Netflix Metacat](https://github.com/Netflix/metacat)
    - Unified metadata management system
    - Makes big data discoverable and meaningful

[info](https://netflixtechblog.com/metacat-making-big-data-discoverable-and-meaningful-at-netflix-56fb36a53520)

---

#### Workflow orchestration systems, execution governance. 
[Estuary](https://estuary.dev/)
    - Real-time data operations platform
    - Supports real-time data integration and ETL
    - Handles streaming and batch data processing
    - Manages schema evolution and data quality

--

[Airflow](https://airflow.apache.org/)
    - Platform to programmatically author, schedule, and monitor workflows
    - Widely used for orchestrating complex data pipelines

[Dagster](https://dagster.io/)
    - Data orchestrator for machine learning, analytics, and ETL
    - Emphasizes software-defined data assets

[Luigi](https://github.com/spotify/luigi)
    - Python module for building complex pipelines
    - Handles dependency resolution and workflow management

--

[Kubelow](https://www.kubeflow.org/)
    - Machine learning toolkit for Kubernetes
    - Facilitates deployment of scalable ML workflows

[Prefect](https://www.prefect.io/)
    - Modern workflow orchestration tool
    - Focuses on dataflow and task scheduling

[Netflix, meastro](https://github.com/Netflix/maestro)
    - Workflow orchestrator for big data jobs
    - Manages job dependencies and scheduling

[Argo workflows](https://argoproj.github.io/workflows/)
    - Container-native workflow engine for Kubernetes
    - Executes DAGs of tasks using Kubernetes resources

---

# FIN




