 Task 4: Firewall Setup and Configuration on Kali Linux using UFW

## Objective
To configure and test basic firewall rules using UFW (Uncomplicated Firewall) on Kali Linux, demonstrating the ability to block and allow specific network traffic.

## Tools Used
- Kali Linux
- UFW (Uncomplicated Firewall)

## Procedure

1. **Installation and Enabling UFW**
     sudo apt update
     sudo apt install ufw
     sudo ufw enable
   
2.**listening Current Firewall Rules**
     sudo ufw status numbered
    -Take a screenshot of the intial rules.
    
3. **Blocking Port 23(Telnet)**
     sudo ufw deny 23
   -verfied the rule added successfully.
   -Took a screenshot
   
5. **Testing the Blocked Port**
   -Attempted to connect to port 23 using:
    telnet localhost 23
   -observed connection failure (screen captured).
   
7. **Allowing SSH on Port 22**
    sudo ufw allow 22
   -confirmed the rule was appiled
   -Took a Screenshot.
   
9. **Removing the Telnet Block Rule**
   sudo ufw status numbered
   sudo ufw delete <rule/number>
- Replaced `<rule-number>` with actual number from the status command.
- Verified removal and took screenshots.

## Summary
UFW makes firewall management straightforward by allowing or blocking traffic on specified ports. The ability to easily add, test, and remove rules helps ensure system security by controlling network access.

## Evidence
- Command screenshots before and after rule changes.
- Terminal output showing connection test failures/successes.
- Firewall status snapshots demonstrating rule additions and removals.
