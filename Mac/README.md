Mac does not have ipset support in dnsmasq. Use a script to monitor dnsmasq results and add route table entries.

1. Setup PPTP VPN. Do not choose "Send all traffic".

2. Install dnsmasq on Mac.

3. Put ip-* scripts under /etc/ppp/. Put router script under the directory where ip-up.local and ip-down.local could find it.

4. Run "router init" to let DNS queries of desired domains go to dnsmasq. Restart dnsmasq.

Then you are good to go. Connect to VPN and take a look at the route table.

TODO: take care of dnsmasq log file with logrotate or something similar.
