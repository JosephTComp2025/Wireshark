# Lifecycle-OF-A-TCP
This case file demonstrates aTCP conversation within a packet capture I had today. This artifact provides: the initial TCP handhshake, data transfers and the TCP teardown.

Packet Breakdown:
Packet # 36 with a sequence# 2105497879 provides a SYN flag from the client side from the ephemeral port 47378 to the destinaton port of 443 (HTTPS) of the Server side.
The Server side sends a SYN/ACK flag on packet 37 with a sequence # 3918335373 and an Aknowledgement #: 2105497880. Then on Packet 40 the client confirms with an ACK flag with an Acknowledgment #: 3818335374. The connection is established.
On packets 44, 49 and 51 are packets that consist of ack flags that appear in the payload exchange.
Packet 62 the client sents a FIN,ACK flag with sequence #: 2105499986 and acknowledgment#: 3918339362. 
Packet 67 the server then sendsa FIN,ACK flag to end the connection with an aknwoledgement# 2105499987.

Why it matters
The TCP handshake is the foundation of all TCP communication
Detection relevance: abnormal handshakes may indicate scanning or spoofing
Incomplete teardowns can indicate resets, DoS, or abnormal terminations.
