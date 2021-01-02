Execute the command to setup a queue for MITM:
iptables -I FORWARD -j NFQUEUE queue-num 0

You can also use:
iptables -I OUTPUT -j NFQUEUE --queue-num 0 
iptables -I INPUT -j NFQUEUE --queue-num 0 
for your local computer.

Make sure to run iptables --flush when you are done 
