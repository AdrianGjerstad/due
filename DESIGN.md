# Design

The user interface of Due is designed to allow users to quickly glance at and
see what they have coming up in the near future, as well as a look at how busy
their week/month is. To do this, there are two "panes" to the UI.

## Calendar View

The top pane is a color-coded day-by-day calendar view. This view can be either
of a traditional month-long calendar with seven columns for days in a week and
several rows for weeks, or it can be a single week reprensented by seven
columns.

Each day is represented as a rectangle with a number in the top-left corner, and
a number of events for that day. These rectangles are almost never going to be
big enough to show the names or descriptions of events, so this is the best that
can be done. In addition, the current day is highlighted for ease of glancing.

## Agenda View

This pane is the meat of Due. It displays a chronological list of events coming
up soon. Each event is prepended with a time represented using the preferred
format, and followed by the name of the event itself. Below this line can be any
amount of information that the user wished to attach to the event. An example
event list in Due may look something like this:

<pre>
June 14th                                                    <font color="#61afef">▼ 1 day</font>

  <font color="#e06c75"> 9:30 AM</font>  <b>Finalize slideshow</b>
            <font color="#7f7f7f">tag:work</font>

  <font color="#e06c75">10:00 AM</font>  <b>Attend meeting</b>
            Presentation about AI
            <font color="#7f7f7f">tag:work  📍Office</font>

  <font color="#e06c75"> 5:00 PM</font>  <b>Send hand-off and go home</b>
            <font color="#7f7f7f">tag:work</font>

  <font color="#e06c75"> 7:30 PM</font>  <b>Concert</b>
            <font color="#7f7f7f">📍Downtown Theatre, 101 Drama Way, City, State, ZIP</font>
</pre>

Navigation around this pane is done using Vim-style keybindings.

- `j` - Next event
- `k` - Previous event
- `i` - Insert new event before current event
- `a` - Insert new event after current event
- `R` - Edit current event
- `d` - Cut the current event
- `y` - Copy the current event
- `p` - Paste the current event
- `u` - Undo the previous action
- `C-r` - Redo an action

