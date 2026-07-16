# Level 15 -> 16

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

I assume we will do another nc message sending but let's see how we send it through SSL/TLS encryption.

So upon reading, you can connect using openssl.

openssl s_client -connect localhost:30001
