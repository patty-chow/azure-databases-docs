---
ms.service: azure-storage
ms.topic: include
ms.date: 08/23/2024
---
If you currently use Azure Table Storage, you gain the following benefits by moving to Azure Cosmos DB for Table:

|Feature | Azure Table Storage | Azure Cosmos DB for Table |
| --- | --- | --- |
| Latency | Fast, but no upper bounds on latency. | Single-digit millisecond latency for reads and writes, backed with <10-ms latency reads and <15-ms latency writes at the 99th percentile, at any scale, anywhere in the world. |
| Throughput | Variable throughput model. Tables have a scalability limit of 20,000 operations per second. | Highly scalable with [dedicated reserved throughput per table](../request-units.md) that's backed by SLAs. Accounts have no upper limit on throughput and support >10 million operations per second per table in provisioned throughput mode. |
| Global distribution | Single region with one optional readable secondary read region for high availability that supports automatic and manual account failover. | [Turnkey global distribution](../distribute-data-globally.md) from one to 30+ regions. Support for [service-managed and manual failovers](../high-availability.md) at any time, anywhere in the world. |
| Indexing | Only primary index on `PartitionKey` and `RowKey`. No secondary indexes. | Automatic and complete indexing on all properties, no index management. |
| Query | Query execution uses index for primary key, and scans otherwise. | Queries can take advantage of automatic indexing on properties for fast query times. |
| Consistency | Strong within primary region. Eventual within secondary region. | [Five well-defined consistency levels](../consistency-levels.md) to trade off availability, latency, throughput, and consistency based on your application needs. |
| Pricing | Consumption-based. | Available in both [consumption-based](../serverless.md) and [provisioned capacity](../set-throughput.md) modes. |
| SLAs | 99.99% availability. | 99.99% availability SLA for all single region accounts and all multi-region accounts with relaxed consistency, and 99.999% read availability on all multi-region database accounts [Industry-leading comprehensive SLAs](https://azure.microsoft.com/support/legal/sla/cosmos-db/) on general availability. |
