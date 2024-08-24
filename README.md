# SQLLite-Database
My current SQLite clone uses a B-Tree data structure to efficiently perform operations in O(log n) time. Operations supported include searches, inserts, and deletions. Data is organized into pages that consist of serialized rows and each row includes a field for an ID, username, and email. The pages are cached in the memory and through the use of the get_page function, memory is dynamically allocated to grow the database when required. 

Currently, basic SQL commands are supported, such as INSERT and SELECT. INSERT allows new rows to be added to the database, while SELECT retrieves the rows and prints them to the console. Data is stored in the nodes of the B-Tree, which allow for efficient data retrieval. The project was built with exception handling at various stages to ensure robust functionality. 

Overall, the goal of the SQLite clone is to provide a foundational understanding of the workings of a database, focusing on efficient data storage, retrieval, and management.
