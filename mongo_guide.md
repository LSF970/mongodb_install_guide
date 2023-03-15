## MongoDB Guide

### What is NoSQL?

- Umbrella term, to refer to any datbase systems that do not primarily run on SQL.

### MongoDB

General purpose Document database with the scalability and flexibility that you want with the querying and indexing that you need.

Stores **JSON-like documents** that allow you to store data with flexible schema while still being able to query, aggregate and more (for analyise access and analysis).

- MongoDB (Local)
- MongoDB Atlas (Multi-Cloud Platform)
- MongoDB Compass (GUI interface for Mongo)

### Common NoSQL DB types

- Key-Value
- Column-Family
- Graph
- Document (MongoDB)

>LEARN MORE: https://www.mongodb.com/scale/types-of-nosql-databases

### What is a Document database?

Document (basic unit of data in MongoDB):

```bson
{
    "_id": "302439049230vi00weuv0wu01",
    "firstname": "Jane",
    "lastname":  "Wi",
    "address": {
        "street": "1 Circle Rd,
        "city": "Los Angeles",
        "state": "CA",
        "zip": "90404"
    }
    "hobbies": ["surfing", "coding"]
}
```

MongoDB Database (Can contain one or more collections)<br>
      -> Collections (Can contain multiple documents)<br>
          -> Document (Key value pair list or array or nested document)