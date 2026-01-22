# Accessibility guidelines

## About accessibility guidelines

Screen readers are complex, and you can easily encounter unexpected results in
FLA files developed for use with screen readers, which is software that visually
impaired users run to read websites aloud. Text is read aloud using specially
designed software. A screen reader can only interpret textual content. However,
any descriptions that you provide for the overall SWF file, movie clips, images,
or other graphical content are also read aloud. Write descriptions for the
important images and animations so that the screen reader can also interpret
these assets in your SWF file. This is the SWF file equivalent to _alt_ text in
an HTML web page.

> **Note:** Flash Pro applications must be viewed in Internet Explorer on
> Windows, because Microsoft Active Accessibility (MSAA) support is limited to
> this browser.

Flash Player uses Microsoft Active Accessibility (MSAA) to expose Flash Pro
content to screen readers. MSAA is a Windows-based technology that provides a
standardized platform for information exchange between assistive technologies,
such as screen readers, and other applications. Events (such as a change in the
application) and objects are visible to screen readers by using MSAA.

> **Note:** Flash Player 7 (and later) does not work with all screen-reader
> technologies. The third-party software provider must handle the information
> that MSAA provides.

## Creating accessible sites

Making a website accessible involves several different criteria:

Expose the information to screen readers  
Make text or images realizable  
Some visitors might have difficulty reading small text or seeing small graphics.
Allow users to zoom in on these elements, taking advantage of scalable vector
graphics in SWF files.

Provide audio narration  
Consider providing an audio narration for visitors without a screen reader, or
where screen readers might not work, such as with video content.

Provide captions for audio narrations  
Some visitors might not be able to hear an audio narration for your site or a
video. Consider providing captions for these visitors.

Do not rely on color to communicate information  
Many visitors might be color blind. If you rely on color to communicate
information (such as: Click the green button to go to page 1, click the red
button to go to page 2), provide text or speech equivalents.

Historically, many online presentations (such as videos) provide alternative
ways for visually impaired visitors to access the content, for instance, a
textual description of a video. However, Flash Pro provides textual information
directly to the screen reader. Although this usually means you need to make
additional settings or ActionScript in a FLA file, you do not have to create a
completely separate version.

Parts of your SWF file can be exposed to screen readers. Text elements (such as
text fields, static text, and dynamic text), buttons, movie clips, components,
and the entire SWF file can be interpreted by MSA-compliant screen readers.

Section 508 is United States legislation that provides guidelines for making
information accessible to people with disabilities. Section 508 specifically
addresses the need for websites to be accessible in several ways. Some websites,
including all federal websites, must comply with these guidelines. If a SWF file
does not communicate all of the information to the screen reader, the SWF file
is no longer Section 508-compliant. For more information, see the Section 508
website.

Many nations have specified guidelines to follow to create accessible web sites,
or follow guidelines established by other organizations. For more information on
accessibility and web standards, see the World Wide Web Consortium (W3C) Web
Accessibility Initiative website. These standards and guidelines describe what
factors you must address when you create accessible HTML websites, and some of
this information applies to Flash Pro.

## Exposing SWF file structure and navigation

Because of the visual nature of some SWF files, the layout and navigation of the
page can be complex and difficult for screen readers to translate. An overall
description of the SWF file is important to communicate information about its
structure and how to navigate through the site's structure. You can provide this
description by clicking the Stage and entering a description into the
Accessibility panel. You can also create a separate area of the site to provide
this description or overview.

> **Note:** If you enter a description for the main SWF file, this description
> is read each time the SWF file refreshes. You can avoid this redundancy by
> creating a separate informational page. Inform the user about any navigational
> elements that change in the SWF file. Perhaps an extra button is added, or the
> text on the face of a button changes, and this change is read aloud by the
> screen reader. Flash Player 7 and later supports updating these properties by
> using ActionScript. You can update the accessibility information in your
> applications if the content changes at runtime.

## Controlling descriptions and repetition

Designers and developers can assign descriptions for the animations, images, and
graphics in a SWF file. Provide names for graphics so the screen reader can
interpret them. If a graphic or animation does not communicate vital information
to the SWF file (perhaps it is decorative or repetitive), or you outlined the
element in the overall SWF file description, do not provide a separate
description for that element. Providing unnecessary descriptions can be
confusing to users who use screen readers.

> **Note:** If you divide text or use images for text in your SWF files, provide
> either a name or description for these elements. If you have several nested
> movie clips that serve a single purpose or convey one idea, ensure that you do
> the following:

- Group these elements in your SWF file.

- Provide a description for the parent movie clip.

- Make all the child movie clips inaccessible.

  This is extremely important, or the screen reader tries to describe all the
  irrelevant nested movie clips, which will confuse the user, and might cause
  the user to leave your website. Make this decision whenever you have more than
  one object, such as many movie clips, in a SWF file. If the overall message is
  best conveyed using a single description, provide a description on one of the
  objects, and make all the other objects inaccessible to the screen reader.

  Looping SWF files and applications cause screen readers to constantly refresh
  because the screen reader detects new content on the page. Because the reader
  thinks the content is updated, it returns to the top of the web page and
  starts rereading the content. Make inaccessible to screen readers any looping
  or refreshing objects that do not have to be reread.

  > **Note:** Do not type a description in the Description field of the
  > Accessibility panel for instances (such as text) that the screen reader
  > reads aloud.

## Using color

You must make decisions about using colors in an accessible file. You must not
rely only on color to communicate particular information or directives to users.
A color-blind user cannot operate a page if it asks to click on the blue area to
launch a new page or the red area to hear music. Offer text equivalents on the
page or in an alternate version to make your site accessible. Also, check that
significant contrast exists between foreground and background colors to enhance
readability. If you place light gray text on a white background, users cannot
easily read it. Similarly, small text is difficult for many visitors to read.
Using high-contrast and large or resizable text benefits most users, even those
without impairments.

## Ordering, tabbing, and the keyboard

Reading order and tabbing are important considerations for making accessible
Flash Pro websites. When you design an interface, the order that it appears on
the page might not match the order in which the screen reader describes each
instance. You can control and test reading order, as well as control tabbing in
the SWF file.

#### Controlling reading order

The default reading order is not predictable and does not always match the
placement of your assets or the visual layout of the page. Keeping the layout
simple can help create a logical reading order without using ActionScript.
However, you have more control over reading order if you use ActionScript and
test the reading order in your SWF files. Important: Do not miss ordering a
single instance in your SWF file, or the reading order reverts to the default
(and unpredictable) reading order.

#### Controlling tabbing and content

Visitors who rely on screen readers to describe a site's content typically use
tabbing and keyboard controls to navigate the operating system and web pages,
because using the mouse is not useful when the screen cannot be seen. Use the
`tabIndex` and `tabEnabled` properties with the movie clip, button, text field,
or component instances to offer intelligent tabbing control in accessible SWF
files. In addition to tabbing, you can use any key-press actions to navigate
through the SWF file, but you must communicate that information using the
Accessibility panel. Use the `Key` class in ActionScript to add key-press
scripts to the SWF file. Select the object for which you want to use the
key-press script, and add the shortcut key in the Shortcut field on the
Accessibility panel. Add keyboard shortcuts to essential and frequently used
buttons in your SWF file.

> **Note:** In ActionScript 3.0, `tabIndex` and `tabEnabled` are properties of
> the `InteractiveObject` class. In ActionScript 2.0, they do not require a
> class reference.

> **Note:** Avoid invisible buttons in accessible SWF files, because screen
> readers do not recognize these buttons. (Invisible buttons are buttons for
> which you define only a hit area, the clickable region, for the button.)

Many SWF files have a rapid succession of information, and screen readers
frequently cannot keep up with this pace. Provide controls for the SWF file,
letting the user use buttons to navigate through the file at their own pace, and
letting them pause the process if necessary.

## Handling audio, video, and animation

When you provide audio narrations or video that contains speech, provide
captions for those users who cannot hear. You can use text fields in Flash Pro,
import video that contains captions, or even use an XML caption file. You can
use video cue points to specify when a text field should update text information
at runtime.

For information on using Hi-Caption SE and the Hi-Caption Viewer component, see
[www.adobe.com/go/flash_extensions](https://web.archive.org/web/20111119002906mp_/http://www.adobe.com/go/flash_extensions).
This third-party extension lets you create captions that you save in an XML file
and load into the SWF file at runtime, among other advanced controls.
Alternatively, you can use cue points and a text field to display caption
information.

## Accessibility and extending Flash

With the extensibility layer in Flash Pro, developers can create extensions that
enable advanced authoring. This lets third-party companies develop extensions
that involve accessibility. You have several options for validating your SWF
files or adding captions.

For example, a validation tool can examine your SWF file for missing
descriptions. It checks to see if a description is added for a group of
instances, or if text has a label for the instance, and tells you about any
problems. The tool also examines the reading order in your SWF file, and finds
all instances that must be specified. You can specify reading order by using a
dialog box after the SWF file is analyzed.

For information on the currently available third-party extensions, see
[www.adobe.com/go/flash_extensions](https://web.archive.org/web/20111119002906mp_/http://www.adobe.com/go/flash_extensions).

## Testing files and making changes

Test any SWF file that is intended for use with screen readers. Test your SWF
files when each new version of Flash Player is released, including minor
revisions, and test it with the following scenarios:

- Using the Window Eyes and JAWS for Windows screen readers. These each handle
  SWF files differently, so you could get different results.

- In a browser without a screen reader, and navigate through your site without
  using the mouse.

- Turn off your monitor and use only the screen reader to navigate your website.

- If you use audio narration, test your site without speakers.

- With several users who are representative of your target web site visitors.

  > **Note:** You do not have to test different browsers, because the technology
  > used to expose SWF files to screen readers (MSAA) is supported only by
  > Internet Explorer on Windows.

When listening to your SWF file using a screen reader, check the following
points:

- Is the reading order correct?

- Do you have descriptions for shortcuts in your SWF file?

- Do you have adequate and complete descriptions for the elements in the
  interface?

- Do you have adequate descriptions for navigating the site's structure?

- Is the SWF file content read when it is updated or refreshed?

- If you change the context of any elements on the Stage (such as a button that
  changes from Play to Pause), is that change announced by the screen reader?

  No official tool is available for validating SWF files, unlike HTML
  validation. However, some third-party tools exist to help you validate the
  file. For more information on these extensions, see
  [www.adobe.com/go/flash_extensions](https://web.archive.org/web/20111119002906mp_/http://www.adobe.com/go/flash_extensions).

More Help topics

[Creating accessibility with ActionScript](../creating-accessible-content/creating-accessibility-with-actionscript.md)

[Using Flash to enter accessibility information for screen readers](../creating-accessible-content/using-flash-to-enter-accessibility-information-for-screen-readers.md)

[Accessibility for hearing-impaired users](../creating-accessible-content/about-accessible-content.md#accessibility-for-hearing-impaired-users)
