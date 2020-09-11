# Database Types

By order of complexity.

1. Key Value  
Like for example `Redis`. Only stores `key-value` pairs, with two commands `get` and `set`. Extremely fast, does not store info on the disk but on the `RAM`.

2. Wide Column  
Like for example `Cassandra`. Adds a new dimension to the value part of the key value database, where you can store tuples of values for every key. Extremely fast and flexible, does not have a `schema` so operations such as `JOIN` are not permited. It's decentralized and scales horizontally. Very useful to access time sorted data such as Twits.

3. Document based db
Like for example `MongoDB` or `Firebase`. All information is stored in `documents`, which makes it extremely easy to read and very flexible for the developer. Whenever there is a complex flow for writing data, such as in social apps, these databases are far from ideal.

4. Ralational databases
Like for example `MySQL` or `PostgreSQL`. Based on the papers and research of `Ted Codd`, who developed enourmously the theories of relational data models, which is a math and science body of knowledge on itself. One of the most important concepts is that of the `Primary Key` and the `Foreign Keys`, used to relate data. Also it requires a `Schema` that defines the structure of the database.

5. Graph database
Entities are represented by nodes connected by vertex. Really good for complex `JOIN` logics, where relational db performance has started to suffer.

6. Search database
Most of the implementations are on top of the `Apache Luceene` project, like `Solr` and `ElasticSearch`, there are cloud-based options like `Algolia` and `meilisearch`, developed in `Rust`. From a developer perspective, they work similarly to a document based database, but under the hood, they will analise large sets of texts and generate indexes to access portions of these text in a very fast and effective way. They are expensive to run at scale, but add a ton of value to the user.

7. Multi-Model database
Like for example `GraphQL` or `Fauna`. You only describe how you want to access your data, then under the hood it takes advantage of multiple database paradigms, and determining at run time how to leverage these paradigms in order to produce the queried information.
