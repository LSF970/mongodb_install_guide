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

## Using Atlas

Make a new organisation and make a project inside it. You will then be greeted with this page:

![Alt Text](./images/atlas_homepage.jpg)

### Making a Cluster

![Alt Text](./images/create_a_cluster.jpg)

## Security setup

User:
![Alt Text](./images/security_quickstart.jpg)

I.P:
![Alt Text](./images/security_quickstart_ip.jpg)


## Cluster Created!

![Alt Text](./images/cluster_created.jpg)


## Load Sample data into the new DB

![Alt Text](./images/load_sample_dataset.jpg)

## Connecct to Atlas DB:

Click 'Connect' when viewing your database

![Alt Text](./images/connecting_to_atlas.jpg)

We can easily use any of these. Let's use Compass first:

Take the URI to connect and paste it your compass connection. Make sure to change the password part of the URI to your password (remove the <> too).

![Alt Text](./images/atlas_local_connection.jpg)

![Alt Text](./images/atlas_connected.jpg)

## Mongo CRUD

Create, Remove, Update, Delete

First, get the connection command from Atlas for Mongosh. Paste it in your terminal of choice.

It should ask for your password. Enter it and you should then be connected:

![Alt Text](./images/atlas_shell_connection.jpg)

- `show databases` to see all the databses available
- `use database` switches to using a particular db (so `use sparta_db`)
- `show collections`

### Make a new collection

If you do db.collection and the collection does not exist, mongo will create it. Be careful!

## Insert (Create)

Simply use the collection you want to use, and then insertOne. See below for syntax

```
db.trainers.insertOne({firstname: "Luke", Surname: "Fairbrass", department: "DevOps", "Data"})
```

```
db.trainers.insertOne({firstname: "Alan", Surname: "Gulle", department: "Data"})
```

## SELECT * FROM TRAINERS

Simlpy use .find() to see everything in the collection (table)
`db.trainers.find()`

## Insert Many

```db.learners.insert```

Will ask if you want One or Many. For many:

```
db.learners.insertMany([{firstname: "Andre"}, {firstname:"Joy"}])
```
![Alt Text](./images/adding_to_collecction.jpg)

Lets see the changes on Atlas:

![Alt Text](./images/changes_on_atlas.jpg)




