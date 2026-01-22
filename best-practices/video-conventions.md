# Video conventions

## About video conventions

Many options are available to edit video before you import it into a FLA
document, or load an FLV file into a SWF file. Flash Pro and Adobe Media Encoder
have greater controls for video compression. Compressing video carefully is
important because it controls the quality of the video footage and the size of
the file. Video files, even when compressed, are large in comparison with most
other assets in your SWF file.

> **Note:** Provide the user with control over the media in a SWF file. For
> example, if you add audio to a document with video (or even a looping
> background sound), let the user control the sound.

## Using video in an application

Before you import video into Flash Pro, consider what video quality you need,
what video format to use with the FLA file, and how to download it. When you
import video into a FLA file (called _embedded video_), it increases the size of
the SWF file that you publish. This video starts progressively downloading to
the user's computer whether or not they view the video.

You can also progressively download or stream the video at runtime from an
external FLV file on your server. When it starts downloading depends on how you
structure your application.

> **Note:** Video progressively downloads from the server like SWF files, which
> is not actually _streaming_. Dynamically loading content has distinct
> advantages over keeping all your content in a single SWF file. For example,
> you will have smaller files and quicker loading, and the user only downloads
> what they want to see or use in your application. You can display external FLV
> video using a component or a video object. A component makes developing
> applications with FLV video easy, because the video controls are prebuilt, and
> you only need to specify an FLV file path to play the content. To keep your
> SWF file as small as possible, display video in a video object and create your
> own assets and code to control the video. Also consider using the FLVPlayback
> component in Adobe® Flash® Professional CS5, which has a smaller file size
> than Media components (Flash MX Professional 2004 and later).

It is a good idea to give users some control (such as the ability to stop,
pause, play, and resume the video, and control volume) over the video in a SWF
file.

To gain certain kinds of flexibility over your video, such as manipulating the
video with animation, or syncing various parts of it with the timeline, embed
the video in the SWF file rather than loading it using ActionScript or one of
the Media components.

For more control over a video instance than the Video class allows, place video
inside a movie clip instance. The video's timeline plays independently from a
Flash Pro timeline, and you can place the content inside a movie clip to control
timelines. You do not have to extend your main Timeline by many frames to
accommodate for the video, which can make working with your FLA file difficult.

## Troubleshooting video

You can create an application and then encounter problems after you upload it to
your server.

- Check that your Flash Player version is correct.

  For example, if you encoded your files using On2 codec, you need Flash Player
  8 or later installed for the browsers you use to view your Flash Pro content.

  > **Note:** For Flash Player and FLV compatibility, see About Using FLV Video
  > in
  > [_Learning ActionScript 2.0 in Adobe Flash_](http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

- Check that your server supports the mime type for the video files you are
  using, FLV or F4V. For more information on video files on a server, see
  Configuring your server for FLV files in [Learning ActionScript 2.0 in Adobe
  Flash]http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

- Check security guidelines.

  If you load FLV files from another server, make sure that you have the proper
  files or code in place to load from that external server. For information on
  policy files, see Server-side policy files for permitting access to data in
  [Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).
  For information about loading and security, see Understanding security in
  [Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

- Check your target paths to your video are correct. If you use relative paths
  (such as /video/water.flv), try using absolute paths (such as
  http://www.helpexamples.com/flash/video/water.flv). If your application
  doesn't work as a relative path, but does work as an absolute path, correct
  the relative path.

- Check that the version of Flash Player you specified in the Publish Settings
  supports the type of video files you are using, either FLV or F4V (H.264).

More Help topics

[Video](../video/index.md)
