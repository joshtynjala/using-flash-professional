# ActionScript publish settings (CS5)

## Modify ActionScript publish settings (CS5)

When you create a new FLA document, Flash asks you which version of ActionScript
you want to use. You can change this setting if you decide later to write your
scripts in a different version of ActionScript.

> **Note:** ActionScript 3.0 is not compatible with ActionScript 2.0. The
> ActionScript 2.0 compiler can compile all ActionScript 1.0 code, except for
> the slash (/) syntax used to indicate movie clip paths (for example,
> `parentClip/testMC:varName= "hello world"`). To avoid this problem, either
> rewrite your code using dot (.) notation, or select the ActionScript 1.0
> compiler.

1.  Select File \> Publish Settings and then select the Flash tab.
2.  Select the ActionScript version from the pop-up menu.

## Class files and configuration files (CS5)

When you install Flash Pro, several ActionScript-related configuration folders
and files are placed on your system. If you modify these files to customize the
authoring environment, back up the original files.

ActionScript classes folder  
Contains all of the built-in ActionScript 2.0 classes (AS files). Typical paths
to this folder are as follows:

- Windows XP: Hard Disk\Documents and Settings\\_user_\Local
  Settings\Application Data\Adobe\Flash CS5\\_language_\Configuration\Classes

- Windows Vista: Hard Disk\Users\\_user_\Local Settings\Application
  Data\Adobe\Flash CS5\\_language_\Configuration\Classes

- Macintosh: Hard Disk/Users/_user_/Library/Application Support/Adobe/Flash
  CS5/_language_/Configuration/Classes

  The Classes folder is organized into classes for Flash Player 7 (FP7), classes
  for Flash Player 8 (FP8), classes for Plash Player 9 (FP9), and the mx
  package, which is used in both players and in ASO files. For more information
  on the organization of this directory, see the Read Me file in the Classes
  folder.

Include class folder  
Contains all of the global ActionScript include files. Locations are as follows:

- Windows XP: Hard Disk\Documents and Settings\\_user_\Local
  Settings\Application Data\Adobe\Flash CS5\\_language_\Configuration\Include

- Windows Vista: Hard Disk\Users\\_user_\Local Settings\Application
  Data\Adobe\Flash CS5\\_language_\Configuration\Include

- Macintosh: Hard Disk/Users/_user_/Library/Application Support/Adobe/Flash
  CS5/_language_/Configuration/Include

ActionsPanel.xml configuration file  
Includes the configuration file for ActionScript code hinting. Separate files
provide configuration for each version of ActionScript and Flash Lite, and for
JavaScript. Locations are as follows:

- Windows XP: Hard Disk\Documents and Settings\\_user_\Local
  Settings\Application Data\Adobe\Flash
  CS5\\_language_\Configuration\ActionsPanel

- Windows Vista: Hard Disk\Users\\_user_\Local Settings\Application
  Data\Adobe\Flash CS5\\_language_\Configuration\ActionsPanel

- Macintosh: Hard Disk/Users/_user_/Library/Application Support/Adobe/Flash
  CS5/_language_/Configuration/ActionsPanel

AsColorSyntax.xml configuration file  
The configuration file for ActionScript code color syntax highlighting.
Locations are as follows:

- Windows XP: Hard Disk\Documents and Settings\\_user_\Local
  Settings\Application Data\Adobe\Flash
  CS5\\_language_\Configuration\ActionsPanel\\

- Windows Vista: Hard Disk\Users\\_user_\Local Settings\Application
  Data\Adobe\Flash CS5\\_language_\Configuration\ActionsPanel\\

- Macintosh: Hard Disk/Users/_user_/Library/Application Support/Adobe/Flash
  CS5/_language_/Configuration/ActionsPanel

## Declare an ActionScript 3.0 document class (CS5)

When you use ActionScript 3.0, a SWF file may have a top-level class associated
with it. This class is called the document class. When the SWF is loaded by
Flash Player, an instance of this class is created to be the SWF file's
top-level object. This object of a SWF file can be an instance of any custom
class you choose.

For example, a SWF file that implements a calendar component can associate its
top level with a Calendar class, with methods and properties appropriate to a
calendar component. When the SWF is loaded, Flash Player creates an instance of
this Calendar class.

1.  Deselect all objects on the Stage and in the Timeline by clicking a blank
    area of the Stage. This displays the Document properties in the Property
    inspector.
2.  Enter the filename of the ActionScript file for the class in the Document
    Class text box in the Property inspector. Do not include the .as filename
    extension.

> **Note:** You can also enter the Document Class information in the Publish
> Settings dialog box.

## Set the location of ActionScript files (CS5)

To use an ActionScript class that you've defined, Flash Pro must locate the
external ActionScript files that contain the class definition. The list of
folders in which Flash Pro searches for class definitions is called the
_classpath_ for ActionScript 2.0 and the _source path_ for ActionScript 3.0.
Classpaths and source paths exist at the application (global) and document
level. For more information about classpaths, see Classes in
[Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120101223847mp_/http://www.adobe.com/go/learn_cs5_learningas2_en)
or
"[Packages](https://web.archive.org/web/20120101223847mp_/http://help.adobe.com/en_US/as3/learn/WS5b3ccc516d4fbf351e63e3d118a9b90204-7f94.html)"
in _Learning ActionScript 3.0_.

You can set the following ActionScript locations in Flash Pro:

- ActionScript 2.0

  - Application level (available to all AS2 FLA files):

    - Classpath (set in ActionScript preferences)

  - Document level (available only to the FLA file that specifies this path):

    - Classpath (set in Publish Settings)

- ActionScript 3.0

  - Application level (available to all AS3 FLA files):

    - Source path (set in ActionScript preferences)

    - Library path (set in ActionScript preferences)

    - External library path (set in ActionScript preferences)

  - Document level (available only to the FLA file that specifies these paths):

    - Source path (set in Publish Settings)

    - Library path (set in Publish Settings)

    - Document class (set in Document Property inspector)

The _Library path_ specifies the location of pre-compiled ActionScript code
which resides in SWC files you have created. The FLA file that specifies this
path loads every SWC file at the top level of this path and any other code
resources that are specified within the SWC files themselves. If you use the
Library path, be sure none of the compiled code in the SWC files is duplicated
in uncompiled AS files in the Source path. The redundant code will slow down
compilation of your SWF file.

You can specify more than one path for Flash Pro to look in. Resources found in
any of the paths specified will be used. When you add or modify a path, you can
add absolute directory paths (for example, C:/my_classes) and relative directory
paths (for example, ../my_classes or ".").

### Set the classpath for ActionScript 2.0

To set the document-level classpath:

1.  Select File \> Publish Settings, and click Flash.
2.  Verify that ActionScript 2.0 is selected in the ActionScript Version pop‑up
    menu, and click Settings.
3.  Specify the frame where the class definition should reside in the Export
    Frame for Classes text field.
4.  To add paths to the classpath list, do any of the following:

    - To add a folder to the classpath, click the Browse to Path
      button ![](../img/browse_to_path.png), browse to the folder to add, and
      click OK.

    - To add a new line to the Classpath list, click the Add New
      Path ![](../img/add_path.png) button. Double-click the new line, type a
      relative or absolute path, and click OK.

    - To edit an existing classpath folder, select the path in the Classpath
      list, click the Browse to Path button, browse to the folder to add, and
      click OK. Alternatively, double-click the path in the Classpath list, type
      the desired path, and click OK.

    - To delete a folder from the classpath, select the path in the Classpath
      list and click the Remove Selected Path
      button ![](../img/remove_path.png).

    To set the application-level classpath:

5.  Choose Edit Preferences (Windows) or Flash \> Preferences (Macintosh) and
    click the ActionScript category.

6.  Click the ActionScript 2.0 Settings button and add the path(s) to the
    Classpath list

### Set the source path for ActionScript 3.0

To set the document-level source path:

1.  Select File \> Publish Settings, and click Flash.
2.  Verify that ActionScript 3.0 is selected in the ActionScript Version pop‑up
    menu, and click Settings. Your Flash Player version must be set to Flash
    Player 9 or later to use ActionScript 3.0.
3.  Specify the frame where the class definition should reside in the Export
    Classes in Frame text field.
4.  Specify the Errors settings. You can select Strict Mode and Warnings Mode.
    Strict Mode reports compiler warnings as errors, which means that
    compilation will not succeed if those types of errors exist. Warnings Mode
    reports extra warnings that are useful for discovering incompatibilities
    when updating ActionScript 2.0 code to ActionScript 3.0.
5.  (Optional) Select Stage to automatically declare stage instances.
6.  Specify ActionScript 3.0 or ECMAScript as the dialect to use. ActionScript
    3.0 is recommended.
7.  To add paths to the source path list, do any of the following:

    - To add a folder to the source path, click the Source path tab and then
      click the Browse To Path button ![](../img/browse_to_path.png), browse to
      the folder to add, and click OK.

    - To add a new line to the Source path list, click the Add New
      Path ![](../img/add_path.png) button. Double-click the new line, type a
      relative or absolute path, and click OK.

    - To edit an existing Source path folder, select the path in the Source path
      list, click the Browse To Path button, browse to the folder to add, and
      click OK. Alternatively, double-click the path in the Source path list,
      type the desired path, and click OK.

    - To delete a folder from the source path, select the path in the Source
      path list and click the Remove From Path
      button ![](../img/remove_path.png).

    To set the application-level source path:

8.  Choose Edit Preferences (Windows) or Flash \> Preferences (Macintosh) and
    click the ActionScript category.

9.  Click the ActionScript 3.0 Settings button and add the path(s) to the Source
    path list.

### Set the Library path for ActionScript 3.0 files

To set the document-level Library path, the procedure is similar to setting the
Source path:

1.  Choose File Publish Settings and click the Flash tab.
2.  Make sure ActionScript 3.0 is specified in the Script menu and click
    Settings.
3.  In the Advanced ActionScript 3.0 Settings dialog box, click the Library path
    tab.
4.  Add the library path to the Library path list. You can add folders or
    individual SWC files to the path list.
5.  To set the Link Type property, double-click Link Type in the property tree
    of the path. The choices for Link Type are:

    - Merged into code: The code resources found in the path are merged into the
      published SWF file.

    - External: The code resources found in the path are not added to the
      published SWF file, but the compiler verifies that they are in the
      locations you specified.

    - Runtime shared library (RSL): Flash Player downloads the resources at
      runtime.

    To set the Application-level Library path:

6.  Choose Edit Preferences (Windows) or Flash \> Preferences (Macintosh) and
    click the ActionScript category.

7.  Click the ActionScript 3.0 Settings button and add the path(s) to the
    Library path list.

## Compiling ActionScript conditionally (CS5)

You can use conditional compilation in ActionScript 3.0 in the same way that it
has been used in C++ and other programming languages. For example, you can use
conditional compilation to turn blocks of code throughout a project on of off,
such as code that implements a certain feature or code used for debugging.

Using config constants that you define in the publish settings, you can specify
whether certain lines of ActionScript code are compiled or not. Each constant
takes the following form:

`CONFIG::SAMPLE_CONSTANT`

In this form, `CONFIG` is the config namespace and `SAMPLE_CONSTANT` is the
constant that you will set to true or false in the publish settings. When the
value of the constant is true, the line of code that follows the constant in
ActionScript is compiled. When the value is false, the line of code that follows
the constant is not compiled.

For example, the following function has 2 lines of code that are compiled only
if the value of the constant that precedes them is set to true in the publish
settings:

    public function CondCompTest() {
        CONFIG::COMPILE_FOR_AIR {
            trace("This line of code will be compiled when COMPILE_FOR_AIR=true.");
        }
        CONFIG::COMPILE_FOR_BROWSERS {
            trace("This line of code will be compiled when COMPILE_FOR BROWSERS=true.");
        }
    }

To define a config constant using the Publish Settings dialog box:

1.  Choose File \> Publish Settings.

2.  In the Publish Settings dialog box, click the Flash tab.

3.  Ensure that the value for Script is set to ActionScript 3.0 and click the
    Settings button next to the value.

4.  In the Advanced ActionScript 3.0 Settings dialog box, click the Config
    Constants tab.

5.  To add a constant, click the Add button.

6.  Type the name of the constant you want to add. The default config namespace
    is `CONFIG` and the default constant name is `CONFIG_CONST`.

    > **Note:** The config namespace `CONFIG` is declared by the Flash Pro
    > compiler automatically. You can add your own config namespaces by entering
    > them with a constant name in the publish settings and adding them to your
    > ActionScript code using the following syntax:
    >
    >     config namespace MY_CONFIG;

7.  Enter the value you want for the constant, either true or false. You change
    this value in order to turn on or off compilation of specific lines of code.

## Customizing context menus in Flash documents (CS5)

You can customize the standard context menu and the text-editing context menu
that appears with SWF files in Flash Player 7 and later.

- The standard context menu appears when a user right-clicks (Windows) or
  Control‑clicks (Macintosh) on a SWF file in Flash Player, in any area except
  an editable text field. You can add custom items to the menu, and hide any
  built‑in items in the menu except Settings and Debugger.

- The editing context menu appears when a user right-clicks (Windows) or
  Control‑clicks (Macintosh) in an editable text field in a SWF file in Flash
  Player. You can add custom items to this menu. You cannot hide any built‑in
  items.
  > **Note:** Flash Player also displays an error context menu when a user
  > right-clicks (Windows) or Control-clicks (Macintosh) in Flash Player and no
  > SWF file is loaded. You cannot customize this menu. Customize context menus
  > in Flash Player 7 by using the ContextMenu and ContextMenuItem objects in
  > ActionScript 2.0. For more information on using these objects, see
  > `ContextMenu` in the
  > [_ActionScript 2.0 Language Reference_](https://web.archive.org/web/20120101223847mp_/http://www.adobe.com/go/learn_cs5_as2lr_en).

Remember the following conditions when creating custom context menu items for
Flash Player:

- Custom items are added to a context menu in the order in which they are
  created. You cannot modify this order after the items are created.

- You can specify the visibility and enabling of custom items.

- Custom context menu items are automatically encoded using Unicode UTF‑8 text
  encoding.

## Configuration folders installed with Flash (CS5)

Flash Pro places several configuration folders on your system when you install
the application. The configuration folders organize files associated with the
application into appropriate levels of user access. You may want to view the
contents of these folders when you are working with ActionScript® or components.
The configuration folders for Flash Pro are as follows:

#### Application-level configuration folder

Because it is in the application level, non-administrative users do not have
write access to this directory. Typical paths to this folder are as follows:

- In Microsoft Windows XP or Microsoft Windows Vista, browse to _boot
  drive_\Program Files\Adobe\Adobe Flash CS3\\_language_\Configuration\\

- On the Macintosh, browse to _Macintosh HD_/Applications/Adobe Flash
  CS3/Configuration/.

#### First Run folder

This sibling to the application-level configuration folder facilitates sharing
configuration files among users of the same computer. Folders and files in the
First Run folder are automatically copied to the user-level configuration
folder. Any new files placed in the First Run folder are copied to the
user-level configuration folder when you start the application.

Typical paths to the First Run folder are as follows:

- In Windows XP or Vista, browse to _boot drive_\Program Files\Adobe\Adobe Flash
  CS3\\_language_\First Run\\

- On the Macintosh, browse to _Macintosh HD_/Applications/Adobe Flash CS3/First
  Run/.

#### User-level configuration folder

Found in the user profile area, this folder is always writable by the current
user. Typical paths to this folder are as follows:

- In Windows XP or Vista, browse to _boot drive_\Documents and
  Settings\\_username_\Local Settings\Application Data\Adobe\Flash
  CS3\\_language_\Configuration.

- On the Macintosh, browse to _Macintosh
  HD_/Users/_username_/Library/Application Support/Adobe/Flash
  CS3/_language_/Configuration/.

#### All-user-level configuration folder

Found in the common user profile area, this folder is part of the standard
Windows and Macintosh operating system installations and is shared by all users
of a particular computer. The operating system makes available to all users of
the computer any files placed in this folder. Typical paths to this folder are
as follows:

- In Windows XP or Vista, browse to _boot drive_\Documents and Settings\All
  Users\Application Data\Adobe\Flash CS3\\_language_\Configuration\\

- On the Macintosh, browse to _Macintosh HD_/Users/Shared/Application
  Support/Adobe/Flash CS3/_language_/Configuration/.

#### Restricted Users configuration folder

For users with restricted privileges on a workstation, typically, in a networked
environment, only system administrators have administrative access to
workstations. All other users are given restricted access, which usually means
that these users can't write to application-level files (such as the Program
Files directory in Windows or the Applications folder in Macintosh OS X).
