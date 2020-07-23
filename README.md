# asmon

![screenshot](https://raw.githubusercontent.com/tanshoku/asmon/master/asmon.png)

This is a fork of asmon, intended to make it work on systems with over 1000MB of used memory, and add a few options such as ignoring buffers and cache, which are easily free-able memory and thus arguably pointless to be contabilized.

### Installation

```
% cd asmon
% make
# make install 
% asmon & (or asmon -h for help)
```

### Usage

```
-display <display name>
-e cmd	 execute 'cmd' on mouse click
-v	 print the version number
-u	 force asmon to show uptime, rather than X mem use
-b	 don't show buffers
-c	 don't show cached
-s	 don't show shared
-h	 show the help screen
```
