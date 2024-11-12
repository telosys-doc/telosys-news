# Version 4.2.0 (2024-November)

Version 4.2.0 mainly includes improvements to CLI commands and configuration

### -> New variables usable in bundles (targets definition)

3 new variables have been added to offer greater flexibility in defining "targets" (in the bundle file):

* **${ENT}**  for current entity (to replace ${BEANNAME} in the future)
* **${BUN}** for current **bundle**&#x20;
* **${MOD}** for current **model**

Each variable can be used with the “\_UC” or “\_LC” suffix for upper/lower case

### -> Specific models folder&#x20;

It is now possible to define a specific directory to contain project models.

In the configuration file, simply define the “**SpecificModelsFolder**” property.\
To see the current "models folder" use "**cfg**" command.

### -> Notion of "depot"

A “**depot**” is the place where "bundles" and "models" are stored and available for installation. \
It's a set of "git repositories" usually located on GitHub

### -> Models installation

It's now possible to install "models" from a "depot" (from GitHub for now), just like for "bundles".

It can be useful to share models between teams.

### -> New commands to list and install "bundles" and "models"&#x20;

* “**lbd**” command -> List "bundles" available in the "depot for bundles"
* "**lmd**" command -> List "models" available in the "depot for models"
* "**im**" command -> Install "model(s)" from a depot

### -> Depots configuration (for bundles and models)

The "depots" to be used for storing and installing models can be defined in the configuration file.

A depot can now be of different types: **organization**, **any user** or **current user** (authenticated with a token)

See documentation for more details.

### -> GitHub authentication with "Personal Acces Token" (PAT)

The new command "**ght**" ("GitHub Token") alows to define (or remove) a "Personal Acces Token" that Telosys will use to call the GitHub API. The token is encrypted and stored locally (on the user workstation)&#x20;

By default the GitHub API is limited to 50 calls for the same IP address. Defining a token increase the "GitHub API rate limit", this can be useful to list and install "bundles" and "models" when multiple users are sharing the same external IP address in an enterprise (due to a proxy).

When a token is defined it's also possible to list and install bundles or models located in "private repositories" (if the authenticated user has the required privileges).

### -> Removing unnecessary commands

* The  "**ghu**" command is replaced by "**ght**" command
* The "**gh**" command has been removed (useless)

### -> "telosys" command

"**telosys**" is now the command to launch Telosys-CLI ;-)\
( "tt" is kept for backward compatibility )

### -> Some minor bug fixes and small improvements in commands
