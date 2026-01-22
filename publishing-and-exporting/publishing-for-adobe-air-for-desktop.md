# Publishing for Adobe AIR for desktop

## About Adobe AIR

Adobe® AIR™ is a cross-operating system runtime that allows you to leverage your
existing web development skills (Adobe® Flash® Professional, Adobe® Flex™,Adobe®
Flash Builder™ HTML, JavaScript®, Ajax) to build and deploy Rich Internet
Applications (RIAs) to the desktop. AIR enables you to work in familiar
environments, to leverage the tools and approaches you find most comfortable,
and by supporting Flash, Flex, HTML, JavaScript, and Ajax, to build the best
possible experience that meets your needs.

Users interact with AIR applications in the same way that they interact with
native desktop applications. The runtime is installed once on the user's
computer, and then AIR applications are installed and run just like any other
desktop application. The runtime provides a consistent cross-operating system
platform and framework for deploying applications and therefore eliminates
cross-browser testing by ensuring consistent functionality and interactions
across desktops. Instead of developing for a specific operating system, you
target the runtime.

AIR dramatically changes how applications can be created, deployed, and
experienced. You gain more creative control and can extend your Flash, Flex,
HTML, and Ajax-based applications to the desktop, without learning traditional
desktop development technologies.

For information about hardware and software requirements for desktop and mobile
AIR applications, see
[AIR system requirements](https://web.archive.org/web/20111114123312mp_/http://www.adobe.com/products/air/systemreqs/).

For complete information about developing Adobe AIR™ applications, see
[_Building Adobe AIR Applications_](https://web.archive.org/web/20111114123312mp_/http://help.adobe.com/en_US/air/build/index.html).

#### Tutorials and other resources

The following tutorials describe how to create AIR™ applications in Flash Pro:

- Blog:
  [One Application, Five Screens](https://web.archive.org/web/20111114123312mp_/http://blogs.adobe.com/cantrell/archives/2010/04/one_application_five_screens.html)
  (Christian Cantrell, Adobe blogs)

- Article:
  [Developing a Mobile Application with Flash](https://web.archive.org/web/20111114123312mp_/http://www.gamedev.net/page/resources/_/reference/programming/game-programming/300/developing-a-mobile-application-with-flash-r2797)
  (John Hattan, gamedev.net)

- TechNote:
  [Overlaying AIR 2.7 SDK for Flash Professional CS5.5](https://web.archive.org/web/20111114123312mp_/http://kb2.adobe.com/cps/908/cpsid_90810.html)

## Create an Adobe AIR file

You can create Adobe AIR Flash documents using the Flash Welcome screen, or the
File \> New command, or you can create an ActionScript® 3.0 Flash File and
convert it to an Adobe AIR file through the Publish Settings dialog box.

To create an Adobe AIR file, do one of the following:

- Start Flash. The Welcome screen appears. If you have already started Flash,
  close any open documents to return to the Welcome screen. In the Welcome
  screen, select Adobe AIR 2 (CS5) or AIR (CS5.5).

  > **Note:** If you've disabled the Flash Welcome screen, you can display it
  > again by selecting Edit \> Preferences and selecting Welcome Screen from the
  > On Launch pop-up menu in the General category.

- Choose File \> New and select Adobe AIR 2 (CS5) or AIR (CS5.5) and click OK.

- Open an existing Flash file and convert it to an AIR file by selecting Adobe
  AIR from the Player menu in the Flash tab of the Publish Settings dialog box
  (File \> Publish Settings).

**Note:** _(Flash CS5 only)_ If you save a Flash CS5 AIR file in Flash CS4
format, set the Player version to AIR 1.5 manually in the Publish Settings
dialog box when opening the file in Flash CS4. Flash CS4 only supports
publishing to AIR 1.5.

## Preview or publish an Adobe AIR application

You can preview a Flash AIR SWF file as it would appear in the AIR application
window. Previewing is useful when you want to see what the visible aspects of
the application look like without packaging and installing the application.

1.  Make sure you've set the Player setting in the Flash tab of the Publish
    Settings dialog box to Adobe AIR.

2.  Select Control \> Test Movie \> Test or press Control+Enter.

If you have not set application settings through the AIR - Application And
Installer Settings dialog box, Flash generates a default application descriptor
file (_swfname_-app.xml) for you in the same folder where the SWF file is
written. If you have set application settings using the AIR Application &
Installer Settings dialog box, the application descriptor file reflects those
settings.

To publish an AIR file, do one of the following:

- Click the Publish button in the Publish Settings dialog box.

- Click the Publish button in the AIR Application & Installer Settings dialog
  box.

- Choose File \> Publish.

- Choose File \>Publish Preview.

When you Publish an AIR file, Flash Pro creates a SWF file and XML application
descriptor file and packages copies of both, along with any other files you have
added to your application, into an AIR installer file (_swfname_.air).

## Creating AIR application and installer files

After you've finished developing your application, specify the settings for the
AIR application descriptor and installer files required to deploy it. Flash Pro
creates the descriptor and installer files along with the SWF file when you
publish an AIR file.

You specify the settings for these files in the AIR - Application & Installer
Settings dialog box. Once you have created an AIR file, this dialog box can be
opened from either the document Property inspector or the Player menu Settings
button in the Flash tab of the Publish Settings dialog box.

#### Create the Adobe AIR application and installer files

1.  In Flash, open the FLA file or set of files that make up your Adobe AIR
    application.

2.  Save the Adobe AIR FLA file before you open the AIR Application & Installer
    Settings dialog box.

3.  Select File \> AIR 2 Settings.

4.  Complete the AIR Application & Installer Settings dialog box, and then click
    Publish.

    When you click the Publish button, the following files are packaged: the SWF
    file, the application descriptor file, the application icon files, and the
    files listed in the Included Files text box. If you have not already created
    a digital certificate, Flash displays the Digital Signature dialog box when
    you click the Publish button.

The AIR Application And Installer Settings dialog box is divided into 4 tabs:
General, Signature, Icons, and Advanced. For more information on these settings,
see the following sections.

### General settings

The General tab of the AIR Application And Installer Settings dialog box
contains the following options:

Output file  
The name and location of the .air file to create when using the Publish command.

Windows Installer  
Select this option to compile a native, platform specific Windows installer
(.exe) instead of a platform-independent AIR installer (.air).

File Name  
The name of the main file of the application. Defaults to the name of the FLA
file.

App Name  
The name used by the AIR application installer to generate the application
filename and the application folder. The name must contain only valid characters
for filenames or folder names. Defaults to the name of the SWF file.

Version  
Optional. Specifies a version number for your application. Defaults to 1.0.

App ID  
Identifies your application with a unique ID. You can change the default ID if
you prefer. Do not use spaces or special characters in the ID. The only valid
characters are 0-9, a-z, A-Z, . (dot), and - (dash), from 1 to 212 characters in
length. Defaults to `com.adobe.example.``applicationName`_._

Description  
Optional. Lets you enter a description of the application to display in the
installer window when the user installs the application. Defaults to blank.

Copyright  
Optional. Lets you enter a copyright notice. Defaults to blank.

Window Style  
Specifies what window style (or chrome) to use for the user interface when the
user runs the application on their computer. You can specify System Chrome (the
default), which refers to the standard window visual style that the operating
system uses. You can also specify Custom Chrome (opaque) or Custom Chrome
(transparent). To display your application without the system chrome, select
None. System Chrome surrounds the application with the operating-system standard
window control. Custom Chrome (opaque) eliminates the standard system chrome and
lets you create a chrome of your own for the application. (You build the custom
chrome directly in the FLA file.) Custom Chrome (transparent) is like Custom
Chrome (opaque), but it adds transparent capabilities to the edges of the page.
These capabilities allow for application windows that are not square or
rectangular in shape.

Profiles  
Which profiles to include when building the AIR file. To limit your AIR
application to a specific profile, deselect the unneeded profiles. For more
information about AIR profiles, see
[Application profiles](https://web.archive.org/web/20111114123312mp_/http://help.adobe.com/en_US/air/build/WS144092a96ffef7cc16ddeea2126bb46b82f-8000.html).

Included Files  
Specifies which additional files and folders to include in your application
package. Click the Plus (+) button to add files, and the folder button to add
folders. To delete a file or folder from your list, select the file or folder
and click the Minus (-) button.

By default, the application descriptor file and the main SWF file are
automatically added to the package list. The package list shows these files even
if you have not yet published the Adobe AIR FLA file. The package list displays
the files and folders in a flat structure. Files in a folder are not listed, and
full path names to files are shown but are truncated if necessary.

Icon files are not included in the list. When Flash packages the files, it
copies the icon files to a temporary folder that is relative to the location of
the SWF file. Flash deletes the folder after packaging is complete.

### Signature settings

The Signature tab of the AIR Application & Installer Settings dialog box allows
you to specify a code signing certificate for your application.

For more information about digital signatures, see
[Signing your application](#signing-your-applicationl) and
[Digitally signing an AIR file](https://web.archive.org/web/20111114123312mp_/http://help.adobe.com/en_US/air/build/WS5b3ccc516d4fbf351e63e3d118666ade46-7ff0.html).

### Icons settings

The Icons tab of the AIR Application And Installer Settings dialog box lets you
specify an icon for the application. The icon is shown after you install the
application and run it in the Adobe AIR runtime. You can specify four different
sizes for the icon (128, 48, 32, and 16 pixels) to allow for the different views
in which the icon appears. For example, the icon can appear in the file browser
in thumbnail, detail, and tile views. It can also appear as a desktop icon and
in the title of the AIR application window, as well as in other places.

The icon image defaults to a sample AIR application icon if no other icon files
are specified (Flash CS5 only).

To specify an icon, click an icon size at the top of the Icons tab and then
navigate to the file you want to use for that size. The files must be in PNG
(Portable Network Graphics) format.

If you do specify an image, it must be the exact size (either 128x128, 48x48,
32x32, or 16x16). If you do not supply an image for a particular icon size,
Adobe AIR scales one of the supplied images to create the missing icon image.

### Advanced settings

The Advanced tab allows you to specify additional settings for the application
descriptor file.

You can specify any associated file types that your AIR application should
handle. For example, if you wanted your application to be the principal
application for handling HTML files, you would specify that in the Associated
File Types text box.

You can also specify settings for the following aspects of the application:

- The size and placement of the initial window

- The folder in which the application is installed

- The Program menu folder in which to place the application.

The dialog box has the following options:

Associated file types  
Lets you specify associated file types that the AIR application will handle.
Click the Plus (+) button to add a new file type to the text box. Clicking the
Plus button displays the File Type Settings dialog box. Clicking the Minus (-)
button removes an item that is selected in the text box. Clicking the Pencil
button displays the File Type Settings dialog box and allows you to edit an item
that you've selected in the text box. By default, the Minus (-) and Pencil
buttons are dimmed. Selecting an item in the text box enables the Minus (-) and
Pencil buttons, allowing you to remove or edit the item. The default value in
the text box is None.

Initial window settings  
Lets you specify size and placement settings for the initial application window.

- Width: Specifies the initial width of the window in pixels. The value is blank
  by default.

- Height: Specifies the initial height of the window in pixels. The value is
  blank by default.

- X: Specifies the initial horizontal position of the window in pixels. The
  value is blank by default.

- Y: Specifies the initial vertical position of the window in pixels. The value
  is blank by default.

- Maximum Width and Maximum Height: Specify the maximum size of the window in
  pixels. These values are blank by default.

- Minimum Width and Minimum Height: Specify the minimum size of the window in
  pixels. These values are blank by default.

- Maximizable: Lets you specify whether the user can maximize the window. This
  option is selected (or true) by default.

- Minimizable: Lets you specify whether the user can minimize the window. This
  option is selected (or true) by default.

- Resizable: Lets you specify whether the user can resize the window. If this
  option is not selected, Maximum Width, Maximum Height, Minimum Width, and
  Minimum Height are dimmed. This option is selected (or true) by default.

- Visible: Lets you specify whether the application window is visible initially.
  The option is selected (or true) by default.

Other Settings  
Lets you specify the following additional information regarding the
installation:

- Install Folder: Specifies the folder in which the application is installed.

- Program Menu Folder (Windows only): Specifies the name of the program menu
  folder for the application.

- Use Custom UI for Updates: Specifies what happens when a user opens an AIR
  installer file for an application that's already installed. By default, AIR
  displays a dialog box that allows the user to update the installed version
  with the version in the AIR file. If you don't want the user to make that
  decision and you want the application to have complete control over its
  updates, select this option. Selecting this option overrides the default
  behavior and gives the application control over its own updates.

### File type settings

Flash displays the File Type Settings dialog box if you click the Plus (+)
button or the Pencil button in the Associated File Types section of the Advanced
tab to add or edit associated file types for the AIR application.

The only two required fields in this dialog box are Name and Extension. If you
click OK and either of those fields is blank, Flash displays an error dialog
box.

You can specify the following settings for an associated file type:

Name  
The name of the file type (for example, Hypertext Markup Language, Text File, or
Example).

Extension  
The filename extension (for example, html, txt, or xmpl), up to 39 basic
alphanumeric characters, (A-Za-z0-9), and without a leading period.

Description  
Optional. A description of the file type (for example, Adobe Video File).

Content type  
Optional. Specifies the MIME type for the file.

File Type Icon Settings  
Optional. Lets you specify an icon that's associated with the file type. You can
specify four different sizes for the icon (128x128, 48x48, 32x32, and 16x16
pixels) to allow for the different views in which the icon appears. For example,
the icon can appear in the file browser in thumbnail, detail, and tile views.

If you specify an image, it must be of the size that you specify. If you do not
specify a file for a particular size, AIR uses the image of the closest size and
scales it to fit for the given occurrence.

To specify an icon, either click the folder for the icon size and select an icon
file to use or enter the path and filename for the icon file in the text box
next to the prompt. The icon file must be in PNG format.

After a new file type is created, it is shown in the File Type list box in the
Advanced Settings dialog box.

### Failure to create application and installer files

The application and installer files fail to be created in the following
instances:

- The application ID string has an incorrect length or contains invalid
  characters. The application ID string can be from 1 to 212 characters and can
  include the following characters: 0-9, a-z, A-Z, . (dot), - (hyphen).

- Files in the Included Files list do not exist.

- The sizes of custom icon files are incorrect.

- The AIR destination folder does not have write access.

- You have not signed the application or have not specified that it is an Adobe
  AIRI application that will be signed later.

## Signing your application

All Adobe AIR applications must be signed to be installed on another system.
Flash provides the ability, however, to create unsigned Adobe AIR installer
files so that the application can be signed later. These unsigned Adobe AIR
installer files are called an AIRI (AIR Intermediate) package. This capability
provides for cases in which the certificate is on a different machine or signing
is handled separately from application development.

#### Sign an Adobe AIR application with a pre-purchased digital certificate from a root certificate authority

1.  Choose File \> AIR 2 Settings and then click on the Signature tab.

    This tab has two radio buttons that allow you to either sign your Adobe AIR
    application with a digital certificate or prepare an AIRI package. If you
    sign your AIR application, you can either use a digital certificate granted
    by a root certificate authority or create a self-signed certificate. A
    self-signed certificate is easy to create but is not as trustworthy as a
    certificate granted by a root certificate authority.

2.  Select a certificate file from the pop-up menu or click the Browse button to
    locate a certificate file.

3.  Select the certificate.

4.  Enter a password.

5.  Click OK.

For more information on signing your AIR application, see
[Digitally signing an AIR file](https://web.archive.org/web/20111114123312mp_/http://help.adobe.com/en_US/air/build/WS5b3ccc516d4fbf351e63e3d118666ade46-7ff0.html).

#### Create a self-signed digital certificate

1.  Click the Create button. The Self-Signed Digital Certificate dialog box
    opens.

2.  Complete the entries for Publisher Name, Organization Unit, Organization
    Name, Country, Password, and Confirm Password. For Country, you can select
    from the menu or enter a 2-letter country code that does not appear in the
    menu. For a list of valid country codes, see
    [http://www.iso.org/iso/country_codes](https://web.archive.org/web/20111114123312mp_/http://www.iso.org/iso/country_codes).

3.  Specify the type of certificate.

    The Type option refers to the level of security that the certificate
    carries: 1024-RSA uses a 1024-bit key (less secure), and 2048-RSA uses a
    2048-bit key (more secure).

4.  Save the information in a certificate file by completing the Save As entry
    or clicking the Browse button to browse to a folder location.

5.  Click OK.

6.  In the Digital Signature dialog box, enter the password you assigned in the
    second step of this procedure and click OK.

To have Flash remember the password you used for this session, click Remember
Password For This Session.

If the Timestamp option is unselected when you click OK, a dialog box warns that
the application will fail to install when the digital certificate expires. If
you click Yes in response to the warning, time stamping is disabled. If you
click No, the Timestamp option is automatically selected and time stamping is
enabled.

For more information on creating a self-signed digital certificate, see
[Digitally signing an AIR file](https://web.archive.org/web/20111114123312mp_/http://help.adobe.com/en_US/air/build/WS5b3ccc516d4fbf351e63e3d118666ade46-7ff0.html).

You can also create an AIR Intermediate (AIRI) application without a digital
signature. A user cannot install the application on a desktop, however, until
you add a digital signature.

#### Prepare an AIRI package that will be signed later

![](../img/dingbat.png) In the Signature tab, select Prepare An AIR Intermediate
(AIRI) File That Will Be Signed Later, and click OK.

The digital signature status changes to indicate that you have chosen to prepare
an AIRI package that will be signed later, and the Set button changes to a
Change button.

If you choose to sign the application later, you will need to use the
command-line AIR Developer Tool included with Flash Pro and with the AIR SDK.
For more information, see
[_Building Adobe AIR Applications_](https://web.archive.org/web/20111114123312mp_/http://help.adobe.com/en_US/air/build/).
