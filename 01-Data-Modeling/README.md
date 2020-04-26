# Data Modeling


## What is a Data Model ?

The process of creating data models for an information system.

## Data Modeling process

> Process to support business and user aplications

> Gather Requirements

> Conceptual Data Modeling

> Logical Data Modeling using the concept of tables, schemas, and columns

> Physical Data Modeling.


### Common Questions

#### Why can't everything be stored in a giant Excel spreadsheet?
gi
There are limitations to the amount of data that can be stored in an Excel sheet. So, a database helps organize the elements into tables - rows and columns, etc. Also reading and writing operations on a large scale is not possible with an Excel sheet, so it's better to use a database to handle most business functions.

#### Does data modeling happen before you create a database, or is it an iterative process?

It's definitely an iterative process. Data engineers continually reorganize, restructure, and optimize data models to fit the needs of the organization.

#### How is data modeling different from machine learning modeling?

Machine learning includes a lot of data wrangling to create the inputs for machine learning models, but data modeling is more about how to structure data to be used by different people within an organization. You can think of data modeling as the process of designing data and making it available to machine learning engineers, data scientists, business analytics, etc., so they can make use of it easily.

### QUIZ 1

True or False: A column holds multiple tables (False).
True or False: An attribute is another name for a column(True). 
True or False: A schema is a collection of tables in some database terminology(True).


### ACID Transactions

> Atomicity: The whole transaction is processed or nothing is processed. A commonly cited example of an atomic transaction is money transactions between two bank accounts. The transaction of transferring money from one account to the other is made up of two operations. First, you have to withdraw money in one account, and second you have to save the withdrawn money to the second account. An atomic transaction, i.e., when either all operations occur or nothing occurs, keeps the database in a consistent state. This ensures that if either of those two operations (withdrawing money from the 1st account or saving the money to the 2nd account) fail, the money is neither lost nor created. 

> Consistency: Only transactions that abide by constraints and rules are written into the database, otherwise the database keeps the previous state. The data should be correct across all rows and tables. Check out additional information about consistency on Wikipedia.

> Isolation: Transactions are processed independently and securely, order does not matter. A low level of isolation enables many users to access the data simultaneously, however this also increases the possibilities of concurrency effects (e.g., dirty reads or lost updates). On the other hand, a high level of isolation reduces these chances of concurrency effects, but also uses more system resources and transactions blocking each other. 

> Durability: Completed transactions are saved to database even in cases of system failure. A commonly cited example includes tracking flight seat bookings. So once the flight booking records a confirmed seat booking, the seat remains booked even if a system failure occurs.

### When Not to Use a Relational Database.

> Have large amounts of data: Relational Databases are not distributed databases and because of this they can only scale vertically by adding more storage in the machine itself. You are limited by how much you can scale and how much data you can store on one machine. You cannot add more machines like you can in NoSQL databases.

> Need to be able to store different data type formats: Relational databases are not designed to handle unstructured data.
Need high throughput -- fast reads: While ACID transactions bring benefits, they also slow down the process of reading and writing data. If you need very fast reads and writes, using a relational database may not suit your needs.

> Need a flexible schema: Flexible schema can allow for columns to be added that do not have to be used by every row, saving disk space.

> Need high availability: The fact that relational databases are not distributed (and even when they are, they have a coordinator/worker architecture), they have a single point of failure. When that database goes down, a fail-over to a backup system occurs and takes time.

> Need horizontal scalability: Horizontal scalability is the ability to add more machines or nodes to a system to increase performance and space for data.





