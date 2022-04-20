# Templates objects

### New objects

4 new objects have been added and are now usable in templates :&#x20;

* **$bundle** \
  ****the current bundle of templates\

* **$now**\
  ****provides the current system date and time in different formats\

* **$file**\
  ****allows to work with a file located on the filesystem, each file instance is created with $fn.file(..) or $fn.fileFromXxx(..)\

* **$fkPart**\
  ****a Foreign Key element (got from an attribute involved in 1 or more Foreign Keys)

For more information see "**Telosys objects reference**" documentation.

### Objects improvement

Many objects have been improved with new attributes and new methods added.

* **$attribute :**&#x20;
  * fkParts&#x20;
  * hasDatabaseComment()&#x20;
  * hasInputType()&#x20;
  * hasLabel()&#x20;
  * hasTag(tagName)&#x20;
  * insertable&#x20;
  * insertableIs(value)&#x20;
  * isTransient()&#x20;
  * sqlType&#x20;
  * tagValue(tagName)&#x20;
  * updatable&#x20;
  * updatableIs(value)\

* **$entity :**&#x20;
  * isJoinEntity()&#x20;
  * linksCount\

* **$fn :**&#x20;
  * className(object)
  * file(filePath)&#x20;
  * fileFromBundle(filePath)&#x20;
  * fileFromModel(filePath)&#x20;
  * join(collection, separator)&#x20;
  * joinWithPrefixSuffix(collection, separator, prefix, suffix)&#x20;
  * replaceInList(list, oldElement, newElement)
  * toList(array)&#x20;
  * trimAll(list)\

* **$jpa :**&#x20;
  * genTargetEntity
  * joinColumnInsertable
  * joinColumnUpdatable&#x20;
  * linkAnnotations(leftMargin, link)
  * linkCardinalityAnnotation(leftMargin,link)&#x20;
  * linkJoinAnnotation(leftMargin, link)&#x20;
  * linkJoinAnnotation(leftMargin, link, alreadyMappedFields)&#x20;
  * manyToManyFetchType&#x20;
  * manyToOneFetchType&#x20;
  * oneToManyFetchType&#x20;
  * oneToOneFetchType\

* **$link :**&#x20;
  * entity&#x20;
  * hasMappedBy()&#x20;
  * insertable
  * insertableIs(boolean value)
  * isEmbedded()&#x20;
  * isTransient()&#x20;
  * updatable&#x20;
  * updatableIs(boolean value)\

* **$model :**&#x20;
  * description&#x20;
  * folderName&#x20;
  * name&#x20;
  * title&#x20;
  * type&#x20;
  * version\

* **$project :**
  * modelsFolderFullPath\

* **$target :**
  * originalFolderDefinition&#x20;
  * outputFileExists()&#x20;
  * outputFileFullPath&#x20;
  * type

****

****
