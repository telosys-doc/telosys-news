# DSL model annotations

### New annotations

* Explicit **Foreign Key** with&#x20;
  * **@FK(**xx**)**
* **@Insertable(**true|false**)** &#x20;
* **@Updatable(**true|false**)**
* **@Optional**
* **@Transient**



### New annotations for links&#x20;

* Link **fetch type** :
  * **@FetchTypeLazy**&#x20;
  * **@FetchTypeEager**\

* Link by **attribute** with
  * **@LinkByAttr(**attribName**)**&#x20;
  * **@LinkByAttr(**attr1 > refAttr1 ,  attr2 > refAttr2 , ...**)**\

* Link by **column** with
  * **@LinkByCol(**column\[, column2 \[, columnN ] ] **)**\

* Link by **Foreign Key** :
  * **@LinkByFK(**fkName**)**\

* Link by "**join entity**" (for "many to many" cardinality)
  * **@LinkByJoinEntity(**entityName**)**\

* Link **cardinality** :
  * **@ManyToMany**&#x20;
  * **@OneToOne**\

* Link "mapped by" (for ORM) :
  * **@MappedBy(**attributeName**)**



### Annotation removed

The useless annotation "**@SqlType**" has been removed

