# DSL model "Tags"

Although Telosys now has many annotations for customizing entities, not all use cases can be predicted in advance and it is not possible to define enough annotations to meet all needs.

This is why the "tags" have been added.&#x20;

The user can now add information to the attributes of an entity by definig tags of his choice.

Tags are an important advance in the adaptability and flexibility of models.

### General principles for tags:

* a tag starts with the character "#"
* it is placed in the same block as the annotations (between {and})
* it can have any name
* it may or may not have a value&#x20;
* in the templates we can check if a tag is present or not and possibly use its value
  * $attrib.**hasTag**("tagName") \
    Check if "tagName" is defined for $attrib
  * $attrib.**tagValue**("tagName")\
    Get "tagName" value



### Example 1 - Simple tag without value :

Tag "**mytag**" in entity file :

```
MyEntity {
  id  : int { @Id } ;

  // tag "mytag" (without value) :
  comment : string { #mytag } ;
}
```

Usage in a template :

```
#if ( $attrib.hasTag("mytag") )  
## do something ...
#end
```



### Example 2 - Tag with value :

Tag "**OpenAPIFormat**" in entity file :

```
MyEntity {
  id  : int { @Id } ;

  // tag "OpenAPIFormat" with value :
  val : long  { #OpenAPIFormat(int64) } ;
}
```

Usage in a template :

```
#if ( $attrib.hasTag("OpenAPIFormat") )  
$attrib.tagValue("OpenAPIFormat")
#end
```
