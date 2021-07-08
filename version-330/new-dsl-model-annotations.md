# DSL model annotations

### New annotations

* Explicit **Foreign Key** with 
  * **@FK\(**xx**\)**
* **@Insertable\(**true\|false**\)**  
* **@Updatable\(**true\|false**\)**
* **@Optional**
* **@Transient**



### New annotations for links 

* Link **fetch type** :
  * **@FetchTypeLazy** 
  * **@FetchTypeEager** 
* Link by **attribute** with
  * **@LinkByAttr\(**attribName**\)** 
  * **@LinkByAttr\(**attr1 &gt; refAttr1 ,  attr2 &gt; refAttr2 , ...**\)** 
* Link by **column** with
  * **@LinkByCol\(**column\[, column2 \[, columnN \] \] **\)** 
* Link by **Foreign Key** :
  * **@LinkByFK\(**fkName**\)** 
* Link by "**join entity**" \(for "many to many" cardinality\)
  * **@LinkByJoinEntity\(**entityName**\)** 
* Link **cardinality** :
  * **@ManyToMany** 
  * **@OneToOne** 
* Link "mapped by" \(for ORM\) :
  * **@MappedBy\(**attributeName**\)**



### Annotation removed

The useless annotation "**@SqlType**" has been removed



