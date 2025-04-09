-> Step-1: Creating Virtual Machines (VMs)

- Download OS images:
   - Ubuntu
   - Kali Linux
   - Windows
- Create new VMs:
- Install the OS:

→ Step-2: Network Settings

- In VM settings, go to Network
- Attach to a Bridged Adapter for home network access
    - File -> Preferences -> Network
- Add a NAT network, e.g., 10.0.2.0/24
- Connect VMs to the NAT network 

-> Step-3: Install tools 

```bash
   sudo apt update && sudo apt upgrade -y
```
- Install wireshark in ubuntu
  
```bash
   sudo apt install wireshark -y
```

- On the attacker machine, the tools will be pre-installed if not
  
```bash
   sudo apt install wireshark -y
```
  
```bash
   sudo apt install ettercap-graphical -y
```

Now MITM Attack 
