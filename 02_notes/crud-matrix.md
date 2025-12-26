---
datecreated: 2025-12-25T09:40:00
topicaltags:
  - "[[04_tags/business|business]]"
  - "[[04_tags/dev|dev]]"
---
# CRUD MATRIX

CRUD Matrix is a high-level planning document used by architects and business analysts to map out how different parts of a system interact with data. 

## What is CRUD?

CRUD refers to the four basic functions of persistent storage.

| **Initial** | **Operation** | **Action**                            | **SQL Equivalent** |
| ----------- | ------------- | ------------------------------------- | ------------------ |
| **C**       | **Create**    | Adding a new record or entry          | `INSERT`           |
| **R**       | **Read**      | Viewing or retrieving existing data   | `SELECT`           |
| **U**       | **Update**    | Modifying or editing existing records | `UPDATE`           |
| **D**       | **Delete**    | Removing data from the system         | `DELETE`           |
## Key Vocabulary

- User Roles: Specific **category** of person interacting with the system (eg: Analysts, Project Managers)
- System Processes: Automated task or background service that interacts with data **without direct human intervention** (eg: Nightly batch backup script, Daily late fee calculator)
- Data Entities: Object that your system needs to store information about (eg: Book, Member, Author)
- Data Lifecycle: The entire "life" of a piece of data, from the moment it is first entered (Create) to its final removal (Delete)
- Orphaned Data: records that remain in a system but have lost their connection to a parent record, or data that is unreachable because the logic to access it is missing

## What is a CRUD Matrix?

CRUD Matrix often lists User Roles or System Processes on one axis and Data Entities on the other. The cells indicate which operations the role/process can perform on the data.

| **Role / Entity** | **Data 1** | **Data 2** | **Data 3** | **Data 4** |
| ----------------- | ---------- | ---------- | ---------- | ---------- |
| **Role 1**        | C          | R          | —          | R          |
| **Role 2**        | R, U       | R          | C, R       | C, R, U, D |
| **Process 1**     | R, U, D    | C, R, U, D | R, U       | R, D       |
| **Process 2**     | —          | —          | U          | —          |
## How to Create a CRUD Matrix

1. Identify your data entities
2. Identify your user roles and system processes
3. Map the interactions
4. Validate the lifecycle by checking for orphaned data