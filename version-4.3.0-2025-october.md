# Version 4.3.0 (2025-October)

Telosys version 4.3.0 brings many significant improvements, such as **4 new neutral types** and new commands in the command-line interface, such as "**git**" and "**sql**".

See the details below:

## 🟠 Telosys model - New neutral types&#x20;

The Telosys model grammar has been enhanced with 4 new neutral types

#### 🔷 **uuid**

This neutral type is for "**Universally Unique Identifier**" (128-bit number used to uniquely identify information). A type that is now supported by almost all programming languages ​​and by some databases.&#x20;

#### 🔷 **datetime**

This neutral type is intended for storing a **date** with a **time**&#x20;

#### 🔷 **datetimetz**

This type is like "datetime" but with "Time Zone Offset"

#### 🔷 **timetz**

This type is like "time" but with "Time Zone Offset"

ℹ️ the type "**timestamp**" is replaced by "**datetime**" and is now deprecated.\
It is maintained to ensure backward compatibility and can be considered a synonym of "**datetime**" .



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

#### 🔷 Python - Type Hints

In Python, "**Type Hints**" allow developers to annotate code by specifying the expected types for variables and function arguments.&#x20;

Python “**Type Hints**” are now supported by Telosys\
for example when using `$fn.argumentsListWithType($entity.keyAttributes)`  \
with  `#set( $env.language = 'Python' )`



## 🟠 Telosys CLI&#x20;

### 🔷 New "git" command

### 🔷 New "sql" command



