# Model from database

Creating a new model from a database is now more accurate and more flexible.

### New model information retrieved from database : &#x20;

* Entity level :&#x20;
  * @DbCatalog(..)&#x20;
  * @DbSchema(..)&#x20;
  * @DbTable(..)&#x20;
  * @DbView \

* Attribute level :&#x20;
  * @DbType(..)&#x20;
  * @DbName(..)



### Customization in "databases.yaml"

New options allow you to define more precisely what you want to get from the database :&#x20;

```
linksManyToOne: true
linksOneToMany: false
linksManyToMany: false

dbComment : false
dbCatalog : false
dbSchema : false
dbTable : false
dbView : false
dbName  :     false    
dbType :     false    
dbDefaultValue: false
```



### Other&#x20;

* model files are now always created in UTF-8

