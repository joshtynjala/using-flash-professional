# About accessible content

## Accessibility overview

You can create content that is accessible to all users, including those with
disabilities, using the accessibility features that
Adobe® Flash® Professional CS5 provides in the authoring environment user
interface, taking advantage of ActionScript® designed to implement
accessibility. As you design accessible Flash applications, consider how users
might interact with the content and follow recommended design and development
practices.

For a sample of accessible rich media content, see the
[Flash Samples page](https://web.archive.org/web/20120102164641/http://www.adobe.com/devnet/flash/samples.html).
Download and decompress the Samples zip file and navigate to the
Accessibility\AccessibleApplications folder to access the sample.

For the latest information on creating and viewing accessible Flash content,
including supported platforms, screen reader compatibility, articles, and
accessible examples, see the
[Flash Accessibility web page](https://web.archive.org/web/20101005081148/http://www.adobe.com/accessibility/products/flash/).

## Worldwide accessibility standards

Many countries have adopted accessibility standards based on the standards
developed by the World Wide Web Consortium (W3C). The W3C publishes the _Web
Content Accessibility Guidelines_, a document that prioritizes actions designers
should take to make web content accessible. For information about the Web
Accessibility Initiative, see the W3C website at w3.org.

In the United States, the law that governs accessibility is commonly known as
Section 508, which is an amendment to the U.S. Rehabilitation Act.

For additional information about Section 508, see the following websites:

- The US government-sponsored website at section508.gov

- The Adobe accessibility site at
  [www.adobe.com/accessibility/](https://web.archive.org/web/20101031170653mp_/http://www.adobe.com/accessibility/)

## Understanding screen reader technology

Screen readers are software applications that visually impaired users can use to
navigate a website and read the web content aloud. To enable a screen reader to
read nontextual objects in your application, such as vector art and animations,
use the Accessibility panel to associate a name and description with the object.
The keyboard shortcuts you define can allow users to use the screen reader to
navigate through your document with ease.

To expose graphic objects, use the Accessibility panel or ActionScript to
provide a description.

You cannot control how any screen reader behaves; you can control only the
content, which you can mark up in your Flash applications to expose the text and
ensure that screen reader users can activate the controls. You decide which
objects in the Flash application are exposed to screen readers, provide
descriptions for them, and decide the order in which they are exposed to screen
readers. You cannot force screen readers to read specific text at specific times
or control the manner in which that content is read. Test your applications with
a variety of screen readers to ensure that they perform as you expect.

Sound is the most important medium for most screen reader users. Consider how
any sound in your document interacts with the text spoken aloud by screen
readers. It might be difficult for screen reader users to hear what their screen
readers are saying if your Flash application contains loud sounds.

#### Platform requirements

You can only create Flash content designed for use with screen readers with
Windows platforms. Viewers of Flash content must have Macromedia Flash® Player 6
from Adobe or later and Internet Explorer on Windows 98 or later.

## Flash and Microsoft Active Accessibility (Windows only)

Flash Player is optimized for Microsoft Active Accessibility (MSAA), which
provides a descriptive and standardized way for applications and screen readers
to communicate. MSAA is available only for Windows operating systems. For more
information on Microsoft Accessibility Technology, visit the Microsoft
Accessibility website at
[www.microsoft.com/enable/default.aspx](https://web.archive.org/web/20101031170653mp_/http://www.microsoft.com/enable/default.aspx).

The Windows ActiveX (Internet Explorer plug‑in) version of Flash Player 6
supports MSAA, but Windows Netscape and Windows stand-alone players do not.
Important: MSAA is currently _not_ supported in the opaque windowless and
transparent windowless modes. (These modes are options in the HTML Publish
Settings panel, available for use with the Windows version of Internet Explorer
4.0 or later, with the Flash ActiveX control.) To make your Flash content
accessible to screen readers, avoid using these modes. Flash Player makes
information about the following types of accessibility objects available to
screen readers that use MSAA.

Dynamic or static text  
The principal property of a text object is its name. To comply with MSAA
conventions, the name is equal to the contents of the text string. A text object
can also have an associated description string. Flash uses the static or dynamic
text immediately above or to the left of an input text field as a label for that
field.

> **Note:** Any text that is a label is _not_ passed to a screen reader, but is
> used as the name of the object that it labels. Labels are never assigned to
> buttons or text fields that have author-supplied names.

Input text fields  
Have a value, an optional name, a description string, and a keyboard shortcut
string. An input text object's name can come from a text object that is above or
to the left of it.

Buttons  
Have a state (pressed or not pressed), support a programmatic default action
that causes the button to depress momentarily, and optionally have a name, a
description string, and a keyboard-shortcut string. Flash uses any text entirely
inside a button as a label for that button.

> **Note:** For accessibility purposes, Flash Player considers movie clips used
> as buttons with button event handlers such as `onPress` to be buttons, not
> movie clips.

Components  
Provide special accessibility implementation.

Movie clips  
Exposed to screen readers as graphic objects when they do not contain any other
accessible objects, or when you use the Accessibility panel to provide a name or
a description for a movie clip. When a movie clip contains other accessible
objects, the clip itself is ignored, and the objects inside it are made
available to screen readers.

> **Note:** All Flash Video objects are treated as simple movie clips.

## Basic accessibility support in Flash Player

By default, the following objects are defined as accessible in all Flash
documents and are included in the information that Flash Player provides to
screen reader software. This generic support for documents that do not use any
accessibility features includes the following:

Dynamic or static text  
Text is transferred to the screen reader program as a name, but with no
description.

Input text fields  
Text is transferred to the screen reader. No names are transferred, except where
a labeling relationship is found for the input text, such as a static text field
positioned close to the input text field. No descriptions or keyboard shortcut
strings are transferred.

Buttons  
The state of the button is transferred to the screen reader. No names are
transferred, except where labeling relationships are found, and no descriptions
or keyboard shortcut strings are transferred.

Documents  
The document state is transferred to the screen reader, but with no name or
description.

## Accessibility for hearing-impaired users

Include captions for audio content that is integral to comprehending the
material. A video of a speech, for example, might require captions for
accessibility, but a quick sound associated with a button probably wouldn't.

Methods to add captions to a Flash document include the following:

- Add text as captions, ensuring that the captions are synchronized with the
  audio in the Timeline.

- Use Hi-Caption Viewer, a component available from Hi Software that works with
  Hi-Caption SE for use with Flash. _Captioning Macromedia Flash Movies with
  Hi-Caption SE_, a white paper, explains how to use Hi-Caption SE and Flash
  together to create a captioned document (see
  [Accesibility White Papers](https://web.archive.org/web/20080411234356/http://www.adobe.com/macromedia/accessibility/whitepapers/)).

## Provide animation accessibility for the visually impaired

You can change the property of an accessible object during SWF file playback.
For example, to indicate changes that take place on a keyframe in an animation.
However, different vendor's screen readers treat new objects on frames
differently. Some screen readers might read only the new object, whereas other
screen readers might re‑read the entire document.

To reduce the chance of causing a screen reader to emit extra "chatter" that can
annoy users, avoid animating the text, buttons, and input text fields in your
document. Also, avoid making your content loop.

Flash Player can't determine the actual text content of features such as Text
Break Apart to animate text. Screen readers can only provide accurate
accessibility to information-carrying graphics such as icons and gestural
animation, if you provide names and descriptions for these objects in your
document or for the entire Flash application. You can also add supplementary
text to your document or shift important content from graphics to text.

1.  Select the object for which you want to change the accessibility properties.

2.  Select Window \> Other Panels \> Accessibility.

3.  Change the properties for the object.

    Alternatively, use ActionScript to update accessibility properties.

## Testing accessible content

When you test your accessible Flash applications, follow these recommendations:

- Download several screen readers and test your application by playing it in a
  browser with the screen reader enabled. Check that the screen reader is not
  attempting to "talk over" places in your document where you inserted separate
  audio. Several screen reader applications provide a demonstration version of
  the software as a free download; test as many screen readers as you can to
  ensure compatibility across screen readers.

- Test interactive content and verify that users can navigate your content
  effectively using only the keyboard. Different screen readers work in
  different ways when processing input from the keyboard; your Flash content
  might not receive keystrokes as you intended. Test all keyboard shortcuts.

More Help topics

[Create a keyboard shortcut to an object for screen readers](./specifying-advanced-accessibility-options-for-screen-readers.md#create-a-keyboard-shortcut-to-an-object-for-screen-readers)

[Using Flash to enter accessibility information for screen readers](./using-flash-to-enter-accessibility-information-for-screen-readers.md)

[Using accessible components](./creating-accessibility-with-actionscript.md#using-accessible-components)

[Creating accessibility with ActionScript](./creating-accessibility-with-actionscript.md)

[Make an entire SWF application accessible](./using-flash-to-enter-accessibility-information-for-screen-readers.md#make-an-entire-swf-application-accessible)
