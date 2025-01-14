---
title: Marks
author: Jeff
date: 2013-07-05T15:03:27+00:00

---

### Marks ###

Marks are a very useful way to label intersting things in a sequence. They are primarily used for timing tracks and marking the beats of a song. The can be added manually, generated by tools in the sequencer, or imported from various 3rd party sources. Marks primarily show up in the Ruler section of the timeline below the audio track if the sequence includes one. But they can also show up in the Marks Bar.

### Mark Collections ###

Mark collections are now entirely managed in the Mark Collection docker. You can add/remove them, adjust their color, set their appearance and their type from the Mark Collection docker. You can import them from various different formats including Audacity, Papagayo, xTiming and other Vixen users amongst many. They also can be exported in Vixen format.

### Marks Bar ##

The Marks Bar can be enabled per Mark Collection in the Mark Collections docker. All marks have a duration, but it may not be relevant for all usages of marks. The Marks Bar provides additional functionality in the form being able to visualize that duration of the Mark. The primary use for this is for Lip Syncing faces. These marks can have text and that can be used to mark the locations of phrases, words, and phonemes.

### Adding Marks ###

Marks are added via the right click functionality in the ruler. Right click on the spot in the ruler you want the mark to start. A default mark will be added to the active collection. The active collection can be set in the Mark Collections docker by checking the box in the Pencil column next to the collection that should be active. Holding the Control Key while right clicking to add a mark will have it fill the time between the two marks you add it between.  You can add text at the same time the mark is added by holding the *Shift* key while right click to add. Adding the *Control* Key to that additionally will have it fill the gap between two marks.

### Editing Marks ###

Simple Marks can be moved by dragging the Mark indicator in the time ruler to the position your want it. The Mark bar itself allows for editing the marks when the bar for the collection is enabled. You can drag their start and end times or the entire mark in the same way you manage effects in the timeline. Dragging in the middle area of the mark will move the entire mark left or right along the timeline. Dragging the beginning or end of the mark will allow you to move those respective times. You can select multiple marks and then drag them right or left along the timeline as a group by dragging in the middle of one of the marks. Similarly, you can drag the start or end times of all selected ones uniformly by dragging the start or end of one of the marks left or right.  While editing marks alignment marks will be projected up through the audio waveform to assist in alignment.

Holding the Alt key and double clicking on a mark will cause it to expand and fill the time between the mark prior to and after it. Right clicking on the mark will invoke a context menu that allows various functions such as Cut/Copy/Paste, Delete, and Edit of the text. Marks can be Cut / Copied along the timeline and can be pasted across collections. The shortcut keys do not work here at the current moment due to conflicts with the same actions on Effects.

### Controlling Play ###

An additional feature allows the the user to play a section of the sequence by double clicking on a Mark in the Mark Bar. When double clicking a mark, the editor will play the sequence over the range of the mark duration in a single pass and stop at the end. If the Loop function of the sequence is enabled, then that duration will loop until the stop button is clicked. This can be very useful in aligning marks to audio especially when doing lip sync.  The marks can be moved while it is looping, but the section of the sequence that is playing will not reset until the loop is restarted.

### Mark Collection Appearance ###

Each Mark collection can have some attributes set to distinguish it from the others. This can be customized by the user in the Mark Collection docker by right clicking on the Mark Collection name. Here the color, line type and weight can be set. The Solid Line, Bold, and Color all influence how the lines through the timeline look as well as the color of the mark in the Mark Bar. The Weight determines how strong the mark influences the snap to mark feature when aligning effects. See [Snap Points]({{< ref snap-points>}})

### Mark Collection Types ###

There are four types of mark collections.

  1. **Generic** This the basic all purpose type and is used for basic timing marks.
  2. **Phrase** This collection is used to denote marks used as the Phrases for Lip Sync purposes. Each mark should contain the text of a vocal phrase.
  3. **Word** This collection should be used for the broken down words of a Phrase type collection. When using the breakdown function in the Mark Bar on a Phrase type mark, it will break out the words and place them in a Word collection.
  4. **Phoneme** This collection is used as the broken down Phonemes for a word.

### Mark Collection Linking ###

The three collection types that pertain to Lip Sync can be linked to each other to make the association. A word collection should be linked to a parent Phrase collection. A Phoneme collection should be linked to a parent Word collection. This guides the breakdown feature in the Marks Bar on where to put the associated breakdown. Under normal workflows this linking would be done automatically. If you create a Phrase collection first and then break that down into words, it will create an appropriate word collection and link it automatically. The user can edit the linking if necessary on each collection. A collection can only be linked to one parent.

### Mark Tapping ###

Tapping can be accomplished by having a Mark Collection defined in the Mark Collection docker. Then with the collection you want to use marked as active, you can hold the *Shift* key and then hit *Space* where you want marks to be placed while the sequence is playing. Once the marks are added, you can later adjust their positioning within the timeline.

### Beat / Bar Detection ###

Marks for audio beats and bars can be automatically detected on an audio track that has been added to the the sequence in the editor. Under Tools -> Audio -> Beat/Bar detection.  This will bring up a dialog to select the type of marks you want to generate. This uses the Queen Mary VAMP plugins that are commonly used in Audacity to detect beats and bars. The defaults on this dialog are generally adequate. You can choose the name of the mark collection prefix you would like to use. It defaults to Beats. You can choose the colors of the marks by double clicking on the color boxes for each option. You can change them later if you need to. In the Clef you can choose the timing of the music. A lot of music is 4/4 so the default may work for most songs. Otherwise you can change it to what the music is. It does not generally do well with tracks that change signatures. Once you click Generate, it will create Mark Collections for all the options that were selected in the editor. See above for editing the generated collections.

### Mark Import ###

Mark collections can be imported from various other sources. The Import menu on the Mark Collections Docker allows you to choose the source for that import. It can be tracks from Audacity, xTiming from XLights, or from the Singing Faces Project.

### XLights Singing Faces Project Import ###

There is a browser under the import menu on the Marks collection docker to browse the available Singing Face tracks available in the project. In many cases that includes information about the audio track that was used to make them. When importing, these will create the Phrases, Words, and Phonemes.

### Audacity ###

Audacity can create a label track that includes the beats (and other things) in a song. Vixen has the capability to import these labels.

Audacity can use various plugins to analyze music and has basic beat detection built in. If you want more advanced beat detection, you can download other plugins for use with Audacity. I have used the Vamp plugins with some success. You can download them here for use in Audacity: <http://www.vamp-plugins.org/>.