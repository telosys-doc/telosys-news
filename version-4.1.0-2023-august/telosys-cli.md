# Telosys-CLI

Telosys-CLI version 4.1.0 brings some minor improvements and 3 new commands.

### New commands&#x20;

#### "genb" command&#x20;

"genb" means "Generation in Batch mode".

It allows to launch code generation for multiple models and multiple bundles of templates

For example  `genb * *`   launch generation for all models with all bundles of templates&#x20;

#### "fx" command

"fx" means "File eXplorer"

It opens a file explorer located in the current directory.

The file explorer tool is customizable in "telosys-cli.cfg" ( FileExplorerCommand ) so you can use your prefered tool.

#### "exit" command   ;-)

Just a synonym for "q" command, for those who are used to quit with the "exit" command in other tools. Telosys don't want to change your habits ;-)



### Minor changes&#x20;

* commands standardization (options and behavior)
* "-none" option for commands "b" and "m" (to clear current model or bundle)
* partial name generalization in many commands (for bundle name and model name)
