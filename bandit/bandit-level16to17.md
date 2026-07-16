# Level 16 -> 17
In port range between 31000 and 32000, you will send the current password to receive the password for the next level. Find which ports have a server listening. Then find which one accepts SSL/TLS. Only 1 server will give you the password.

I used nmap to scan the ports in the given range.

nmap -v localhost -p31000-32000

31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Then I didn't know if there's a way to automate checking the ports for SSL/TLS, so I went through them manually. Found out that two listen, 31518 and 31790.

31518 gives nothing while 31790 gives KEYUPDATE when I enter the current password

I used the flag -ign_eof and it worked (dunno if this is a good thing to do though). I got credentials:
