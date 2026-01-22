# Displaying special characters

Computer operating systems have a specific code page that is regional. For
example, a computer in Japan has a different code page than a computer in
England. Flash Player 5 and earlier versions relied on the code page to display
text; Flash Player 6 and later versions use Unicode to display text. Unicode is
more reliable and standardized for displaying text because it is a universal
character set that contains characters for all languages. Most current
applications use Unicode.

You can use Unicode escape sequences to display special characters in Flash
Player 6 and later. However, not all your characters display correctly if you do
not load text that is UTF‑8 or UTF‑16 encoded (Unicode) or if you do not use a
Unicode escape sequence to display the special character. For a set of Unicode
code charts, see the Unicode web site at Unicode.org. For a list of commonly
used escape sequences, see the table that follows in this section.

A non-Unicode application uses the operating system's code page to render
characters on a page. In this case, the code page specifies the characters you
see, so the characters appear correctly only when the code page on the user's
operating system matches the application's code page. The code page that was
used to create the SWF file needs to match the code page on the end user's
computer. Using code pages is not a good idea for applications that an
international audience might use; in this case, use Unicode instead.

Using `System.useCodepage` in your code forces the SWF file to use the system's
code page instead of Unicode.

Only use this process when you are loading non-Unicode encoded text from an
external location and when this text is encoded with the same code page as the
user's computer. If both these conditions are true, the text appears without a
problem. If both of these conditions are not true, use Unicode and a Unicode
escape sequence to format your text. To use an escape sequence, add the
following ActionScript 2.0 on Frame 1 of the Timeline:

    this.createTextField("myText_txt", 99, 10, 10, 200, 25);
    myText_txt.text = "this is my text, \u00A9 2004";

This ActionScript creates a text field, and enters text that includes a
copyright symbol (`©`) into the text field.

You can make a SWF file use the operating system's code page, which is
controlled by the `useCodepage` property. When Flash Pro exports a SWF file, it
defaults to exporting Unicode text and `System.useCodepage` is set to `false`.
You might encounter problems displaying special text, or text on international
systems, where using the system's code page can seem to solve the problem of
text incorrectly displaying. However, using `System.useCodePage` is always a
last resort.

To use the system's code page, place the following line of ActionScript 2.0 code
on Frame 1 of the Timeline:

    System.useCodepage = true;

Important: A special character can appear only if the user's computer has the
character included in the font that is being used. If you are not sure, embed
the character or font in the SWF file. The following table contains a number of
commonly used Unicode escape sequences. | Character description | Unicode escape
sequence | | ----------------------- | ----------------------- | | em-dash (`—`)
| \u2014 | | registered sign (®) | \u00AE | | copyright sign (`©`) | \u00A9 | |
trademark sign (™) | \u2122 | | Euro sign (`€`) | \u20AC | | backslash (`\`) |
\u005C | | forward slash (`/`) | \u002F | | open curly brace (`{`) | \u007B | |
close curly brace (`}`) | \u007D | | greater than (`<`) | \u003C | | less than
(`>`) | \u003E | | asterisk (`*`) | \u002A |
