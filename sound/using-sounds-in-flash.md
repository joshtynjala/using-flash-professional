# Using sounds in Flash

## About sounds and Flash

Adobe® Flash® Professional CS5 offers several ways to use sound. Make sounds
that play continuously, independent of the Timeline, or use the Timeline to
synchronize animation to a sound track. Add sounds to buttons to make them more
interactive, and make sounds fade in and out for a more polished sound track.

There are two types of sounds in Flash Pro: event sounds and stream sounds. An
event sound must download completely before it begins playing, and it continues
playing until explicitly stopped. Stream sounds begin playing as soon as enough
data for the first few frames has been downloaded; stream sounds are
synchronized to the Timeline for playing on a website.

If you're creating Flash Pro content for mobile devices, Flash Pro also lets you
include device sounds in your published SWF file. Device sounds are encoded in
the device's natively supported audio format, such as MIDI, MFi, or SMAF.

You can use shared libraries to link a sound to multiple documents. You can also
use the ActionScript® 2.0 `onSoundComplete` event or ActionScript® 3.0
`soundComplete` event to trigger an event based on the completion of a sound.

You can load sounds and control sound playback using prewritten behaviors or
media components; the latter also provide a controller for stop, pause, rewind,
and so on. You can also use ActionScript 2.0 or 3.0 to load sounds dynamically.

For more information, see `attachSound (Sound.attachSound method)` and
`loadSound (Sound.loadSound method)`in _ActionScript 2.0 Language Reference_ or
`Sound class` in _ActionScript 3.0 Language and Components Reference_.

## Importing sounds

You place sound files into Flash Pro by importing them into the library for the
current document.

1.  Select File \> Import \> Import To Library.
2.  In the Import dialog box, locate and open the desired sound file.

> **Note:** You can also drag a sound from a common library into the library for
> the current document. Flash Pro stores sounds in the library along with
> bitmaps and symbols. You need only one copy of a sound file to use that sound
> multiple ways in your document.

If you want to share sounds among Flash Pro documents, you can include the
sounds in shared libraries.

Flash Pro includes a Sounds library containing many useful sounds that can be
used for effects. To open the Sounds library, choose Window \> Common
Libraries \> Sounds. To import a sound from the Sounds library to your FLA file,
drag the sound from the Sounds library to the Library panel of your FLA file.
You can also drag sounds from the Sounds library to other shared libraries.

Sounds can use large amounts of disk space and RAM. However, mp3 sound data is
compressed and smaller than WAV or AIFF sound data. Generally, when using WAV or
AIFF files, it's best to use 16-22 kHz mono sounds (stereo uses twice as much
data as mono), but Flash Pro can import either 8- or 16-bit sounds at sample
rates of 11, 22, or 44 kHz. Sounds recorded in formats that are not multiples of
11 kHz (such as 8, 32, or 96 kHz) are resampled when imported into Flash Pro.
Flash Pro can convert sounds to lower sample rates on export.

If you want to add effects to sounds in Flash Pro, it's best to import 16-bit
sounds. If you have limited RAM, keep your sound clips short or work with 8-bit
sounds instead of 16‑bit sounds.

## Supported sound file formats

You can import the following sound file formats into Flash Pro:

- ASND (Windows or Macintosh). This is the native sound format of Adobe®
  Soundbooth™.

- WAV (Windows only)

- AIFF (Macintosh only)

- mp3 (Windows or Macintosh)

  If you have QuickTime® 4 or later installed on your system, you can import
  these additional sound file formats:

- AIFF (Windows or Macintosh)

- Sound Designer® II (Macintosh only)

- Sound Only QuickTime Movies (Windows or Macintosh)

- Sun AU (Windows or Macintosh)

- System 7 Sounds (Macintosh only)

- WAV (Windows or Macintosh)

  > **Note:** The ASND format is a non-destructive audio file format, native to
  > Adobe Soundbooth. ASND files can contain audio data with effects that can be
  > modified later, Soundbooth multitrack sessions, and snapshots that allow you
  > to revert to a previous state of the ASND file.

## Add a sound to the Timeline

You can add a sound to a document using the library, or you can load a sound
into a SWF file during runtime, using the `loadSound` method of the Sound
object. For more information, see `loadSound (Sound.loadSound method)` in the
[_ActionScript 2.0 Language Reference_](https://web.archive.org/web/20110926102307mp_/http://www.adobe.com/go/learn_cs5_as2lr_en)
or `Sound Class` in the
[_ActionScript 3.0 Reference_](https://web.archive.org/web/20110926102307mp_/http://www.adobe.com/go/learn_flcs5_as3lr_en).

1.  Import the sound into the library if it has not already been imported.

2.  Select Insert \> Timeline \> Layer.

3.  With the new sound layer selected, drag the sound from the Library panel
    onto the Stage. The sound is added to the current layer.

    You can place multiple sounds on one layer or on layers containing other
    objects. However, it is recommended that each sound be placed on a separate
    layer. Each layer acts as a separate sound channel. The sounds on all layers
    are combined when you play the SWF file.

4.  In the Timeline, select the first frame that contains the sound file.

5.  Select Window \> Properties, and click the arrow in the lower-right corner
    to expand the Property inspector.

6.  In the Property inspector, select the sound file from the Sound pop-up menu.

7.  Select an effect option from the Effects pop-up menu:

    **None**  
    Applies no effects to the sound file. Select this option to remove
    previously applied effects.

    **Left Channel/Right Channel**  
    Plays sound in the left or right channel only.

    **Fade Left To Right/Fade Right To Left**  
    Shifts the sound from one channel to the other.

    **Fade In**  
    Gradually increases the volume of a sound over its duration.

    **Fade Out**  
    Gradually decreases the volume of a sound over its duration.

    **Custom**  
    Lets you create custom in and out points of sound using the Edit Envelope.

8.  Select a synchronization option from the Sync pop-up menu:

    > **Note:** If you are placing the sound on a frame other than frame 1 in
    > the main Timeline, select the Stop option.

    **Event**  
    Synchronizes the sound to the occurrence of an event. An event sound, such
    as a sound that plays when a user clicks a button, plays when its starting
    keyframe first appears and plays in its entirety, independently of the
    Timeline, even if the SWF file stops playing. Event sounds are mixed when
    you play your published SWF file. If an event sound is playing and the sound
    is instantiated again (for example, by the user clicking the button again),
    the first instance of the sound continues to play and another instance
    begins to play simultaneously.

    **Start**  
    The same as Event, except that if the sound is already playing, no new
    instance of the sound plays.

    **Stop**  
    Silences the specified sound.

    **Stream**  
    Synchronizes the sound for playing on a website. Flash Pro forces animation
    to keep pace with stream sounds. If Flash Pro can't draw animation frames
    quickly enough, it skips frames. Unlike event sounds, stream sounds stop if
    the SWF file stops playing. Also, a stream sound can never play longer than
    the length of the frames it occupies. Stream sounds are mixed when you
    publish your SWF file.

    An example of a stream sound is the voice of a character in an animation
    that plays in multiple frames.

    **Note:** If you use an mp3 sound as a stream sound, you must recompress the
    sound for export. You can export the sound as an mp3 file, with the same
    compression settings that it had on import.

9.  Enter a value for Repeat to specify the number of times the sound should
    loop, or select Loop to repeat the sound continuously.

    For continuous play, enter a number large enough to play the sound for an
    extended duration. For example, to loop a 15-second sound for 15 minutes,
    enter 60. Looping stream sounds is not recommended. If a stream sound is set
    to loop, frames are added to the file and the file size is increased by the
    number of times the sound is looped.

10. To test the sound, drag the playhead over the frames containing the sound or
    use commands in the Controller or the Control menu.

## Add a sound to a button

You can associate sounds with the different states of a button symbol. Because
the sounds are stored with the symbol, they work for all instances of the
symbol.

1.  Select the button in the Library panel.

2.  Select Edit from the Panel menu in the upper-right corner of the panel.

3.  In the button's Timeline, add a layer for sound (Insert \> Timeline \>
    Layer).

4.  In the sound layer, create a regular or blank keyframe to correspond with
    the button state to which you want to add a sound (Insert \> Timeline \>
    Keyframe or Insert \> Timeline \> Blank Keyframe).

    For example, to add a sound that plays when you click the button, create a
    keyframe in the frame labeled Down.

5.  Click the keyframe you created.

6.  Select Window \> Properties.

7.  In the Property inspector, select a sound file from the Sound pop-up menu.

8.  Select Event from the Sync pop-up menu.

    To associate a different sound with each of the button's keyframes, create a
    blank keyframe and add another sound file for each keyframe. You can also
    use the same sound file and apply a different sound effect for each button
    keyframe.

## Synchronize a sound with animation

To synchronize a sound with animation, you start and stop the sound at
keyframes.

1.  Add a sound to a document.

2.  To synchronize this sound with an event in the scene, select a beginning
    keyframe that corresponds to the keyframe of the event in the scene. You can
    select any of the synchronization options.

3.  Create a keyframe in the sound layer's Timeline at the frame where you want
    the sound to end. A representation of the sound file appears in the
    Timeline.

4.  Select Window \> Properties, and click the arrow in the lower-right corner
    to expand the Property inspector.

5.  In the Property inspector, select the same sound from the Sound pop-up menu.

6.  Select Stop from the Sync pop-up menu.

    When you play the SWF file, the sound stops playing when it reaches the
    ending keyframe.

7.  To play back the sound, simply move the playhead.

## Edit a sound in Flash

In Flash Pro, you can define the starting point of a sound or control the volume
of the sound as it plays. You can also change the point at which a sound starts
and stops playing. This is useful for making sound files smaller by removing
unused sections.

1.  Add a sound to a frame, or select a frame that already contains a sound.
2.  Select Window \> Properties.
3.  Click the Edit button on the right side of the Property inspector.
4.  Do any of the following:
    - To change the start and end points of a sound, drag the Time In and Time
      Out controls in the Edit Envelope.

    - To change the sound envelope, drag the envelope handles to change levels
      at different points in the sound. Envelope lines show the volume of the
      sound as it plays. To create additional envelope handles (up to eight
      total), click the envelope lines. To remove an envelope handle, drag it
      out of the window.

    - To display more or less of the sound in the window, click the Zoom In or
      Out buttons.

    - To switch the time units between seconds and frames, click the Seconds and
      Frames buttons.

5.  To hear the edited sound, click the Play button.

## Edit a sound in Soundbooth

If you have Adobe Soundbooth installed, you can use Soundbooth to edit sounds
you have imported into your FLA file. After making changes in Soundbooth, when
you save the file and overwrite the original, the changes are automatically
reflected in the FLA file.

If you change the filename or format of the sound after editing it, you will
need to re-import it into Flash Pro.

> **Note:** Soundbooth is available only on Windows computers and Intel®-based
> Macintoshes. To edit an imported sound in Soundbooth:

1.  Right-click (Windows) or Ctrl-click (Macintosh) the sound in the Library
    panel.

2.  Choose Edit in Soundbooth from the context menu. The file opens in
    Soundbooth.

3.  Edit the file in Soundbooth.

4.  When you are finished, save the file. To save the changes in a
    non-destructive format, choose the ASND format.

    If you save the file in a different format from the original, you will need
    to re-import the sound file into Flash Pro.

5.  Return to Flash Pro to see the edited version of the sound file in the
    Library panel.

> **Note:** You cannot edit sounds from the Sounds library (Window \> Common
> Libraries \> Sounds) with the Edit in Soundbooth command. To edit these sounds
> in Soundbooth, open Soundbooth and select the sound from the Resource Central
> panel. Edit the sound and then import it into Flash Pro.

## Using sounds in Flash Lite

Adobe® Flash® Lite supports two types of sound: standard Flash Pro sounds, like
those used in Flash Pro desktop applications, and device sounds. Flash Lite 1.0
supports device sounds only; Flash Lite 1.1 and 2.x support both standard sounds
and device sounds.

Device sounds are stored in the published SWF file in their native audio format
(such as MIDI or MFi); during playback, Flash Lite passes the sound data to the
device, which decodes and plays the sound. Because you can't import most device
audio formats into Flash Pro, you instead import a _proxy_ sound in a supported
format (such as mp3 or AIFF) that is replaced with an external device sound that
you specify.

You can use device sounds only as event sounds—you can't synchronize device
sounds with the Timeline as you can with standard sounds.

Flash Lite 1.0 and Flash Lite 1.1 do not support the following features
available in the desktop version of Flash® Player:

- The ActionScript Sound object

- Loading of external mp3 files

- The Speech Audio Compression option

For more information, see "Working with Sound, Video, and Images" in _Developing
Flash Lite 2.x Applications_ or "Working with Sound" in _Developing Flash Lite
1.x Applications_.

More Help topics

[Sharing library assets at runtime](../symbols-instances-and-library-assets/sharing-library-assets-across-files.md#sharing-library-assets-at-runtime)

[Work with common libraries](../symbols-instances-and-library-assets/working-with-the-library.md#work-with-common-libraries)

![](../img/as3LinkIndicator.png)
[Working with sound](https://web.archive.org/web/20110926102307mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b8f2ae-8000.html)
