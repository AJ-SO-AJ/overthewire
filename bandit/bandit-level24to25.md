# Level 24 -> 25

For this one, there's a server listening to our input on port 30002. The input we need is the previous password + a 4 digit pin. If that combo (pass + pin) is correct, the server will give us the password for the next level and exit.

We need to brute force, i.e., check every combination (10000 possible combinations). Doing this manually would take forever. So we need to write a script.

pass=(replace with password of the previous level)

for i in {0000..9999}; do

    echo "$pass $i"
    
done | nc localhost 30002

