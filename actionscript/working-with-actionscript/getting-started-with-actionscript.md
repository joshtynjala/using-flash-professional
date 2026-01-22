# Getting started with ActionScript

The ActionScript® scripting language lets you add complex interactivity,
playback control, and data display to your application. You can add ActionScript
in the authoring environment by using the Actions panel, Script window, or an
external editor.

ActionScript follows its own rules of syntax, reserved keywords, and lets you
use variables to store and retrieve information. ActionScript includes a large
library of built‑in classes that let you create objects to perform many useful
tasks. For more information on ActionScript, see the following Help titles:

- [Learning ActionScript 3.0](http://help.adobe.com/en_US/as3/learn/index.html)

- [ActionScript 3.0 Developer's Guide](http://help.adobe.com/en_US/as3/dev/index.html)

- [ActionScript 3.0 Language and Components Reference](https://help.adobe.com/en_US/FlashPlatform/reference/actionscript/3/index.html)

- [Learning ActionScript 2.0 in Adobe Flash](http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)

- [ActionScript 2.0 Language Reference](https://open-flash.github.io/mirrors/as2-language-reference/index.html)

You don't need to understand every ActionScript element to begin scripting; if
you have a clear goal, you can start building scripts with simple actions.

ActionScript and JavaScript are both rooted in the ECMA-262 standard, the
international standard for the ECMAScript scripting language. For this reason,
developers who are familiar with JavaScript should find ActionScript immediately
familiar. For more information about ECMAScript, go to ecma-international.org.

#### ActionScript versions

Flash includes more than one version of ActionScript to meet the needs of
different kinds of developers and playback hardware. ActionScript 3.0 and 2.0
_are not_ compatible with each other.

- ActionScript 3.0 executes extremely fast. This version requires somewhat more
  familiarity with object-oriented programming concepts than the other
  ActionScript versions. ActionScript 3.0 is fully compliant with the ECMAScript
  specification, offers better XML processing, an improved event model, and an
  improved architecture for working with onscreen elements. FLA files that use
  ActionScript 3.0 cannot include earlier versions of ActionScript.

- ActionScript 2.0 is simpler to learn than ActionScript 3.0. Although Flash
  Player runs compiled ActionScript 2.0 code slower than compiled ActionScript
  3.0 code, ActionScript 2.0 is still useful for many kinds of projects that are
  not computationally intensive; for example, more design-oriented content.
  ActionScript 2.0 is also based on the ECMAScript spec, but is not fully
  compliant.

- ActionScript 1.0 is the simplest form of ActionScript, and is still used by
  some versions of the Flash Lite Player. ActionScript 1.0 and 2.0 can coexist
  in the same FLA file.

- Flash Lite 2.x ActionScript is a subset of ActionScript 2.0 that is supported
  by Flash Lite 2.x running on mobile phones and devices.

- Flash Lite 1.x ActionScript is a subset of ActionScript 1.0 that is supported
  by Flash Lite 1.x running on mobile phones and devices.

#### Using the ActionScript documentation

Because there are multiple versions of ActionScript (2.0 and 3.0), and multiple
ways of incorporating it into your FLA files, there are several different ways
to learn ActionScript.

This chapter describes the graphical user interface for working with
ActionScript. This interface includes the Actions panel, Script window, Script
Assist mode, Behaviors panel, Output panel, and Compiler Errors panel. These
topics apply to all versions of ActionScript.

Other ActionScript documentation from Adobe will help you learn about the
individual versions of ActionScript; see _Programming ActionScript 3.0_,
_Learning ActionScript 2.0 in Adobe Flash_, _Developing Flash Lite 1.x
Applications_ or _Developing Flash Lite 2.x Applications_. For information about
the ActionScript vocabulary, see the _ActionScript Language Reference_ for the
version you are working with.

## Adobe recommends

The following **articles and tutorials** provide additional detailed information
about working with ActionScript:

- [Introduction to ActionScript 3.0](https://web.archive.org/web/20111025171038/http://slekx.com/as3-intro/)
  (Slekx.com)

- [Tips for learning ActionScript 3](https://web.archive.org/web/20110820021354mp_/http://www.adobe.com/devnet/actionscript/articles/actionscript_tips.html)
  (Adobe.com)

- [Introduction to event handling in ActionScript 3](https://web.archive.org/web/20110820021354mp_/http://www.adobe.com/devnet/actionscript/articles/event_handling_as3.html)
  (Adobe.com)

- [ActionScript 3.0 Migration Resources for Flash](https://web.archive.org/web/20110820021354mp_/http://www.adobe.com/devnet/actionscript/migration.html)
  (Adobe.com)

- [Migrating to ActionScript 3: Key concepts and changes](https://web.archive.org/web/20110820021354mp_/http://www.adobe.com/devnet/flash/articles/first_as3_application.html)
  (Adobe.com)

- [Top five misperceptions about ActionScript 3](https://web.archive.org/web/20110820021354mp_/http://www.adobe.com/devnet/actionscript/articles/as3_misperceptions.html)
  (Adobe.com)

- [ActionScript 3 migration cookbook](https://web.archive.org/web/20110820021354mp_/http://www.adobe.com/devnet/actionscript/cookbook/)
  (Adobe.com)

- [ActionScript 3 migration table](https://web.archive.org/web/20100115142701/http://www.adobe.com/devnet/actionscript/as3_migration_table.html)
  (Adobe.com)

- [Flash and ActionScript components learning guide](https://web.archive.org/web/20110820021354mp_/http://www.adobe.com/devnet/flash/articles/components_guide.html)
  (Adobe.com)

- [Flash ActionScript 2.0 Learning Guide](https://web.archive.org/web/20110820021354mp_/http://www.adobe.com/devnet/flash/articles/actionscript_guide.html)
  (Adobe.com)

#### Ways of working with ActionScript

There are several ways to work with ActionScript.

- Script Assist mode lets you add ActionScript to your FLA file without writing
  the code yourself. You select actions, and the software presents you with a
  user-interface for entering the parameters required for each one. You must
  know a little about what functions to use to accomplish specific tasks, but
  you don't have to learn syntax. Many designers and non-programmers use this
  mode.

- Behaviors also let you add code to your file without writing it yourself.
  Behaviors are prewritten scripts for common tasks. You can add a behavior and
  then easily configure it in the Behaviors panel. Behaviors are available only
  for ActionScript 2.0 and earlier.

- Writing your own ActionScript gives you the greatest flexibility and control
  over your document, but it requires you to become familiar with the
  ActionScript language and conventions.

- Components are prebuilt movie clips that help you implement complex
  functionality. A component can be a simple user interface control, such as a
  check box, or it can be a complicated control, such as a scroll pane. You can
  customize a component's functionality and appearance, and you can download
  components created by other developers. Most components require you to write
  some ActionScript code of your own to trigger or control a component. For more
  information, see
  [Using ActionScript 3.0 Components](https://web.archive.org/web/20110816072725/http://help.adobe.com/en_US/as3/components/index.html).

#### Writing ActionScript

When you write ActionScript code in the authoring environment, you use the
Actions panel or Script window. The Actions panel and Script window contain a
full-featured code editor that includes code hinting and coloring, code
formatting, syntax highlighting, syntax checking, debugging, line numbers, word
wrapping, and support for Unicode.

- Use the Actions panel to write scripts that are part of your Flash document
  (that is, scripts that are embedded in the FLA file). The Actions panel
  provides features such as the Actions toolbox, which gives you quick access to
  the core ActionScript language elements, and Script Assist mode, in which you
  are prompted for the elements needed to create scripts.

- Use the Script window if you want to write external scripts—that is, scripts
  or classes that are stored in external files. (You can also use a text editor
  to create an external AS file.) The Script window includes code-assistance
  features such as code hinting and coloring, syntax checking, and
  auto-formatting.

More Help topics

[Symbols and ActionScript](../../symbols-instances-and-library-assets/symbols-and-actionscript.md)

[Timelines and ActionScript](../../timelines-and-animation/timelines-and-actionscript.md)

[Sound and ActionScript](../../sound/sound-and-actionscript.md)

[Controlling external video playback with ActionScript](../../video/controlling-external-video-playback-with-actionscript.md#controlling-external-video-playback-with-actionscript)

[Multilanguage text and ActionScript](../../text/multilanguage-text.md#multilanguage-text-and-actionscript)

[Creating accessibility with ActionScript](../../creating-accessible-content/creating-accessibility-with-actionscript.md)

[Organizing ActionScript in an application](../../best-practices/organizing-actionscript-in-an-application.md)

[Debugging ActionScript 1.0 and 2.0](../debugging-actionscript-1.0-and-2.0.md)

[Debugging ActionScript 3.0](../debugging-actionscript-3.0.md)

[Script Assist mode and behaviors](../script-assist-mode-and-behaviors.md)
