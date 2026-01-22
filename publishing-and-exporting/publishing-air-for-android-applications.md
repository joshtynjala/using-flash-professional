# Publishing AIR for Android applications

Beginning with Flash Professional CS5.5, you can publish content for Adobe® AIR™
for Android, a mobile device operating system from Google.

This article describes configuring the AIR for Android publish settings in Flash
Professional. For complete information about developing Adobe AIR™ applications,
see
[_Building Adobe AIR Applications_](https://web.archive.org/web/20120101152026mp_/http://help.adobe.com/en_US/air/build/index.html).

For information about hardware and software requirements for desktop and mobile
AIR applications, see
[AIR system requirements](https://web.archive.org/web/20120101152026mp_/http://www.adobe.com/products/air/systemreqs/).

#### Tutorials

The following tutorials describe how to create AIR™ for Android applications in
Flash Pro:

- Blog:
  [One Application, Five Screens](https://web.archive.org/web/20120101152026mp_/http://blogs.adobe.com/cantrell/archives/2010/04/one_application_five_screens.html)
  (Christian Cantrell, Adobe blogs)

- Article:
  [Developing a Mobile Application with Flash](https://web.archive.org/web/20120101152026mp_/http://www.gamedev.net/page/resources/_/reference/programming/game-programming/300/developing-a-mobile-application-with-flash-r2797)
  (John Hattan, gamedev.net)

## Create an Adobe AIR for Android file

You can create Adobe AIR for Android documents in Flash using the File \> New
command. You can also create an ActionScript® 3.0 FLA file and convert it to an
AIR for Android file through the Publish Settings dialog box.

To create an AIR for Android file, do one of the following:

- Choose AIR for Android from the Welcome screen or the New Document dialog box
  (File \> New).

- Open an existing FLA file and convert it to an AIR for Android file. Select
  AIR for Android from the Player menu in the Flash tab of the Publish Settings
  dialog box (File \> Publish Settings).

## Preview or publish an AIR for Android application

**You can preview** a Flash AIR for Android SWF file as it would appear in the
AIR application window. Previewing is useful when you want to see what the
visible aspects of the application look like without packaging and installing
the application.

1.  Make sure you've set the Player setting in the Publish Settings dialog box
    to AIR for Android.

2.  Select Control \> Test Movie \> Test or press Control+Enter.

If you have not set application settings through the Application & Installer
Settings dialog box, Flash generates a default application descriptor file
(_swfname_-app.xml) for you. Flash creates the file in the same folder where the
SWF file is written. If you have set application settings using the Application
& Installer Settings dialog box, the application descriptor file reflects those
settings.

**To publish** an AIR for Android file, do one of the following:

- Click the Publish button in the Publish Settings dialog box.

- Click the Publish button in the Application & Installer Settings dialog box.

- Choose File \> Publish.

- Choose File \>Publish Preview.

When you Publish an AIR file, Flash Pro creates a SWF file and XML application
descriptor file. Then Flash packages copies of both, along with any other files
you have added to your application, into an AIR installer file (_swfname_.apk).

## Creating AIR for Android applications

After you've finished developing your application, specify the settings for the
AIR for Android application descriptor and installer files required to deploy
it. Flash Pro creates the descriptor and installer files along with the SWF file
when you publish an AIR for Android file.

You specify the settings for these files in the AIR for Android - Application &
Installer Settings dialog box. Once you have created an AIR for Android file,
this dialog box can be opened from the document Property inspector. You can also
access it from the Player menu Settings button in the Flash tab of the Publish
Settings dialog box.

#### Create the Adobe AIR application file

1.  In Flash, open the FLA file or set of files that make up your Adobe AIR
    application.

2.  Save the AIR for Android FLA file before you open the AIR Application &
    Installer Settings dialog box.

3.  Select File \> AIR for Android Settings.

4.  Complete the AIR for Android Application & Installer Settings dialog box,
    and then click Publish.

    When you click the Publish button, the following files are packaged:
    - The SWF file

    - The application descriptor file

    - The application icon files

    - The files listed in the Included Files text box

The AIR for Android Application and Installer Settings dialog box is divided
into four tabs: General, Deployment, Icons, and Permissions.

### General settings

The General tab of the AIR for Android Application and Installer Settings dialog
box contains the following options:

Output file  
The name and location of the AIR file to create when using the Publish command.
The output filename extension is APK.

App Name  
The name used by the AIR application installer to generate the application
filename and the application folder. The name must contain only valid characters
for filenames or folder names. Defaults to the name of the SWF file.

App ID  
Identifies your application with a unique ID. You can change the default ID if
you prefer. Do not use spaces or special characters in the ID. The only valid
characters are 0-9, a-z, A-Z, and . (dot), from 1 to 212 characters in length.
Defaults to `com.adobe.example.``applicationName`_._

Version  
Optional. Specifies a version number for your application. Defaults to 1.0.

Version label  
Optional. A string to describe the version.

Aspect Ratio  
Allows you to select Portrait, Landscape, or Auto orientation for the
application. When Auto is selected along with Auto orientation, the application
launches on the device depending on its current orientation.

Full Screen  
Sets the application to run in full screen mode. This setting is deselected by
default.

Auto orientation  
Allows the application to switch from portrait to landscape mode, depending on
the current orientation of the device. This setting is deselected by default.

Included Files  
Specifies which additional files and folders to include in your application
package. Click the Plus (+) button to add files, and the folder button to add
folders. To delete a file or folder from your list, select the file or folder
and click the Minus (-) button.

By default, the application descriptor file and the main SWF file are
automatically added to the package list. The package list shows these files even
if you have not yet published the Adobe AIR FLA file. The package list displays
the files and folders in a flat structure. Files in a folder are not listed, and
full paths to files are shown but are truncated if necessary.

Icon files are not included in the list. When Flash packages the files, it
copies the icon files to a temporary folder that is relative to the location of
the SWF file. Flash deletes the folder after packaging is complete.

### Deployment settings

The Deployment tab of the AIR for Android Application and Installer Settings
dialog box lets you specify the following settings.

Certificate  
The digital certificate for the application. You can browse to a certificate or
create a new one. For information about creating a digital certificate, see
[Signing your application](./publishing-for-adobe-air-for-desktop.md#signing-your-application).
Note certificates for Android applications must have a validity period set to at
least 25 years.

Password  
The password for the selected digital certificate.

Android deployment type  
The Device debugging deployment type allows you to do on-device debugging,
including setting breakpoints in Flash and remote debugging the application
running on the Android device.

The Release setting allows you to create packages for the marketplace or any
other distribution medium such as a website.

After publish  
Allows you to specify whether to install the application on a currently
connected Android device, and whether to immediately launch the application
after the installation.

### Icons settings

The Icons tab of the AIR for Android Application And Installer Settings dialog
box lets you specify an icon for the Android application. The icon is shown
after you install the application and run it in the AIR for Android runtime. You
can specify three different sizes for the icon (72, 48, and 36 pixels) to allow
for the different views in which the icon appears. The icons you choose for
Android do not have to strictly adhere to these sizes.

To specify an icon, click an icon size in the Icons tab and then navigate to the
file you want to use for that size. The files must be in PNG (Portable Network
Graphics) format.

If you do not supply an image for a particular icon size, Adobe AIR scales one
of the supplied images to create the missing icon image.

### Permissions settings

The Permissions tab allows you to specify which services and data the
application has access to on the device.

- To apply a permission, select its checkbox.

- To see a description of a permission, click the permission name. The
  description appears below the permission list.

- To manually manage permissions instead of using the dialog box, select
  "Manually manage permissions and manifest additions in the application
  descriptor file".
