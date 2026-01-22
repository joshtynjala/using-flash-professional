# Best practices - Structuring FLA files

## Organizing timelines and the library

Frames and layers on a timeline show you where assets are placed and determine
how your document works. How a timeline and the library are set up and used
affect the entire FLA file and its overall usability. The following guidelines
help you author content efficiently, and let other authors who use your FLA
documents have a greater understanding of how the document is structured.

- Give each layer an intuitive layer name, and place related assets together in
  the same location. Avoid using the default layer names (such as Layer 1, Layer
  2).

  Clearly describe the purpose or content of each layer or folder when you name
  them.

  If applicable, place your layers that include ActionScript and a layer for
  frame labels at the top of the layer stack in the timeline. For example, name
  the layer that contains your ActionScript actions.

- Use layer folders to group and organize similar layers, to facilitate locating
  the layers that include code and labels.

- Lock layers that you are not using or do not want to modify. Lock your
  ActionScript layer immediately so that symbol instances or media assets are
  not placed on that layer.

- Never put any instances or assets on a layer that includes ActionScript.
  Because this can potentially cause conflicts between assets on the Stage and
  ActionScript that references them, keep all of your code on its own actions
  layer, and lock it after you create it.

- Use frame labels in a FLA file instead of using frame numbers in your
  ActionScript code if you reference frames in your code. If those frames change
  later when you edit the timeline, and you use frame labels and move them on
  the timeline, you do not have to change any references in your code.

- Use library folders.

  Use folders in the library to organize similar elements (such as symbols and
  media assets) in a FLA file. If you name library folders consistently each
  time you create a file, it is easier to remember where you put assets.
  Commonly used folder names are Buttons, MovieClips, Graphics, Assets,
  Components, and, sometimes, Classes.

## Using scenes

Using scenes is similar to using several SWF files to create a larger
presentation. Each scene has a timeline. When the playhead reaches the final
frame of a scene, the playhead progresses to the next scene. When you publish a
SWF file, the timeline of each scene combines into a single timeline in the SWF
file. After the SWF file compiles, it behaves as if you created the FLA file
using one scene. Because of this behavior, avoid using scenes for the following
reasons:

- Scenes can make documents confusing to edit, particularly in multiauthor
  environments. Anyone using the FLA document might have to search several
  scenes within a FLA file to locate code and assets. Consider loading content
  or using movie clips instead.

- Scenes often result in large SWF files.

- Scenes force users to progressively download the entire SWF file, instead of
  loading the assets they actually want to see or use. If you avoid scenes, the
  user can control what content they download as they progress through your SWF
  file. The user has more control over how much content they download, which is
  better for bandwidth management. One drawback is the requirement for managing
  a greater number of FLA documents.

- Scenes combined with ActionScript might produce unexpected results. Because
  each scene timeline is compressed onto a single timeline, you might encounter
  errors involving your ActionScript and scenes, which typically requires extra,
  complicated debugging.

  If you create lengthy animations, you might find it advantageous to use
  scenes. If disadvantages apply to your document, consider using multiple FLA
  files, or movie clips to build an animation instead of using scenes.

## Saving files and version control

When you save your FLA files, use a consistent naming scheme for your documents.
This is particularly important if you save multiple versions of a single
project.

Some problems might occur if you only work with one FLA file and do not save
versions when you create the file. Files might become larger because of the
history that's saved in the FLA file, or become corrupt (as with any software
you use) while you are working on the file.

If you save multiple versions while developing, you have an earlier version
available if you need to revert. Use intuitive names for your files that are
easy to read, not cryptic, and work well online:

- Do not use spaces, capitalization, or special characters.

- Only use letters, numbers, dashes, and underscores.

- If you save multiple versions of the same file, devise a consistent numbering
  system such as menu01.swf, menu02.swf and so on.

- Consider using all lowercase characters in your naming schemes, because some
  server software is case sensitive.

- Consider a naming system that uses a noun-verb or adjective-noun combination
  for naming files, for instance, classplanning.swf and myproject.swf. Use the
  following methods to save new versions of a FLA file when you build an
  extensive project:

- Select File \> Save As, and save a new version of your document.

- Use version control software or the Project panel to control your Flash Pro
  documents.

  If you are not using version control software to create backups of your FLA
  file, use Save As and type a new file name for your document after every
  milestone in your project.

  Many software packages allow users to use version control with their files,
  which enables teams to work efficiently and reduce errors (such as overwriting
  files or working on old versions of a document). As with other documents, you
  can use these programs to organize the Flash Pro documents outside Flash Pro.
