# Working with components in Flash Player

The component framework lets you add functionality to components, but it can
potentially add considerable file size to an application. Components inherit
from each other. One component adds size to your Flash Pro document, but
subsequent components that use the same framework do not necessarily add more
size. As you add components to the Stage, the file size increases, but at some
point, it levels off because components share classes and do not load new copies
of those classes.

If you use multiple components that do not share the same framework, they might
add substantial file size to the SWF file. For example, the XMLConnector
component adds 17K to the SWF file, and TextInput components add 24K to your
document. If you add the ComboBox component, it adds 28K, because it is not part
of the framework of either previous component. Because the XMLConnector
component uses data binding, the classes add 6K to the SWF file. A document that
uses all these components has 77K before you add anything else to the file.
Carefully consider your SWF file size when you add a new component to the
document.

Components must exist in the parent SWF file's library. For example, an
application must have a copy of the components it uses in its library, even if
those components are required only by child SWF files that are loaded at
runtime. This is necessary to ensure that the components function properly, and
slightly increases the download time of the parent SWF file. However, the parent
library isn't inherited or shared in the SWF files that you load into the
parent. Each child SWF file must download to the application with its own copy
of the same components.

When you are planning to publish a SWF file with backward compatibility, you
must have a good understanding of which components have that capability. The
following table provides information about component availability in different
versions of Flash Player:

| Components          | Flash Player 6 (6.0.65.0) and earlier | Flash Player 6 (6.0.65.0) | Flash Player 7 and 8 | Flash Player 9 |
| ------------------- | ------------------------------------- | ------------------------- | -------------------- | -------------- |
| ActionScript 3.0    | Not supported                         | Not supported             | Not supported        | Supported      |
| ActionScript 2.0    | Supported                             | Supported                 | Supported            | Supported      |
| V2 UI component set | Not supported                         | Supported                 | Supported            | Supported      |
| Media components    | Not supported                         | Not supported             | Supported            | Supported      |
| Data components     | Not supported                         | Not supported             | Supported            | Supported      |

Deselect the Optimize for Flash Player 6r65 option in Publish Settings for the
V2 UI components to work.
