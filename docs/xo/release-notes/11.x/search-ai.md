# Search AI Updates

This document provides information on the feature updates and enhancements introduced in **Search AI** of XO v11.x releases.

## v11.3.0 June 29, 2024

<u> Patch Release </u>

Key features and enhancements included in this release are summarized below.

### Support for Filtered Content Ingestion from third-party applications

Search AI now extends support for content ingestion from a wider variety of third-party applications, including Confluence Cloud, Azure Storage, Salesforce, Oracle Knowledge, and dotCMS, in addition to the existing connectors. The connectors now offer customizable filters that give platform users the flexibility to selectively ingest data, allowing for precise and targeted indexing and enhancing the search index's efficiency and accuracy.

### Advanced Web Crawl Configurations

Search AI now offers advanced web crawl capabilities that allow platform users to remove redundant sections of a web page while indexing. Also, for JavaScript-rendered pages, the users can now introduce a delay after which the crawler starts indexing the page, allowing all dynamic content to load properly. These enhancements provide greater control and precision in web crawling, leading to a more efficient and accurate search experience.

<hr>

## v11.2.1 June 15, 2024

<u>Patch Release</u>

Key features and enhancements included in this release are summarized below.

###  Automated Content Syncing and Training with Connectors

Search AI now offers the capability to schedule automatic content syncing from third-party applications using connectors. The data is automatically ingested, and the application is trained with the new data, ensuring that the content is always up to date.

###  Enhanced Web Crawl Error Reporting

The enhanced web crawl error reporting feature in Search AI provides detailed information about crawl failures, enabling quick identification and resolution of issues. 


<hr>

## v11.2 June 01, 2024

<u>Patch Release</u>

Key features and enhancements included in this release are summarized below.

###  Support for Hybrid Chunk Retrieval Strategy

Search AI now supports the Hybrid Chunk Retrieval strategy, which leverages both keyword-based and semantic search techniques to deliver more precise and contextually appropriate answers. This improvement ensures that users receive high-quality responses tailored to their queries, enhancing the overall search experience.

###  Chunk Order Configuration 

Search AI now allows adding relevant chunks in your preferred order within the prompt. The order of the chunks in the prompt can affect the performance depending upon the LLM limitations of context retention, prompt lengths, and attention mechanism. By allowing users to configure the chunk order, SearchAI ensures that relevant data is prioritized, improving the generated responses' quality and reliability.

<hr>

## v11.1.1 May 11, 2024

<u>Patch Release</u>

This update includes feature enhancements and bug fixes. Key enhancement included in this release is summarized below.

### Extended Connector Support

In addition to the existing ServiceNow connector, Search AI now supports more knowledge base connectors, including Zendesk, Confluence Server, Google Drive, and Dropbox. The new connectors make it easier to integrate Search AI with these platforms, helping users quickly find and access information to boost productivity. [Learn more :octicons-arrow-right-24:](../../searchai/content-sources/connectors.md)

<hr>

## v11.1.0 April 27, 2024

<u>Minor Release</u>

This update includes feature enhancements and bug fixes. Key feature included in this release is summarized below.

### Business Rules Support

Business Rules Support allows users to define custom rules that modify the answers provided by the AI search system. By using contextual data specific to their needs, users can create tailored rules to refine the AI's responses. The system also suggests relevant context variables dynamically to assist in defining these rules. [Learn more :octicons-arrow-right-24:](../../searchai/business-rules.md)
