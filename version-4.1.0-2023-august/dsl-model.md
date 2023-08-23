# DSL model

### New annotations&#x20;

* **@Cascade** : for ORM cascade management (MERGE, REMOVE, etc)
* **@JoinEntity** : to explicitly define a 'join entity' (for ORM)
* **@OrphanRemoval** : for ORM like JPA, Doctrine, etc





### Modified annotations

* **@AutoIncremented** : this annotation is now just a shortcut for 'GeneratedValue(IDENTITY)'
* **@GeneratedValue** : the parameters are different&#x20;



### Model objects&#x20;

* $entity.entity.isJoinEntity() : **new**\

* $attribute.fkPartsCount : **new**
* $attribute.ini : **new**
* $attribute.hasGeneratedValueStrategy(...)  : **new**&#x20;
* $attribute.hasGeneratedValueAllocationSize()  : **new** \
  $attribute.generatedValueAllocationSize : **new**&#x20;
* $attribute.hasGeneratedValueInitialValue[^1]\()  : **new** \
  $attribute.generatedValueInitialValue : **new**&#x20;
* $attribute.hasGeneratedValueSequenceName()  : **new** $attribute.generatedValueSequenceName : **new**&#x20;
* $attribute.hasGeneratedValueTablePkValue() : **new** \
  $attribute.generatedValueTablePkValue: **new**&#x20;
* $attribute.isSelected() : removed&#x20;
* $attribute.isDatabaseNotNull() : removed&#x20;
* $attribute.isAutoIncremented() : removed - use isGeneratedValue() instead
* $attribute.jdbcInfo : removed
* $attribute.jdbcRecommendedJavaType : removed
* $attribute.jdbcTypeCode : removed
* $attribute.jdbcTypeName : removed\

* $link.isOrphanRemoval() : **new**&#x20;
* $link.isOwningSide() : removed&#x20;
* $link.isInverseSide() : removed \

* $fk.isExplicit() : **new**,  true if 'real FK' ( with a name )\










[^1]: 
