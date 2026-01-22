# Working with video cue points

Use video cue points to allow events to be triggered at specific times in the
video. There are two kinds of cue points that you can work with in Flash:

- Encoded cue points. These are cue points you add when encoding video with
  Adobe Media Encoder. For more information about adding cue points in Adobe
  Media Encoder, see
  [Using Adobe Media Encoder](https://web.archive.org/web/20120108055632mp_/http://help.adobe.com/en_US/AdobeMediaEncoder/4.0/WSC039D82B-0C0E-4c53-BEBA-4C6C4B400160.html).
  Encoded cue points can be accessed by other applications in addition to Flash.

- ActionScript cue points. These are cue points you add to a video with the
  Property inspector in Flash. ActionScript cue points are accessible only to
  Flash and Flash Player. For more information about ActionScript cue points,
  see
  [Understanding Cue Points](https://web.archive.org/web/20120108055632mp_/http://help.adobe.com/en_US/FlashPlatform/develop/actionscript/3/WS5b3ccc516d4fbf351e63e3d118a9b90204-7d36.html)
  in the _ActionScript 3.0 Developer's Guide_.

When an FLVPlayback component instance is selected on the Stage, the video cue
points list appears in the Property inspector. You can also preview the entire
video on the Stage and add ActionScript cue points using the Property inspector
while previewing the video, including videos served by Flash Media Server.

To work with cue points in the Property inspector:

1.  Import video as progressive download, or place the FLVPlayback component on
    the stage and specify the source video. You can specify the source video in
    the Property inspector.

2.  In the Property inspector, click Cue Points to expand the section, if it's
    not already open.

3.  Click the Add button (+) to add an ActionScript cue point, and the Delete
    button (-) to delete an existing cue point. You can specify the time by
    dragging the mouse right or left to increase or decrease the timecode value,
    or by typing in a value.

4.  To add a parameter to a cue point, select the ActionScript cue point and
    click the Add button (+) at the bottom of Parameters section.

5.  You can rename the ActionScript cue points and any parameters by clicking in
    the name field and editing the name.

You can import and export lists of cue point from within the Property inspector.
Only ActionScript cue points can be imported to avoid conflicts with cue points
that have already been embedded inside the video during encoding.

The Import and Export cue point buttons at the top of Cue Points section allow
you to import or export cue point lists in XML format. When exporting, the list
includes all Navigation and Event cue points which are embedded in the video,
along with all ActionScript cue points you have added. When importing, a dialog
showing the number of ActionScript cue points imported is displayed.
