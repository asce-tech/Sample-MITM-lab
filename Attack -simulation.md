-> Before we start the process, make sure all the machines are communicating with each other. 
    ```bash
     ping "machine ip"
    ```
- Start Ettercap on the Attacker machine
     ```bash
     sudo ettercap -G
     ```
- Scan for hosts:
   - In ettercap GUI, go to Sinff -> Unified sniffing -> choose the network interface
   - Verify and scan for hosts
   - Go to Hosts -> hosts list
- Select targets:
   - Select ubuntu and windows as Target 1
   - Select Linux as Target 2
- Begin ARP Poisoning:
   - Click Globe icon -> MITM -> ARP poisoning
   - Select "Sniff remote connections."
   - Start Attack
- Verify:
   - Run the ARP command
     ```bash
     arp -a
     ```
   - You should see the MAC address pointing to the attacker's MAC instead of the actual target
- Monitor Traffic:
   - Open Wireshark
   - Start capturing 
   - Use a filter
      ```bash
         arp || ip.addr == 192.168.X.X   # replace with actual IP's
      ```

-> Observations
   - Ping between machines
   - Observe Ping latency, which indicates packet redirection
   - Analyze traffic in Wireshark
   - Check Duplicate connection warnings It confirms MITM setup
     
  
  
  
