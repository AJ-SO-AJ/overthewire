# Level 11 -> 12

cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

Feed data.txt into tr

tr is used to translate chars from one set to another. We translate A-Za-z (upper and lower case chars) into 'N-ZA-Mn-za-m'

a-z is abcdefghijklmnopqrstuvwxyz, n-za-m is nopqrstuvwxyzabcdefghijklm
