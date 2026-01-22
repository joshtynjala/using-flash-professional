# Debugging ActionScript 3.0

## About the ActionScript 3.0 debugger

Flash includes a separate debugger for ActionScript 3.0 that operates somewhat
differently from the ActionScript 2.0 debugger. The ActionScript 3.0 debugger
only works with ActionScript 3.0 FLA and AS files. FLA files must have publish
settings set to Flash Player 9. When you initiate an ActionScript 3.0 debugging
session, Flash launches the stand-alone debug version of Flash Player to play
the SWF file. The debug Flash player plays the SWF in a separate window from the
Flash authoring application window.

The ActionScript 3.0 debugger converts the Flash workspace to a debug workspace
that displays panels that are used for debugging, including the Actions panel
and/or Script window, the Debug console, and the Variables panel. The Debug
console displays the call stack and contains tools for stepping through scripts.
The Variables panel displays the variables in the current scope with their
values and allows you to update those values yourself.

#### Additional resources

The following resources provide additional detailed information about debugging
ActionScript 3.0:

- Article:
  [Understanding ActionScript 3 debugging in Flash](https://web.archive.org/web/20120101152016mp_/http://www.adobe.com/devnet/flash/articles/flcs4_as3_debugging.html)
  (Adobe.com)

- Article:
  [Introducing the ActionScript 3 debugger](https://web.archive.org/web/20120101152016mp_/http://www.adobe.com/devnet/flash/articles/as3_debugger.html)
  (Adobe.com)

## Enter debugging mode

The way you begin a debugging session depends on the type of file you are
working on. During a debugging session, Flash interrupts the execution of
ActionScript when it encounters a breakpoint or a runtime error.

When Flash initiates a debug session, it adds special information to the SWF
file that it exports for the session. This information allows the debugger to
provide the specific line numbers in the code where errors are encountered.

You can include this special debugging information in all SWF files created from
a specific FLA file in the Publish settings. This allows you to debug the SWF
file even if you do not explicitly initiate a debug session. This debugging
information makes the SWF file slightly larger.

#### Choose a default debugging environment

- Choose Debug  Debug Movie and then choose one of the following:
  - Flash Professional

  - Device Central

  - AIR Debug Launcher (Desktop)

  - AIR Debug Launcher (Mobile)

  - on Device via USB (CS5.5 only)

  All debug sessions will take place in the environment you choose. You can
  change the default environment at any time.

#### Start debugging from a FLA file

![](../img/dingbat.png) Select Debug \> Debug Movie \> Debug.

#### Start debugging from an ActionScript 3.0 AS file

1.  With the ActionScript file open in the Script window, select the FLA file
    that the ActionScript file should be compiled with from the Target menu at
    the top of the Script window. The FLA file must also be open in Flash to
    appear in this menu.

2.  Select Debug \> Debug Movie \> Debug.

#### Add debugging information to all SWF files created from a FLA file

1.  With the FLA file open, select File \> Publish Settings.

2.  In the Publish Settings dialog box, click the Flash tab (CS5) or Flash
    category (CS5.5).

3.  Select Permit Debugging.

#### Exit debugging mode

![](../img/dingbat.png) Click the End Debug Session button in the Debug Console.

## Set and remove breakpoints

Add breakpoints to ActionScript code to interrupt the execution of the code.
After execution is interrupted, you can step through and execute the code line
by line, view different sections of your ActionScript, view the values of
variables and expressions, and edit variable values.

> **Note:** Breakpoints cannot be added to ASC (ActionScript for Communication)
> or JSFL (Flash JavaScript) files.

#### Set a breakpoint

![](../img/dingbat.png) In the Actions panel or Script window, click in the left
margin next to the line of code where you want the breakpoint to appear.

#### Remove a breakpoint

![](../img/dingbat.png) In the Actions panel or Script window, click on the
breakpoint to remove.

## Step through lines of code

After the ActionScript execution is interrupted at a breakpoint or runtime
error, you can step through the code line by line, choosing to step into
function calls or step over them. You can also choose to continue executing the
code without stepping.

#### Step into code line by line

![](../img/dingbat.png) Click the Step In button in the Debug Console.

#### Step over a function call

![](../img/dingbat.png) Click the Step Over button in the Debug Console.

#### Step out of a function call

![](../img/dingbat.png) Click the Step Out button in the Debug Console.

#### Resume normal code execution

![](../img/dingbat.png) Click the Continue button in the Debug Console.

## Display and examine scripts in the call stack

When code execution stops in the debugger, you can view the call stack in the
Debug Console and display the scripts containing the functions in the call
stack. The call stack shows the current list of nested function calls that are
waiting to complete execution.

You can view the individual scripts that contain each function.

![](../img/dingbat.png) In the Debug Console panel, double click the name of the
script in the call stack.

## Display and modify variable values

View and edit the values of variables and properties in the Variables panel.

#### View a variable value

1.  In the Variables panel, select the types of variables to display from the
    Panel menu.
    - Show Constants displays the values constants (variables having a fixed
      value).

    - Show Statics displays variables that belong to the class, rather than to
      instances of the class.

    - Show Inaccessible Member Variables displays variables that are not
      accessible to other classes or namespaces. This includes variables that
      are protected, private or internal to the namespace.

    - Show Additional Hexadecimal Display adds hexadecimal values wherever
      decimal values are displayed. This is mainly useful for color values.
      Hexadecimal values are not displayed for decimal values from 0 through 9.

    - Show Qualified Names displays variables types with both the package name
      and the class name.

2.  Expand the tree view of the object structure of the FLA until you see the
    variable to view.

#### Edit the value of a variable

1.  In the Variables panel, double click on the value of the variable.

2.  Enter the new value for the variable and press Enter. The new value is used
    during subsequent code execution.

## Control compiler warnings

Control the types of compiler warnings that the ActionScript compiler generates
in the Compiler Errors panel. When the compiler reports an error, double click
the error to navigate to the line of code that caused the error.

1.  Select File \> Publish Settings.
2.  Click Flash.
3.  Click the ActionScript Settings button.
4.  Select among the Errors options:
    - Strict Mode reports warnings as errors, which means that compilation will
      not succeed if those errors exist.

    - Warnings Mode reports extra warnings that are useful for discovering
      incompatibilities when updating ActionScript 2.0 code to ActionScript 3.0.

## Navigate to errors in code

When Flash encounters an error in ActionScript code, either during compiling or
execution, it reports the error in the Compiler Errors panel. Navigate to the
line of code that caused the error from the Compiler Errors panel.

![](../img/dingbat.png) Double click the error in the Compiler Errors panel.

## Debug a remote ActionScript 3.0 SWF file

With ActionScript 3.0, you can debug a remote SWF file by using the stand-alone,
ActiveX, or plug‑in version of the Debug Flash Player, which you can find in the
_Flash install directory_/Players/Debug/ directory. However, in the ActionScript
3.0 Debugger, remote debugging is limited to files located on the same localhost
as the Flash authoring application, being played in the stand alone debug
player, ActiveX control, or plugin.

To permit remote debugging of the file, enable debugging in the Publish
settings. You can also publish your file with a debugging password to ensure
that only trusted users can debug it.

As in JavaScript or HTML, users can view client-side variables in ActionScript.
To store variables securely, send them to a server-side application instead of
storing them in your file. However, as a developer, you may have other trade
secrets, such as movie clip structures, that you do not want to reveal. You can
use a debugging password to protect your work.

#### Enable remote debugging of a SWF file and set a debugging password

In ActionScript 3.0 FLA files, code in frame scripts cannot be debugged. Only
code in external AS files can be debugged with the ActionScript 3.0 Debugger.

1.  Open the FLA file.

2.  Select File \> Publish Settings.

3.  In the Publish Settings dialog box, click the Flash tab (CS5) or Flash
    category (CS5.5), and then select Permit Debugging.

4.  Close the Publish Settings dialog box, and select one of the following
    commands:
    - File \> Export \> Export Movie

    - File \> Publish

5.  Leave the SWF file on the local machine to perform a remote debug session on
    the localhost, or upload it to your web server.

    The SWF file contains no breakpoint information, so if you upload the file
    to a remote server you will not be able to step through code. Use the
    localhost to perform this task.

6.  In Flash, select Debug \> Begin Remote Debug Session \> ActionScript 3.0.

    Flash opens the ActionScript 3.0 Debugger and waits for a debug Flash Player
    to connect. You have 2 minutes to start the debug Flash Player. If more than
    2 minutes elapse, repeat this step.

7.  Open the SWF file in the debug version of the Flash Player plugin, ActiveX
    control, or stand-alone player. The debug stand-alone player is located in
    the _Flash install directory_/Players/Debug/ directory. Do not connect to a
    file on another machine, as debugger will not be able to receive any
    breakpoint information.

    The debug session begins when the debug player connects to the Flash
    ActionScript 3.0 Debugger panel.

#### Activate the Debugger from a remote location

1.  Open the Flash authoring application if it is not already open.

2.  Select Debug \> Begin Remote Debug Session \> ActionScript 3.0.

3.  In a browser or in the debugger version of the stand-alone player, open the
    published SWF file from the remote location.

    If the Remote Debug dialog box does not appear, right-click (Windows) or
    Control-click (Macintosh) in the SWF file to display the context menu, and
    select Debugger.

4.  In the Remote Debug dialog box, select Localhost and select the file to
    open.

    The display list of the SWF file appears in the Debugger. If the SWF file
    doesn't play, the Debugger might be paused, so click Continue to start it.
