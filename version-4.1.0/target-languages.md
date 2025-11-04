# Target languages

### Kotlin&#x20;

Kotlin is a new predefined target language added in version 4.1.0&#x20;

It supports nullable types.



### C\#

C# target language has been improved&#x20;

New temporal types have been added :&#x20;

* **DateOnly** ( Day / Month / Year ) &#x20;
* **TimeOnly** ( Hour / Min / Sec / NanoSec )

Nullable types are now supported for C#



### PHP

Typed class properties have been added in PHP 7.4&#x20;

So it's now possible to generate PHP code with the type corresponding to the attribute.

The type can be : string, bool, int, float or DateTime

Nullable types are supported for PHP



### Nullable types&#x20;

Nullable types are now automatically provided for the languages concerned ( C#, PHP and Kotlin )

A nullable type is a type with a "nullable mark" at the end or at the beginning of the type,   \
for example : &#x20;

* "in&#x74;**?**" and "strin&#x67;**?**" for C#&#x20;
* "**?**&#x69;nt" and "**?**&#x73;tring" for PHP

The "nullable mark" is automatically added to the type if : \
&#x20;  the attribute is 'nullable' \
&#x20;  and \
&#x20;  $env.typeWithNullableMark  is set to TRUE



