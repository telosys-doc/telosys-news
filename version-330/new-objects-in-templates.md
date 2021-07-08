# Templates objects

## New objects

4 new objects have been added and are now usable in templates : 

* **$bundle**  the current bundle of templates 
* **$now** provides the current system date and time in different formats 
* **$file** allows to work with a file located on the filesystem, each file instance is created with $fn.file\(..\) or $fn.fileFromXxx\(..\) 
* **$fkPart** a Foreign Key element \(got from an attribute involved in 1 or more Foreign Keys\) 

xxx



## Objects improvement

Many objects have been improved with new methods added

#### $attribute **: new methods** 

* fkParts 
* hasDatabaseComment\(\) 
* hasInputType\(\) 
* hasLabel\(\) 
* hasTag\(String tagName\) 
* insertable 
* insertableIs\(boolean value\) 
* isTransient\(\) 
* sqlType 
* tagValue\(String tagName\) 
* updatable 
* updatableIs\(boolean value\)

\*\*\*\*
