# Add video to Flash

Flash provides several methods by which you can incorporate video into your
Flash document and play it back for users.

## Before you begin

Before you start working with video in Flash Pro, it is important to understand
the following information:

- Flash Pro can only play specific video formats.

  These include FLV, F4V, and MPEG video. For instructions on converting video
  in other formats, see
  [Create video files for use in Flash](./create-video-files-for-use-in-flash.md).

- Use the separate Adobe Media Encoder application (included with Flash Pro) to
  convert other video formats to FLV and F4V. For instructions, see
  [Create video files for use in Flash](./create-video-files-for-use-in-flash.md).

- There are different ways of adding video to Flash Pro, each with advantages in
  different situations. See below for a list of these methods.

- Flash Pro includes a Video Import Wizard that opens when you choose File \>
  Import \> Import Video.

- Using the FLVPlayback component is the simplest way to quickly get video
  playing in a Flash Pro file.

  For instructions, see
  [Progressively download video using a web server](#progressively-download-video-using-a-web-server).

## Methods for using video in Flash

You can use video in Flash Pro in different ways:

- Progressive download from a web server

  This method keeps the video file external to the Flash Pro file and the
  resulting SWF file. This keeps the SWF file size small. This is the most
  common method of using video in Flash Pro.

- Stream video using Adobe Flash Media Server.

  This method also keeps the video file external to your Flash Pro file. Adobe
  Flash Media Streaming Server gives you secure protection of your video content
  in addition to a smooth streaming playback experience.

- Embed video data directly inside a Flash Pro file

  This method results in very large Flash Pro files, and is only recommended for
  short video clips. For instructions, see
  [Embed a video file within a Flash file](#embed-a-video-file-within-a-flash-file).

## Progressively download video using a web server

Progressive downloading lets you use either the FLVPlayback component or
ActionScript that you write to load and play back external FLV or F4V files in a
SWF file at runtime.

Because the video file is kept external to the other Flash Pro content, it's
relatively easy to update video content without republishing the SWF file.

Progressive downloading provides the following advantages over embedding video
in the Timeline:

- During authoring, you can publish only your SWF file to preview or test part
  or all of your Flash Pro content. This results in faster preview times and
  quicker turnaround on iterative experimentation.

- During playback, video begins playing as soon as the first segment of video is
  downloaded and cached to the local computer's disk drive.

- At runtime, video files are loaded by Flash Player from the computer's disk
  drive into the SWF file, with no limitation on video file size or duration. No
  audio synchronization issues or memory restrictions exist.

- The frame rate of the video file can be different from the frame rate of the
  SWF file, allowing for greater flexibility in authoring Flash Pro content.

### Import video for progressive download

You can import a video file that is stored locally on your computer, and then
upload the video file to a server after importing it to your FLA file. In Flash,
when you import video for progressive download, you are really adding only a
reference to the video file. Flash uses the reference to find the video file on
your local computer or on a web server.

You can also import a video file that is already uploaded to a standard web
server, an Adobe Flash Media Server (FMS), or Flash Video Streaming Service
(FVSS).

1.  Select File \> Import \> Import Video to import the video clip into the
    current Flash Pro document.

2.  Select the video clip to import. You can select either a video clip located
    on your local computer, or enter the URL of a video already uploaded to a
    web server or Flash Media Server.
    - To import video located on your local computer, select Load external video
      with playback component.

    - To import video already deployed to a web server, Flash Media Server, or
      Flash Video Streaming Service, select Already deployed to a web server,
      Flash Video Streaming Service, or Stream From Flash Media Server, and
      enter the URL of the video clip.

      > **Note:** The URL for a video clip located on a web server will use the
      > http communication protocol. The URL for a video clip located on a Flash
      > Media Server or Flash Streaming Service will use the RTMP communication
      > protocol.

3.  Select a skin for your video clip. You can choose to:
    - Not use a skin with the FLVPlayback component by selecting None.

    - Select one of the predefined FLVPlayback component skins. Flash Pro copies
      the skin into the same folder as the FLA file.

      > **Note:** FLVPlayback component skins are slightly different depending
      > on whether you are creating an AS2- or AS3-based Flash document.

    - Select a custom skin of your own design by entering the URL of the skin on
      the web server.

4.  The Video Import Wizard creates an FLVPlayback video component on the Stage
    that you can use to test video playback locally. When you finish creating
    your Flash document and want to deploy the SWF file and video clip, upload
    the following assets to the web server or Flash Media Server hosting your
    video:
    - If using a local copy of the video clip, upload the video clip (which is
      located in the same folder as the source video clip you selected with a
      .flv extension)

      > **Note:** Flash Pro uses a relative path to point to the FLV or F4V file
      > (relative to the SWF file), letting you use the same directory structure
      > locally that you use on the server. If the video was previously deployed
      > to your FMS or the FVSS hosting your video, you can skip this step.

    - The video skin (if you chose to use a skin)

      To use a predefined skin, Flash Pro copies the skin into the same folder
      as the FLA file.

    - The FLVPlayback component

      To edit the FLVPlayback component's URL field to that of the web server or
      Flash Media Server that you are uploading the video to, use the Component
      inspector (Windows \> Component inspector) to edit the `contentPath`
      parameter.

## Stream video using Adobe Flash Media Server

Flash Media Server streams media in real-time to Flash Player and AIR. Flash
Media Server uses bandwidth detection to deliver video or audio content based on
the user's available bandwidth.

Streaming video with Flash Media Server provides the following advantages over
embedded and progressively downloaded video:

- Video playback starts sooner than it does using other methods of incorporating
  video.

- Streaming uses less of the client's memory and disk space, because the clients
  don't need to download the entire file.

- Network resources are used more efficiently, because only the parts of the
  video that are viewed are sent to the client.

- Delivery of media is more secure, because media is not saved to the client's
  cache when streamed.

- Streaming video provides better tracking, reporting, and logging ability.

- Streaming lets you deliver live video and audio presentations, or capture
  video from a web cam or digital video camera.

- Flash Media Server enables multiway and multiuser streaming for video chat,
  video messaging, and video conferencing applications.

- By using server-side scripting to control video and audio streams, you can
  create server-side play lists, synchronized streams, and more intelligent
  delivery options based on the client's connection speed.

To learn more about Flash Media Server, see
[www.adobe.com/go/flash_media_server](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/go/flash_media_server).

To learn more about Flash Video Streaming Service, see
[www.adobe.com/go/learn_fvss_en](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/go/learn_fvss_en).

## Embed a video file within a Flash file

When you embed a video file, all of the video file data is added to the Flash
Pro file. This results in a much larger Flash Pro file and subsequent SWF file.
The video is placed in the Timeline where you can see the individual video
frames represented in the Timeline frames. Because each video frame is
represented by a frame in the Timeline, the frame rate of the video clip and the
SWF file must be set to the same rate. If you use different frame rates for the
SWF file and the embedded video clip, video playback is inconsistent.

> **Note:** To use variable frame rates, stream the video using either
> progressive downloading or Flash Media Server. When you import video files
> using either of these methods, the FLV or F4V files are self-contained and run
> at a frame rate separate from that of all other timeline frame rates included
> in the SWF file.

Embedded video works best for smaller video clips, with a playback time of less
than 10 seconds. If you are using video clips with longer playback times,
consider using progressively downloaded video, or streaming video using Flash
Media Server.

The limitations of embedded video include:

- You might encounter problems if the resulting SWF files become excessively
  large. Flash Player reserves a lot of memory when downloading and attempting
  to play large SWF files with embedded video, which can cause Flash Player to
  fail.

- Longer video files (over 10 seconds long) often have synchronization issues
  between the video and audio portions of a video clip. Over time, the audio
  track begins playing out of sequence with the video, causing a less than
  desirable viewing experience.

- To play a video embedded in a SWF file, the entire video file must be
  downloaded before the video starts to play. If you embed an excessively large
  video file, it might take a long time for the SWF file to download in its
  entirety and for playback to start.

- After a video clip is imported, it cannot be edited. Instead, you must re-edit
  and re-import the video file.

- When publishing your SWF file via the web, the entire video must be downloaded
  to the viewer's computer before video playback can begin.

- At runtime, the entire video must fit into the local memory of the playback
  computer.

- The length of an imported video file cannot exceed 16000 frames.

- The video frame rate and Flash Pro Timeline frame rate must be the same. Set
  the frame rate of your Flash Pro file to match the frame rate of the embedded
  video.

You can preview frames of an embedded video by dragging the playhead along the
Timeline (scrubbing). Note that the video sound track does not play back during
scrubbing. To preview the video with sound, use the Test Movie command.

### Embed video within a Flash file

1.  Select File \> Import \> Import Video to import the video clip into the
    current Flash Pro document.

2.  Select the video clip on your local computer to import.

3.  Select Embed FLV In SWF and Play In Timeline.

4.  Click Next.

5.  Choose the symbol type with which to embed the video in the SWF file.

    **Embedded Video**  
    If you're using the video clip for linear playback in the Timeline,
    importing the video into the Timeline is the most appropriate method.

    **Movie Clip**  
    A best practice is to place video inside a movie clip instance, because you
    have the most control over the content. The video's Timeline plays
    independently from the main Timeline. You do not have to extend your main
    Timeline by many frames to accommodate the video, which can make working
    with your FLA file difficult.

    **Graphic**  
    When you embed a video clip as a graphic symbol, you cannot interact with
    the video using ActionScript (typically you use graphic symbols for static
    images and to create reusable pieces of animation that are tied to the main
    Timeline).

6.  Import the video clip directly onto the Stage (and the Timeline) or as a
    library item.

    By default, Flash Pro places the video you import on the Stage. To import
    into the library only, deselect Place Instance on Stage.

    If you're creating a simple video presentation with linear narration and
    little to no interaction, accept the default setting and import the video to
    the Stage. To create a more dynamic presentation, work with multiple video
    clips, or add dynamic transitions or other elements using ActionScript,
    import the video into the library. After a video clip is in the library,
    customize it by converting it into a MovieClip object that you can more
    easily control with ActionScript.

    By default, Flash Pro expands the Timeline to accommodate the playback
    length of the video clip you are embedding.

7.  Click Finish.

    The Video Import wizard embeds the video into the SWF file. The video
    appears either on the Stage or in the library depending on the embedding
    options you chose.

8.  In the Property inspector (Window \> Properties), give the video clip an
    instance name, and make any modifications to the video clip's properties.

### Import video files into the library

To import files in the FLV or F4V format, use the Import or Import To Library
commands or the Import button in the Video Properties dialog box.

To create your own video player, which dynamically loads FLV or F4V files from
an external source, place your video inside a movie clip symbol. When you load
FLV or F4V files dynamically, adjust the dimensions of the movie clip to match
the actual dimension of the video file and scale the video by scaling the movie
clip.

> **Note:** A best practice is to place video inside a movie clip instance,
> which gives you the most control over the content. The video's Timeline plays
> independently from the main Timeline. You do not have to extend your main
> Timeline by many frames to accommodate the video, which can make working with
> your FLA file difficult.

![](../img/dingbat.png) To import an FLV or F4V file into the library, do one of
the following:

- Select File \> Import \> Import To Library.

- Select any existing video clip in the Library Panel, and select Properties
  from the Library Panel menu. Click Import. Locate the file to import, and
  click Open.

### Change the properties of a video clip

You can change properties for an instance of an embedded video clip on the
Stage, assign the instance an instance name, and change its width, height, and
position on the Stage using the Property inspector. You can also _swap_ an
instance of a video clip—assign a different symbol to an instance of a video
clip. Assigning a different symbol to an instance displays a different instance
on the Stage but leaves all the other instance properties (such as dimensions
and registration point) intact. In the Video Properties dialog box, you can do
the following:

- View information about an imported video clip, including its name, path,
  creation date, pixel dimensions, length, and file size

- Change the video clip name

- Update the video clip if you modify it in an external editor

- Import an FLV or F4V file to replace the selected clip

- Export a video clip as an FLV or F4V file For lessons on working with video,
  see the Adobe Flash Support Center at
  [www.adobe.com/go/flash_video](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/go/flash_video).

#### Change video instance properties in the Property inspector

1.  Select an instance of an embedded or linked video clip on the Stage.
2.  Select Window \> Properties, and do any of the following:
    - Enter an instance name in the Name text field on the left side of the
      Property inspector.

    - Enter values for W and H to change the dimensions of the video instance.

    - Enter values for X and Y to change the position of the upper-left corner
      of the instance on the Stage.

    - Click Swap. Select a video clip to replace the clip currently assigned to
      the instance.

    > **Note:** You can swap an embedded video clip only with another embedded
    > video clip, and you can swap a linked video clip only with another linked
    > video clip.

#### View video clip properties in the Video Properties dialog box

1.  Select a video clip in the Library Panel.
2.  Select Properties from the Library Panel menu, or click the Properties
    button located at the bottom of the Library Panel. The Video Properties
    dialog box is displayed.

#### Assign a new name to, update, or replace a video with an FLV or F4V file

1.  Select the video clip in the Library Panel and select Properties from the
    Library Panel menu.
2.  Do one of the following:
    - To assign a new name, enter the name in the Name text field.

    - To update a video, navigate to the updated video file and click Open.

    - To replace a video with an FLV or F4V file, click Import, navigate to the
      FLV or F4V file to replace the current clip, and click Open.

### Control video playback using the Timeline

To control playback of an embedded video file, control the Timeline that
contains the video. For example, to pause a video playing on the main Timeline,
you would call a `stop()` action that targets that Timeline. Similarly, you can
control a video object in a movie clip symbol by controlling the playback of
that symbol's Timeline.

You can apply the following actions to imported video objects in movie clips:
`goTo`, `play`, `stop`, `toggleHighQuality`, `stopAllSounds`,
`getURL,``FScommand`, `loadMovie`, `unloadMovie`, `ifFrameLoaded`, and
`onMouseEvent`. To apply actions to a Video object, first convert the Video
object to a movie clip.

To show a live video stream from a camera, use ActionScript. First, place a
Video object on the Stage, select New Video from the Library Panel menu. To
attach the video stream to the Video object, use `Video.attachVideo`.

See also Video and attachVideo (Video.attachVideo method) in the _ActionScript
2.0 Language Reference_, and fl.video in the _ActionScript 3.0 Language
Reference_.

### Update an embedded video after editing its source file

1.  Select the video clip in the Library Panel.

2.  Select Properties and click Update.

    The embedded video clip is updated with the edited file. The compression
    settings you selected when you first imported the video are reapplied to the
    updated clip.

## Tutorials and examples

The following videos and articles provide additional detailed information about
working with video in Flash Pro. Some videos show Flash Pro CS3 or CS4, but
still apply to Flash Pro CS5.

- Article:
  [Video Learning Guide for Flash](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/devnet/flash/learning_guide/video/)
  (Adobe.com)

- Article:
  [Video Learning Guide for Flash](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/devnet/flash/learning_guide/video/)
  (Adobe.com)

- Article:
  [Getting started with the ActionScript 3 FLVPlayback component](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/devnet/flash/quickstart/flvplayback_component/)
  (Adobe.com)

- Article:
  [Skinning the ActionScript 3 FLVPlayback component](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/devnet/flash/articles/skinning_as3_flvcomp.html)
  (Adobe.com)

- Article:
  [Controlling web video with ActionScript 3 FLVPlayback programming](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/devnet/flash/articles/flvplayback_programming.html)
  (Adobe.com)

- Article:
  [Web video template: Spokesperson presentation with synchronized graphics](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/devnet/flash/articles/vidtemplate_corppreso.html)
  (Adobe.com)

- Article:
  [Web video template: Showcase website for personal video](https://web.archive.org/web/20111229165022mp_/http://www.adobe.com/devnet/flash/articles/vidtemplate_vidshowcase.html)
  (Adobe.com)

More Help topics

[Specify the contentPath or source parameter](./controlling-external-video-playback-with-actionscript.md#specify-the-contentpath-or-source-parameter)

[The FLVPlayback component](./controlling-external-video-playback-with-actionscript.md#the-flvplayback-component)

[Video formats and Flash](./create-video-files-for-use-in-flash.md#video-formats-and-flash)

[Test document download performance](../best-practices/optimizing-fla-files-for-swf-output/test-document-download-performance.md)

[About symbols](../symbols-instances-and-library-assets/working-with-symbols.md#about-symbols)

[Playing external FLV or F4V files dynamically](./controlling-external-video-playback-with-actionscript.md#playing-external-flv-or-f4v-files-dynamically)

![](../img/as3LinkIndicator.png)
[Working with video](https://web.archive.org/web/20111229165022mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b90204-7e1a.html)
