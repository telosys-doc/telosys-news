# DSL model annotations

### New annotations

* Explicit **Foreign Key** with&#x20;
  * **@FK(**&#x78;&#x78;**)**
* **@Insertable(**&#x74;rue|fals&#x65;**)** &#x20;
* **@Updatable(**&#x74;rue|fals&#x65;**)**
* **@Optional**
* **@Transient**



### New annotations for links&#x20;

* Link **fetch type** :
  * **@FetchTypeLazy**&#x20;
  * **@FetchTypeEager**\

* Link by **attribute** with
  * **@LinkByAttr(**&#x61;ttribNam&#x65;**)**&#x20;
  * **@LinkByAttr(**&#x61;ttr1 > refAttr1 ,  attr2 > refAttr2 , ...**)**\

* Link by **column** with
  * **@LinkByCol(**&#x63;olumn\[, column2 \[, columnN ] ] **)**\

* Link by **Foreign Key** :
  * **@LinkByFK(**&#x66;kNam&#x65;**)**\

* Link by "**join entity**" (for "many to many" cardinality)
  * **@LinkByJoinEntity(**&#x65;ntityNam&#x65;**)**\

* Link **cardinality** :
  * **@ManyToMany**&#x20;
  * **@OneToOne**\

* Link "mapped by" (for ORM) :
  * **@MappedBy(**&#x61;ttributeNam&#x65;**)**



### Annotation removed

The useless annotation "**@SqlType**" has been removed

