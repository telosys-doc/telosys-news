# Version 4.3.0 (2025-November)

Telosys version 4.3.0 brings many significant improvements, such as **4 new neutral types** and new commands in the command-line interface, such as "**git**" and "**sql**".

See the details below:

## 🟠 Telosys model - New neutral types&#x20;

The Telosys model grammar has been enhanced with 4 new neutral types

#### 🔷 **uuid**

This type is for "**Universally Unique Identifier**" (128-bit number used to uniquely identify information). A type that is now supported by almost all programming languages ​​and by some databases.&#x20;

#### 🔷 **datetime**

This type is intended for storing a **date** with a **time**&#x20;

#### 🔷 **datetimetz**

This type is like "**datetime**" but with "**Time Zone Offset**"

#### 🔷 **timetz**

This type is like "**time**" but with "**Time Zone Offset**"

ℹ️ the type "**timestamp**" is replaced by "**datetime**" and is now deprecated.\
It is maintained to ensure backward compatibility and can be considered a synonym of "**datetime**" .

For more details about new model types conversion to target language types&#x20;\
see [https://doc.telosys.org/target-languages](https://doc.telosys.org/target-languages)&#x20;



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

In Python, "**Type Hints**" allow developers to annotate code by specifying the expected types for variables and function arguments (type hints were introduced in Python 3.5).

Python “**Type Hints**” are now supported by Telosys:

* Define Python as the current target language&#x20;
  * &#x20;`#set( $env.language = 'Python' )`
* When Python is the current target language the "Type Hint" is used or returned by all objects using an attribute type:
  * &#x20;`$attribute.type`
  * &#x20;`$attribute.simpleType`
  * &#x20;`$fn.argumentsListWithType($entity.keyAttributes)` &#x20;
  * etc

For more details about model types conversion to Python type hints \
see [https://doc.telosys.org/target-languages/python](https://doc.telosys.org/target-languages/python)



## 🟠 Database configuration

#### 🔷 "databases.yaml"  simplification

Default values ​​have been added to simplify database configuration.

The "databases.yaml" file is therefore less verbose.



## 🟠 Telosys CLI&#x20;

#### 🔷 New "git" command

Git is now embedded in Telosys-CLI in order to execute some basic Git commands directly in the CLI, even if Git is not installed on the workstation.

This makes it easy to manage the creation and modification of **models** and **bundles**, which are made available as Git repositories.

Here are some examples of commands:

* **Init**   **`git initm`** (for a model)  or  **`git initb`** (for a bundle)
* **Clone    `git clonem`** (for a model)  or  **`git cloneb`** (for a bundle)
* **Status    `git statusm`** (for a model)  or  **`git statusb`** (for a bundle)
* **Publish    `git pubm`** (for a model)  or  **`git pubb`** (for a bundle)  => add + commit + push&#x20;

The "Git remote" is the current "Telosys depot" (GitHub, etc)

#### 🔷 New "sql" command

With this new version it is now possible to execute a **SQL script** on a database.

Command usage:   **`sql database-id sql-file`**

The **database-id** is one of the databases defined in **databases.yaml**



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



