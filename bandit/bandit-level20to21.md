# Level 20 to 21

The setuid binary in the homedirectory makes a connection to localhost with a port that you specify as an argument. It then reads a line of text from the connection and compares it to the password of the previous level. If the password is correct it will give you the password for the next level.

The binary makes a connection that READS from text. Meaning: It's a client that connects to a server.

Solution: You need to open a server/listener on a port so that the binary can connect to it.

nc -l localhost port (creates a listener). Catch: Ports below 1024 are privileged (only root can bind to them), so you either start the listener on a port higher than 1024, or use special privilege.

You need a new terminal/session to be able to do this, as you need one terminal to create the listener. Another terminal to use the suconnect setuid binary. tmux, screen, etc.

So I created one on 1025. Connected ./suconnect 1025

Then I thought I have to send it from suconnect, but I needed to send it from the nc listener (server). If it's the correct, suconnect sends the password of the next level.
