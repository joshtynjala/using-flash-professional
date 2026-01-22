# Symbols and ActionScript

With ActionScript®, you can control symbols at runtime. Using ActionScript
allows you to create interaction and other capabilities in your FLA files that
are not possible with the Timeline alone.

## Controlling instances and symbols with ActionScript

To control movie clip and button instances, use ActionScript®. The movie clip or
button instance must have a unique instance name to be used with ActionScript.
You can write the ActionScript yourself or use the pre-defined behaviors
included with Flash Pro.

For more information, see Handling events in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)
or
[Handling events](https://web.archive.org/web/20120102230800mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b90204-7fca.html)
in the _ActionScript 3.0 Developer's Guide_.

## Controlling instances with behaviors

In FLA files where the ActionScript Publish setting is set to ActionScript 2.0,
you can use behaviors to control movie clip and graphic instances in a document
without writing ActionScript. Behaviors are prewritten ActionScript scripts that
let you add ActionScript coding to your document without having to create the
ActionScript code yourself. Behaviors are not available for ActionScript 3.0.

You can use behaviors with an instance to arrange it in the stacking order on a
frame, as well as to load or unload, play, stop, duplicate, or drag a movie
clip, or to link to a URL.

In addition, you can use behaviors to load an external graphic or an animated
mask into a movie clip.

Flash Pro includes the behaviors in the following table.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Behavior</p></th>
<th><p>Purpose</p></th>
<th><p>Select or input</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Load Graphic</p></td>
<td><p>Loads an external JPEG file into a movie clip or screen.</p></td>
<td><p>Path and filename of JPEG file.</p>
<p>Instance name of movie clip or screen receiving the graphic.</p></td>
</tr>
<tr class="even">
<td><p>Load External Movieclip</p></td>
<td><p>Loads an external SWF file into a target movie clip or
screen.</p></td>
<td><p>URL of external SWF file.</p>
<p>Instance name of movie clip or screen receiving the SWF
file.</p></td>
</tr>
<tr class="odd">
<td><p>Duplicate Movieclip</p></td>
<td><p>Duplicates a movie clip or screen.</p></td>
<td><p>Instance name of movie clip to duplicate.</p>
<p>X-offset and Y-offset of pixels from original to copy.</p></td>
</tr>
<tr class="even">
<td><p>Goto And Play at frame or label</p></td>
<td><p>Plays a movie clip from a particular frame.</p></td>
<td><p>Instance name of target clip to play.</p>
<p>Frame number or label to play.</p></td>
</tr>
<tr class="odd">
<td><p>Goto And Stop at frame or label</p></td>
<td><p>Stops a movie clip, optionally moving the playhead to a
particular frame.</p></td>
<td><p>Instance name of target clip to stop.</p>
<p>Frame number or label to stop.</p></td>
</tr>
<tr class="even">
<td><p>Bring To Front</p></td>
<td><p>Brings target movie clip or screen to the top of the stacking
order.</p></td>
<td><p>Instance name of movie clip or screen.</p></td>
</tr>
<tr class="odd">
<td><p>Bring Forward</p></td>
<td><p>Brings target movie clip or screen one position higher in the
stacking order.</p></td>
<td><p>Instance name of movie clip or screen.</p></td>
</tr>
<tr class="even">
<td><p>Send To Back</p></td>
<td><p>Sends the target movie clip to the bottom of the stacking
order.</p></td>
<td><p>Instance name of movie clip or screen.</p></td>
</tr>
<tr class="odd">
<td><p>Send Backward</p></td>
<td><p>Sends the target movie clip or screen one position lower in the
stacking order.</p></td>
<td><p>Instance name of movie clip or screen.</p></td>
</tr>
<tr class="even">
<td><p>Start Dragging Movieclip</p></td>
<td><p>Starts dragging a movie clip.</p></td>
<td><p>Instance name of movie clip or screen.</p></td>
</tr>
<tr class="odd">
<td><p>Stop Dragging Movieclip</p></td>
<td><p>Stops the current drag.</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Unload Movieclip</p></td>
<td><p>Removes a movie clip that was loaded by means of loadMovie() from
Flash Player.</p></td>
<td><p>Instance name of movie clip.</p></td>
</tr>
</tbody>
</table>

## Add and configure a behavior

Be sure you are working in a FLA file whose ActionScript Publish setting is
ActionScript 2.0 or earlier.

1.  Select the object, such as a button, to trigger the behavior.
2.  In the Behaviors panel (Window \> Behaviors), click the Add (+) button and
    select the desired behavior from the Movieclip submenu.
3.  Select the movie clip to control with the behavior.
4.  Select a relative or absolute path.
5.  If required, select or input settings for the behavior parameters and click
    OK. Default settings for the behavior appear in the Behaviors panel.
6.  Under Event, click On Release (the default event) and select a mouse event
    from the menu. To use the On Release event, leave the option unchanged.

## Create custom behaviors

To write custom behaviors, create an XML file that contains the ActionScript 2.0
code to perform the desired behavior, and save the file in the Behaviors folder
of your local computer. Behaviors are stored in the following location:

- Windows XP: C:\Documents and Settings\\_user name_\Local Settings\Application
  Data\Adobe\Flash CS3\\_language_\Configuration\Behaviors

- Windows Vista: C:\Users\\_user name_\Local Settings\Application
  Data\Adobe\Flash CS3\\_language_\Configuration\Behaviors

- Macintosh: Macintosh HD/Users/_user name_/Library/Application
  Support/Adobe/Flash CS3/\_language\_/Configuration/Behaviors/

  Before you create your own behaviors, examine the Behavior XML files to
  develop an understanding of the syntax of the XML files, as well as the
  ActionScript code used to create behaviors. If you are new to writing
  behaviors, familiarize yourself with the XML tags used to create user
  interface elements (such as dialog boxes), and with ActionScript, the coding
  language used to create behaviors. To learn about the XML used to create
  interface elements, see _Extending Flash_. To learn about ActionScript, see
  [Learning ActionScript 3.0](https://web.archive.org/web/20111211032821/http://help.adobe.com/en_US/as3/learn/index.html)
  or
  [Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

  You can also download behaviors that other Flash Pro users have created from
  the Adobe Flash Exchange website.

1.  Using an XML editor, open an existing behavior's XML file, and rename the
    file appropriately for the behavior you intend to create.

2.  Enter a new value for the `category` attribute of the `behavior_devinition`
    tag in the XML file.

    The following XML code creates a category named myCategory in the Flash
    Behaviors panel under which the behavior will be listed.

        <behavior_definition dialogID="Trigger-dialog" category="myCategory"
        authoringEdition="pro" name="behaviorName">

3.  Enter a new value for the name attribute of the behavior_definition tag.
    This will be the name of the behavior as it will appear in the Flash
    authoring environment.

4.  (Optional) If your custom behavior requires a dialog box, enter parameters
    using the `<properties>` and `<dialog>` tags.

    To learn about the tags and parameters used to create your own custom dialog
    boxes, see _Extending Flash_.

5.  In the `<actionscript>` tag, insert the ActionScript code to create the
    behavior.

    If you are new to ActionScript, see
    [_Learning ActionScript 3.0_](https://web.archive.org/web/20111211032821/http://help.adobe.com/en_US/as3/learn/index.html)
    or
    [_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

    For example (from the Movieclip_loadMovie.xml behavior file) (ActionScript
    2.0):

        <actionscript>
          <![CDATA[     //load Movie Behavior
            if($target$ == Number($target$)){
                loadMovieNum($clip$,$target$);
            } else {
                $target$.loadMovie($clip$);
            }
            //End Behavior
          ]]>
        </actionscript>

6.  Save the file and test the behavior.

More Help topics

[Edit symbols](./working-with-symbols.md#edit-symbols)

[Control sounds using behaviors](../sound/sound-and-actionscript.md#control-sounds-using-behaviors)

[Control video playback using behaviors](../video/controlling-external-video-playback-with-actionscript.md#control-video-playback-using-behaviors)

[Relative paths](../timelines-and-animation/timelines-and-actionscript.md#relative-paths)

[Absolute paths](../timelines-and-animation/timelines-and-actionscript.md#absolute-paths)

[Break apart a symbol instance](./working-with-symbol-instances.md#break-apart-a-symbol-instance)
