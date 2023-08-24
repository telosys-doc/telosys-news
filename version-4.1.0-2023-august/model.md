# Model

### New annotations&#x20;

* **@JoinEntity**  (for entity) : to explicitly define a 'join entity' (for ORM)
* **@Cascade** (for link) : for ORM cascade management (MERGE, REMOVE, etc)
* **@OrphanRemoval** (for link) : for ORM like JPA, Doctrine, etc



### Modified annotations

* **@AutoIncremented** : this annotation is now just a shortcut for 'GeneratedValue(IDENTITY)'
* **@GeneratedValue** : the parameters are different&#x20;



### Model objects in template context

* $entity.hasGeneratedKey() : **new**&#x20;
* $entity.isJoinEntity() : now based on annotation @JoinEntity   \

* $attribute.fkPartsCount : **new**&#x20;
* $attribute.ini : **new**&#x20;
* $attribute.hasGeneratedValueStrategy(...)  : **new** &#x20;
* $attribute.hasGeneratedValueAllocationSize()  : **new**  \
  $attribute.generatedValueAllocationSize : **new** &#x20;
* $attribute.hasGeneratedValueInitialValue() : **new**  \
  $attribute.generatedValueInitialValue : **new** &#x20;
* $attribute.hasGeneratedValueSequenceName()  : **new**  $attribute.generatedValueSequenceName : **new** &#x20;
* $attribute.hasGeneratedValueTablePkValue() : **new** \
  $attribute.generatedValueTablePkValue: **new**&#x20;
* $attribute.generatedValueGenerator : removed  &#x20;
* $attribute.isSelected() : removed &#x20;
* $attribute.jdbcRecommendedJavaType : removed &#x20;
* $attribute.jdbcTypeCode : removed&#x20;
* $attribute.jdbcTypeName : removed  \

* $link.isOrphanRemoval() : **new**&#x20;
* $link.joinEntity : **new**  \

* $fk.isExplicit() : **new**,  true if 'real FK' ( with a name )\

* $fkPart.referencedAttribute : new &#x20;
* $fkPart.referencedEntity : new  \








