# Controlling external video playback with ActionScript

## Playing external FLV or F4V files dynamically

An alternative to importing video into the Flash Pro authoring environment is to
use either the FLVPlayback component or ActionScript to dynamically play
external FLV or F4V files in Flash Player. You can also use the FLVPlayback
component and ActionScript together.

You can play FLV or F4V files posted as HTTP downloads or as local media files.
To play back an external FLV or F4V file, post an FLV or F4V file to a URL
(either an HTTP site or a local folder) and add either the FLVPlayback component
or ActionScript code to the Flash Pro document to access the file and control
playback during runtime.

Using external FLV or F4V files provides the following capabilities that are not
available when using imported video:

- You can use longer video clips without slowing down playback. External FLV or
  F4V files are played using _cached memory_, which means that large files are
  stored in small pieces and accessed dynamically; they do not require as much
  memory as embedded video files.

- An external FLV or F4V file can have a different frame rate from the Flash Pro
  document in which it plays. For example, you can set the Flash Pro document
  frame rate to 30 fps and the video frame rate to 21 fps, which gives you
  greater control in ensuring smooth video playback.

- With external FLV or F4V files, Flash Pro document playback does not have to
  be interrupted while the video file is loading. Imported video files can
  sometimes interrupt document playback to perform certain functions (for
  example, to access a CD-ROM drive). FLV or F4V files can perform functions
  independently of the Flash Pro document, and so do not interrupt playback.

- Captioning video content is easier with external FLV or F4V files because you
  can use callback functions to access metadata for the video.

For more information on playing back FLV or F4V files, see "Playing back
external FLV files dynamically" in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)
or
[Basics of video](https://web.archive.org/web/20111109131151mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b90204-7d50.html)
in the _ActionScript 3.0 Developer's Guide_.

### Additional resources

The following resources are available with additional information about video
and ActionScript:

Articles:

- [Deconstructing the ActionScript 3 Flash video gallery application](https://web.archive.org/web/20111109131151mp_/http://www.adobe.com/devnet/flash/articles/vidgal_structure.html)
  (Adobe.com)

## Behaviors used in video playback

Video behaviors provide one way to control video playback. Behaviors are
prewritten ActionScript scripts that you add to a triggering object to control
another object. Behaviors add the power, control, and flexibility of
ActionScript coding to your document without having to create the ActionScript
code. Video behaviors play, stop, pause, rewind, fast-forward, show, and hide a
video clip.

To control a video clip with a behavior, use the Behaviors panel to apply the
behavior to a triggering object, such as a movie clip. Specify the event that
triggers the behavior (such as releasing the movie clip), select a target object
(the video that is affected by the behavior), and when necessary, select
settings for the behavior, such as the number of frames to rewind.

> **Note:** The triggering object must be a movie clip. You cannot attach video
> playback behaviors to button symbols or button components.

The following behaviors in Flash Pro control embedded video:

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
<th><p>Parameters</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Play Video</p></td>
<td><p>Plays a video in the current document.</p></td>
<td><p>Instance name of target video</p></td>
</tr>
<tr class="even">
<td><p>Stop Video</p></td>
<td><p>Stops the video.</p></td>
<td><p>Instance name of target video</p></td>
</tr>
<tr class="odd">
<td><p>Pause Video</p></td>
<td><p>Pauses the video.</p></td>
<td><p>Instance name of target video</p></td>
</tr>
<tr class="even">
<td><p>Rewind Video</p></td>
<td><p>Rewinds the video by the specified number of frames.</p></td>
<td><p>Instance name of target video</p>
<p>Number of frames</p></td>
</tr>
<tr class="odd">
<td><p>Fast Forward Video</p></td>
<td><p>Fast-forwards the video by the specified number of
frames.</p></td>
<td><p>Instance name of target video</p>
<p>Number of frames</p></td>
</tr>
<tr class="even">
<td><p>Hide Video</p></td>
<td><p>Hides the video.</p></td>
<td><p>Instance name of target video</p></td>
</tr>
<tr class="odd">
<td><p>Show Video</p></td>
<td><p>Shows the video.</p></td>
<td><p>Instance name of target video</p></td>
</tr>
</tbody>
</table>

### Control video playback using behaviors

1.  Select the movie clip to trigger the behavior.
2.  In the Behaviors panel (Window \> Behaviors), click the Add (+) button, and
    select the desired behavior from the Embedded Video submenu.
3.  Select the video to control.
4.  Select a Relative or Absolute path.
5.  If required, select settings for the behavior parameters and click OK.
6.  In the Behaviors panel under Event, click On Release (the default event) and
    select a mouse event. To use the On Release event, leave the option
    unchanged.

## The FLVPlayback component

The FLVPlayback component lets you include a video player in your Flash
application to play progressively downloaded video (FLV or F4V) files over HTTP,
or play streaming FLV files from Flash Media Server (FMS) or a Flash Video
Streaming Service (FVSS).

The FLVPlayback component does the following:

- Provides a set of prefabricated skins to customize playback controls and the
  look and feel of the user interface.

- Lets advanced users create their own custom skins.

- Provides cue points to synchronize your video with the animation, text, and
  graphics in your Flash Pro application.

- Provides live preview of customizations.

- Maintains a reasonably sized SWF file for easy download.

  The FLVPlayback component is the display area in which you view video. The
  FLVPlayback component includes the FLV Custom UI controls, a set of control
  buttons that play, stop, pause, and control playback the video.

### Configure the FLVPlayback component

1.  With the FLVPlayback component selected on the stage, open the Property
    inspector (Window \> Properties) and enter an instance name.

2.  Select Parameters in the Property inspector or open the Component inspector
    (Window \> Components).

3.  Enter values for parameters or use default settings.

    For each FLVPlayback component instance you can set the following parameters
    in the Property inspector or in the Component inspector:

    > **Note:** In most instances, it is not necessary to alter the settings in
    > the FLVPlayback component unless you want to change the appearance of a
    > video skin. The Video Import wizard sufficiently configures the parameters
    > for most deployments.

    autoPlay  
    Boolean value that determines how to play the FLV or F4V. If `true`, the
    video plays immediately when it is loaded. If `false`, loads the first frame
    and pauses. The default value is `true`.

    autoRewind  
    Boolean value that determines whether the video is automatically rewound. If
    `true`, the FLVPlayback component automatically rewinds the video to the
    beginning when the playhead reaches the end or when the user clicks the stop
    button. If `false`, the component does not automatically rewind the video.
    The default value is `true.`

    autoSize  
    Boolean value that, if `true`, resizes the component at runtime to use the
    source video dimensions. The default value is `false`.

    > **Note:** The encoded frame size of the video is not the same as the
    > default dimensions of the FLVPlayback component.

    bufferTime  
    Number of seconds to buffer before beginning playback. The default value
    is 0.

    contentPath (AS2 files)  
    String that specifies the URL to an FLV, F4V, or to an XML file that
    describes how to play the video. Double-click the Value cell for this
    parameter to activate the Content Path dialog box. The default is an empty
    string. If you do not specify a value for the `contentPath` parameter,
    nothing happens when Flash Pro executes the FLVPlayback instance.

    source (AS3 files)  
    String that specifies the URL to an FLV, F4V, or to an XML file that
    describes how to play the video. Double-click the Value cell for this
    parameter to activate the Content Path dialog box. The default is an empty
    string. If you do not specify a value for the `contentPath` parameter,
    nothing happens when Flash Pro executes the FLVPlayback instance.

    isLive  
    Boolean value that, if `true`, specifies that the video is streaming live
    from FMS. The default value is `false`.

    cuePoints  
    A string that specifies the cue points for the video. Cue points allow you
    to synchronize specific points in the video with Flash Pro animation,
    graphics, or text. The default value is an empty string.

    maintainAspectRatio  
    A Boolean value that, if `true`, resizes the video player in the FLVPlayback
    component to retain the source video aspect ratio; the source video is still
    scaled and the FLVPlayback component itself is not resized. The `autoSize`
    parameter takes precedence over this parameter. The default value is `true`.

    skin  
    A parameter that opens the Select Skin dialog box and allows you to choose a
    skin for the component. The default value is None. If you choose None, the
    FLVPlayback instance does not have control elements that allow the user to
    play, stop, or rewind the video, or take other actions that the controls
    make possible. If the `autoPlay` parameter is set to true, the video plays
    automatically. For more information, see "Customizing the FLVPlayback
    component" in _Using ActionScript 3.0 Components_ or _ActionScript 2.0
    Components Language Reference_.

    totalTime  
    Total number of seconds in the source video. The default value is 0. If you
    use progressive download, Flash Pro uses this number if it is set to a value
    greater than zero (0). Otherwise, Flash Pro tries to take the time from
    metadata.

    > **Note:** If you're using FMS or FVSS, this value is ignored; the total
    > time of the video is taken from the server.

    volume  
    A number from 0 to 100 that represents the percentage of maximum volume at
    which to set the volume.

### Specify the contentPath or source parameter

If you imported a local video clip into Flash Pro for use with progressively
downloaded or streaming video content, update the `contentPath` (AS2 FLA files)
or `source` (AS3 FLA files) parameter of the FLVPlayback component before
uploading your content to a web server or Flash Media Server. The `contentPath`
or `source` parameter specifies the name and location of the video file on the
server, and implies the playback method (for example, progressively downloading
using HTTP, or streaming from Flash Media Server using RTMP).

1.  With the FLVPlayback component selected on the Stage, open the Property
    inspector (Window \> Properties) and select Parameters in the Property
    inspector, or open the Component inspector (Window \> Component Inspector).

2.  Enter values for parameters, or use the default settings as appropriate. For
    the `contentPath` or `source` parameter, do the following:
    1.  Double-click the Value cell for the `contentPath` or `source` parameter
        to activate the Content Path dialog box.
    2.  Enter the URL or local path to the FLV or F4V file, or the XML file (for
        Flash Media Server or FVSS) that describes how to play the video.

    If you do not know the location of the video or XML file, click the folder
    icon to navigate to the correct location. When browsing for an video file,
    if it is at or below the location of the target SWF file, Flash Pro
    automatically makes the path relative to that location so that it is ready
    for serving from a web server. Otherwise, it is an absolute Windows or
    Macintosh file path.

    If you specify an HTTP URL, the video file is a progressive download FLV or
    F4V file. If you specify a URL that is a Real-Time Messaging Protocol (RTMP)
    URL, the video streams from a Flash Media Server (FMS). A URL to an XML file
    could also be a streaming video file from FMS or from a FVSS.

    > **Note:** When you click OK on the Content Path dialog box, Flash Pro
    > updates the value of the `cuePoints` parameter, too, because you might
    > have changed the `contentPath` parameter so that the `cuePoints` parameter
    > no longer applies to the current content path. As a result, you lose any
    > disabled cue points, although not ActionScript cue points. For this
    > reason, you may want to disable non-ActionScript cue points through
    > ActionScript, rather than through the Cue Points dialog box.

    When you specify the `contentPath` or `source` parameter, Flash Pro attempts
    to verify that the video you specified is compatible with Flash Player. If
    you see a warning dialog box, try re-encoding the video to FLV or F4V format
    with Adobe Media Encoder.

    You can also specify the location of an XML file that describes how to play
    multiple video streams for multiple bandwidths. The XML file uses
    Synchronized Multimedia Integration Language (SMIL) to describe the video
    files.

## Media components (Flash Player 6 and 7)

> **Note:** The media components were introduced in Macromedia Flash MX
> Professional 2004 and are intended for use with Flash Player 6 or 7. If you
> are developing video content to use with Flash Player 8, instead use the
> FLVPlayback component introduced in Macromedia Flash Professional 8. The
> FLVPlayback component provides improved functionality, giving you more control
> over video playback in the Flash Pro environment.

The media component suite consists of three components: MediaDisplay,
MediaController, and MediaPlayback. With the MediaDisplay component, to add
media to your Flash Pro documents, drag the component to the Stage and configure
it in the Component inspector. In addition to setting the parameters in the
Component inspector, you can add cue points to trigger other actions. The
MediaDisplay component has no visual representation during playback; only the
video clip is visible.

The MediaController component provides user interface controls that let the user
interact with streaming media. The Controller features Play, Pause, and Rewind
to Start buttons and a volume control. It also includes playbars that show how
much of the media has loaded and how much has played. A playhead slider can be
dragged forward and backward on the playbar to navigate quickly to different
parts of the video. Using behaviors or ActionScript, you can easily link this
component to the MediaDisplay component to show streaming video and provide user
control.

The MediaPlayback component provides the easiest and quickest way to add video
and a controller to your Flash Pro documents. The MediaPlayback component
combines the MediaDisplay and MediaController components into a single,
integrated component. The MediaDisplay and MediaController component instances
are automatically linked to each other for playback control.

To configure parameters for playback, size, and layout for all three components,
use the Component inspector or the Parameters tab in the Property inspector. All
the media components work equally well with mp3 audio content.

For more information on the media components, "Media components," in the
_ActionScript 2.0 Components Language Reference_.

More Help topics

[Stream video using Adobe Flash Media Server](./add-video-to-flash.md#stream-video-using-adobe-flash-media-server)

[Progressively download video using a web server](./add-video-to-flash.md#progressively-download-video-using-a-web-server)

[Controlling instances with behaviors](../symbols-instances-and-library-assets/symbols-and-actionscript.md#controlling-instances-with-behaviors)

[Control video playback using the Timeline](./add-video-to-flash.md#control-video-playback-using-the-timeline)
