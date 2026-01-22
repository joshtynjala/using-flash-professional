# Sound and ActionScript

With ActionScript®, you can control sounds at runtime. Using ActionScript allows
you to create interaction and other capabilities in your FLA files that is not
possible with the Timeline alone.

The additional resources describe how to work with sound in ActionScript 3.0:

- AS3 Developer's Guide:
  [Working with Sound](https://web.archive.org/web/20111231232952mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b8f2ae-8000.html)

## Control sounds using behaviors

Using sound behaviors, prewritten ActionScript 2.0, you can add sounds to your
document and control sound playback. Adding a sound using these behaviors
creates an instance of the sound, which is then used to control the sound.

> **Note:** ActionScript 3.0 and Flash Lite 1.x and Flash Lite 2.x do not
> support behaviors.

### Load a sound to a file using a behavior

1.  Select the object, such as a button, that you want to use to trigger the
    behavior.
2.  In the Behaviors panel (Window \> Behaviors), click the Add (+) button and
    select Sound \> Load Sound from Library or Sound \> Load Streaming mp3 File.
3.  In the Load Sound dialog box, enter the linkage identifier for a sound from
    the Library, or the sound location for a streaming mp3 file. Next, enter a
    name for this instance of the sound, and click OK.
4.  In the Behaviors panel under event, click On Release (the default event),
    and select a mouse event from the menu. If you want to use the `OnRelease`
    event, do not change the option.

### Play or stop sounds using a behavior

1.  Select the object, such as a button, that you want to use to trigger the
    behavior.
2.  In the Behaviors panel (Window \> Behaviors), click the Add (+) button.
3.  Select Sound \> Play Sound, Sound \> Stop Sound, or Sound \> Stop All
    Sounds.
4.  In the dialog box that appears, do one of the following:
    - Enter the linkage identifier and the instance name of the sound you want
      to play or stop, and click OK.

    - Click OK to verify that you want to stop all sounds.

5.  In the Behaviors panel under Event, click On Release (the default event) and
    select a mouse event from the menu. If you want to use the `OnRelease`
    event, do not change the option.

## Control sounds with the ActionScript 2.0 Sound object

Use the Sound object in ActionScript 2.0 to add sounds to a document and to
control sound objects in a document, including adjusting the volume or the right
and left balance while a sound plays. For more information, see Creating sound
controls in
[_Learning ActionScript 2.0 in Flash_](https://web.archive.org/web/20111231232952mp_/http://www.adobe.com/go/learn_cs5_learningas2_en).

1.  Select the sound in the Library panel.
2.  Select Linkage from the Panel menu in the upper-right corner of the panel,
    or right-click (Windows) or Control-click (Macintosh) the sound name in the
    Library panel and select Linkage from the context menu.
3.  Under Linkage in the Linkage Properties dialog box, select Export for
    ActionScript.
4.  Enter an identifier string in the box, and click OK.

## About the ActionScript 2.0 onSoundComplete event

The `onSoundComplete` event of the ActionScript 2.0 Sound object lets you
trigger an event in a Flash Pro application based on completing an attached
sound file. The Sound object is a built-in object that lets you control sounds
in a Flash Pro application. For more information, see Sound in the
[_ActionScript 2.0 Language Reference_](https://web.archive.org/web/20111231232952mp_/http://www.adobe.com/go/learn_cs5_as2lr_en).
The `onSoundComplete` event of a Sound object is invoked automatically when the
attached sound file finishes playing. If the sound is looped a specified number
of times, the event is triggered when the sound finishes looping.

The Sound object has two properties that you can use with the `onSoundComplete`
event. The `duration` property is a read-only property representing the
duration, in milliseconds, of the sound sample attached to the sound object. The
`position` property is a read-only property representing the number of
milliseconds the sound has been playing in each loop.

The `onSoundComplete` event lets you manipulate sounds in a many ways, such as
the following:

- Creating a dynamic playlist or sequencer

- Creating a multimedia presentation that checks for narration completion before
  advancing to the next frame or scene

- Building a game that synchronizes sounds to particular events or scenes and
  transitions smoothly between different sounds

- Timing an image change to a sound—for example, changing an image when a sound
  is halfway through at playback time

## Accessing ID3 properties in mp3 files with Flash Player

Macromedia Flash Player 7 from Adobe and later supports ID3 v2.4 and v2.4 tags.
With this version, when you load an mp3 sound using the ActionScript 2.0
`attachSound()` or `loadSound()` method, the ID3 tag properties are available at
the beginning of the sound data stream. The onID3 event executes when the ID3
data is initialized.

Flash Player 6 (6.0.40.0) and later supports mp3 files with ID3 v1.0 and v1.1
tags. With ID3 v1.0 and v1.1 tags, the properties are available at the end of
the data stream. If a sound does not contain an ID3v1 tag, the ID3 properties
are undefined. Users must have Flash Player 6 (6.0.40.0) or later for the ID3
properties to function.

For more information on using the ID3 properties, see `id3` (`Sound.id3`
property) in the
[_ActionScript 2.0 Language Reference_](https://web.archive.org/web/20111231232952mp_/http://www.adobe.com/go/learn_cs5_as2lr_en).
