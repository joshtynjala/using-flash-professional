# Working with scenes

To organize a document thematically, you can use scenes. For example, you might
use separate scenes for an introduction, a loading message, and credits. Though
using scenes has some disadvantages, there are some situations in which few of
these disadvantages apply, such as when you create lengthy animations. When you
use scenes, you avoid having to manage a large number of FLA files because each
scene is contained within a single FLA file.

Using scenes is similar to using several FLA files together to create a larger
presentation. Each scene has a Timeline. Frames in the document are numbered
consecutively through the scenes. For example, if a document contains two scenes
with ten frames each, the frames in Scene 2 are numbered 11–20. The scenes in
the document play back in the order they are listed in the Scene panel. When the
playhead reaches the final frame of a scene, the playhead progresses to the next
scene.

#### Disadvantages of scenes

When you publish a SWF file, the Timeline of each scene combines into a single
Timeline in the SWF file. After the SWF file compiles, it behaves as if you
created the FLA file using one scene. Because of this behavior, scenes have some
disadvantages:

- Scenes can make documents confusing to edit, particularly in multi-author
  environments. Anyone using the FLA document might have to search several
  scenes within a FLA file to locate code and assets. Consider loading external
  SWF content or using movie clips instead.

- Scenes often result in large SWF files. Using scenes encourages you to place
  more content in a single FLA file, which results in larger FLA files and SWF
  files.

- Scenes force users to progressively download the entire SWF file, even if they
  do not plan or want to watch all of it. If you avoid scenes, users can control
  what content they download as they progress through your SWF file.

- Scenes combined with ActionScript might produce unexpected results. Because
  each scene Timeline is compressed onto a single Timeline, you might encounter
  errors involving your ActionScript and scenes, which typically require extra,
  complicated debugging.

#### Controlling scene playback

To stop or pause a document after each scene, or to let users navigate the
document in a nonlinear fashion, you use ActionScript. For more information see,
[ActionScript](./timelines-and-actionscript.md).

## Display the Scene panel

![](../img/dingbat.png) Select Window \> Other Panels \> Scene.

## Add a scene

![](../img/dingbat.png) Select Insert \> Scene, or click the Add Scene
button ![](../img/new_layer.png) in the Scene panel.

## Delete a scene

![](../img/dingbat.png) Click the Delete Scene button ![](../img/Trashcan.png)
in the Scene panel.

## Change the name of a scene

![](../img/dingbat.png) Double-click the scene name in the Scene panel and enter
the new name.

## Duplicate a scene

![](../img/dingbat.png) Click the Duplicate Scene
button ![](../img/duplicate_scene.png) in the Scene panel.

## Change the order of a scene in the document

![](../img/dingbat.png) Drag the scene name to a different location in the Scene
panel.

## View a particular scene

![](../img/dingbat.png) Do one of the following:

- Select View \> Go To, and then select the name of the scene from the submenu.

- Click on the Edit Scene button at the upper right corner of the document
  window and choose the scene name from the pop-up menu.
