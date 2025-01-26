## How to setup Mongo databases locally
1. Go to mongo db site and open community server
2. Download community server, mongo compass and mongo shell
3. go to the extracted shell file and in bin folder open cmd prompt and write mongosh.exe

## Mongo Compass setup
1. Open mongo Compasss and click on connect
2. If the server connects and show three files made `admin , config, local`, correct
3. Else the db server is not working

## Some shell commands
1. `show dbs` - shows all databases in the server
2. `use db_name` - go to a particular database
> if you use a new databases name it creates one, but will only save if you create al least one collection in it<br/>
3. `show collections` - show all collections in that database
4. `db.collection_name.find()` - to show all data inside the collection

#### Suppose you created a databases with `use ecomerce` and a collection name `products` in it.
1. `db.products.insertOne({ "name" : "dummy" }) ` - inserts one object at a time
2. `db.products.find()` - to show all products
3. `db.products.insertMany([ obj1, obj2 ])` - insert many objects at once seperated by commas
> all objects should be passed inside an array [],
4. `db.products.find( {"name" : "Akhilesh"} )` - returns an array of objects with same fields5.
5. `db.products.findOne( {"name" : "Akhilesh"} )` - return an single object
> The whole query is as follow `db.proucts.find( {"name" : {$eq: "Akhilesh"}} )` $eq -> equals to(default value)
> Some others are `$gt, $lt, $lte` etc
6. `db.products.find($or: [ {obj1}, {obj2} ])` - filters objects on OR operation, change `or` to `and` for and operations
7. `db.products.find().sort({ "price" : -1 })` - sorts in descending order, 1 for low to high and -1 for high to low.
> These functions are known as cursor functions some more are
8. `db.products.find().limit(2)` - shows the top two products
9. `db.products.countDocuments()` - count the number of documents, you can pass filters just as the `find` funtion in this too..
10. ` db.products.find({"price" : {$gt : 1}}, {"title" : 1, "price" : 1})` - this will now show only the title and price of the products
> id will be shown as default to hide it you have to do  `db.products.find({"price" : {$gt : 1}}, {"title" : 1, "price" : 1, "_id": 0})`


