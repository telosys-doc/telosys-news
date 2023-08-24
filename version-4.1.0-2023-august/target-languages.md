# Target languages

### Kotlin&#x20;

Kotlin is a new predefined target language added in version 4.1.0&#x20;

It supports nullable types ( )&#x20;



### C\#

C# target language has been improved&#x20;

New temporal types have been added :&#x20;

* **DateOnly** ( Day / Month / Year ) &#x20;
* **TimeOnly** ( Hour / Min / Sec / NanoSec )

Nullable types (marked with "?" at the end) are now automatically provided  \
if the attribute is 'nullable' and '$env.typeWithNullableMark' is TRUE



### PHP

xx



### Nullable types&#x20;

Nullable types are now automatically provided for the languages concerned ( C#, PHP and Kotlin )

A nullable type is a type with a "nullable mark" at the end or at the beginning of the type,   \
for example : &#x20;

* "int**?**" and "string**?**" for C#&#x20;
* "**?**int" and "**?**string" for PHP

The "nullable mark" is automatically added to the type if : \
&#x20;  the attribute is 'nullable' \
&#x20;  and \
&#x20;  $env.typeWithNullableMark  is set to TRUE



