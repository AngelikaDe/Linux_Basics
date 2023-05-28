## Part 1. Installation of the OS
* Ubuntu version using `"cat /etc/issue"` coomand
![Part_1](screenshots/Part_1.png)
---
## Part 2. Creating a user
* Creating new user using `"useradd"` command
![Part_2](screenshots/Part_2.png)
* User is in a group adm
![Part_2](screenshots/Part_2_2.png)
![Part_2](screenshots/Part_2_3.png)
---
## Part 3. Setting up the OS network
* Correct timezone for my region
![Part_3_1](screenshots/Part_3_1.png)
![Part_3_2](screenshots/Part_3_2.png)
* Names of the neetwork interfaces
lo interface is a virtual interface present by default on any Linux. It is used to debug network programs and run server applications on the local machine.
![Part_3_3](screenshots/Part_3_3.png)
* Ip address of the device I`m working in from DHCP server
![Part_3_4](screenshots/Part_3_4.png)
* External Ip of the gateway(ip)
![Part_3_5](screenshots/Part_3_5.png)
* Internal IP address of the gateway, aka default ip address (gw)
![Part_3_6](screenshots/Part_3_6.png)
* Manually set ip, gw, dns settings using `sudo vim /etc/netplan/00-installer-config.yaml`
![Part_3_7](screenshots/Part_3_7.png)
![Part_3_7_1](screenshots/Part_3_7_1.png)
* Ping 1.1.1.1 and ya.ru remote hosts
![Part_3_8](screenshots/Part_3_8.png)
![Part_3_8](screenshots/Part_3_9.png)
---
## Part 4. OS Update
* All packages updated to the latest version
![Part_4](screenshots/Part_4.png)
---
## Part 5. Using the sudo command
* Useradded to sudo group
![Part_5](screenshots/Part_5.png)
* Hostaname changed using `"sudo nano /etc/hostname"` command
![Part_5](screenshots/Part_5_2.png)
---
## Part 6. Installing and configuring the time service
* Automatic time synchronisation service setup
![Part_6](screenshots/Part_6.png)
* NTPS synchronization
![Part_6](screenshots/Part_6_2.png)
---
## Part 7. Installing and using text editors
### VIM usage:
- Create with saving the changes `:wq`
![Part_7](screenshots/Part_7_1.png)
- Update without saving `:q!`
![Part_7](screenshots/Part_7_2.png)
- Search `:/`
![Part_7](screenshots/Part_7_3.png)
- Search and Replace`:s/search str/replace str`
![Part_7](screenshots/Part_7_4.png)
### NANO usage:
- Create with saving the changes `^X+Y`
![Part_7](screenshots/Part_7_5.png)
- Update without saving `^X+N`
![Part_7](screenshots/Part_7_6.png)
- Search `^X`
![Part_7](screenshots/Part_7_7.png)
- Replace`^R`
![Part_7](screenshots/Part_7_8.png)
### MCEDIT usage:
- Create with saving the changes `F2`
![Part_7](screenshots/Part_7_9.png)
- Update without saving `F10`
![Part_7](screenshots/Part_7_10.png)
- Search `F7`
![Part_7](screenshots/Part_7_11.png)
- Search and Replace `F4`
![Part_7](screenshots/Part_7_12.png)
---
## Part 8. Installing and basic setup of the SSHD service
* Install the SSHd service `"sudo apt install openssh-server"`
![Part_8](screenshots/Part_8_1.png)
* Auto-start of the service whenever the system boots added
![Part_8](screenshots/Part_8_2.png)
* Reset the SSHd service to port 2022
![Part_8](screenshots/Part_8_3.png)
* Sshd process using the `ps` command. `ps -e` command writes information to standard output about all processes, except kernel processes.
![Part_8](screenshots/Part_8_4.png)
### `Netstat -tan` command
#### Keys explaned:
* -t - filter TCP protocol
* -a - all ports
* -n - shows ip instead of host, port number instead of name, UID instead of username.
#### Table explained:
* The `"Proto"` column tells us whether the specified socket is TCP or UDP. These are network protocols.
* The `"Recv-Q"` and `"Send-Q"` columns tell us how much data is queued for this socket, waiting to be read (Recv-Q) or sent (Send-Q).
* The `"Local Address"` and "External Address" columns tell you which hosts and ports the listed sockets are connected to. The local end is always on the computer on which you run netstat (in the example, the computer is called "Trafalgar"), and the external end is on another computer (may be somewhere on the local network or somewhere on the Internet).
* The `Status column` tells you what state the listed sockets are in. The TCP protocol defines states, including "LISTENING" (wait for some external computer to contact us)
#### 0.0.0.0 explained:
* Foreign address 0.0.0.0 - no one connected
* Local address 0.0.0.0 - listening on all interfaces 
![Part_8](screenshots/Part_8_5.png)
---
## Part 9. Installing and using the top, htop utilities
### `top` command:
* uptime - 2:34
* number of authorised users - 1
* total system load - 0.00
* total number of processes - 97
* cpu load - 0.0 us
* memory load - 3924.3
![Part_9](screenshots/Part_9_1.png)
* pid of the process with the highest memory usage - 1306, 781
* pid of the process taking the most CPU time - 3454
![Part_9](screenshots/Part_9_2.png)
### `htop` command:
* sorted by PID
![Part_9](screenshots/Part_9_3.png)
* sorted by PERCENT_CPU
![Part_9](screenshots/Part_9_4.png)
* sorted by PERCENT_MEM
![Part_9](screenshots/Part_9_5.png)
* sorted by TIME
![Part_9](screenshots/Part_9_6.png)
* filtered for sshd process
![Part_9](screenshots/Part_9_7.png)
* with the syslog process found by searching
![Part_9](screenshots/Part_9_8.png)
* with hostname, clock and uptime output added
![Part_9](screenshots/Part_9_9.png)
---
## Part 10. Using the fdisk utility
* Running `fdisk -l` command
name of the hard disk  - /sda
capacity - 40G
number of sectors - 83886080
![Part_10](screenshots/Part_10.png)
---
## Part 11. Using the df utility
### Running `df` command for the root partition(/):
* kB - kilobyte
* partition size  - 40970464kB
* space used - 7215408kB
* space free - 3164167kB
* percentage used - 19%
![Part_11](screenshots/Part_11_1.png)
### Running `df -Th` command for the root partition(/):
* file system type - ext4 aka fourth extended file system
* partition size  -  40G
* space used - 6.9G
* space free - 31G
* percentage used - 19%
![Part_11](screenshots/Part_11_2.png)
---
## Part 12. Using the du utility
* Running `du` command
#### Output the size of folders:
* /home
![Part_12](screenshots/Part_12_1.png)
* /var
![Part_12](screenshots/Part_12_2.png)
* /var/log
![Part_12](screenshots/Part_12_3.png)
* /var/log (using *)
![Part_12](screenshots/Part_12_4.png)
---
## Part 13. Installing and using the ncdu utility
* Installing ncdu utility using `sudo apt install ncdu` command
* Running `ncdu` command
#### Output the size of folders:
* /home
![Part_13](screenshots/Part_13_1.png)
* /var
![Part_13](screenshots/Part_13_2.png)
* /var/log
![Part_13](screenshots/Part_13_3.png)
---
## Part 14. Working with system logs
* Open for viewing: /var/log/dmesg, /var/log/syslog, /var/log/auth.log
* The last successful login time - 17:57:57
* User name - alcestis
* Login method - pam-unix
![Part_14](screenshots/Part_14_1.png)
* Restart SSHd service using `sudo systemctl restart ssh.service` command
![Part_14](screenshots/Part_14_2.png)
---
## Part 15. Using the CRON job scheduler
* Using the job scheduler, run the uptime command in every 2 minutes
![Part_15](screenshots/Part_15_2.png)
* Lines in the system logs (at least two within a given time range) about the execution
![Part_15](screenshots/Part_15_3.png)
* A list of current jobs for CRON
![Part_15](screenshots/Part_15_1.png)
![Part_15](screenshots/Part_15_2.png)
* Remove all tasks from the job scheduler
![Part_15](screenshots/Part_15_4.png)
---