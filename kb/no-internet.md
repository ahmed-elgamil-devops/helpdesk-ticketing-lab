# KB: User has no internet

**Steps (bottom up)**
1. Cable or Wi-Fi connected? Other users affected? (One user = the PC; many = the network.)
2. `ipconfig /all`: an address starting with 169.254 means no DHCP answer.
3. `ping <gateway>`, then `ping 8.8.8.8`, then `ping google.com`.
4. IP works but names fail: DNS problem. Check the DNS servers, run `ipconfig /flushdns`, test with `nslookup`.
5. No IP: `ipconfig /release` and `/renew`, check the DHCP scope is not full.
6. Gateway unreachable: check the switch port and VLAN.

**Escalate** with the results of each step if the switch, firewall or ISP link is involved.
