# Creating accessibility with ActionScript

[Add your comment and rating](#ionCTAAnchor)

## About ActionScript and accessibility

You can create accessible documents with ActionScript® code. For accessibility
properties that apply to the entire document, you can create or modify a global
variable called `_accProps`. See the `_accProps` property in
[_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

For properties that apply to a specific object, you can use the syntax
`instancename._accProps`. The value of `_accProps` is an object that can include
any of the following properties:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Property</p></th>
<th><p>Type</p></th>
<th><p>Equivalent selection in the Accessibility panel</p></th>
<th><p>Applies to</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>.<samp>silent</samp></p></td>
<td><p>Boolean</p></td>
<td><p>Make Movie Accessible/Make Object Accessible (inverse
logic)</p></td>
<td><p>Entire documents</p>
<p>Buttons</p>
<p>Movie clips</p>
<p>Dynamic text</p>
<p>Input text</p></td>
</tr>
<tr class="even">
<td><p><samp>.forceSimple</samp></p></td>
<td><p>Boolean</p></td>
<td><p>Make Child Objects Accessible (inverse logic)</p></td>
<td><p>Entire documents</p>
<p>Movie clips</p></td>
</tr>
<tr class="odd">
<td><p><samp>.name</samp></p></td>
<td><p>string</p></td>
<td><p>Name</p></td>
<td><p>Entire documents</p>
<p>Buttons</p>
<p>Movie clips</p>
<p>Input text</p></td>
</tr>
<tr class="even">
<td><p><samp>.description</samp></p></td>
<td><p>string</p></td>
<td><p>Description</p></td>
<td><p>Entire documents</p>
<p>Buttons</p>
<p>Movie clips</p>
<p>Dynamic text</p>
<p>Input text</p></td>
</tr>
<tr class="odd">
<td><p><samp>.shortcut</samp></p></td>
<td><p>string</p></td>
<td><p>Shortcut</p></td>
<td><p>Buttons</p>
<p>Movie clips</p>
<p>Input text</p></td>
</tr>
</tbody>
</table>

> **Note:** With inverse logic, a value of `true` in ActionScript corresponds to
> a check box that is not selected in the Accessibility panel, and a value of
> `false` in ActionScript corresponds to a selected check box in the
> Accessibility panel.

Modifying the `_accProps` variable has no effect by itself. You must also use
the `Accessibility.updateProperties` method to inform screen reader users of
Flash content changes. Calling the method causes Flash Player to re‑examine all
accessibility properties, update property descriptions for the screen reader,
and, if necessary, send events to the screen reader that indicate changes have
occurred.

When updating accessibility properties of multiple objects at once, include only
a single call to `Accessiblity.updateProperties` (too frequent updates to the
screen reader can cause some screen readers to become too verbose).

See the `Accessibility.updateProperties` method in the
[_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

## Implementing screen reader detection with the Accessibility.isActive() method

To create Flash content that behaves in a specific way if a screen reader is
active, use the `Accessibility.isActive()` ActionScript method, which returns a
value of `true` if a screen reader is present, and `false` otherwise. You can
then design your Flash content to perform so that it's compatible with screen
reader use (for example, by hiding child elements from the screen reader). For
more information, see the `Accessibility.isActive` method in the
[_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

For example, you could use the `Accessibility.isActive()` method to decide
whether to include unsolicited animation. Unsolicited animation happens without
the screen reader doing anything, which can be confusing for screen readers.

The `Accessibility.isActive()` method provides asynchronous communication
between the Flash content and Flash Player; a slight real-time delay can occur
between the time the method is called and the time when Flash Player becomes
active, returning an incorrect value of `false`. To ensure that the method is
called correctly, do one of the following:

- Instead of using the` Accessibility.isActive()` method when the Flash content
  first plays, call the method whenever you need to make a decision about
  accessibility.

- Introduce a short delay of one or two seconds at the beginning of your
  document to give the Flash content enough time to contact Flash Player.

  For example, you can use an `onFocus` event to attach this method to a button.
  This approach generally gives the SWF file enough time to load and you can
  assume a screen reader user will tab to the first button or object on the
  Stage.

## Use ActionScript to create a tab order for accessible objects

To create the tab order with ActionScript® code, assign the `tabIndex` property
to the following objects:

- Dynamic text

- Input text

- Buttons

- Movie clips, including compiled movie clips

- Timeline frames

- Screens

Provide a complete tab order for all accessible objects. If you create a tab
order for a frame and you don't specify a tab order for an accessible object in
the frame, Flash Player ignores all the custom tab-order assignments.
Additionally, all objects assigned to a tab order, except frames, must have an
instance name specified in the Instance Name text field of the Property
inspector. Even items that are not tab stops, such as text, need to be included
in the tab order if they are to be read in that order.

Because static text cannot be assigned an instance name, it cannot be included
in the list of the `tabIndex` property values. As a result, a single instance of
static text anywhere in the SWF file causes the reading order to revert to the
default.

To specify a tab order, assign an order number to the `tabIndex` property, as
the following example shows:

    _this.myOption1.btn.tabIndex = 1
    _this.myOption2.txt.tabIndex = 2

See `tabIndex`in `Button`, `MovieClip`, and `TextField` in the
[_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

You can also use the `tabChildren()` or `tabEnabled()` methods to assign custom
tab order. See `MovieClip.tabChildren`, `MovieClip.tabEnabled`, and
`TextField.tabEnabled` in the
[_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

## Using accessible components

A core set of UI components accelerates building accessible applications. These
components automate many of the most common accessibility practices related to
labeling, keyboard access, and testing and help ensure a consistent user
experience across rich applications. Flash includes the following set of
accessible components:

- SimpleButton

- CheckBox

- RadioButton

- Label

- TextInput

- TextArea

- ComboBox

- ListBox

- Window

- Alert

- DataGrid

Accessible Flash components must contain ActionScript that defines their
accessible behavior. For information on which accessible components work with
screen readers, see the
[Flash Accessibility web page](https://web.archive.org/web/20101005081148/http://www.adobe.com/accessibility/products/flash//).

For general information about components, see "About Components" in _Using
ActionScript 2.0 Components_.

For each accessible component, enable the accessible portion of the component
with the `enableAccessibility()` command. This command includes the
accessibility object with the component as the document is compiled. Because no
simple way exists to remove an object after it is added to the component, these
options are disabled by default. Therefore, it's important that you enable
accessibility for each component. Perform this step only once for each
component; you do not need to enable accessibility for each instance of a
component for a given document. See "Button component", "CheckBox component",
"ComboBox component", "Label component", "List component", "RadioButton
component", and "Window component" in the
[_ActionScript 2.0 Components Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

More Help topics

[Create a tab-order index for keyboard navigation in the Accessibility panel](./using-flash-to-enter-accessibility-information-for-screen-readers.md#create-a-tab-order-index-for-keyboard-navigation-in-the-accessibility-panel)
