Title | 001: Decision to choose a DB 
--- | --- 
Status | Accepted
Context | Our project involves real time updates to product information system, requiring a reliable and performant and scalable DB. Relational (postgres) vs No-SQL (cassandra) was evaluated
Decision | After thorough evaluation, we choose `Cassandra` as the DB. Rationale: Postgres supports complex queries and joins, ACID compliance and can handle high volume of reads. Cassandra can handle high volume of writes and is designed for high availability and massive scalability. Postgres is strongly consistent whereas Cassandra is eventually consistent. Cassandra is also inherently horizontally scalable compared to postgres. Since we expect high traffic, massive growth, low-latency, and need a distributed database with high availability and horizontal scaling out of the box and are fine with eventual consistency, cassandra is a better choice.
Consequences | We will achieve low latency and would be able to handle load however it might cost us a bit more. 
