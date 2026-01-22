# Working with Flash Pro and Flash Builder

Adobe® Flash® Professional CS5 and Flex® can be used together in a variety of
ways, including creating custom graphics and components in Flash Pro for use in
Flex®. The following tutorials demonstrate several of the ways Flash® and Flex®
can be used together.

- Tutorial:
  [Sharing projects between Flash Pro and Flash Builder](https://web.archive.org/web/20111231232914mp_/http://www.adobe.com/devnet/flashbuilder/articles/sharing-projects-flashbuilder-flash.html)
  (Adobe.com)

## Editing and debugging ActionScript with Flash Professional and Flash Builder

Flash Professional CS5 offers enhanced workflows between Flash Pro and Flash
Builder 4.

The enabled workflows include:

- Edit ActionScript 3.0 in Flash Builder 4 and test, debug, or publish in Flash
  Pro CS5.

- Launch ActionScript 3.0 files from Flash Professional for edit in Flash
  Builder 4.

#### Before you begin

In order to enable these Flash Pro/Flash Builder workflows, ensure that the
following conditions are true:

- Both Flash Professional CS5 and Flash Builder 4 are installed.

- To launch a FLA file from Flash Builder, your project must be assigned the
  Flash Professional project nature in the Package Explorer panel.

  For more information about assigning project natures in Flash Builder, see
  Flash Builder Help.

- To launch a FLA file Flash Builder, your project must have a FLA file assigned
  to be used for testing and debugging in the Flash Professional properties of
  the project.

#### Additional resources

- Tutorial:
  [Create a Flash Professional Project in Flash Builder - Part 1](https://web.archive.org/web/20111231232914mp_/http://flashauthoring.blogspot.com/2010/05/create-flash-professional-project-in.html)
  (flashauthoring.blogspot.com)

- Tutorial:
  [Create a Flash Professional Project in Flash Builder - Part 2](https://web.archive.org/web/20111231232914mp_/http://flashauthoring.blogspot.com/2010/06/create-flash-professional-project-in.html)
  (flashauthoring.blogspot.com)

- Tutorial:
  [Using the Flash Builder 4 Debugger to Debug Flash Professional Projects](https://web.archive.org/web/20111231232914mp_/http://flashauthoring.blogspot.com/2010/06/using-flash-builder-4-debugger-to-debug.html)
  (flashauthoring.blogspot.com)

#### Testing, debugging, and publishingin Flash Pro from Flash Builder

To perform testing or debugging in Flash Pro with a file you are editing in
Flash Builder 4:

- From the Flash Builder development perspective, choose Run \> Test Movie or
  Run \> Debug Movie. Note that each menu item has a Flash Pro icon next to it.
  Once the SWF window or debug session is closed, focus will return to Flash
  Builder unless there are compiler errors in frame scripts inside the FLA file
  associated with the project. Information about all errors is sent to the
  Errors panel in Flash Builder.

To publish the FLA file associated with the current project in Flash Builder:

- From the Flash Builder development perspective, choose Project \> Publish
  Movie. Note the Flash Pro icon next to the menu command.

#### Editing AS files in Flash Builder from Flash Pro

To create a new ActionScript 3.0 class or interface and assign Flash Builder as
the editor:

1.  Choose File \> New.

2.  In the New Document dialog box, choose ActionScript 3.0 class or
    ActionScript 3.0 interface.

3.  In the Create ActionScxript 3.0 dialog box, select Flash Builder as the
    application to create the file and click OK. Flash Builder opens.

4.  In Flash Builder, choose a FLA file or XFL file to be associated with the
    ActionScript file and click Finish.

To open and edit an AS file in Flash Builder from Flash Pro:

1.  In the Library panel, right-click a symbol associated with the class or
    interface and choose Properties.

2.  In the Symbol Properties dialog box, click Edit Class Definition.

3.  In the Edit ActionScript 3.0 dialog box that appears, verify that the editor
    assigned to the AS file is Flash Builder and click OK.

    If Flash Builder is not assigned to edit the file, select Flash Builder as
    the application to edit the class file and click OK.

    Flash Builder opens to edit the file.

## Creating components for Flex

In Adobe® Flash® Professional CS5, you can create content for use as components
in Adobe® Flex® applications. This content can include both visual elements and
Adobe® ActionScript® 3.0 code.

Creating components in Flash Pro for use in Flex allows you to take advantage of
the flexible graphic design capabilities of Flash Pro while still utilizing the
capabilities of Flex.

In order to create Flex components in Flash Pro, you must install the Flex
Component Kit for Flash Pro. You install the component kit using Adobe Extension
Manager. Some versions of the component kit may not support all features of
Adobe® Flash® Professional CS5, so be sure to download the latest version of the
[Flex component kit](https://github.com/apache/flex-sdk/tree/develop/frameworks/projects/flash-integration).

For more information about using Flex and Flash Pro together, refer to the
[Flex documentation on the Adobe web site](https://web.archive.org/web/20100627004209/http://www.adobe.com/support/documentation/en/flex/).

To create a Flex component in Flash:

1.  Be sure you have Adobe Extension Manager installed.

    By default, Extension Manager is installed with the Adobe Creative Suite
    applications.

2.  Download and install the
    [Flex Component Kit](https://github.com/apache/flex-sdk/tree/develop/frameworks/projects/flash-integration).
    Be sure to quit Flash Pro before installing the component kit.

3.  Launch Flash Pro. Two new commands appear in the Commands menu, Convert
    Symbol to Flex Component and Convert Symbol to Flex Container.

4.  In Flash Pro, create a movie clip symbol containing the artwork and
    ActionScript 3.0 code you want to include in the Flex component. The content
    must be contained in a movie clip symbol before conversion to a Flex
    component.

5.  Before converting the movie clip to a Flex component, be sure that it meets
    the following requirements for compatibility with Flex:
    - The frame rate of the FLA file should be 24 fps and should match the frame
      rate of any Flex projects that will make use of the component.

    - The registration point should be located at the 0, 0 point in the movie
      clip.

      > **Note:** To ensure that all content in the movie clip has a
      > registration point of 0, 0, click the Edit Multiple Frames button at the
      > bottom of the Timeline, select all frames in the movie clip timeline,
      > select all of your content in all the frames, and move it to 0, 0 in the
      > Property inspector.

6.  Select the movie clip in the Library panel and choose Commands \> Convert
    Symbol to Flex Component.

    Flash Pro converts the movie clip to a Flex component, changes its icon to a
    Flex icon in the Library, and imports the FlexComponentBase class compiled
    clip to the Library. Flash Pro embeds the FlexComponentBase into the Flex
    component SCW file created in the next step.

    Note the progress messages displayed in the Output panel while Flash Pro
    converts the movie clip.

7.  Choose File \> Publish to create a SWC file containing the compiled Flex
    component. Flash Pro also creates a SWF file from the main FLA file, but you
    can ignore the SWF file if you choose. The published component SWC file is
    now ready for use in Flex.

8.  To use the SWC file in Flex, do one of the following:
    - Copy the SWC file from Flash Pro and paste it into the bin folder of your
      Flex project.

    - Add the SWC file to library path of your Flex project. For more
      information, see the
      [Flex Builder documentation](https://web.archive.org/web/20100627004209/http://www.adobe.com/support/documentation/en/flex/).

## Using Flex metadata

If you are writing ActionScript 3.0 code to be used in Flex, you can place
metadata in the code to embed external files in any published SWF that includes
the ActionScript code. Usually, these `[Embed]` metadata declarations are used
to embed image files, fonts, individual symbols, or other SWF files into the
SWF.

Remember that metadata is "data about data." You add metadata to ActionScript on
the line immediately preceding the line of code that the metadata applies to.
The compiler then takes the metadata into account when compiling the line of
code that follows it.

For example, to embed an image called button_up.png that is stored in the
directory one level above the ActionScript file, you would use the following
ActionScript:

`[Embed("../button_up.png")]`

`private var buttonUpImage:Class;`

The `[Embed]` metadata tag tells the compiler to embed the file named
button_up.png in the SWF file and that the file should be associated with the
variable named `buttonUpImage`.

For more information about embedding assets with metadata in Flex, see Embedding
Assets in the
[Flex 3 Developer Guide](https://web.archive.org/web/20100627004209/http://www.adobe.com/support/documentation/en/flex/).

If you use a feature that requires the Flex SDK, such as `[Embed]` metadata, at
compile time Flash Pro prompts you to add the Flex.SWC file to the Library path
of your FLA file. The Flex.SWC file contains compiled classes needed to support
Flex metadata. Click Update Library Path in the dialog box to add Flex.SWC to
the Library path. You can also add the Flex.SWC file to the Library path in the
ActionScript publish settings later.

## Additional resources

The following resources provide additional information and examples about
integrating Flash Pro with Flash Builder:

- Site:
  [http://jessewarden.com/](https://web.archive.org/web/20111231232914mp_/http://jessewarden.com/)
