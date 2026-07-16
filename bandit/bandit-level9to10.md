# Level 9 -> 10

There's a few human readable strings inside data.txt, the password is preceded by several "=" characters.

data.txt is a data file, not an ASCII string text.

Commands: strings, grep

strings gives the human readable strings of a data/binary file. Pipe that into grep finding pattern "="

strings data.txt | grep "-"
