## Comparing Data Products and Systems of Record

**Data products** and **systems of record** serve distinct purposes within an organization's data landscape. Contrasting their characteristics and weighing their pros and cons can help you understand their respective roles and how they can work together to support data-driven decision-making.

### Systems of Record (SOR)

* **Purpose:** Systems of record primarily serve operational needs. They are **designed to capture, store, and manage transactional data that is essential for running the business.** This data is often structured and relational, residing in databases behind business capabilities served with microservices.
* **Focus:** SORs prioritize data accuracy, consistency, and availability for real-time operational use.


### Data Products

* **Purpose:** Data products are **designed for analytical consumption**, aiming to **provide insights, support decision-making, and enable data-driven applications.** They focus on historical and aggregated views of business facts over time, often tailored to specific use cases. 
* **Focus:** Data products prioritize data quality, discoverability, understandability, and usability for consumers such as data scientists and analysts.


### Pros and Cons

| Feature        | System of Record               | Data Product                     |
| -------------- | ----------------------------- | -------------------------------- |
| **Data Focus** | Transactional, operational data | Analytical, historical data       |
| **Purpose**    | Operational efficiency         | Data-driven insights & decisions |
| **Accuracy**    | High, real-time updates        | High, but may have some latency  |
| **Structure**   | Structured, relational         | Polyglot, diverse formats        |
| **Ownership**   | Centralized, IT-driven        | Decentralized, domain-driven    |
| **Accessibility** | Limited to operational users  | Broad, self-service access        |

### Key Differences and Considerations

**Ownership and Accessibility:** While SORs are typically owned and managed centrally by IT departments, **data mesh promotes decentralized ownership of data products by domain experts.** This fosters data democratization and allows for faster iteration and innovation.  Data products are designed to be discoverable and accessible through self-service mechanisms like data catalogs, empowering a wider range of users to leverage data for their needs.

**Data Transformation and Context:** Data in systems of record often requires transformation and enrichment to become valuable for analytical purposes. **Data products encapsulate the necessary logic and processing to deliver data in a ready-to-use format for specific consumers.**

**Data as a Product Mindset:**  Shifting to a data-as-a-product mindset requires a cultural change within an organization. **Treating data as a product means focusing on the needs of data consumers, ensuring data quality, and fostering a culture of continuous improvement.**

### Interplay and Synergy

Systems of record and data products are not mutually exclusive. They can **work in tandem to create a comprehensive data ecosystem**. SORs provide the foundational data that fuels data products. In a data mesh architecture, data products can act as an abstraction layer on top of systems of record, delivering domain-specific insights and value to data consumers.

### Examples from Sources

* **Domain-Oriented Data Ownership:** In the media streaming example from the sources, instead of a centralized data platform ingesting and managing all data, the "player domain" could own and serve its datasets, such as play events, as a data product for consumption by other domains.
* **Data Product Qualities:** The sources emphasize the importance of making data products discoverable, addressable, trustworthy, self-describing, interoperable, and secure. These qualities ensure that data products are valuable and usable for their intended consumers.

By understanding the differences and interplay between data products and systems of record, organizations can create a more efficient, scalable, and data-driven environment that empowers all stakeholders to unlock the full potential of their data. 
