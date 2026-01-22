# About exporting from Flash

## Export SWF files

The Flash Export commands do not store export settings separately with each
file, as does the Publish command. (To create all the files you need to put
Flash Pro content on the web, use the Publish command.)

Export Movie exports a Flash Pro document to a still-image format, creates a
numbered image file for every frame in the document, and exports the sound in a
document to a WAV file (Windows only).

1.  Open the Flash Pro document to export, or select the frame or image to
    export in the current document.
2.  Select File \> Export \> Export Movie, or File \> Export \> Export Image.
3.  Enter a name for the output file.
4.  Select the file format and click Save. If the format you selected requires
    more information, an Export dialog box appears.
5.  Set the export options for the format you selected. See
    [About export file formats](#about-export-file-formats).
6.  Click OK, and then click Save.

## About export file formats

Remember the following:

- If the format you selected requires more information, an Export dialog box
  appears.

- When you save a Flash Pro image as a bitmap GIF, JPEG, PICT (Macintosh), or
  BMP (Windows) file, the image loses its vector information and is saved with
  pixel information only. You can edit images exported as bitmaps in image
  editors such as Adobe® Photoshop®, but you can no longer edit them in
  vector‑based drawing programs.

- When you export a Flash Pro file in the SWF format, text is encoded as
  Unicode, providing support for international character sets, including
  double-byte fonts. Flash Pro Player 6 and later versions support Unicode
  encoding.

Flash Pro content is exported as sequences and images are exported as individual
files. PNG is the only cross-platform bitmap format that supports transparency
(as an alpha channel). Some non-bitmap export formats do not support alpha
(transparency) effects or mask layers.

The following table lists the formats that you can export Flash Pro content and
images to: | File type | Extension | Windows | Macintosh | |

---

| --------- | ------- | --------- | |
[Animated GIF, GIF Sequence, and GIF Image](./exporting.md#animated-gif-gif-sequence-and-gif-image)
| .gif | • | • | | [Bitmap (BMP) image](./exporting.md#bitmap-bmp-image) | .bmp
| • |   | | [Flash document (SWF)](./exporting.md#flash-document-swf) | .swf | •
| • | |
[JPEG Sequence and JPEG Image](./exporting.md#jpeg-sequence-and-jpeg-image) |
.jpg | • | • | | PICT Sequence and PICT Image (Macintosh) | .pct |   | • | |
[PNG Sequence and PNG Image](./exporting.md#png-sequence-and-png-image) | .png |
• | • | | [Export QuickTime](./exporting.md#export-quicktime) | .mov | • | • | |
[WAV audio (Windows)](./exporting.md#wav-audio-windows) | .wav | • |   | |
[Windows AVI (Windows)](./exporting.md#windows-avi-windows) | .avi | • |   |

## Update SWF files for Dreamweaver

To add the content to your page, export SWF files directly to an Adobe®
Dreamweaver® site. Dreamweaver generates all the needed HTML code. You can start
Flash Pro from Dreamweaver to update the content. In Dreamweaver, you can update
the Flash Pro document (FLA file) and re-export the updated content
automatically.

For more information on working with Dreamweaver, see _Using Dreamweaver_ in
Dreamweaver Help.

1.  In Dreamweaver, open the HTML page that contains the Flash Pro content.
2.  Do one of the following:

    - Select the Flash Pro content within the HTML page, and click Edit.

    - In Design view, press Control (Windows) or Command (Macintosh), and
      double-click the Flash Pro content.

    - In Design view, right-click (Windows) or Control‑click (Macintosh) the
      Flash Pro content, and select Edit with Flash.

    - In Design view, in the Site panel, right-click (Windows) or Control‑click
      (Macintosh) the Flash Pro content, and select Open with Flash.

3.  If the FLA file for the exported file does not open, the Open File dialog
    box appears. Navigate to the FLA file, and click Open.
4.  If the user used the Change Link Sitewide feature in Dreamweaver, a warning
    appears. To apply link changes to the SWF file, click OK. To prevent the
    warning message from appearing when you update the SWF file, click Don't
    Warn Me Again.
5.  Update the FLA file as needed in Flash Pro.
6.  To save the FLA file and reexport it to Dreamweaver, do one of the
    following:

    - To update the file and close Flash Pro, click the Done button above the
      upper-left corner of the Stage.

    - To update the file and keep Flash Pro open, select File \> Update for
      Dreamweaver.

More Help topics

[Publishing Flash documents](./publishing-flash-documents.md)

[Creating multilanguage text](../text/multilanguage-text.md#creating-multilanguage-text)
