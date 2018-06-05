# Monitoring traffic using tcpdump
To monitor traffic on a given port:

`tcpdump -A -s 0 port 514 -v`

The s flag indicates the maximum packet size to show - 0 is unlimited.

#linux #networking