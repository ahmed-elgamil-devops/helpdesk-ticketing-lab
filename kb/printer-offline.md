# KB: Network printer shows offline

**Steps**
1. Check the printer screen for errors (paper, toner, jam) and that it is on the network.
2. Print a configuration page and note its IP address.
3. From the user's PC: `ping <printer IP>`.
4. If the IP changed, add a DHCP reservation for the printer's MAC address and update the printer port on the PC or print server.
5. Restart the Print Spooler service: `Restart-Service Spooler`.
6. Clear stuck jobs in the queue and print a test page.

**Escalate** if the printer has a hardware fault: log it with the vendor and note the serial number.
