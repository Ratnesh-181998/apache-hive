
# Apache-hive

Apache Hive is a distributed data warehouse system built on top of Apache Hadoop. It allows you to read, write, and manage petabytes of structured and semi-structured data using a SQL-like language called HiveQL (HQL)

- https://github.com/apache/hive

# Key FeaturesSQL Accessibility: 
- Translates HiveQL queries into MapReduce, Apache Tez, or Apache Spark jobs, allowing analysts to query massive datasets without writing Java
- Schema-on-Read: Imposes structure onto raw data files only when they are read, allowing for extreme flexibility in data ingestion.
- Optimizations: Supports partitioning and bucketing to speed up query execution by only scanning relevant subsets of data.
- Data Management: Catalogs data schemas and provides integrations with other processing tools in the big data ecosystem (like Apache Pig, Spark, and Impala)


# Core Architecture 

## Hive consists of a few major components that work together to translate queries into distributed compute jobs:

- Metastore: The central repository that stores the metadata, schema definitions, table structures, and partition details.
- Driver: Manages the lifecycle of a HiveQL statement, parsing the query, compiling it into an execution plan, and scheduling tasks.
- Execution Engines: Translates the execution plan into tasks executed across a distributed compute framework like Hadoop YARN.
