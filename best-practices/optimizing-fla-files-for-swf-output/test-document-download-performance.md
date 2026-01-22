# Test document download performance

Flash Player attempts to meet the frame rate you set; the actual frame rate
during playback can vary on different computers. If a document that is
downloading reaches a particular frame before the frame's required data is
downloaded, the document pauses until the data arrives.

To view downloading performance graphically, use the Bandwidth Profiler, which
shows how much data is sent for each frame according to the modem speed you
specify.

In simulating the downloading speed, Flash Pro uses estimates of typical
Internet performance, not the exact modem speed. For example, if you select to
simulate a modem speed of 28.8 Kbps, Flash Pro sets the actual rate to 2.3 Kbps
to reflect typical Internet performance. The profiler also compensates for the
added compression support for SWF files, which reduces the file size and
improves streaming performance.

When external SWF files, GIF and XML files, and variables are streamed into a
player by using ActionScript calls such as `loadMovie` and `getUrl`, the data
flows at the rate set for streaming. The stream rate for the main SWF file is
reduced based on the reduction of bandwidth that the additional data requests
cause. Test your document at each speed and on each computer that you plan to
support to ensure that the document doesn't overburden the slowest connection
and computer for which it is designed.

You can also generate a report of frames that are slowing playback and then
optimize or eliminate some of the content in those frames.

To change the settings for the SWF file created using the Test Movie and Test
Scene commands, use File \> Publish Settings.

## Test download performance

1.  Do one of the following:

    - Select Control \> Test Scene or Control \> Test Movie \> Test.

      If you test a scene or document, Flash Pro publishes the current selection
      as a SWF file using the settings in the Publish Settings dialog box. The
      SWF file opens in a new window and begins playing immediately.

    - Select File \> Open, and select a SWF file.

2.  Select View \> Download Settings, and select a download speed to determine
    the streaming rate that Flash Pro simulates. To enter a custom user setting,
    select Customize.

3.  When viewing the SWF file, select View \> Bandwidth Profiler to show a graph
    of the downloading performance.

    The left side of the profiler displays information about the document, its
    settings, its state, and streams, if any are included in the document.

    The right section of the profiler shows the Timeline header and graph. In
    the graph, each bar represents an individual frame of the document. The size
    of the bar corresponds to that frame's size in bytes. The red line beneath
    the Timeline header indicates whether a given frame streams in real time
    with the current modem speed set in the Control menu. If a bar extends above
    the red line, the document must wait for that frame to load.

4.  Select View \> Simulate Download to turn streaming off or on.

    If you turn streaming off, the document starts over without simulating a web
    connection.

5.  Click a bar on the graph to show settings for the corresponding frame in the
    left window and stop the document.

6.  If necessary, adjust the view of the graph by taking one of the following
    actions:

    - Select View \> Streaming Graph to show which frames cause pauses.

      This default view displays alternating light and dark gray blocks that
      represent each frame. The side of each block indicates its relative byte
      size. The first frame stores a symbol's contents, so it is often larger
      than other frames.

    - Select View \> Frame by Frame Graph to display the size of each frame.

      This view helps you see which frames contribute to streaming delays. If
      any frame block extends above the red line in the graph, Flash Player
      stops playback until the entire frame downloads.

7.  Close the test window to return to the authoring environment.

    After you set up a test environment using the Bandwidth Profiler, you can
    open any SWF file directly in the test environment. The file opens in a
    Flash Player window, using the Bandwidth Profiler and other selected viewing
    options.

## Generate a final report

1.  Select File \> Publish Settings, and click the Flash Pro tab.

2.  Select Generate Size Report.

3.  Click Publish.

    Flash Pro generates a text file with the .txt extension. (If the document
    file is myMovie.fla, the text file is myMovie Report.txt.) The report lists
    the size of each frame, shape, text, sound, video and ActionScript script by
    frame.

More Help topics

[Optimize Flash documents](./optimize-flash-documents.md)

[Publishing overview](../../publishing-and-exporting/publishing-flash-documents.md#publishing-overview)

[Debugging ActionScript 1.0 and 2.0](../../actionscript/debugging-actionscript-1.0-and-2.0.md)

[Debugging ActionScript 3.0](../../actionscript/debugging-actionscript-3.0.md)
