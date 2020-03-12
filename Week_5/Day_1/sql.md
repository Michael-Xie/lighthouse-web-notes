# SQL Intro

## Why are databases important?

- Efficient reading/writing of the data
- Security
	- Not anyone can just access/change data
- Redundancy
	- multiple stores with the same data
- Relationships
	- one-to-one
	- one-to-many
	- many-to-many
- Persistance
	- Data is saved to disk, and reloaded on a reboot of the server
- Transactional
	- ie. B gives 20$ to A, B gets $ and A loses $, must happen in tandem, else fail

## RBDMS Vendors
- PostgreSQL
- MySQL
- MSSQL
- MariaDB
- Oracle
- ...

## Relational Database Models

- `Database` - store of data, its the thing we connect to when we initialize connection to our database server
- `Schema`
- `Table` - store individual entities of data i.e. `Users` or `Tweets`
- `Columns` - store a single typed value of information about the table
	- `name varchar(255) NOT NULL`
		- Column name: `name`
		- Column type: `varchar(255)`
		- Column arguments: `NOT NULL`
- `Rows` - Stores an entry of data for the given entity

- DQL, DDL, DCL, DML

- can override SERIAL when inserting data
	- can return all values inserted `RETURNING *`; --specific to postgres

- `psql -d <db name> < seed.sql` from cmd line feeding seed to db
- `psql -d <db name>` go to db

- `ILIKE` - case insensitive

## Aside
- databases in copies as shards across clusters

