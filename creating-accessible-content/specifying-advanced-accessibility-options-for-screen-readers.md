# Specifying advanced accessibility options for screen readers

## Turn off automatic labeling and specify an object name for screen readers

1.  On the Stage, select the button or input text field for which you want to
    control labeling.
2.  Select Window \> Other Panels \> Accessibility.
3.  Select Make Object Accessible (the default setting).
4.  Enter a name for the object. The name is read as the label for the button or
    text field.
5.  To turn off accessibility for the automatic label (and hide it from screen
    readers), select the text object on the Stage.
6.  If the text object is static text, convert it to dynamic text (in the
    Property inspector, select Text type \> Dynamic Text).
7.  Deselect Make Object Accessible.

## Hide an object from the screen reader

You can hide a selected object from screen readers, and you can decide to hide
accessible objects that are contained inside a movie clip or Flash application
and expose only the movie clip or Flash application to screen readers.

> **Note:** Only hide objects that are repetitive or convey no content.

When an object is hidden, the screen reader ignores the object.

1.  On the Stage, select the button or input text field to hide from the screen
    reader.
2.  Select Window \> Other Panels \> Accessibility.
3.  In the Accessibility panel, do one of the following:

    - If the object is a movie clip, button, text field, or another object,
      deselect Make Object Accessible.

    - If the object is the child of a movie clip, deselect Make Child Objects
      Accessible.

## Create a keyboard shortcut to an object for screen readers

You can create a keyboard shortcut for an object, such as a button, so users can
navigate to it without listening to the contents of an entire page. For example,
you can create a keyboard shortcut to a menu, a toolbar, the next page, or a
submit button.

To create a keyboard shortcut, write ActionScript code for an object. If you
provide a keyboard shortcut for an input text field or button, you must also use
the ActionScript Key class to detect the key the user presses during Flash
content playback. See Key in the _ActionScript 2.0 Language Reference_. See
Capturing keypresses in _Learning ActionScript 2.0 in Adobe Flash_ at
[www.adobe.com/go/learn_cs5_learningas2_en](https://web.archive.org/web/20110128165312mp_/http://www.adobe.com/go/learn_cs5_learningas2_en).

Select the object and add the name of the keyboard shortcut to the Accessibility
panel so the screen reader can read it.

Test your Flash content with multiple screen readers. Keyboard shortcut
functionality also depends on the screen reader software used. The key
combination Control+F, for example, is a reserved keystroke for both the browser
and the screen reader. The screen reader reserves the arrow keys. Generally, you
can use the 0 to 9 keys on the keyboard for keyboard shortcuts, however, screen
readers increasingly use even these keys.

### Create a keyboard shortcut

1.  On the Stage, select the button or input text field to create a keyboard
    shortcut for.
2.  Select Window \> Other Panels \> Accessibility.
3.  In the Shortcut field, type the name of the keyboard shortcut, using the
    following conventions:

    - Spell out key names, such as Control or Alt.

    - Use capital letters for alphabetic characters.

    - Use a plus sign (+) between key names, with no spaces (for example,
      Control+A).

Important: Flash does not check that the ActionScript to code the keyboard
shortcut was created.

### Map a keyboard shortcut to a button instance Control+7 to myButton instance

1.  Select the object on the Stage, display the Accessibility panel, and in the
    Shortcut field, type the key combination of the shortcut. For example,
    `Control+7`.

2.  Enter the following ActionScript 2.0 code in the Actions panel:

    > **Note:** In this example the shortcut is Control+7.

        function myOnPress() {
            trace( "hello" );
        }
        function myOnKeyDown() {
            if (Key.isDown(Key.CONTROL) && Key.getCode() == 55) // 55 is key code for 7
            {
                Selection.setFocus(myButton);
                myButton.onPress();
            }
        }
        var myListener = new Object();
        myListener.onKeyDown = myOnKeyDown;
        Key.addListener(myListener);
        myButton.onPress = myOnPress;
        myButton._accProps.shortcut = "Ctrl+7"
        Accessibility.updateProperties();

> **Note:** The example assigns the Control+7 keyboard shortcut to a button with
> an instance name of myButton and makes information about the shortcut
> available to screen readers. In this example, when you press Control+7, the
> `myOnPress` function displays the text "hello" in the Output panel. See
> addListener (IME.addListener method) in ActionScript 2.0 Language Reference at
> [www.adobe.com/go/learn_cs5_as2lr_en](https://web.archive.org/web/20110128165312mp_/http://www.adobe.com/go/learn_cs5_as2lr_en).

More Help topics

[Testing accessible content](./about-accessible-content.md#testing-accessible-content)
