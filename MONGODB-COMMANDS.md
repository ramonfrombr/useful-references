## Access database

`mongosh -u "username" -p "password"`

## List current database

`db`

## Create new database

`use DATABASE_NAME`

## List databases

`show dbs`

## Inserts a row in a table(and creates table if does not exist)

`db.books.insertOne({"name": "harry potter"})`

## Finds all rows in table

`db.books.find()`

