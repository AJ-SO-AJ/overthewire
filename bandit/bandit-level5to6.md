# Level 5 -> 6
Find the file that's 1033 character long, non executable and human readable.
You can just use find with the size option
find -size 1033c (can also add -type f -not -executable)
then concat it out to standard output (cat file)
