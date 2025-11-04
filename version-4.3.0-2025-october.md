# Version 4.3.0 (2025-October)



## 🟠 Telosys model&#x20;

#### 🔷 New neutral types&#x20;



#### 🔷 Annotations





## 🟠 Telosys objects for templates

#### 🔷 $model

* `$model.`**`entities`**  →  **NEW** (same as “allEntities”)
* `$model.`_**`folderName`**_  →  is now deprecated
* `$model.`_**`type`**_  →  is now deprecated

#### 🔷 $entity

* `$entity.`**`hasUuidAttribute`**`()`  →  **NEW**
* `$entity.`**`hasBinaryAttribute`**`()`  →  **NEW**
* `$entity.`**`hasTemporalAttribute`**`()`  →  **NEW**
* `$entity.`_**`selectedLinks`**_ → deprecated

#### 🔷 $attribute

* `$attribute.`**`isDatetimeType`**`()`  →  **NEW**
* `$attribute.`**`isDatetimetzType`**`()`  →  **NEW**
* `$attribute.`**`isTimetzType`**`()`  →  **NEW**
* `$attribute.`**`isUuidType`**`()`  →  **NEW**
* `$attribute.`_**`dateAfterValue`**_  → deprecated
* `$attribute.`_**`hasDateAfterValidation`**_  → deprecated
* `$attribute.`_**`dateBeforeValue`**_  → deprecated
* `$attribute.`_**`hasDateBeforeValidation`**_  → deprecated

#### 🔷 $link

* `$link.`_`isSelected`_`()`  →  removed (useless)&#x20;

#### 🔷 $java

* `$java.`**`hashCodeMethod`**`(..)`  and `$java.`**`equalsMethod`**`(..)`\
  parameters standardization, same parameters as in other languages
* new methods:
  * `$java.`**`validationAnnotations`**`(4, $attribute)`
  * `$java.`**`validationAnnotationsMultiline`**`(4, $attribute)`
  * `$java.`**`hasValidationAnnotations`**`($attribute)`

#### 🔷 $beanValidation  is now DEPRECATED

all methods have been moved in **$java** object

#### 🔷 $fn

* `$fn.`**`attributeNames`**`(..)`  →  **NEW**
* `$fn.`**`joinWithTransformation`**`(..)`  →  **NEW**
* _`$fn.`**`firstCharToUpperCase`**_ → deprecated
* _`$fn.`**`tab`**_ → deprecated

#### 🔷 $values

* `$values.`**`contains`**`(”val”)`  →  **NEW**
* `$values.`**`getValues`**`(attributes, separator)`  →  **NEW**

#### 🔷 $\_, $\_\_, $\_\_\_, etc

Special "empty variables" that can be used for indenting directives in templates.

## 🟠 Target languages&#x20;

#### 🔷 Python

Python “**Type Hints**” are now supported&#x20;





## 🟠 Telosys CLI&#x20;

### 🔷 New "git" command

### 🔷 New "sql" command



