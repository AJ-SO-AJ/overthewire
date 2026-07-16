# Level 12 -> 13

Password is stored in data.txt which is a hexdump of a file that has been repeatedly compressed.

So we need to undo that?

If you reverse hexdump, you get the file that has been repeatedly compressed. If you decompress, you get og file?

So I reverse hexdump using xxd -r

Then I checked the file type of the result, it was a heavily compressed gzip originally called data2.bin, I renamed it to data2.gz, used gzip -d to decompress

This turned it into a bzip2 compressed data.

I used bzip2 -d to decompress that, it gave me data2.out (another gzip, originally data4.bin)

Renamed it to data4.gz

Gave me data4, a POSIX tar archive (GNU). Renamed to data4.tar

Extracted using tar -x -f data4.tar

Gave me data5.bin, another POSIX tar, gave me data6.bin (bzip2)

bzip2 decompressed it to data6.bzip2.out, another POSIX tar. Gave me data8.bin (gzip that was data9.bin)

gzip decompressed, gave me data9, finally an ASCII text.
