# W.E.D.L
Windows Event Data Logger (pronounced WEEDLE) is an application that uses windows providers to records event logs into many readable formats. WEDL, is customizable in the sense where you can change the default providers, and the file format (TXT, JSON, XML, and CSV) from within the configuration file, or from the application itself.

##Usage
In order to use WEDL, you must first run  WEDL.exe. Commands are passed to WEDL via a command.txt file within the directory of the application. Valid commands are: "start" "pause" "bookmark" "stop" "provider".

### start
 start
will start the event logging cycle with your specified providers and formats (defaults are specified within the config.cfg).
*NOTE: A bookmark is place at the beginning of the events that you recorded by default.

### pause
"pause" will stop the event logging, but will keep the application running, Pausing the logging will also print all the log(in the formats specified within configuration.cfg) to the WEDL\Logs\ directory. 
*Note: All bookmarks made before pausing will remain there, until you delete them, or stop the application.

### bookmark
"bookmark" will save the last recorded file's position, until you quit the program with the "stop" command.
*Note: When you start WEDL after pausing it, logging will continue from where you left off.

### stop
"stop" is what you'll use to safely exit WEDL all together. The stop command, will cleanup WEDL by getting rid of all bookmarks saved, but will create one at the last event logged (this allows you to continue where you left off without having to go through and record the same events again)

### provider
"provider <provider> allows you to add a provider to your event search without having to stop the WEDL program to change the configuration.cfg.

##Formats

### evtx
 -Windows XML event log. A .evtx format allows you to open the event log within Windows Event Viewer
 
### txt
-Text File, a .txt formatm can be opened with notepad or just about any text editor, very easy to read.
 
### csv
-Comma Serperated Values
 
### xml
-Extensible Markup language
 
### json
-Javascript Object Notation
