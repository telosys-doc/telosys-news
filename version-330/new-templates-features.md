# Templates features

### New target languages

2 new predefined target languages have been added : **C++** and **Scala**   


### Files usage

It's now possible to use files located in a bundle folder, in a model folder or anywhere on the filesystem.

Examples :

```text
## Get a file :
#set( $file = $fn.fileFromBundle("foo.txt") )
#set( $file = $fn.fileFromModel("foo.txt") )
#set( $file = $fn.file("/foo/bar/foo.txt") )

## File information :
file.name          : $file.name
file.parent        : $file.parent
file.path          : $file.path
file.absolutePath  : $file.absolutePath
file.canonicalPath : $file.canonicalPath
file.exists()      : $file.exists()
file.isFile()      : $file.isFile()
file.isDirectory() : $file.isDirectory()
file.isHidden()    : $file.isHidden()
file.length        : $file.length

## Load file content :
#set($content = $file.loadContent() )
#set($lines = $file.loadLines() )

#if( $file.exists() && $file.isFile() )
$file.loadContent(2)## NO EOL
#end

#foreach ( $line in $file.loadLines(3) )
 . $line
#end

## CSV file
#set( $file = $fn.fileFromBundle("enum-csv.txt") )
#set( $lines = $file.loadValues(",", 1) )
#foreach ( $line in $lines )
 $line.get(0) : $line.get(1) 
#else
```



### $jpa functions improvements

xxx



### \#cancel directive

It's now possible to cancel the current file generation in a template.  
The cancel directive just stop the generation without writing the output file \(with a message explaining why the generation has been canceled\).

Example to avoid overwriting an existing file :

```text
#if($target.outputFileExists() )
#cancel("File already exists")
#end
```

