# Level 8 to 9

Find the line that is unique (doesnt repeat).

Commands: sort, uniq

uniq -u gives unique line, but the catch is that it only compares adjacent lines.

sort sorts the lines alphabetically, so it puts the repeats adjacent.

Pipe the output of sort into uniq.

sort data.txt | uniq -u
