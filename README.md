# SQLLite-Database
My current SQLite clone operates by transforming SQL queries into bytecode, which is then executed by a custom virtual machine. It utilizes a B-Tree data structure to efficiently perform operations such as searches, inserts, and deletes. The B-Tree structure ensures O(log n) performance. Data storage is organized into pages constisting of serialized rows of data. Fields for an ID, username, and email are included. Pages are cached in memory and managed by a Pager, which handles reading from and writing to the disk, ensuring that the database is efficiently managed as it grows.

The system supports basic SQL commands like INSERT and SELECT, with a custom implementation of parsing for and executing these commands. The INSERT operation adds new rows to the database, while SELECT retrieves and prints them. The rows are stored in the leaf and internal nodes of the B-Tree, resulting in structured data retrieval.  

This clone also includes functionality for managing cache misses through the get_page function, which dynamically allocates memory for new pages when needed. Mechanisms for handling full pages, such as splitting leaf nodes to maintain the B-Tree balance and performance, are used. The project is built with exception handling for various stages, ensuring robustness against errors such as syntax issues. 

Overall, the goal of the SQLite clone is to provide a foundational understanding of the workings of a database, focusing on efficient data storage, retrieval, and management.
