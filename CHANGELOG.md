# 8.3.2 Changelog

* Fixed an offset bug in Code Assist Replace mode (holding CTRL during Code Assist)
* Added database name Code Assist
* Fixed Code Assist for tables prefixed with a database name
* Added match underscore to Code assist (t_h -> finds table_history)
* Fixed Code Assist for .net collections
* Redesign Clean Build -> (Refreshes Project, Removes RCode, Rebuilds Model and compiles all files)
* Fixed Compile Files/Projectbuilder to compile only files under a SRC propath entry (see the BUILD Tab in project settings)
* Added option to exclude parameters/variables/buffers in procedures/functions/methods from Quick Outline
* Added option to exclude buffer/temptable fields from Quick Outline 

# 8.3.1 Changelog

* Fixed "Open Declaration F3" in Includetext {... hit F3 ...}
* Fixed "Exclude From Build" evaluation 

# 8.3.0 Changelog

* Added OEDT License Model
* Added Eclipse UpdateSite mechanism
* Fixed Update to Propath changes
* Added Replacement of @{ROOT} with project name in exclude from build entries
* Fixed Unused Occurrence for Buffer references in Variable LIKE definitions
* Fixed Code Assist in Property GET/SET implementations (was not working before)
* Fixed Unused Occurrence in Property GET/SET implementations
* Removed OedtDoc Overhead in Model
* Fixed Memory Overhead (removed storing AST) for parsing files or opened editors
* Fixed NPE in Code Assist for Function Declarations
* Added Copy Annotation in Override/Implements Action
* Added Copy Comment/Generate Comment/None to Override/Implements Action
* Fixed Override/Implements Action for abstract Property from super classes
* Added Name-Refactoring for function declarations (Renaming Function or Function declaration updates the other definition as well)
* Added Editor-Model Update Delay Option for fast Coder
