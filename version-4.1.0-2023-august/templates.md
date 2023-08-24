# Templates

### Generator objects&#x20;

In addition to the evolutions concerning the objects related to the model, some technical objects  have also changed.

#### New objects&#x20;

* **$csharp** : utility functions for C#code generation
* **$php** : utility functions for PHP code generation&#x20;

#### Changed objects&#x20;

* **$java** : toStringMethod(..) new arguments (same as in $csharp and $php )
* **$jdbc** : provides automatic conversion to SQL column and type

#### Deprecated objects&#x20;

* **$today** : use $now instead



### New features&#x20;

* Improvements regarding generic ORM 'GeneratedValues' ('AutoIncremented')
* JPA code generation improvements ( $jpa object ) : generated value, cascade, etc
* Many to many relationship is now simpler to manage ( with JoinTable based on @JoinEntity )



