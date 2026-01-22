# Best practices - Advertising with Flash

## Using recommended dimensions

Use the Interactive Advertising Bureau (IAB) guidelines to set dimensions for
your Flash Pro advertisements. The following table lists the recommended
Interactive Marketing Unit (IMU) ad formats measurements: | Type of
advertisement | Dimensions (pixels) | | --------------------- |
------------------- | | Wide skyscraper | 160 x 600 | | Skyscraper | 120 x 600 |
| Half-page ad | 300 x 600 | | Full banner | 468 x 60 | | Half banner | 234 x 60
| | Micro bar | 88 x 31 | | Button 1 | 120 x 90 | | Button 2 | 120 x 60 | |
Vertical banner | 120 x 240 | | Square button | 125 x 125 | | Leaderboard | 728
x 90 | | Medium rectangle | 300 x 250 | | Square pop‑up | 250 x 250 | | Vertical
rectangle | 240 x 400 | | Large rectangle | 336 x 280 | | Rectangle | 180 x 150
| When you create a FLA file from a template (Select File \> New, and click the
Templates tab), you see many of these sizes.

## Creating SWF file advertisements

Use these guidelines when you create advertisements:

- Optimize your graphics. Make SWF file banner advertisements 15K or smaller.

- Create a GIF banner advertisement in Flash Pro that is 12K or smaller.

- Limit looping banner advertisements to three repetitions. Many websites adopt
  the standardized file size recommendations as advertising specifications.

- Use the `GET` command to pass data between an advertisement and a server, and
  do not use the `POST` command. For more information on GET and POST, see the
  getURL function in _ActionScript 2.0 Language Reference_.

> **Note:** Provide control to the user. If you add sound to an advertisement,
> also add a mute button. If you create a transparent Flash Pro ad that hovers
> over a web page, provide a button to close the advertisement for its duration.

## Tracking advertisements

Several leading advertising networks now support standardized tracking methods
in Flash Pro SWF files. The following guidelines describe the supported tracking
methodology:

Create a button or movie clip button  
Use standardized dimensions outlined by the IAB. For a list of standardized
dimensions, see the IAB website. For more information on creating a button in
Flash Pro, see
[Creating buttons](../symbols-instances-and-library-assets/creating-buttons.md).

Add a script to the button  
Executes when a user clicks the banner. You might use the `getURL()` function to
open a new browser window. The following code snippets are two examples of
ActionScript 2.0 code you might add to Frame 1 of the Timeline:

    myButton_btn.onRelease = function() {
        getURL(clickTAG, "_blank");
    };

You might add the following code to Frame 1 of the Timeline:

    myButton_btn.onRelease = function() {
        if (clickTAG.substr(0, 5) == "http:") {
            getURL(clickTAG);
        }
    };

The `getURL()` function adds the variable passed in the `object` and `embed`
tags, and then sends the browser that is launched to the specified location. The
server hosting the ad can track clicks on the advertisement. For more
information on using the `getURL()` function, see _ActionScript 2.0 Language
Reference_.

Assign clickTAG code for tracking  
Tracks the advertisement and helps the network serving the ad to track where the
ad appears and when it is clicked.

The process is the standard way of creating an advertising campaign for a
typical Flash Pro advertisement. If you assign the `getURL()` function to the
banner, you can use the following process to add tracking to the banner. The
following example lets you append a variable to a URL string to pass data, which
lets you set dynamic variables for each banner, instead of creating a separate
banner for each domain. You can use a single banner for the entire campaign, and
any server that is hosting the ad can track the clicks on the banner.

In the `object` and `embed` tags in your HTML, you would add code similar to the
following example (where www.helpexamples.com is the ad network, and adobe.com
is the company with an advertisement):

    <EMBED src="your_ad.swf?clickTAG= http://helpexamples.com/tracking?http://www.adobe.com">

Add the following code in your HTML:

    <PARAM NAME=movie VALUE="your_ad.swf?clickTAG =http: //helpexamples.com/tracking?http://www.adobe.com">

For more information on advanced tracking techniques, see the Rich Media
Advertising Center at
[www.adobe.com/go/rich_media_ads](https://web.archive.org/web/20120101020605mp_/http://www.adobe.com/go/rich_media_ads).

To download the Rich Media Tracking Kit, which includes examples and
documentation, see
[www.adobe.com/go/richmedia_tracking](https://web.archive.org/web/20120101020605mp_/http://www.adobe.com/go/richmedia_tracking).

To learn more about and download the Flash Ad Kit, which helps you deliver
integrated and sophisticated advertisements, see
[www.adobe.com/go/learn_fl_flash_ad_kit](https://web.archive.org/web/20120101020605mp_/http://www.adobe.com/go/learn_fl_flash_ad_kit).

## Testing your ads

Test your SWF file ad on the most common browsers, especially the browsers that
your target audience uses. Some users might not have Flash Player installed or
they might have JavaScript disabled. Plan for these circumstances by having a
replacement (default) GIF image or other scenarios for these users. For more
information on detecting Flash Player, see
[Specify publish settings for SWF files (CS5)](../publishing-and-exporting/publish-settings-cs5.md#specify-publish-settings-for-swf-files-cs5).
Give the user control of the SWF file. Let the user control any audio in the ad.
If the advertisement is a borderless SWF file that hovers over a web page, let
the user close the advertisement immediately and for the duration of the ad.

For the latest information on Flash Player version penetration for different
regions, go to
[www.adobe.com/go/fp_version_penetration](https://web.archive.org/web/20120101020605mp_/http://www.adobe.com/go/fp_version_penetration).

More Help topics

[Optimizing graphics and animation](./optimizing-fla-files-for-swf-output/optimizing-graphics-and-animation.md)
