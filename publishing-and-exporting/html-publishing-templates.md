# HTML publishing templates

## About HTML publishing templates

A Flash Pro HTML template is a file that contains static HTML code and flexible
template code consisting of a special type of variables (which differ from
ActionScript variables). When you publish a SWF file, Flash Pro replaces these
variables with the values you select in the HTML tab of the Publish Settings
dialog box and produces an HTML page with your SWF file embedded.

Flash Pro includes templates, suitable for most users' needs, that eliminate the
need to manually create an HTML page that displays the SWF file. For example,
the Flash Only template is useful for testing your files in a browser. It places
the SWF file on the HTML page so that you can view it through a web browser with
the Flash Player installed.

To publish a new HTML page, use the same template and change the settings. You
can create custom templates using any HTML editor. Creating a template is the
same as creating a standard HTML page, except that you replace specific values
pertaining to a SWF file with variables that begin with a dollar sign (\$).

Flash Pro HTML templates have the following special characteristics:

- A one-line title that appears on the Template pop‑up menu on the HTML tab of
  the Publish Settings dialog box.

- A longer description that appears when you click Info on the HTML tab of the
  Publish Settings dialog box.

- Template variables beginning with a dollar sign (\$) that specify where
  parameter values should be substituted when Flash Pro generates the output
  file.

  > **Note:** Use a backslash and dollar sign (\\) combination to use a dollar
  > sign for another purpose in the document.

- HTML `object` and `embed` tags that follow the tag requirements of Microsoft
  Internet Explorer and Netscape® Communicator® or Navigator®, respectively. To
  display a SWF file properly on an HTML page, follow these tag requirements.
  Internet Explorer uses the `object` HTML tag to open a SWF file; Netscape uses
  the `embed` tag.

## Customize HTML publishing templates

Modify HTML template variables to create an image map, a text report, or a URL
report, or to insert custom values for some of the most common Flash Pro HTML
`object` and `embed` tag parameters (for browsers that use ActiveX controls and
plug-ins, respectively).

Flash Pro templates can include any HTML content for your application or even
code for interpreters such as ColdFusion and ASP.

1.  Using an HTML editor, open the Flash Pro HTML template to change. These
    templates are in the following locations:

    - Windows XP or Vista: _boot drive_:\Documents and Settings\\_user_\Local
      Settings\Application Data\Adobe\Flash CS5\\_language_\Configuration\HTML\\
      The Application Data folder is usually a hidden folder; you might need to
      change your Windows Explorer settings to see this folder.

    - Mac OS X 10.3 and later: _Macintosh HD_/Applications/Adobe Flash
      CS5/_language_/First Run/HTML.

      The _boot drive_ is the drive from which the Windows operating system
      boots (usually C:). The _user_ is the name of the person logged in to the
      Windows operating system. The _language_ is set to an abbreviated language
      name. For example, in the US, _language_ is set to "en" for English.

2.  Edit the template.
3.  Save the template in the same folder that you retrieved it from.
4.  To apply the template settings to your SWF file, select File \> Publish
    Settings, click HTML, and select the template you modified. Flash Pro
    changes only the template variables in the template selected.
5.  Select your remaining publish settings, and click OK.

## HTML template variables

The following table lists the template variables that Flash Pro recognizes: |
Attribute/parameter | Template variable | |
------------------------------------------------------ | ----------------- | |
`Template title` | `$TT` | | `Template description start` | `$DS` | |
`Template description finish` | `$DF` | | `Flash Pro (SWF file) title` | `$T1` |
| `Flash Pro (SWF file) title for`search engine metadata | `$TL` | | Description
for search engine metadata | `$DC` | | Metadata XML string for use with search
engines | `$MD` | | `Width` | `$WI` | | `Height` | `$HE` | | `Movie` | `$MO` | |
`HTML alignment` | `$HA` | | `Looping` | `$LO` | | `Parameters for object` |
`$PO` | | `Parameters for embed` | `$PE` | | `Play` | `$PL` | | `Quality` |
`$QU` | | `Scale` | `$SC` | | `Salign` | `$SA` | | `Wmode` | `$WM` | |
`Devicefont` | `$DE` | | `Bgcolor` | `$BG` | |
`Movie text (area to write movie text)` | `$MT` | |
`Movie URL (location of SWF file URL)` | `$MU` | |
`Image width (unspecified image type)` | `$IW` | |
`Image height (unspecified image type)` | `$IH` | |
`Image filename (unspecified image type)` | `$IS` | | `Image map name` | `$IU` |
| `Image map tag location` | `$IM` | | `QuickTime width` | `$QW` | |
`QuickTime height` | `$QH` | | `QuickTime filename` | `$QN` | | `GIF width` |
`$GW` | | `GIF height` | `$GH` | | `GIF filename` | `$GN` | | `JPEG width` |
`$JW` | | `JPEG height` | `$JH` | | `JPEG filename` | `$JN` | | `PNG width` |
`$PW` | | `PNG height` | `$PH` | | `PNG filename` | `$PN` |

#### Using shorthand template variables

The `$PO` (for `object` tags) and `$PE` (for `embed` tags) template variables
are useful shorthand elements. Each variable causes Flash Pro to insert into a
template any nondefault values for some of the most common `object` and `embed`
parameters, including `PLAY` (`$PL`), `QUALITY` (`$QU`), `SCALE` (`$SC`),
`SALIGN` (`$SA`), `WMODE` (`$WM`), `DEVICEFONT` (`$DE`), and `BGCOLOR` (`$BG`).

#### Sample HTML template

The following Default.HTML template file in Flash Pro includes many of the
commonly used template variables:

    $TTFlash Only
    $DS
    Display Adobe SWF file in HTML.
    $DF
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
    <head>
    $CS
    <title>$TI</title>
    </head>
    <body bgcolor="$BG">
    <!--url's used in the movie-->
    $MU
    <!--text used in the movie-->
    $MT
    <object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" codebase="http://fpdownload.adobe.com/pub/shockwave/cabs/flash/swflash.cab#version=7,0,0,0" width="$WI" height="$HE" id="$TI" align="$HA">
    <param name="allowScriptAccess" value="sameDomain" />
    $PO
    <embed $PEwidth="$WI" height="$HE" name="$TI" align="$HA" allowScriptAccess="sameDomain" type="application/x-shockwave-flash" pluginspage="http://www.adobe.com/go/getflashplayer" />
    </object>
    </body>
    </html>

## Create an image map to substitute for a SWF file

Flash Pro can generate an image map to show any image and maintain the function
of buttons that link to URLs. When an HTML template includes the `$IM` template
variable, Flash Pro inserts the image map code. The `$IU` variable identifies
the name of the GIF, JPEG, or PNG file.

1.  In your document, select the keyframe to use for the image map and label it
    `#Map` in the frame Property inspector (Window \> Properties). Use any
    keyframe with buttons that have attached ActionScript 1.0 or 2.0 `getURL`
    actions.

    If you don't create a frame label, Flash Pro creates an image map using the
    buttons in the last frame of the SWF file. This option generates an embedded
    image map, not an embedded SWF file.

2.  To select the frame to show the image map, do one of the following:

    - For PNG or GIF files, label the frame to appear as `#Static`.

    - For JPEG, during the publish operation, place the playhead on the frame to
      be used for display.

3.  In an HTML editor, open the HTML template you'll modify.

4.  Save your template.

5.  Select File \> Publish Settings, click Format, select a format for the image
    map, and click OK.

    For example, insert the following code in a template:

        $IM
        <img src=$IS usemap=$IU width=$IW height=$IH BORDER=0>

    This might produce the following code in the HTML document that the Publish
    command creates:

        <map name="mymovie">
        <area coords="130,116,214,182" href="http://www.adobe.com">
        </map>
        <img src="mymovie.gif" usemap="#mymovie" width=550 height=400 border=0>

## Creating text and URL reports

The `$MT` template variable causes Flash Pro to insert all the text from the
current SWF file as a comment in the HTML code. This is useful for indexing the
content of a SWF file and making it visible to search engines.

The `$MU` template variable makes Flash Pro generate a list of the URLs that
actions in the current SWF file refer to and insert the list at the current
location as a comment. This action lets link verification tools detect and
verify the links in the SWF file.

## Embedding search metadata

The `$TL` (SWF file title) and `$DC` (description metadata) template variables
let you include search metadata in the HTML. This ability can make the SWF file
more visible to search engines, and provide meaningful search results. Use the
`$MD`template variable to include the search metadata as an XML string.

More Help topics

[Examples using object and embed tags](./publish-settings-cs5.md#examples-using-object-and-embed-tags)

[Publishing overview](./publishing-flash-documents.md#publishing-overview)

[Specify publish settings for HTML wrapper files (CS5)](./publish-settings-cs5.md#specify-publish-settings-for-html-wrapper-files-cs5)
