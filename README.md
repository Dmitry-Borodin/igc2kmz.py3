igc2kmz IGC to Google Earth converter. Python3 version.
=====================================

igc2kmz converts paraglider and hang glider track logs into Google Earth KML format with lots of features, notably:

* track colored by altitude, climb rate, ground speed and total energy
* shadow feature makes it easier to judge the track's altitude by eye
* animation of the flight
* photos automatically placed where they were taken and with an optional comment
* XC optimisation output
* altitude graph and high and low points labelled
* thermal and glide analysis
* time marks

It's used by the following XC league servers:

* [Leonardo](http://www.paraglidingforum.com/leonardo)
* [UK National XC League](http://www.uknxcl.org.uk/)

Just upload your flight to one of these and you can download your flight in Google Earth format without having to install any extra software on your computer.

It is designed to run on XC league servers, and as such is not designed to be directly used by pilots.


Requirements
------------

* [Python](http://www.python.org/) version 3.

Run it
------

Change to the directory where you unpacked the archive and run:

	bin/igc2kmz.py -i <input-filename>.igc -o <output-filename>.kmz


Customise it
------------

You can set various parameters via the command line, including the time zone offset in hours relative to UTC. For example, use `-z 2` for Central European Time during the summer. For individual flights you can override the pilot name and glider type (otherwise they are taken from the IGC file), set the line color and width, add optimized XC information and photos with comments. Run `bin/igc2kmz.py --help` for a full list of options. For example use, look at the Makefile.

Rebuild the examples
--------------------

You can rebuild the example files with the command `make examples`. This will build the `olc2002` flight optimizer, optimize a number of flights, and create the KMZ files in the examples/ subdirectory. Be warned that the flight optimization step can take a long time (30 minutes on a 2.4GHz Core 2 Duo).
