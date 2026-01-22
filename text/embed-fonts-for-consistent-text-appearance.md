# Embed fonts for consistent text appearance

When your published SWF files play on computers across the Internet, there is no
guarantee that the fonts you used are available on those machines. To ensure
that your text maintains the appearance you intended, you can embed entire fonts
or specific subsets of characters from a font. By embedding the characters in
your published SWF file, you make the font available to the SWF file regardless
of the computer that plays the file. Once a font is embedded, you can use it
anywhere in your published SWF file.

Beginning with Flash Professional CS5, Flash automatically embeds all characters
used by any text objects that contain text. Creating an embedded font symbol
yourself allows your text objects to use additional characters, such as when
accepting user input at runtime or when editing text with ActionScript. Embedded
fonts are not necessary for text objects that have the Anti-alias property set
to Use Device Fonts. You specify which fonts you want embedded in your FLA file,
and Flash embeds the fonts when you publish a SWF file.

There are 4 common situations in which to ensure correct text appearance by
embedding fonts in a SWF file:

- When creating text objects in your FLA file that are part of a design that
  requires consistent text appearance.

- When you are using an anti-alias option other than Use Device Fonts, you must
  embed the fonts or text may disapppear or appear incorrectly. See
  [Work with text anti-aliasing](./working-with-classic-text.md#work-with-text-anti-aliasing).

- When generating text dynamically with ActionScript in your FLA file.

  When creating dynamic text with ActionScript, you must specify in ActionScript
  which font to use.

- When your SWF file contains text objects and may be loaded by another SWF file
  that does not have the required fonts embedded.

The Font Embedding dialog box allows you to:

- Manage all embedded fonts in one place.

- Create font symbols for each embedded font.

- Select custom ranges of embedded characters for a font as well as pre-defined
  ranges.

- Work with both Text Layout Framework (TLF) text and Classic text in the same
  file and use embedded fonts with each.

- Continue to work with Flash Professional CS4 and earlier FLA files that
  contain fonts embedded with the older method that associated the embedded
  characters with a specific text object. When you open an older FLA file, Flash
  Professional CS5 and later allow you to edit these older embedded fonts with
  the Font Embedding dialog box.

#### To embed characters from a font in a SWF file:

1.  With your FLA file open in Flash, open the Font Embedding dialog box by
    doing one of the following:
    - Choose Text \> Font Embedding.

    - From the Library panel options menu, choose Add Font.

    - Right-click in empty space in the Library panel tree view, and choose New
      Font.

    - In the Text Property inspector, click on the Embed button.

2.  If your font is not already selected in the Font Embedding dialog box, click
    the Add (+) button to add a new embedded font to your FLA file.

    When you open the Font Embedding dialog box from the Library or the Text
    Property inspector, a font item appears automatically in the dialog box.

3.  In the Options tab, select the Family and Style of the font you want to
    embed.

    If you opened the Font Embedding dialog box from the Text Property inspector
    or from the Library panel, the font used by the current selection appears
    automatically in the dialog box.

4.  In the Character Ranges section, select the character ranges you want to
    embed. The more characters you embed, the larger your published SWF file
    will be.

5.  If you want to embed any additional specific characters, enter them in the
    "Also include these characters" field.

6.  To enable the embedded font symbol to be accessed with ActionScript code,
    select Export for ActionScript in the ActionScript tab.

7.  If you selected Export for ActionScript, select an outline format also. For
    TLF text containers, select TLF (DF4) as the Outline Format. For Classic
    text containers, select Classic (DF3).

    You must create separate embedded font symbols for use in TLF and Classic
    text containers. The TLF (DF4) outline format is not available for
    PostScript Type 1 fonts. TLF (DF4) requires Flash Player version 10 or
    later.

8.  If you want to use the font symbol as a shared asset, select options in the
    Sharing section of the ActionScript tab. For more information about using
    shared assets, see
    [Sharing library assets at runtime](../symbols-instances-and-library-assets/sharing-library-assets-across-files.md#sharing-library-assets-at-runtime).

#### To edit the parameters of an embedded font symbol:

1.  Do one of the following:
    - Right-click the font symbol in the Library and choose Properties.

    - Select a text container on the Stage and click the Embed button in the
      Character section of the Property inspector.

    - Select the font symbol in the Library and choose Edit Properties from the
      panel options menu.

    - Double-click the icon of the font symbol in the Library.

    - Choose Text \> Font Embedding, and then select the font symbol you want to
      edit in the tree view on the left of the dialog.

2.  Make changes in the Font Embedding dialog box and click OK.

The tree view in the Font Embedding dialog box displays all font symbols in the
current FLA file, organized by font family. You can edit any or all of the fonts
while the dialog is open, and the changes will be committed when you press the
OK button.

> **Note:** If you save a Flash Professional CS5 FLA file to CS4 format, font
> symbols are converted to CS4 Font Symbols which will embed the entire range of
> characters in a font, not a selected sub-range. All TLF text blocks are
> converted to Classic text fields. Font symbols are saved in DefineFont3 format
> to ensure compatibility with Classic text. Each CS4 font symbol will contain
> an entire copy of the embedded font information for each font it uses. Saving
> in CS4 format also causes the embedding information to move into any text
> objects that referenced font symbols, as this is how embedded font information
> was stored in Flash Pro CS4 and earlier versions.

#### Additional resources

- Article:
  [Formatting text for localized Flash projects: Font embedding for multiple languages](https://web.archive.org/web/20111122163656mp_/http://www.adobe.com/devnet/flash/articles/text_localization_04.html)
  (Adobe.com)
