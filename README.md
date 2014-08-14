gparse
======

A simple (limited), dependency-free gcode parser for use in reprap-style 3d printers.

gparse was designed for the Printipi project (https://github.com/Wallacoloo/printipi). It takes input from a file-like object (.gcode file, stdin, or serial port) and parses each line into a Command object. 

gparse does not manage any of the state associated with gcode commands (eg unit modes or relative/absolute coordinates), rather it just parses the opcode and parameters for each command and allows one to return a response.

Limitations
======

gparse doesn't currently support the parsing of comments (causes a crash). Also, checksums are parsed, but not checked.
Note, it is currently not buildable without the printip logging.h file (this will be fixed).
