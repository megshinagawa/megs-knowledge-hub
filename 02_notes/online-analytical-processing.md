---
datecreated: 2025-12-26
topicaltags:
  - "[[04_tags/dev|dev]]"
  - "[[04_tags/systems|systems]]"
---
# ONLINE ANALYTICAL PROCESSING

Online Analytical Processing (OLAP) system allows for speedy analysis by processing vast historical data sets. 

- Data structure: Denormalized, columnar, or multidimensional to minimize the number of joins required for complex queries
- Transaction type: Mainly large, complex read operations to calculate aggregates but when writing, it's often done in large batches
- Purpose: Speedy analysis by processing vast historical data sets