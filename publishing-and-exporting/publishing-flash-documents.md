# Publishing Flash documents

## Publishing overview

You can play content in the following ways:

- In Internet browsers that are equipped with Flash Player

- As a stand-alone application called a projector

- With the Flash ActiveX control in Microsoft Office and other ActiveX hosts

- With Flash Xtra in Director® and Authorware® from Adobe®

By default, the Publish command creates a Flash Pro SWF file and an HTML
document that inserts your Flash Pro content in a browser window. The Publish
command also creates and copies detection files for Macromedia Flash 4 from
Adobe and later. If you change publish settings, Flash Pro saves the changes
with the document. After you create a publish profile, export it to use in other
documents or for others working on the same project to use.

When you use the Publish, Test Movie, or Debug Movie commands, Flash creates a
SWF file from your FLA file. You can view the sizes of all the SWF files created
from the current FLA file in the Document Property inspector.

Flash® Player 6 and later support Unicode text encoding. With Unicode support,
users can view multilanguage text, regardless of the language that the operating
system running the player uses.

You can publish the FLA file in alternative file formats—GIF, JPEG, and PNG
—with the HTML needed to display them in the browser window. Alternative formats
allow a browser to show your SWF file animation and interactivity for users who
don't have the targeted Adobe Flash Player installed. When you publish a Flash
Pro document (FLA file) in alternative file formats, the settings for each file
format are stored with the FLA file.

You can export the FLA file in several formats, similar to publishing FLA files
in alternative file formats, except that the settings for each file format are
not stored with the FLA file.

Alternatively, create a custom HTML document with any HTML editor and include
the tags required to display a SWF file.

To test how the SWF file works before you publish your SWF file, use Test Movie
(Control \> Test Movie \> Test) and Test Scene (Control \> Test Scene).

> **Note:** In Flash Professional CS5, when you set the Flash Player target to
> Flash Player 10 in the Publish Settings, the target is actually Flash Player
> 10.1.

## HTML documents

You need an HTML document to play a SWF file in a web browser and specify
browser settings. To display a SWF file in a web browser, an HTML document must
use the `object` and` embed` tags with the proper parameters.

> **Note:** You can generate an HTML document using the correct object and embed
> tags using the Publish Settings dialog box, and selecting the HTML option. For
> more information, see
> [Specify publish settings for HTML wrapper files (CS5)](./publish-settings-cs5.md#specify-publish-settings-for-html-wrapper-files-cs5).

Flash Pro can create the HTML document automatically when you publish a SWF
file.

## Detecting whether Flash Player is present

In order for your published Flash Pro content to be seen by Web users, Flash
Player must be installed in their Web browser.

The following resources and articles provide up-to-date information about how to
add code to your web pages to determine if Flash Player is installed and provide
alternative content in the page if it is not.

- [Flash Player Developer Center: Detection, installation, and administration](https://web.archive.org/web/20120101113637mp_/http://www.adobe.com/devnet/flashplayer/detection_installation.html)
  (Adobe.com)

- [Flash Player Detection Kit](https://web.archive.org/web/20120101113637mp_/http://www.adobe.com/products/flashplayer/download/detection_kit/)
  (Adobe.com)

- [Adobe Flash Player version checking protocol](https://web.archive.org/web/20120101113637mp_/http://www.adobe.com/devnet/flashplayer/articles/version_checking_protocol.html)
  (Adobe.com)

- [Future-Proofing Flash Player Detection Scripts](https://web.archive.org/web/20120101113637mp_/http://www.adobe.com/devnet/flashplayer/articles/future_detection.html)
  (Adobe.com)

- [Experiencing Flash Player Express Install](https://web.archive.org/web/20120101113637mp_/http://www.adobe.com/devnet/flashplayer/articles/express_install.html)
  (Adobe.com)

## Publishing for mobile devices

Adobe® Flash® Lite® lets Flash Pro users create engaging content for mobile
phones using the ActionScript® scripting language, drawing tools, and templates.
For detailed information on authoring for mobile devices, see _Developing Flash
Lite Applications_ and the Content Development Kits on the
[Mobile and Devices Development Center](https://web.archive.org/web/20111125223202/http://www.adobe.com/devnet/devices.html).

> **Note:** Depending on the mobile device for which you are developing, certain
> restrictions can apply as to which ActionScript commands and sound formats are
> supported. For more details, see Mobile Articles on the Mobile and Devices
> Development Center. Adobe also provides Adobe Device Central, a new way to
> test content created with Adobe products on emulated mobile devices. When
> creating a new mobile document of any kind, start the creation process from
> Device Central. Device Central lets you select a target device from the
> beginning of the development process, and have a clear idea what a device's
> limitations are.

## Publishing secure Flash documents

Flash Player 8 and later contain the following features that help you ensure the
security of your Flash Pro documents:

#### Buffer overrun protection

Enabled automatically, this feature prevents the intentional misuse of external
files in a Flash Pro document to overwrite a user's memory or insert destructive
code such as a virus. This prevents a document from reading or writing data
outside the document's designated memory space on a user's system.

#### Exact domain matching for sharing data between Flash documents

Flash Player 7 and later enforce a stricter security model than earlier
versions. The security model changed in two primary ways between Flash Player 6
and Flash Player 7:

Exact domain matching  
Flash Player 6 lets SWF files from similar domains (for example, `www.adobe.com`
and `store.adobe.com`) communicate freely with each other and with other
documents. In Flash Player 7, the domain of the data to be accessed must match
the data provider's domain _exactly_ for the domains to communicate.

HTTPS/HTTP restriction  
A SWF file that loads by using nonsecure (non-HTTPS) protocols cannot access
content loaded by using a secure (HTTPS) protocol, even when both protocols are
in exactly the same domain.

For more information about ensuring that content performs as expected with the
new security model, see Understanding security in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

#### Local and network playback security

Flash Player 8 and later include a security model that lets you determine the
local and network playback security for SWF files that you publish. By default,
SWF files are granted read access to local files and networks. However, a SWF
file with local access cannot communicate with the network, and the SWF file
cannot send files or information to any networks.

Allow SWF files to access network resources, letting the SWF file send and
receive data. If you grant the SWF file access to network resources, local
access is disabled, protecting information on the local computer from
potentially being uploaded to the network.

To select the local or network playback security model for your published SWF
files, use the Publish Settings dialog box.

## Flash Player

Flash Player plays Flash Pro content in the same way as it appears in a web
browser or an ActiveX host application. Flash Pro Player is installed with the
Flash Pro application. When you double-click Flash Pro content, the operating
system starts Flash Player, which then plays the SWF file. Use the player to
make Flash Pro content viewable for users who aren't using a web browser or an
ActiveX host application.

To control Flash Pro content in Flash Player, use menu commands and the
`fscommand()` function. For more information, see Sending messages to and from
Flash Player in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

Use the Flash Player context menu to print Flash Pro content frames.
![](../img/dingbat.png) Do one of the following:

- To open a new or existing file, select File \> New, or Open.

- To change your view of the application, select View \> Magnification and make
  a selection.

- To control Flash Pro content playback, select Control \> Play, Rewind, or Loop
  Playback.

## Reinstall Flash Player

If you are having trouble with your Flash Player installation, you can reinstall
it.

1.  Close your browser.

2.  Remove any currently installed version of the player.

    For instructions, see
    [TechNote 14157 on the Adobe® Flash® Support Center](https://web.archive.org/web/20111221092653/http://kb2.adobe.com/cps/141/tn_14157.html).

3.  To begin the installation, download the Adobe Flash Player installer.

    Follow the on-screen instructions to install the player.

    You can also run one of the following installers in your Players folder.
    However, the installer on the Adobe website is usually more up to date than
    those in the Players folder.
    - For the ActiveX control for Windows® (Internet Explorer or AOL), run the
      Install Flash Player 9 AX.exe file.

    - For the plug‑in for Windows (Firefox, Mozilla, Netscape, Safari, or
      Opera), run the Install Flash Player 9.exe file.

    - For the plug‑in for Macintosh® (AOL, Firefox, Internet Explorer for
      Macintosh, Netscape, Opera, or Safari), run Install Flash Player 10
      (Mac OS 9.x) or Install Flash Player 10 OS X (Mac OS X.x).

      > **Note:** To verify the installation visit
      > http://www.adobe.com/shockwave/welcome/ from within your web browser.

## Configure a server for Flash Player

For users to view your Flash Pro content on the web, the web server must be
properly configured to recognize SWF files.

Your server may already be configured properly. To test server configuration,
see
[TechNote 4151 on the Adobe Flash Support Center](https://web.archive.org/web/20100601132631/http://kb2.adobe.com/cps/415/tn_4151.html).

Configuring a server establishes the appropriate Multipart Internet Mail
Extension (MIME) types so that the server can identify files with the .swf
extension as Flash Pro files.

A browser that receives the correct MIME type can load the appropriate plug‑in,
control, or helper application to process and properly display the incoming
data. If the MIME type is missing or not properly delivered by the server, the
browser might display an error message or a blank window with a puzzle-piece
icon.

- If your site is established through an Internet service provider (ISP), ask
  the ISP to add this MIME type to the server: application/x-shockwave-flash
  with the .swf extension.

- If you are administering your own server, see your web server documentation
  for instructions on adding or configuring MIME types.

- Corporate and enterprise system administrators can configure Flash Pro to
  restrict Flash Player access to resources in the local file system. Create a
  security configuration file that limits Flash Player functionality on the
  local system.

The security configuration file is a text file placed in the same folder as the
Flash Player installer. The Flash Player installer reads the configuration file
during installation and follows its security directives. Flash Player uses the
System object to expose the configuration file to ActionScript.

With the configuration file, disable Flash Player access to the camera or
microphone, limit the amount of local storage Flash Player can use, control the
auto-update feature, and block Flash Player from reading anything from the
user's local hard disk.

For more information about security, see System in
[_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

#### Adding MIME Types

When a web server accesses files, the server must properly identify the files as
Flash Pro content to display them. If the MIME type is missing or not properly
delivered by the server, the browser can show error messages or a blank window
with a puzzle-piece icon.

If your server is not properly configured, you (or your server's administrator)
must add the SWF file MIME types to the server's configuration files and
associate the following MIME types with the SWF file extensions:

- MIME type application/x-shockwave-flash has the .swf file extension.

- MIME type application/futuresplash has the .spl file extension.

If you are administering a server, consult your server software documentation
for instructions on adding or configuring MIME types. If you are not
administering a server, contact your Internet service provider, web master, or
server administrator to add the MIME type information.

If your site is on a Mac OS server, you must also set the following parameters:
Action: Binary; Type: SWFL; and Creator: SWF2.

## Search engine optimization for Flash content

In mid-2008, Adobe announced a significant advance in Flash Player technology
that allows the text content inside SWF files to be indexed by search engines
such as Google and Yahoo!. There are a variety of strategies you can employ to
optimize the visibility of your SWF content to search engines. These practices
as a whole are referred to as _search engine optimization_ (SEO).

Adobe has added a
[SEO Technology Center](https://web.archive.org/web/20120101113637mp_/http://www.adobe.com/devnet/seo/)
to the Developer Connection section of Adobe.com. The SEO Technology Center
contains the following articles that detail some of the techniques you can use
to increase the visibility of your SWF files to internet searches:

- [Search optimization techniques for RIAs](https://web.archive.org/web/20120101113637mp_/http://www.adobe.com/devnet/seo/articles/techniques_ria.html)

- [Search optimization checklist for RIAs](https://web.archive.org/web/20120101113637mp_/http://www.adobe.com/devnet/seo/articles/checklist_ria.html)

## About Omniture and Flash

Flash content can be integrated with Omniture SiteCatalyst and Omniture
Test&Target. SiteCatalyst helps marketers quickly identify the most profitable
paths through their website, determine where visitors are navigating away from
their site, and identify critical success metrics for online marketing
campaigns. Test&Target gives marketers the capability to continually make their
online content more relevant to their customers. Test&Target provides an
interface for designing and executing tests, creating audience segments and
targeting content.

Omniture customers can use SiteCatalyst and Test&Target with Flash by
downloading and installing the Omniture Extension pack.

- To download the Omniture extensions and access instructions for using them,
  choose Help \> Omniture.

More Help topics

[Using publish profiles (CS5)](./publish-settings-cs5.md#using-publish-profiles-cs5)

[Publish settings (CS5)](./publish-settings-cs5.md)

[Creating multilanguage text](../text/multilanguage-text.md#creating-multilanguage-text)

[Specify publish settings for SWF files (CS5)](./publish-settings-cs5.md#specify-publish-settings-for-swf-files-cs5)
