---

theme : sky
---

## Comparing Data Mesh, Pipelines, Systems of Record, and Siloed Sources of Truth
The sources describe **data mesh** as a **decentralized data architecture** that breaks down monolithic data platforms into smaller, domain-oriented data products. These products are owned and managed by teams with deep domain knowledge, promoting data quality and agility.

--

In contrast, traditional **data pipelines** are often designed around a **centralized data platform**, like a data lake or data warehouse, with data flowing through a series of ingestion, cleansing, and transformation stages. This centralized approach can struggle to scale as data volume and diversity grow, and it can lead to slow delivery of new data products due to tight coupling between pipeline stages.

--

**Systems of record**, on the other hand, represent the **operational systems** that capture and manage the **core transactional data of a business**, such as customer information, orders, or inventory. They are typically designed for high-volume, transactional operations and prioritize data consistency and integrity for operational purposes.

--

**Siloed sources of truth** refer to situations where **data is fragmented and isolated** within different departments or systems, often due to a lack of data sharing and integration. This makes it difficult to gain a holistic view of the data and can lead to inconsistencies and challenges in data analysis and decision-making.

--

Here's a comparison table summarizing these concepts:
| Feature                 | Data Mesh                                    | Pipelines                                     | Systems of Record                | Siloed Sources of Truth             |
| ----------------------- | -------------------------------------------- | -------------------------------------------- | --------------------------------- | ------------------------------------ |
| Architecture           | Decentralized, domain-oriented               | Centralized, pipeline-based                  | Typically centralized             | Fragmented, isolated                 |
| Data Ownership         | Distributed, domain-specific                | Often centralized                           | Defined by system boundaries       | Scattered, unclear ownership          |
| Focus                  | Data products as value units                 | Data flow and processing stages             | Transactional data consistency    | Limited data sharing and integration |
| Scalability             | High, through distributed ownership         | Limited by central platform                 | Dependent on specific system      | Low, hindered by silos              |
| Data Quality           | Emphasized through product thinking          | Dependent on centralized cleansing           | Critical for operational integrity | Inconsistent, prone to errors        |
| Agility                | High, through domain autonomy               | Limited by pipeline coupling                | Dependent on system architecture | Low, hampered by data isolation    

---
 |
### Data Mesh vs. Traditional Approaches
Data mesh aims to address the limitations of traditional data management approaches by:
*   **Shifting data ownership**: From centralized teams to domain experts who understand the data best, leading to better data quality and governance.
*   **Decoupling data pipelines**: Into smaller, domain-specific units, allowing for more agile development and deployment of data products.
*   **Emphasizing data as a product**: Encourages domain teams to focus on delivering value to data consumers through high-quality, discoverable data products.
*   **Providing self-service infrastructure**: Empowers domain teams to manage their data products independently, promoting agility and innovation.
This distributed approach promotes scalability, agility, and data quality by empowering domain teams and fostering a data-driven culture. Data mesh recognizes that data is not a monolithic entity but rather a collection of interconnected, domain-specific datasets that can be best managed by those closest to them.