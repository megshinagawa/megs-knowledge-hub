---
datecreated: 2025-12-24
topicaltags:
  - "[[04_tags/business|business]]"
  - "[[04_tags/dev|dev]]"
---
# ENTITY RELATIONSHIP DIAGRAM

Entity Relationship diagrams, also known as ER diagrams, are specialized flowcharts that illustrate how "entities" relate to each other within a system

## Types 

- Conceptual (概念)
	- High level view of business concepts (entities) and their relationships
	- Used to explain data scope to business analysts and stakeholders 
- Logical (論理)
	- Focuses on depicting detailed data structure with attributes and keys but does not rely on any specific database
	- Used by data architects and developers to define data structures 
- Physical (物理)
	- Implementation specific database design blueprint
	- Used by developers to actually build the database

## Key Vocabulary

- Entities: Core objects that need to be tracked within a system
	- Denoted by rectangle in conceptual ERs
	- Examples: Customer, Order, Product, Employee
- Weak Entities: Objects that cannot exist without a parent entity
	- Denoted by double rectangle in conceptual ERs
	- Example: Order Item cannot exist without Order
- Attributes: Specific data points that describe each entity
	- Primary Key (PK): The most important attribute that uniquely identifies each record
	- Foreign Key (FK): Key that provides a like between data in two tables and often points to the PK of another table
	- Multivalued Attributes: Entities that can have more than one value for a category
	- Derived Attributes: Values calculated from other data
- Relationships: Defines how your entities interact with each other
	- Recursive Relationship: If an entity relates to itself, the line loops back to the same entity
- Cardinality: Specifies how many instances of one entity are associated with another
	- Numerical (Chen Notation):Placing "1" and "N" or "M" next to entities to show relationships like 1:N (one to many)
	- [[02_notes/crows-foot-notation|Crow's Foot Notation]]: A visual style where a three-pronged "crow's foot" at the end of a line indicates "many"

## How to Draw an ER Diagram

1. Identify your audience and scope to determine what kind of ER diagram you'll draw
2. Identify your entities (nouns)
3. Add attributes to your entities (description)
4. Establish relationships (verbs)
5. Define cardinality if relevant

## Denotation Cheat Sheet 

| Object                | Conceptual       | Logical                           | Physical                                     |
| --------------------- | ---------------- | --------------------------------- | -------------------------------------------- |
| Entities              | Rectangle        | Rectangle or Table                | Tables                                       |
| Weak Entities         | Double Rectangle | Rectangle                         | Table including Foreign Key                  |
| Attributes            | Oval             | Listed inside rectangle or table  | Listed in table with specific data types     |
| Primary Key           | Underlined       | Listed at the top with a PK label | Column marked as PK with defined constraints |
| Multivalued Attribute | Double Oval      | Separate linked entity/table      | Separate table with FK back to parent        |
| Derived Attribute     | Dashed Oval      | Omitted or marked as calculated   | Omitted                                      |
| Cardinality           | Chen Notation    | Crow's Foot Notation              | Crow's Foot Notation                         |

