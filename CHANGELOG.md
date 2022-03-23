# 9.4.1

* Fixed No support to switch between Visual Designer and code for User Controls #127
* Fixed Refactoring & CallHierarchy for Enum Values #128
* Fixed View Design for extern Controls (Telerik) #129
* Fixed Wizards, Link to Outline, Refactoring if code folding is used #131
* Added Basic-Support for Generics in 12.5 (Parsing, Hyperlinks, Refactoring)
* Added Override Properties support in 12.5
* Added Safe-Navigation Support (?:)

# 9.4.0

* Added features to database view #122
* Fixed code formatting #119
* Added option in preferences for hyperlinks to procedure files without file extension #123
* Added Hyperlinksresolution to "Open Declaration" (Open Implementation, Returntype, Returntype Implementation)
* Added Classdefinition changes to dependency build #124

# 9.3.8

* Fixed hyperlinks in console output for projects with a dot in the name
* Added correct indentation to 12.2+ #115

# 9.3.7

* Fixed several minor issues with "Add missing using statements"
* Added hyperlinks in console output
* Added better code assist for handle-datatyp #93
* Fixed autobracketing
* Fixed casing after bracket

# 9.3.6

* Fixed Correct Using - wildcard imports #105
* Fixed Keywords as identifiers breaking AST generation #111
* Fixed Toggle Comment #110
* Added Show compilation summary #106
* Fixed Rename of variables with same name (global and local) #98
* Added Correct Using - preserve Sonarlint PP-Token #11
* Added Format Code Action (for 12.x only) #59

# 9.3.5

* Added support for features in the upcoming OpenEdge release
* Added option to align the FROM-phrase in USING statements #103
* Fixed unused variable regarding variable name equals to validate #104
* Added new code assist priority for table proposals inside query context #102

# 9.3.4

* Fixed Dialog-Title for member refactoring
* Added preferences (Oedt -> Editor) for coloring buffer, temptables and temptable-buffers #100
* Fixed Exception for "Oedt Database Update" Job #101
* Fixed Keyword-Expansion for datatype LOGICAL (LOG -> LOGICAL) #94
* Added some keyword method and function overloads #97
* Fixed unused variables detection for output parameters with initial value #95

# 9.3.3

* Fixed ConcurrentModificationException during startup for OedtDatabase #92

# 9.3.2

* Fixed possible NPE during Startup for Oedt Database
* Fixed Parser for Preprocessor statements in case block
* Added preference for annotation and single line comment, should fix #86
* Added option to disable "Refresh using native hook" during compilation #91
> Window -> Preference -> Oedt -> Compile -> "Suspend native refresh hook during compilation"
* Fixed "Correct Keywords" Action #90
> Added Context-aware variant for editor menu ("Correct on Save" still uses the context-free version)
>       The computation may take a while, depending on the size of the file
>       The new computation fixed wrong cased keywords, which are identifiers
>       Example: MyEvent:PUBLISH() -> MyEvent:Publish(), DEFINE VARIABLE oError AS ERROR. -> DEFINE VARIABLE oError AS Error.
> Added Context-aware CodeAssist for DEFINE, CONSTRUCTOR, DESTRUCTOR, METHOD statements
>       Example: CONSTRUCTOR <CTRL + SPACE> -> "Simple Classname" and modifiers

# 9.3.1

* Fixed new using engine regarding FROM ASSEMBLY #89
* Added optional file encoding menu to the project explorer (Activate: Window -> Preferences -> Oedt -> View Preferences)

# 9.3.0

* Added support for Openedge 12.2 - droped support for Openedge 12.0
  > Note: Openedge 12.2 requires Java 11 - OEDT for Openedge 12.2 is compiled againt Java 11
* Added Support for new PACKAGE-PRIVATE and PACKAGE-PROTECTED modifiers
  * Code Assist
  * Wizards
  * Icons
* Added UpperCase CodeAssist for Elements with an underscore ("_") or dash ("-")
  * Element: tt_my_long_table_name -> TMLTN + CodeAssit(CTRL + SPACE) -> tt_my_long_table_name
* Added new Using-Statement Engine (disabled by default)
  * Option: Window -> Preferences -> Oedt -> Using Statement -> "Use new Using-Engine (BETA)"
  * Main goals:
    * handle using statements in preprocessor blocks
    * automatically add missing using statements on save (if enabled)
  > Note: This feature is in beta status and is therefore disabled by default
  >       Feedback regarding Performance and Issues are welcome
* Fixed CodeAssist for super classes referenced via qualifiedname
* Improved calculation of class references

# 9.2.7

* Fixed Before-Table and Temp-Table collision in argument code completion #82

# 9.2.6

* Added Buffers, Temptables, Tables and Datasets in argument code completion for handle parameters #81
* Added Blocklables (Code Assist, Outline) #80
* Fixed License Info regarding wrong month (Oedt Preferences)
* Fixed Parameter usage evaluation for Datasets
* Fixed "Open Implementation" for implementations in parent classes

# 9.2.5

* Added Automatic replacement of DLC Propath entries with choosen Runtime to OEDT Run Configurations
> Note: Example: PDSOE with 12.1, Run Configuration with 11.7 -> Replaces DLC 12.1 with DLC 11.7
>       This replacement is not visible in the Propath tab.

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
