---
title: "CAP Theorem"
date: 2022-03-17T00:24:24+09:00
draft: true
authorImage: "images/ProfilePic.jpg"
---

CAP Theorem states that a distributed system can only satisfy 2 out of 3 properties simultaneously.

C = Consistency 
In a Consistent system, all nodes see same data and will return same, most recent write.

A = Availability
It means that a system will be available all the time, regardless that some nodes are down or all nodes don't have same data.

P = Partition Tolerance
It means even if communication between nodes break, system will continue to work. 

CA db
- No practical use
- Example: PostgreSQL

CP db
- Example: MongoDB
- Turn off nodes with don't have same data.

AP db
- Example: Apache Cassandra
- Returned data might not be the most up-to-date from every node incase of fault
