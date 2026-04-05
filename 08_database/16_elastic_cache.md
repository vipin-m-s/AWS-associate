- It is a managed in memeory database.
- It is used for caching purposes to reduce load on the data base.
- It is used for high performance, low latency storage
- There are 3 stratregies for caching
  - lazy loading :-
    - 1. Check if data exists in cache
      2. If not, fetch the data from db
      3. Write the data to cache
  - Write through :-
    1. Write data to cache when writing data to db
    2. High chance that data is present in cache
  - TTL :-
    - there will be a ttl attached to the data
    - It will expire afetr ttl
- AWS supports multiple cache engines
  - redis oss -> Feature rich, global databsae, replication
  - Memcached -> High performance, multi threaded
  - walkey ->  compatible with opern source redis to avoid license of redis

# Difference between redis and memcached
- persistence :- redis offers persistence/replication/automatic backup. Memachde no persistence, no backups
- Multi AZ :- redis supports multi az, whereas memcahced does not
- global database :- redis supports global read , fail over. Memcached does not support
- Auth :- reids has inbuilt auth, memcahched does not support
- encyrption :- redis has encryption at rest and transsit . memcached does not support encryption at rest. Minimal encryption at transit.
- Replication:- redis has replication. memcached does not support repliocation
- Use case :- redis - session store, pub sub. memcached - simple key/value caching, multi threaded, high performance
- both supports vpc, subnet, security group and route table rule. 
