# Optimizing component styles and performance

When using ActionScript 2.0, one of the most processor-intensive calls in a
component framework is the `setStyle` call. The `setStyle` call executes
efficiently, but the call is intensive because of the way it is implemented. The
`setStyle` call is not always necessary in all applications, but if you use it,
consider its performance effect.

To enhance performance, you can change styles before they are loaded,
calculated, and applied to the objects in your SWF file. If you can change
styles before the styles are loaded and calculated, you do not have to call
`setStyle`.

To improve performance when using styles, set properties on each object as
objects are instantiated. When you dynamically attach instances to the Stage,
set properties in `initObj` in the call that you make to `createClassObject()`,
as the following ActionScript shows:

    createClassObject(ComponentClass, "myInstance", 0, {styleName:"myStyle", color:0x99CCFF});

For instances that you place directly on the Stage, you can use `onClipEvent()`
for each instance, or you can use subclasses (recommended). For information on
subclasses, see About writing a subclass in
[Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html).

If you must restyle your components, you can improve efficiency in your
application by using the Loader component. To implement several styles in
different components, place each component in its own SWF file. If you change
styles on the Loader component and reload the SWF file, the components in the
SWF file are recreated. When the component is recreated, the cache of styles is
emptied, and the style for the component is reset and referenced again.

> **Note:** To apply a single style to all instances of a component in your SWF
> file, change the style globally using `_global.styles.``ComponentName`.
