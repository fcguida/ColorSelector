# ColorSelector
Simple HTML/X11 color selector dialog.
This is a single page web app using a javascript include file as an xml data island.

While easy enough to do, it's messy to include the entire color table in the main file,
and there's no easy way to link in or embed an xml file.  You can load one easily enough
using XMLHttpRequest(), but most browsers won't let you load a local file for security reasons.
Chrome will allow it if you launch with the --allow-file-access-from-files option, but it
has to be the first web page launched for this to work.

With a little reformatting (double to single quotes, and javascript newline escapes) you can
create a pseudo xml data island, as done in the XmlColors.js file, that can be included in the
main file.

# Usage
Copy the three files:  ColorSelector.htm, ColorSelector.css, and XmlColors.js to a single
directory and run ColorSelector.htm.

On Windows you can create a shortcut to run this with Chrome as a standard looking app
(simple frame, no tabs, etc).  Just create the shorcut and set the target field as follows,
substituting {$PATH} to point to the location of ColorSelector.htm on your machine:

"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --app="file://{$PATH}\ColorSelector.htm"

# History
In the original version of this app that I wrote many years ago, IE supported Web "apps" or .hta
files that rendered as dhtml and had local file access, ActiveX xml objects and other nice
features to build a local application.  This was before WPF was popular.  HTAs are no longer
supported.
