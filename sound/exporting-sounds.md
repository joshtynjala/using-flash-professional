# Exporting Sounds

## About compressing sounds for export

You can select compression options for individual event sounds and export the
sounds with those settings. You can also select compression options for
individual stream sounds. However, all stream sounds in a document are exported
as a single stream file, using the highest setting of all those applied to
individual stream sounds. This includes stream sounds in video objects.

If you select global compression settings for event sounds or stream sounds in
the Publish Settings dialog box, these settings are applied to individual event
sounds or all stream sounds if you do not select compression settings for the
sounds in the Sound Properties dialog box.

You can also override export settings specified in the Sound Properties dialog
box by selecting Override Sound Settings in the Publish Settings dialog box.
This option is useful if you want to create a larger high-fidelity audio file
for local use and a smaller low-fidelity version for the web.

The sampling rate and degree of compression make a significant difference in the
quality and size of sounds in exported SWF files. The more you compress a sound
and the lower the sampling rate, the smaller the size and the lower the quality.
You should experiment to find the optimal balance between sound quality and file
size.

When working with imported mp3 files, you can export the files in mp3 format
using the same settings that the files had when imported.

> **Note:** In Windows, you can also export all the sounds from a document as a
> WAV file using File \> Export \> Export Movie.

## Compress a sound for export

1.  Do one of the following:

    - Double-click the sound's icon in the Library panel.

    - Right-click (Windows) or Control-click (Macintosh) a sound file in the
      Library panel and select Properties from the context menu.

    - Select a sound in the Library panel and select Properties from the Panel
      menu in the upper-right corner of the panel.

    - Select a sound in the Library panel and click the Properties button at the
      bottom of the Library panel.

2.  If the sound file has been edited externally, click Update.

3.  For Compression, select Default, ADPCM, mp3, Raw, or Speech.

    The Default compression option uses the global compression settings in the
    Publish Settings dialog box when you export your SWF file. If you select
    Default, no additional export settings are available.

4.  Set export settings.

5.  Click Test to play the sound once. Click Stop if you want to stop testing
    the sound before it finishes playing.

6.  Adjust export settings if necessary until the desired sound quality is
    achieved, and then click OK.

### ADPCM and Raw compression options

**ADPCM** compression sets compression for 8- or 16-bit sound data. Use the
ADPCM setting when you export short event sounds such as button clicks.

**Raw** compression exports sounds with no sound compression.

Preprocessing  
Converts mixed stereo sounds to monaural (mono) when you select Convert Stereo
To Mono (mono sounds are unaffected by this option).

Sample Rate  
Controls sound fidelity and file size. Lower rates decrease file size but can
also degrade sound quality. Rate options are as follows:

5 kHz  
Barely acceptable for speech.

11 kHz  
The lowest recommended quality for a short segment of music and one-quarter the
standard CD rate.

22 kHz  
A popular choice for web playback and half the standard CD rate.

44 kHz  
The standard CD audio rate.

> **Note:** Flash Pro cannot increase the kHz rate of an imported sound above
> the rate at which it was imported.

ADPCM Bits  
(ADPCM only) Specifies the bit depth of the sound compression. Higher bit depths
produce higher quality sound.

### mp3 compression options

MP3 Compression  
Lets you export sounds with mp3 compression. Use mp3 when you are exporting
longer stream sounds such as music sound tracks.

If you are exporting a file that was imported in mp3 format, you can export the
file using the same settings the file had when it was imported.

Use Imported mp3 Quality  
Default setting. Deselect to select other mp3 compression settings. Select to
export an imported mp3 file with the same settings the file had when it was
imported.

Bit Rate  
Determines the bits per second in the exported sound file. Flash Pro supports 8
through 160 Kbps CBR (constant bit rate). When you export music, set the bit
rate to 16 Kbps or higher for best results.

Preprocessing  
Converts mixed stereo sounds to monaural (mono sounds are unaffected by this
option).

> **Note:** The Preprocessing option is available only if you select a bit rate
> of 20 Kbps or higher.

Quality  
Determines the compression speed and sound quality:

Fast  
Yields faster compression but lower sound quality.

Medium  
Yields somewhat slower compression but higher sound quality.

Best  
Yields the slowest compression and the highest sound quality.

### Speech compression option

**Speech** compression exports sounds using a compression that is adapted to
speech.

> **Note:** Flash Lite 1.0 and Flash Lite 1.1 do not support the Speech
> compression option. For content targeting those player versions, use mp3,
> ADPCM, or Raw compression.

Sample rate  
Controls sound fidelity and file size. A lower rate decreases file size but can
also degrade sound quality. Select from the following options:

5 kHz  
Acceptable for speech.

11 kHz  
Recommended for speech.

22 kHz  
Acceptable for most types of music on the web.

44 kHz  
The standard CD audio rate. However, because compression is applied, the sound
is not CD quality in the SWF file.

## Guidelines for exporting sound in Flash documents

Besides sampling rate and compression, there are several ways to use sound
efficiently in a document and keep file size small:

- Set the in and out points to prevent silent areas from being stored in the
  Flash Pro file and to reduce the size of the sound data in the file.

- Get more out of the same sounds by applying different effects for sounds (such
  as volume envelopes, looping, and in/out points) at different keyframes. You
  can get a number of sound effects by using only one sound file.

- Loop short sounds for background music.

- Do not set streaming sound to loop.

- When exporting audio in embedded video clips, remember that the audio is
  exported using the global streaming settings selected in the Publish Settings
  dialog box.

- Use stream synchronization to keep the animation synchronized to your sound
  track when you preview your animation in the editor. If your computer is not
  fast enough to draw the animation frames so that they keep up with your sound
  track, Flash Pro skips frames.

- When exporting QuickTime movies, use as many sounds and channels as you want
  without worrying about file size. The sounds are combined into a single sound
  track when you export as a QuickTime file. The number of sounds you use has no
  effect on the final file size.

More Help topics

[Publishing overview](../publishing-and-exporting/publishing-flash-documents.md#publishing-overview)

[Specify publish settings for SWF files (CS5)](../publishing-and-exporting/publish-settings-cs5.md#specify-publish-settings-for-swf-files-cs5)

[About exporting from Flash](../publishing-and-exporting/about-exporting-from-flash.md)
