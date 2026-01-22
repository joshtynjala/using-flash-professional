# Create video files for use in Flash

Adobe® Flash® Professional CS5 can incorporate digital video footage into
web-based presentations. The FLV and F4V (H.264) video formats offer
technological and creative benefits that let you fuse video together with data,
graphics, sound, and interactive control. FLV and F4V video let you easily put
video on a web page in a format that almost anyone can view.

How you choose to deploy your video determines how you create your video
content, and how you integrate it with Flash Pro. You can incorporate video into
Flash Pro in the following ways:

Stream video with Adobe Flash Media Server  
You can host video content on Adobe® Flash® Media Server, a server solution
optimized to deliver real-time media. Flash Media Server uses the Real-Time
Messaging Protocol (RTMP), a protocol designed for real-time server applications
such as streaming video and audio content. You can host your own Flash Media
Server, or use a hosted Flash® Video® Streaming Service (FVSS). Adobe has
partnered with several content delivery network (CDN) providers to offer hosted
services for delivering on-demand FLV or F4V file video across high-performance,
reliable networks. Built with Flash Media Server and integrated directly into
the delivery, tracking, and reporting infrastructure of the CDN network, FVSS
provides the most effective way to deliver FLV or F4V files to the largest
possible audience without the hassle of setting up and maintaining your own
streaming server hardware and network.

To control video playback and provide intuitive controls for users to interact
with the streaming video, use the FLVPlayback component, Adobe® ActionScript®,
or the
[Open Source Media Framework](https://web.archive.org/web/20120212222322mp_/http://www.opensourcemediaframework.com/)
(OSMF). For more information about using the OSMF, see the
[OSMF documentation](https://web.archive.org/web/20120212222322mp_/http://www.adobe.com/go/learn_fms_docs_en).

Progressively download video from a web server  
If you don't have access to Flash Media Server or FVSS, or your video needs are
for a low-volume website with only limited amounts of video content, you can
consider _progressive downloading_. Progressively downloading a video clip from
a web server doesn't provide the real-time performance that Flash Media Server
does; however, you can use relatively large video clips, and keep the size of
your published SWF files to a minimum.

To control video playback and provide intuitive controls for users to interact
with the video, use the FLVPlayback component or ActionScript.

Embed video in the Flash document  
You can embed a small, short-duration video file directly into the Flash Pro
document, and publish it as part of the SWF file. Embedding video content
directly into the Flash Pro SWF file significantly increases the size of
published file, and is only suitable for small video files (typically less then
10 seconds in length). In addition, the audio to video synchronization (also
known as audio/video sync) can become mis-synchronized when using longer video
clips embedded in the Flash document. Another disadvantage to embedding video
within the SWF file is that you cannot update the video without republishing the
SWF file.

## Control video playback

You can control the playback of video in Flash Pro using the FLVPlayback
component, by writing custom ActionScript to play an external video stream, or
by writing custom ActionScript to control the playback of video in the Timeline
for embedded video.

FLVPlayback component  
Lets you quickly add a full-featured FLV playback control to your Flash Pro
document and provides support for both progressive downloading and streaming FLV
or F4V files. FLVPlayback lets you easily create intuitive video controls for
users to control video playback and apply pre-made skins, or apply your own
custom skins to the video interface. For more information see
[The FLVPlayback component](./controlling-external-video-playback-with-actionscript.md#the-flvplayback-component).

Open Source Media Framework (OSMF)  
The OSMF enables developers to easily choose and combine pluggable components to
create high-quality, full-featured playback experiences. For more information,
see the
[OSMF web site](https://web.archive.org/web/20120212222322mp_/http://www.opensourcemediaframework.com/),
and the
[OSMF documentation](https://web.archive.org/web/20120212222322mp_/http://www.adobe.com/go/learn_fms_docs_en).
The Adobe DevNet article
[RealEyes OSMF Player Sample - Part 1: Setup and Deployment](https://web.archive.org/web/20120212222322mp_/http://www.adobe.com/devnet/flash/articles/reops_pt1.html)
provides a detailed example of working with the OSMF.

Control external video using ActionScript  
Play back external FLV or F4V files in a Flash Pro document at runtime using the
`NetConnection` and `NetStream` ActionScript objects. For more information see
[Controlling external video playback with ActionScript](./controlling-external-video-playback-with-actionscript.md).

You can use video behaviors (pre-written ActionScript scripts) to control video
playback.

Control embedded video in the Timeline  
To control playback of embedded video files, you must write ActionScript to
control the Timeline containing the video. For more information see
[Control video playback using the Timeline](./add-video-to-flash.md#control-video-playback-using-the-timeline).

## The Video Import Wizard

The Video Import Wizard simplifies the importing of video into a Flash Pro
document by guiding you through the process of selecting an existing video file,
and importing the file for use in one of three different video playback
scenarios. The Video Import Wizard provides a basic level of configuration for
the import and playback method you choose, which you can later modify for your
specific requirements.

The Video Import dialog box provides three video import options:

Load external video with playback component  
Imports the video and creates an instance of the FLVPlayback component to
control video playback. When you are ready to publish the Flash document as a
SWF and upload it to your web server, you must also upload the video file to
either a web server or Flash Media Server, and configure the FLVPlayback
component with the location of the uploaded video file.

Embed FLV or F4V in SWF and play in timeline  
Embeds the FLV or F4V into the Flash document. When you import video this way,
the video is placed in the Timeline where you can see the individual video
frames represented in the Timeline frames. An embedded FLV or F4V video file
becomes part of the Flash Pro document.

> **Note:** Embedding video content directly into the Flash Pro SWF file
> significantly increases the size of published file, and is only suitable for
> small video files. In addition, the audio to video synchronization (also known
> as audio/video sync) can become mis-synchronized when using longer video clips
> embedded in the Flash document.

Import as mobile device video bundled in SWF  
Similar to embedding a video in a Flash Pro document, you bundle a video into a
Flash Lite document for deployment to a mobile device. For information on using
video in Flash Lite documents, see
[Working with video](https://web.archive.org/web/20120212222322mp_/http://help.adobe.com/en_US/flashlite/dev/2x3x/WS5b3ccc516d4fbf351e63e3d118d293e4ad-7ffc.html)
in _Developing Flash Lite 2.x and 3.x Applications_ or
[Working with video](https://web.archive.org/web/20120212222322mp_/http://help.adobe.com/en_US/flashlite/dev/4/WS58a04a822e3e5010-41107fe1122f625ada8-8000.html)
in _Developing Flash Lite 4 Applications_.

## Video formats and Flash

To import video into Flash you must use video encoded in the FLV or H.264
format. The Video Import Wizard (File \> Import \> Import Video) checks video
files that you select for import, and alerts you if the video might not be in a
format that Flash can play. In the event that the video is not in either the FLV
or F4V format, you can use Adobe® Media® Encoder to encode the video in the
appropriate format.

### Adobe Media Encoder

Adobe® Media® Encoder is a stand-alone encoding application employed by programs
such as Adobe® Premiere® Pro, Adobe® Soundbooth®, and Flash Pro for output to
certain media formats. Depending on the program, the Adobe Media Encoder
provides a specialized Export Settings dialog box that accommodates the numerous
settings associated with certain export formats, such as Adobe Flash Video and
H.264. For each format, the Export Settings dialog box includes a number of
presets that are tailored for particular delivery media. You can also save
custom presets, which you can share with others or reload as needed.

For information on encoding video in the FLV or F4V format using Adobe Media
Encoder, see
[Using Adobe Media Encoder](https://web.archive.org/web/20120212222322mp_/http://www.adobe.com/go/learn_amecs5_usingame_en).

### The H.264, On2 VP6, and Sorenson Spark video codecs

When encoding video using Adobe Media Encoder, you can choose from three
different video codecs with which to encode your video content for use with
Flash:

H.264  
Support for the H.264 video codec was incorporated into Flash Player beginning
with version 9.0.r115. The F4V video format which uses this codec provides a
significantly better quality-to-bitrate ratio than previous Flash video codecs,
however, it is more computationally demanding than the Sorenson Spark and On2
VP6 video codecs released with Flash Player 7 and 8.

> **Note:** If you need to use video with alpha channel support for compositing,
> you must use the On2 VP6 video codec; F4V does not support alpha video
> channels.

On2 VP6  
The On2 VP6 codec is the preferred video codec to use when creating FLV files
you intend to use with Flash Player 8 and higher. The On2 VP6 codec provides:

- Higher quality video when compared to the Sorenson Spark codec encoded at the
  same data rate

- Support for the use of an 8-bit alpha channel to composite video

  To support better quality video at the same data rate, the On2 VP6 codec is
  noticeably slower to encode and requires more processor power on the client
  computer to decode and play back. For this reason, carefully consider the
  lowest common denominator of computer you intend your viewing audience to use
  when accessing your FLV video content.

Sorenson Spark  
Introduced in Flash Player 6, the Sorenson Spark video codec should be used if
you intend to publish Flash documents requiring backwards compatibility to Flash
Player 6 and 7. If you anticipate a large user base that uses older computers,
you should consider FLV files encoded with the Sorenson Spark codec, as it is
much less computationally demanding to play back than either the On2 VP6 or
H.264 codecs.

If your Flash Pro content dynamically loads Flash Pro video (using either
progressive download or Flash Media Server), you can use On2 VP6 video without
having to republish a SWF file originally created for use with Flash Player 6 or
7, as long as users use Flash Player 8 or later to view your content. By
streaming or downloading On2 VP6 video into Flash SWF versions 6 or 7, and
playing the content using Flash Player 8 or later, you avoid having to recreate
your SWF files for use with Flash Player 8 and later versions. Important: Only
Flash Player 8 and 9 support both publish and playback of On2 VP6 video.

| Codec          | SWF version (publish version) | Flash Player version (required for playback) |
| -------------- | ----------------------------- | -------------------------------------------- |
| Sorenson Spark | 6                             | 6, 7, 8                                      |
|                | 7                             | 7, 8, 9, 10                                  |
| On2 VP6        | 6, 7, 8                       | 8, 9, 10                                     |
| H.264          | 9.2 or later                  | 9.2 or later                                 |

### Tips for creating Adobe FLV and F4V video

Follow these guidelines to deliver the best possible FLV or F4V video:

#### Work with video in the native format of your project until your final output

If you convert a precompressed digital video format into another format such as
FLV or F4V, the previous encoder can introduce video noise. The first compressor
already applied its encoding algorithm to the video, reducing its quality, frame
size, and rate. That compression may have also introduced digital artifacts or
noise. This additional noise affects the final encoding process, and a higher
data rate may be required to encode a good-quality file.

#### Strive for simplicity

Avoid elaborate transitions—they don't compress well and can make your final
compressed video look "chunky" during the change. Hard cuts (as opposed to
dissolves) are usually best. Eye-catching video sequences—for instance showing
an object zooming from behind the first track, doing a "page peel," or wrapping
around a ball and then flying off the screen—don't compress well and should be
used sparingly.

#### Know your audience data rate

When you deliver video over the Internet, produce files at lower data rates.
Users with fast Internet connections can view the files with little or no delay
for loading, but dial‑up users must wait for files to download. Make the clips
short to keep the download times within acceptable limits for dial‑up users.

#### Select the proper frame rate

Frame rate indicates frames per second (fps). If you have a higher data rate
clip, a lower frame rate can improve playback through limited bandwidth. For
example, if you are compressing a clip with little motion, cutting the frame
rate in half probably saves you only 20% of the data rate. However, if you are
compressing high-motion video, reducing the frame rate has a much greater effect
on the data rate.

Because video looks much better at native frame rates, leave the frame rate high
if your delivery channels and playback platforms allow. For web delivery, get
this detail from your hosting service. For mobile devices, use the
device-specific encoding presets, and the device emulator available through
Adobe Media Encoder in Adobe Premiere Pro. If you need to reduce the frame rate,
the best results come from dividing the frame rate by whole numbers.

#### Select a frame size that fits your data rate and frame aspect ratio

At a given data rate (connection speed), increasing the frame size decreases
video quality. When you select the frame size for your encoding settings,
consider frame rate, source material, and personal preferences. To prevent
pillarboxing, it's important to choose a frame size of the same aspect ratio as
that of your source footage. For example, you get pillarboxing if you encode
NTSC footage to a PAL frame size.

Adobe Media Encoder makes several Adobe FLV or F4V video presets available.
These include preset frame sizes and frame rates for the different television
standards at different data rates. Use the following list of common frame sizes
(in pixels) as a guide, or experiment with the various Adobe Media Encoder
presets to find the best setting for your project.

Dial-up Modem NTSC 4 x 3  
162 x 120

Dial-up Modem PAL 4 x 3  
160 x 120

T1/DSL/cable NTSC 4 x 3  
648 x 480

T1/DSL/cable PAL 4 x 3  
768 x 576

#### Stream for best performance

To eliminate download time, provide deep interactivity and navigation
capabilities, or monitor quality of service, stream Adobe FLV or F4V video files
with the Flash Media Server or use the hosted service from one of Adobe's Flash
Video Streaming Service partners available through the Adobe website. For more
details on the difference between Progressive Download and Streaming with Flash
Media Server, see "Delivering Flash Video: Understanding the Difference Between
Progressive Download and Streaming Video" on the Flash Developer Center website.

#### Know progressive download times

Know how long it will take to download enough of your video so that it can play
to the end without pausing to finish downloading. While the first part of your
video clip downloads, you may want to display other content that disguises the
download. For short clips, use the following formula: Pause = download time –
play time + 10% of play time. For example, if your clip is 30 seconds long and
it takes one minute to download, give your clip a 33‑second buffer (60 seconds –
30 seconds + 3 seconds = 33 seconds).

#### Remove noise and interlacing

For the best encoding, you might need to remove noise and interlacing.

The higher the quality of the original, the better the final result. Although
frame rates and sizes of Internet video are usually smaller than those of
television, computer monitors have much better color fidelity, saturation,
sharpness, and resolution than conventional televisions. Even with a small
window, image quality can be more important for digital video than for standard
analog television. Artifacts and noise that are barely noticeable on TV can be
obvious on a computer screen.

Adobe Flash is intended for progressive display on computer screens and other
devices, rather than on interlaced displays such as TVs. Interlaced footage
viewed on a progressive display can exhibit alternating vertical lines in
high-motion areas. Thus, Adobe Media Encoder removes interlacing from all video
footage that it processes.

#### Follow the same guidelines for audio

The same considerations apply to audio production as to video production. To
achieve good audio compression, begin with clean audio. If you are encoding
material from a CD, try to record the file using direct digital transfer instead
of through the analog input of your sound card. The sound card introduces an
unnecessary digital-to-analog and analog-to-digital conversion that can create
noise in your source audio. Direct digital transfer tools are available for
Windows and Macintosh platforms. To record from an analog source, use the
highest-quality sound card available.

> **Note:** If your source audio file is monaural (mono), it is recommended that
> you encode in mono for use with Flash. If you are encoding with Adobe Media
> Encoder, and using an encoding preset, be sure to check if the preset encodes
> in stereo or mono, and select mono if necessary.

## Tutorials and examples

The following articles provide detailed explanations of creating and preparing
video for use in Flash Pro. Some items show Flash Pro CS3 or CS4, but still
apply to Flash Pro CS5.

- Article:
  [Using Adobe Media Encoder](https://web.archive.org/web/20120212222322mp_/http://www.adobe.com/devnet/flash/quickstart/video_encoder/)
  (Adobe.com)

- Article:
  [H.264 for the rest of us](https://web.archive.org/web/20120212222322mp_/http://www.adobe.com/devnet/flashmediaserver/articles/h264_primer.html)
  (Adobe.com)

More Help topics

[Add video to Flash](./add-video-to-flash.md)

[The FLVPlayback component](./controlling-external-video-playback-with-actionscript.md#the-flvplayback-component)

[Controlling external video playback with ActionScript](./controlling-external-video-playback-with-actionscript.md)
