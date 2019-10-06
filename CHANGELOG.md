# 9.2.4

* Added Parameter evaluation to unused definitions #30
* Fixed CodeAssist for CREATE DATASET #8
* Added Goto Source Line #74
* Fixed False/Positiv for static methods in used defintions #78
* Fixed False/Positiv for private methods #6
* Fixed Occurrence selection for private static method invocations
* Added Preference tab with license informations and reorganized some preferences

# 9.2.3

* Fixed Code Assist for static methods and property

# 9.2.2

* Fixed Oedt Run Configurations always starting in debug mode
* Added Option to compile files with missing rcode #70

# 9.2.1

* Added Support for variables in the environment tab for Oedt Run Configurations

# 9.2.0

* Added Support for OpenEdge 12.1
* Fixed Check-Syntax #66
* Fixed Exception with empty test suites #76
* Added Option for skipping derived files #44
* WIP Correct Usings - add missing using statements #16
* Added Copy file names from include view #65
* Added Compile Xref XML #67
* WIP Multi project dependencies compile #15

# 9.1.1

* Enhanced Refactoring (Move, Rename) for Packages and Files (for example TestSuites)
> Note: If you have already installed OEDT 9.1.0 you need the rebuild the source model (context menu from the project explorer)

# 9.1.0

* Added addional validation for #61
* Fixed Unused procedure if reference is in a trigger phrase #62
* Added NPE handling from Progress compilation #63
* Updated recognition of new keywords for 11.7.4 and 12.0.0 #64
* Added Refactoring (Move) of directories #29
* Fixed Refactoring (Rename) of directories #29
* Fixed Memberrefactoring (Rename), added some more validations and fixed references #20
* Started main work on Using Statements #11 and #16 -> fix will be included in 9.1.1

# 9.0.3

* Removed dependency from OpenEdge 11.7.4 #60

# 9.0.2

* Added Hover/CodeAssist generate parameter for Assembly classes
* Added "Progress OpenEdge Application by OEDT" Run/Debug Launch Configuration
> Note: These Run/Debug configuration has only one goal, to allow debugging 32bit applications from 64bit PDSOE. I have no idea wether this is working under all circumstances, but I did a few successful test cases.

# 9.0.1

* Fixed NPE Run/Debug ABLUnit Application #56
* Fixed Code Assist includeTooling=false #14

# 9.0.0

* Added Code Assist ignore classes with includeTooling=false #14
* Added Hover/CodeAssist generate parameter names if OedtDoc is not present
* Added ToggleComment action for Single line comment (CTRL+7), Multi line comment is now (CTRL+SHIFT+7) #52
* Added ABLUnit Run/Debug Configuration to OEDT editor #45
* Added Switch to Designer (Appbuilder/Visual Designer) to OEDT editor (F9) #47
* Fixed Procedure/Function Wizard code generation in Appbuilder files #46
* Added Preference for Appbuilder file extensions (default = .w)
* Added Aligned facet version and plug-in version #37
> Note: OEDT 9 is only available for OpenEdge 11.7.x and OpenEdge 12.x

# 8.5.1

* Fixed Macro/template expansion with multiple placeholders broken #48

# 8.5.0

* Added Export/Import OEDT preferences #39
* Fixed Compile and Checksyntax for files with different source file encoding #40
* Fixed Macro/Template with pressing return instead of spacebar #41
* Fixed Override/Implement of method with returntype extent #42
* Fixed Autocompletion for temp-tables with nested preprocessor suffixes #43

# 8.4.8

* Fixed "Auto-Check-Syntax" #36
* Fixed "Compile on Save if Auto-Build disabled" #38
> Note: OEDT depends on the "Autobuild" feature of eclipse. If "Autobuild" is disabled, the OEDT Model which is responsible for code assist and finding references (refactoring) will not updated properly. If you just want to disable the compilation, then use the option "Disable Compile for Auto-Build". This way, the model gets updated, but no compilation is done. To add compilation to the files opened in the OEDT editor, activate "Compile on Save if Auto-Build is disabled" additionaly.

# 8.4.7

* Added Support for Sonarlint #35
* Fixed Unused Variables False Positive for some keywords which are used as identifier #32

# 8.4.6

* Added OEDTDocParser for ABLDoc (OEDT for OE 11.6 and 11.7) #31
> Note: This option is disabled per default and can be changed via 
Window - Preferences - Oedt - Use OedtDocTagParser for ABL Doc
The OEDTDocParser removes the leading stars from OEDTDoc and sends the modified comment back to the default ABLDoc Parser.
* Added .sonarlint folder filter to the Project Explorer #34

# 8.4.5

* Fixed Code Assist Using statement recognition #10
* Fixed Catched possible exception while reading connected database schema

# 8.4.4

* Added GET-CLASS buildin function
* Added include file evaluation for "Unused variables" functionality
* Added support for member-references (variables, methods, etc) which are keywords
* Added parser tracks NEW SHARED, SHARED option for a better support for "Unused variables" functionality
* Added REPOSITION-BACKWARD and REPOSITION-FORWARD
* Fixed code assist for Assembly Enums (wrong internal type-mapping)
* Fixed Using statement order is now taken into account for code assist
* Fixed OEDT database load procedure for connected oracle databases (load only databases with type 'PROGRESS')
* Fixed code assist for keyword abbreviations (instead of DEF to DEFINE, DEF+DEFI+DEFIN to DEFINE)
* Fixed duplicate Using statement for different classes (second class get's now fully qualified)
* Fixed possible NPE in ImageProvider
* Fixed Editor, Compile on Save for include files (was generating r-files)
* Added better description for "Compile on Save" option (is executed only if Autobuild is disabled)
* Fixed Parameter wizard dialog datatype evaluation
* Added evaluation of using statements in include files, fixes code assist for these kind of references
* Added evaluation of temptable like definition per include parameter (DEFINE TEMP-TABLE tt LIKE {3})
* Fixed "Autobuild", "Disable Compile" and "Compile on Save" interaction
> Note: OEDT depends on the "Autobuild" feature of eclipse. If "Autobuild" is disabled, the OEDT Model which is responsible for code assist and finding references (refactoring) will not updated properly. If you just want to disable the compilation, then use the option "Disable Compile". This way, the model gets updated, but no compilation is done. To add compilation to the files opened in the OEDT editor, activate "Compile on Save" additionaly.
* Added JFace Fix from Eclipse 4.6/4.7 for Eclipse 4.5.2 which fixes comment block editing
* Added option to skip preprocessor block evaluation during parsing (default: true), allows tracking of references in inactive preprocessor blocks  

# 8.4.3

* Added Search for Eclipse Helpsystem in Editor (Shift + F2)
* Fixed Editor coloring after shortest comment block definition
* Added Preference for Correct Using on Save (default is true)

# 8.4.2

* Fixed SpeedScript Compile
* Fixed Annotation Hovertext for Override and Implements
* Added Code Assist for chain calls with leading whitespaces

# 8.4.1

* Fixed Coloring of Nested Comments starting with /** and containing /*
* Fixed File Refactoring with overlapping package import
* Fixed Parsing Temptable like definition (not all places where you can put the LIKE definition where covered)
* Fixed Smart Casing for the keyword EVENT
* Fixed Constructor Argument Completion for Assembly and Proclib Classes (inserting the datatype instead of the parameter name) 

# 8.4.0

* Fixed Override Implement Wizard Code generation
* Fixed Cursor position for OEDT Doc Block Start
* Added Smart Keyword Casing + preference (fixes the casing of .net properties which are often keywords)
* Fixed Event-Methods Casing (publish, subscribe, unsubscribe)
* Fixed CodeAssist/Hover for Temptable FIELD LIKE definitions
* Added some optimization to auto bracketing

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
