# Multilanguage text

## About multilanguage text

You can configure a FLA file to display text in different languages depending on
the language of the operating system that plays the Flash Pro content.

### Multilanguage text in Flash

You can include multilanguage text in your document in the following ways:

- The Strings panel lets localizers edit strings in a central location in Flash
  Pro or in external XML files with their preferred software or translation
  memory. Flash supports multiline strings in both the Strings panel and the XML
  files.

- Select which character sets to embed in your applications, which limits the
  number of character glyphs in your published SWF file and reduces its size.

- Use a Western-style keyboard to create text on the Stage in Chinese, Japanese,
  and Korean.

- If you have Unicode fonts installed on your system, enter text directly into a
  text field. Because the fonts are not embedded, your users must also have
  Unicode fonts.

  Other, less common methods of including multilingual text in your Flash Pro
  documents include the following:

- Include an external text file in a dynamic or input text field by using the
  `#include` action.

- Load external text or XML files into a Flash Pro application at runtime by
  using the `loadVariables` or `getURL` actions, or the `LoadVars` or `XML`
  objects.

- Enter Unicode escape characters in the string value for a dynamic or input
  text field variable.

- Create an embedded font as a symbol in your Library.

  For Unicode-encoded text to appear correctly, users must have access to fonts
  containing the glyphs (characters) used in that text.

For a sample of multilingual content, see the
[Flash Samples page](https://web.archive.org/web/20120102164641/http://www.adobe.com/devnet/flash/samples.html).
Download and decompress the Samples zip file and navigate to the
Text\MultilingualContent folder to access the sample.

### About fonts for Unicode-encoded text

When you use external files that are Unicode encoded, your users must have
access to fonts containing all the glyphs used in your text files. By default,
Flash Pro stores the names of fonts used in dynamic or input text files. During
SWF file playback, Flash Player 7 (and earlier versions) looks for those fonts
on the operating system running the player.

If the text in a SWF file contains glyphs that the specified font does not
support, both Flash Player 7 and Flash Player 8 attempt to locate a font on the
user's system that supports those glyphs. The player cannot always locate an
appropriate font. This behavior depends on the fonts available on the user's
system, as well as on the operating system running Flash Player.

### XML font embedding table

When you select ranges of fonts to embed in a FLA file, Flash Pro uses the
UnicodeTable.xml file to determine which characters to embed. The
UnicodeTable.xml file contains ranges of characters required for various
languages and resides in the user configuration folder of your computer. The
file is located in the following directories:

- Windows: \<boot drive\>\Documents and Settings\\user\>\Local
  Settings\Application
  Data\Adobe\Flash\<version\>\\language\>\Configuration\FontEmbedding\\

- Macintosh: \<user\>/Library/Application Support/Adobe/Flash
  \<version\>/\<language\>/Configuration/FontEmbedding/

The font set groupings are based on the Unicode Blocks as defined by the Unicode
Consortium. To provide a simpler workflow, when you select a particular
language, all related glyph ranges are embedded even if they are scattered into
disjointed groupings.

For example, if you select Korean, the following Unicode character ranges are
embedded:

3131‑318E Hangul symbols

3200‑321C Hangul specials

3260‑327B Hangul specials

327F‑327F Korean symbol

AC00‑D7A3 Hangul symbols

If you select Korean + CJK, a larger font set is embedded:

3131‑318E Hangul symbols

3200‑321C Hangul specials

3260‑327B Hangul specials

327F‑327F Korean symbol

4E00‑9FA5 CJK symbols

AC00‑D7A3 Hangul symbols

F900‑FA2D CJK symbols

For more information about specific Unicode ranges for different writing
systems, see the
[Unicode 5.2.0 specification](https://web.archive.org/web/20120113163334mp_/http://www.unicode.org/versions/Unicode5.2.0/).

The following table gives more details about the font selections for embedded
fonts: | Range | Description | | ----------------------------- |

---

| | Uppercase \[A–Z\] | Basic Latin uppercase glyphs, plus the space character
0x0020. | | Lowercase \[a–z\] | Basic Latin lowercase glyphs, plus the space
character 0x0020. | | Numerals \[0–9\] | Basic Latin numeral glyphs | |
Punctuation \[!@#%...\] | Basic Latin punctuation | | Basic Latin | Basic Latin
glyphs within the Unicode range 0x0020 to 0x007E. | | Japanese Kana | Hiragana
and Katakana glyphs (including half-width forms) | | Japanese Kanji – Level 1 |
Japanese Kanji characters | | Japanese (All) | Japanese Kana and Kanji
(including punctuation and special characters) | | Basic Hangul | Most commonly
used Korean characters, Roman characters, punctuations, and special
characters/symbols | | Hangul (All) | 11,720 Korean characters (sorted by Hangul
syllables), Roman characters, punctuations, and special characters/symbols) | |
Traditional Chinese – Level 1 | 5000 most commonly used Traditional Chinese
characters used in Taiwan | | Traditional Chinese (All) | All Traditional
Chinese characters used in Taiwan and Hong Kong, and punctuations | | Simplified
Chinese – Level 1 | 6000 most commonly used Simplified Chinese characters used
in mainland of China and punctuations | | Chinese (All) | All Traditional and
Simplified Chinese characters and punctuations | | Thai | All Thai glyphs | |
Devanagari | All Devanagari glyphs | | Latin I | Latin‑1 Supplement range 0x00A1
to 0x00FF (including punctuation, superscripts and subscripts, currency symbols,
and letter-like symbols) | | Latin Extended A | Latin Extended‑A range 0x0100 to
0x01FF (including punctuation, superscripts and subscripts, currency symbols,
and letter-like symbols) | | Latin Extended B | Latin Extended‑B range 0x0180 to
0x024F (including punctuation, superscripts and subscripts, currency symbols,
and letter-like symbols) | | Latin Extended Add'l | Latin Extended Additional
range 0x1E00 to 0x1EFF (including punctuation, superscripts and subscripts,
currency symbols, and letter-like symbols) | | Greek | Greek and Coptic, plus
Greek Extended (including punctuation, superscripts and subscripts, currency
symbols, and letter-like symbols) | | Cyrillic | Cyrillic (including
punctuation, superscripts and subscripts, currency symbols, and letter-like
symbols) | | Armenian | Armenian plus ligatures | | Arabic | Arabic plus
Presentation Forms‑A and Presentation Forms‑B | | Hebrew | Hebrew plus
Presentation Forms (including punctuation, superscripts and subscripts, currency
symbols, and letter-like symbols) |

### Non-Unicode external files

If you load external text or XML files that are not Unicode-encoded into a Flash
Player 7 application, the text in the external files does not appear correctly
when Flash Player attempts to show them as Unicode. To tell Flash Player to use
the traditional code page of the operating system that is running the player,
add the following code as the first line of code in the first frame of the Flash
Pro application that is loading the data:

    system.useCodepage = true;

Set the `system.useCodepage` property only once in a document; do not use it
multiple times in a document to make the player interpret some external files as
Unicode and some as other encoding, because this can yield unexpected results.

If you set the `system.useCodepage` property to `true`, the traditional code
page of the operating system running the player must include the glyphs used in
your external text file for the text to appear. For example, if you load an
external text file that contains Chinese characters, those characters do not
appear on a system that uses the CP1252 code page, because that code page does
not include Chinese characters. To ensure that users on all platforms can view
external text files used in your Flash Pro applications, encode all external
text files as Unicode and leave the `system.useCodepage` property set to `false`
by default. This causes Flash Player to interpret the text as Unicode. For more
information, see useCodepage (System.useCodepage property) in the
[_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

### Text encoding

All text in a computer is encoded as a series of bytes. Many different forms of
encoding (and therefore, different bytes) represent text. Different kinds of
operating systems use different kinds of encoding for text. For example, Western
Windows operating systems usually use CP1252 encoding; Western Macintosh
operating systems usually use MacRoman encoding; Japanese Windows and Macintosh
systems usually use Unicode encoding.

Unicode can encode most languages and characters used throughout the world. The
other forms of text encoding that computers use are subsets of the Unicode
format, tailored to specific regions of the world. Some of these forms are
compatible in some areas and incompatible in other areas, so using the correct
encoding is critical.

Unicode has several forms. Flash Player versions 6 and 7 and later support text
or external files in the 8‑bit Unicode format UTF‑8, and in the 16‑bit Unicode
formats UTF‑16 BE (Big Endian) and UTF‑16 LE (Little Endian).

### Unicode and Flash Player

Flash Player 6 and later versions support Unicode text encoding. Users with
Flash Player 6 or later can view multilanguage text, regardless of the language
that the operating system running the player uses, if they have the correct
fonts installed.

Flash Player assumes that all external text files associated with a Flash Player
application are Unicode encoded, unless you tell the player otherwise.

For Flash Pro applications in Flash Player 5 or earlier that are authored in
Flash MX or earlier, Flash Player 6 and earlier versions display the text by
using the traditional code page of the operating system running the player.

For background information on Unicode, see Unicode.org.

#### Text encoding in Flash Player

By default, Flash Player 7 and later assumes that all text it encounters is
Unicode encoded. If your document loads external text or XML files, the text in
these files should be UTF‑8 encoded. Create these files by using the Strings
panel or using a text or HTML editor that can save the files in Unicode format.

#### Unicode encoding formats that Flash Player supports

When reading text data in Flash Pro, Flash Player looks at the first two bytes
in the file to detect a byte order mark (BOM), a standard formatting convention
used to identify the Unicode encoding format. If no BOM is detected, the text
encoding is interpreted as UTF‑8 (an 8‑bit encoding format). It is recommended
that you use UTF‑8 encoding in your applications.

If Flash Player detects either of the following BOMs, the text encoding format
is interpreted as follows:

- If the first byte of the file is OxFE and the second is OxFF, the encoding is
  interpreted as UTF‑16 BE (Big Endian). This is used for Macintosh operating
  systems.

- If the first byte of the file is OxFF and the second is OxFE, the encoding is
  interpreted as UTF‑16 LE (Little Endian). This is used for Windows operating
  systems.

  Most text editors that can save files in UTF‑16BE or LE automatically add the
  BOMs to the files.

  > **Note:** If you set the `system.useCodepage` property to `true`, the text
  > is interpreted using the traditional code page of the operating system that
  > is running the player; it is not interpreted as Unicode.

#### Encoding in external XML files

You cannot change the encoding of an XML file by changing the encoding tag.
Flash Player identifies the encoding of an external XML file using the same
rules as for all external files. If no BOM is encountered at the beginning of
the file, the file is assumed to be in UTF‑8 encoding. If a BOM is encountered,
the file is interpreted as UTF‑16BE or LE.

## Creating multilanguage text

You can configure a FLA file to display text in different languages depending on
the language of the operating system that plays the Flash Pro content.

### Workflow for authoring multilanguage text with the Strings panel

The Strings panel lets you create and update multilingual content. You can
specify content for text fields that span multiple languages, and have Flash Pro
automatically determine the content that should appear in a certain language
based on the language of the computer running Flash Player.

The following steps describe the general workflow:

#### 1. Author a FLA file in one language.

Any text to enter in another language must be in a dynamic or input text field.

#### 2. In the Strings Panel Settings dialog box, select the languages to include and designate one of them as the default language.

A column for the language is added to the Strings panel. When you save, test, or
publish the application, a folder with an XML file is created for each language.

#### 3. In the Strings panel, encode each text string with an ID.

#### 4. Publish the application.

A folder is created for each language you select, and within each language
folder is an XML file for that language.

#### 5. Send the published FLA file and XML folders and files to your translators.

Author in your native language and let the translators make the translation.
They can use translation software directly in the XML files or in the FLA file.

#### 6. When you receive the translations from your translators, import the translated XML files back into the FLA file.

> **Note:** Flash Pro CS4 files with anti-aliased classic, dynamic text fields
> populated from the Strings panel may not display properly when updated to
> Flash Pro CS5. This is due to changes in font embedding in Flash Pro CS5. To
> solve this problem, manually embed the fonts used by the text fields. For
> instructions, see
> [Embed fonts for consistent text appearance](./embed-fonts-for-consistent-text-appearance.md).

### Select and remove languages for translation

As many as 100 languages can appear on the Stage and in the Strings panel for
translation. Each language you select becomes a column in the Strings panel. To
show the text on the Stage in any of the languages you selected, change the
Stage language. The selected language appears when you publish or test the file.

When selecting languages, use any of the languages provided in the menu, as well
as any other Unicode-supported language.

#### Select a language

1.  Select Window \> Other Panels \> Strings, and click Settings.

2.  Add a language by doing one of the following:
    - In the Languages box, highlight a language to select, and click Add.

    - If the language does not appear in the Languages box, in the blank field
      below the Languages box, type a language code in the format _xx._ (The
      language code is from ISO 639‑1.) Click Add.

3.  Repeat step the previous step until you have added all the necessary
    languages.

4.  Select a default language from the Default runtime language menu. This
    language appears on systems that do not have one of the active languages you
    selected.

5.  To load an XML file for the languages from a different URL at runtime, type
    the URL in the URL text field and click OK.

    A column for each selected language appears in the Strings panel. The
    columns appear in alphabetical order.

6.  Save the FLA file. When you save the FLA file, a folder for each language
    you selected is created in the same folder indicated in the SWF publish
    path. If no SWF publish path has been selected, it is created in the folder
    the FLA file resides in. Within each language file an XML file is created
    that is used to load translated text.

#### Remove a language

1.  Select Window \> Other Panels \> Strings, and click Settings.

2.  In the Active languages field, highlight a language and click Remove.

3.  Repeat step 3 until you have removed all the unwanted languages.

4.  When you finish removing languages, click OK.

    The column for each removed language no longer appears in the Strings panel.

> **Note:** When you remove a language from the Strings panel, the language XML
> file is not deleted from the local file system. This lets you add the language
> back into the Strings panel by using the previous XML file, and prevents
> accidental deletion. To completely remove the language, you must delete or
> replace the language XML file.

### Add strings to the Strings panel

Assign text strings to the Strings panel in the following ways:

- Assign a string ID to a dynamic or input text field

- Add a string to the Strings panel without assigning it to a text field

- Assign an existing string ID to an existing dynamic or input text field

#### Assign a string ID to a text field

1.  Select Window \> Other Panels \> Strings.
2.  Select the Text tool. On the Stage, create an input or dynamic text field.
3.  While the text field is selected, type a unique ID in the ID field in the
    Strings panel.
4.  Click the Settings button and select a language or languages from the list
    in the Settings dialog box. The languages you select should include the
    default language you wish to use and any other languages in which you plan
    to publish your work.
5.  Click Apply.

> **Note:** If a static text field is selected on the Stage, the Stage text
> selection section on the Strings panel displays the message "Static text
> cannot have an ID associated with it." If a nontext item is selected or
> multiple items are selected, the message "Current selection cannot have an ID
> associated with it" appears.

#### Add a string ID to the Strings panel without assigning it to a text field

1.  Select Window \> Other Panels \> Strings.
2.  Click the Settings button and select a language or languages from the list
    in the Settings dialog box. The languages you select should include the
    default language you wish to use and any other languages in which you plan
    to publish your work.
3.  Type a new string ID and new string in the Strings panel, and click Apply.

#### Assign an existing ID to a text field

1.  Select the Text tool. On the Stage, create an input or dynamic text field.
2.  Type the name of an existing ID in the ID section of the Strings panel, and
    click Apply.

> **Note:** Press Shift+Enter to apply the ID to the text field, or Enter if the
> focus is on the ID field.

### Editing strings in the Strings panel

After you enter text strings in the Strings panel, use one of the following
methods to edit the text strings:

- Directly in the Strings panel cells.

- On the Stage in the language selected as the Stage language, using features
  such as find and replace and spelling checking. Text that you change using
  these features is changed on the Stage and in the Strings panel.

- Edit the XML file directly.

### Change the language displayed on the Stage

1.  Select Window \> Other Panels \> Strings.

2.  In the Stage Language menu, select the language to use for the Stage
    language. This must be a language you added as an available language.

    After you change the Stage language, any new text you type on the Stage
    appears in that language. If you previously entered text strings for the
    language in the Strings panel, any text on the Stage appears in the selected
    language. If not, the text fields already on the Stage are blank.

### Enter Asian characters on a Western keyboard

With Flash Pro, you can use Input Method Editors (IMEs) and standard Western
keyboards to enter Asian characters on the Stage. Flash Pro supports more than
two dozen IMEs.

For example, to create a website that reaches a broad range of Asian viewers,
you can use a standard Western (QWERTY) keyboard and change the IME to create
text in Chinese, Japanese, and Korean.

> **Note:** This feature affects only text input on the Stage, not text entered
> in the Actions panel. This feature is available for all supported Windows
> operating systems and Mac OS X.

1.  Select Edit \> Preferences (Windows) or Flash \> Preferences (Macintosh),
    and click Text in the Category list.
2.  Under Input Method, select one of the options to input characters from a
    Western keyboard. The default is Chinese and Japanese and it should also be
    selected for Western languages.

### Publishing multilanguage FLA files

When you save, publish, or test the FLA file, a folder with an XML file is
created for each available language you selected in the Strings panel. The
default location for the XML folders and files is the same folder indicated as
the SWF publish path. If no SWF publish path was selected, the XML folder and
files are saved in the folder in which the FLA file is located. For example, if
you have a file named Test in the mystuff folder, and you selected English (en),
German (de), and Spanish (es) as active languages, and you did not select a SWF
publish path, when you save the FLA file, the following folder structure is
created:

    \mystuff\Test.fla
    \mystuff\de\Test_de.xml
    \mystuff\en\Test_en.xml
    \mystuff\es\Test_es.xml

When you start a SWF file, you also need to start the associated XML files with
the string translations in the web server. The first frame that contains text
cannot appear until the entire XML file is downloaded.

### Manually replace strings at publish time

Manually replace strings by using the Stage language when you publish your Flash
Pro SWF file. This method uses the Stage language to replace all instances of
input and dynamic text with an associated string ID. In this case, text strings
are only updated when you publish the SWF file; language detection is not
automatic, and you must publish a SWF file for each language to support.

1.  Select Window \> Other Panels \> Strings, and click Settings.
2.  Select the Replace Strings Automatically At Runtime check box.

### Use automatic language detection with the default language

You can change the default runtime language to any language that you selected as
an available language. When automatic language detection is on, and you view the
SWF file on the system that uses the language, any system that is set to a
language other than one of the active languages uses the default language. For
example, if you set your default language to English and you select ja, en, and
fr as active languages, users who have their system language set to Japanese,
English, or French automatically see text strings in their chosen language.
However, users who have their system language set to Swedish, which is not one
of the selected languages, automatically see text strings in the default
language you selected—in this case, English.

1.  Select Window \> Other Panels \> Strings, and click Settings.
2.  In the Default language menu, select the default language. This must be a
    language you added as an available language.
3.  To enable automatic language detection, select Replace Strings Automatically
    At Runtime, and click OK. Flash Pro generates the following ActionScript®,
    which stores the language XML file paths. Use this code as a starting point
    for your own language detection script.

        import mx.lang.Locale;
        Locale.setFlaName("<flaFileName>");
        Locale.setDefaultLang("langcode");
        Locale.addXMLPath("langcode", "url/langcode/flaname_langcode.xml");

    > **Note:** The ActionScript code that the Strings panel generates does not
    > use the `Locale.initialize` function. Decide how to call this function
    > based on the language detection customizations your project requires.

### Use custom language detection

To access the language XML files to control text replacement at a time that you
designate, create your own custom component or use ActionScript code. For
example, you might create a pop‑up menu that lets users select a language for
viewing content.

For information on writing ActionScript code to create custom language
detection, see About the Strings panel in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

1.  Select Window \> Other Panels \> Strings, and click Settings.

2.  In the Default Language menu, select the default language.

    This must be a language you added as an available language.

3.  Select the Replace Strings Via ActionScript check box, and click OK.

    Flash Pro generates the following ActionScript code, which stores the
    language XML file paths. Use this code as a starting point for your own
    language detection script.

        import mx.lang.Locale;
        Locale.setFlaName("<flaFileName>");
        Locale.setDefaultLang("langcode");
        Locale.addXMLPath("langcode", "url/langcode/flaname_langcode.xml");

> **Note:** The ActionScript that the Strings panel generates does not use the
> `Locale.initialize` function. Decide how to call this function based on the
> language detection customizations your project requires.

### Additional resources

- Article:
  [Formatting text for localized Flash projects](https://web.archive.org/web/20120113163334mp_/http://www.adobe.com/devnet/flash/articles/text_localization.html)
  (Adobe.com)

## XML file format for multilanguage text

When you use multilanguage text in Flash Pro, the text is stored in XML files.

### About the XML file format

Exported XML is in UTF‑8 format and follows the XML Localization Interchange
File Format (XLIFF)1.0 standard. It defines a specification for an extensible
localization interchange format that lets any software provider produce a single
interchange format that can be delivered to, and understood by, any localization
service provider. For more information about XLIFF, see
[www.oasis-open.org/committees/xliff/](https://web.archive.org/web/20120113163334mp_/http://www.oasis-open.org/committees/xliff/).

#### XLIFF examples

If any of the following characters are entered in the Strings panel, they are
replaced by the appropriate entity reference when written to XML files: |
Character | Replaced by | | --------- | ----------- | | & | &amp; | | ' | &apos;
| | " | &quot; | | \< | &lt; | | \> | &gt; |

#### Exported XML file sample

The following examples show what an XML file that the Strings panel generates
looks like in the source language—in this example, English—and in another
language—in this example, French:

English source version sample:

    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE xliff PUBLIC "-//XLIFF//DTD XLIFF//EN"
    "http://www.oasis-open.org/committees/xliff/documents/xliff.dtd" >
    <xliff version="1.0" xml:lang="en">
        <file datatype="plaintext" original="MultiLingualContent.fla" source-language="EN">
            <header></header>
            <body>
                <trans-unit id="001" resname="IDS_GREETINGS">
                    <source>welcome to our web site!</source>
                </trans-unit>
                <trans-unit id="002" resname="IDS_MAILING LIST">
                    <source>Would you like to be on our mailing list?</source>
                </trans-unit>
                <trans-unit id="003" resname="IDS_SEE YOU">
                    <source>see you soon!</source>
                </trans-unit>
                <trans-unit id="004" resname="IDS_TEST">
                    <source></source>
                </trans-unit>
            </body>
        </file>
    </xliff>

French source version sample:

    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE xliff PUBLIC "-//XLIFF//DTD XLIFF//EN"
    "http://www.oasis-open.org/committees/xliff/documents/xliff.dtd" >
    <xliff version="1.0" xml:lang="fr">
        <file datatype="plaintext" original="MultiLingualContent.fla" source-language="EN">
            <header></header>
            <body>
                <trans-unit id="001" resname="IDS_GREETINGS">
                    <source>Bienvenue sur notre site web!</source>
                </trans-unit>
                <trans-unit id="002" resname="IDS_MAILING LIST">
                    <source>Voudriez-vous être sur notre liste de diffusion?</source>
                </trans-unit>
                <trans-unit id="003" resname="IDS_SEE YOU">
                    <source>A bientôt!</source>
                </trans-unit>
                <trans-unit id="004" resname="IDS_TEST">
                    <source></source>
                </trans-unit>
            </body>
        </file>
    </xliff>

### Translate text in the Strings panel or an XML file

When sending files to translators, include not only the FLA file but also the
folders for the XML files and the XML file for each language.

Translators can either work directly in the language columns in the Strings
panel or work in the XML files for each language to translate the FLA file to
selected languages. If you translate directly in the XML file, you must either
import the XML file to the Strings panel or save it in the default directory for
that language.

#### Translate text in the Strings panel

1.  Select Window \> Other Panels \> Strings.

2.  For each language to be translated, select the appropriate language column,
    then type the translated text for that language to be associated with each
    string ID.

3.  To show the text on the Stage in the language you selected, select the
    language in the Stage Language field.

4.  When you are finished, save, publish, or test the file.

    All XML files for all languages are overwritten with the information in the
    Strings panel.

    > **Note:** To preserve the translation in an XML file, save it in a
    > different folder.

#### Translate text in an XML file

1.  Using an XML file editor or translating software, open the folder for the
    desired language, then the XML file for that language. The XML file is
    populated with the IDs for each text string.
2.  Enter the text string for the language next to the ID.
3.  If necessary, import the translated XML file into the Strings panel.

### Import an XML file into the Strings panel

After you modify an XML file, if you place it in the folder specified in the
Strings panel for that language, the XML file is loaded into the Flash Pro
document (FLA file) when it opens.

Regardless of where the XML file you imported was located, when you save, test,
or publish the FLA file, a folder for each language in the Strings panel and an
XML file for each language are created in the location indicated for publishing
SWF files. If no publish path is indicated, the folder and file are saved in the
same folder in which the FLA file is located. The XML files that the Strings
panel generates are always populated with the information in the Strings panel.

Alternatively, import an XML file into the Strings panel from another location.
After you import it, when you save, test, or publish the file, the XML file in
the folder specified for that language is overwritten. You cannot import an XML
file for a language unless it is already selected as an available language in
the Strings panel. You can also add a language and import an XML file with the
translation for that language.

1.  Select Window \> Other Panels \> Strings, and click Import XML.

2.  In the Select a Language menu, select the language of the XML file you are
    importing, and click OK.

3.  Navigate to the folder and XML file to import.

    The XML information is loaded into the column in the Strings panel for the
    language you selected in step 3.

> **Note:** Select the same language in steps 2 and 3. Otherwise, you could, for
> example, import a French XML file into the column for German.

## Multilanguage text and ActionScript

You can control multilanguage text and import multilanguage XML files with
ActionScript®.

### Use ActionScript to load external files

To load existing XML data, or use a different format for the XML file, use the
`loadVariables` action, the `getURL` action, the `LoadVars` object, or the `XML`
object to create a document that contains multilanguage text by placing the text
in an external text or XML file and loading the file into the movie clip at
runtime. Save the external file in UTF‑8 (recommended), UTF‑16BE, or UTF‑16LE
format, using an application that supports the format. If you are using UTF‑16BE
or UTF‑16LE format, the file must begin with a BOM to identify the encoding
format to Flash Player. The following table lists the BOM to include to identify
the encoding:

> **Note:** Most text editors that can save files in UTF‑16BE or LE
> automatically add the BOMs to the files.

| UTF Format | First Byte | Second Byte |
| ---------- | ---------- | ----------- |
| UTF‑16BE   | OxFE       | OxFF        |
| UTF‑16LE   | OxFF       | OxFE        |

> **Note:** If the external file is an XML file, you cannot use an XML encoding
> tag to change the file encoding. Save the file in a supported Unicode format.

1.  In the Flash Pro authoring application, create a dynamic or input text field
    to show the text in the document.
2.  In the Property inspector, with the text field selected, assign an instance
    name to the text field.
3.  Outside of Flash, create a text or XML file that defines the value for the
    text field variable.
4.  Save the XML file in UTF‑8 (recommended), UTF‑16BE, or UTF‑16LE format.
5.  Use one of the following ActionScript procedures to reference the external
    file and load it into the dynamic or input text field:
    - Use the `loadVariables` action to load an external file.

    - Use the `getURL` action to load an external file from a specified URL.

    - Use the `LoadVars` object (a predefined client-server object) to load an
      external text file from a specified URL.

    - Use the `XML` object (a predefined client-server object) to load an
      external XML file from a specified URL. For more information, see XML in
      the
      [_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

### Create multilanguage documents using the \#include action

To create a document that contains multiple languages, use the `#include`
action.

Use an application that supports UTF‑8 encoding, such as Dreamweaver, to save
the text file in UTF‑8 format.

To identify the file as Unicode to the Flash Pro authoring tool, include the
following header as the first line of the file:

    //!-- UTF8

> **Note:** Include a space after the second dash (-). By default, the Flash Pro
> authoring application assumes that external files that use the `#include`
> action are encoded in the traditional code page of the operating system
> running the authoring tool. Using the `//!-- UTF8`header in a file tells the
> authoring tool that the external file is encoded as UTF‑8.

1.  In the Flash Pro authoring tool, create a dynamic or input text field to
    display the text in the document.
2.  In the Property inspector, with the text field selected, assign an instance
    name to the text field.
3.  Outside of Flash, create a text file that defines the value for the text
    field variable. Add the `//!-- UTF8` header at the beginning of the file.
4.  Save the text file in UTF‑8 format.
5.  To include the external file in the dynamic or input text field, use the
    `#include` directive. For more information, see `#include` directive in the
    [_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

### Creating multilanguage documents by using text variables

To include Unicode-encoded contents in text variables, use the syntax `\uXXXX`,
where `XXXX` is the four-digit hexadecimal code point, or _escape_ character,
for the Unicode character. The Flash Pro authoring tool supports Unicode escape
characters through `\uFFFF`. To find the code points for Unicode characters, see
the Unicode Standard at Unicode.org.

You can use Unicode escape characters only in text field variables. You cannot
include Unicode escape characters in external text or XML files; Flash Player 6
does not recognize Unicode escape characters in external files.

For example, to set a dynamic text field (with the `myTextVar` instance name)
that contains Japanese, Korean, Chinese, English, and Greek characters and the
Euro sign, enter the following:

    myTextVar.text = "\u304B\uD55C\u6C49hello\u03BB\u20AC";

When the SWF file plays, the following characters appear in the text field:

![](../img/tx_textvariables.png)

For best results when creating a text field that contains multiple languages,
use a font that includes all the glyphs your text needs.

### Using the XMLConnector component to connect to external XML files

Use the version 2 XMLConnector component to connect to an external XML document
to bind to properties in the document. Its purpose is to read or write XML
documents by using HTTP `GET` operations, `POST` operations, or both. It acts as
a connector between other components and external XML documents. The
XMLConnector communicates with components in your application by using either
data-binding features in the Flash authoring environment or ActionScript code.
For more information, see XML Connector component in the _ActionScript 2.0
Components Language Reference_.

More Help topics

[Embed fonts for consistent text appearance](./embed-fonts-for-consistent-text-appearance.md)

[Publishing overview](../publishing-and-exporting/publishing-flash-documents.md#publishing-overview)

[Working with Text Layout Framework (TLF) text](../text/working-with-text-layout-framework-tlf-text.md)

[Find and Replace in Flash](../managing-documents/find-and-replace-in-flash.md)

[Check spelling](./check-spelling.md)

[Publishing Flash documents](../publishing-and-exporting/publishing-flash-documents.md)

[Text](./index.md)

![](../img/as3LinkIndicator.png)
[Working with Unicode Text](https://web.archive.org/web/20120113163334mp_/http://help.adobe.com/en_US/as3/dev/WS8d7bb3e8da6fb92f-20050207122bd5f80cb-7fe9.html)
