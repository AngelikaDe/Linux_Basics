## Part 1. Installation of the OS
* Ubuntu version using "cat /etc/issue" coomand
![Part_1](screenshots/Part_1.png)
## Part 2. Creating a user
* Creating new user using `#ffffff "useradd"` command
![Part_2](screenshots/Part_2.png)
* User is in a group adm
![Part_2](screenshots/Part_2_2.png)
## Part 3. Setting up the OS network
* Creating user user_1
![Part_3]
* Correct timezone for my region
![Part_3_2]
* Names of the neetwork interfaces
lo interface is a virtual interface present by default on any Linux. It is used to debug network programs and run server applications on the local machine.
![Part_3_3]
* Ip address of the device I`m working in from DHCP server
![Part_3_4]
* External Ip of the gateway(ip)
![Part_3_5]
* Internal IP address of the gateway, aka default ip address (gw)
![Part_3_6]
* Manually set ip, gw, dns settings
![Part_3_7]
* Ping 1.1.1.1 and ya.ru remote hosts
![Part_3_8](screenshots/Part_3_8.png)
## Part 4. OS Update
* All packages updated to the latest version
![Part_4](screenshots/Part_4.png)
## Part 5. Using the sudo command
* Useradded to sudo group
![Part_5](screenshots/Part_5.png)
* Hostaname changed using "sudo nano /etc/hostname" command
![Part_5](screenshots/Part_5_2.png)
## Part 6. Installing and configuring the time service
* Automatic time synchronisation service setup
![Part_6](screenshots/Part_6.png)
* NTPS synchronization
![Part_6](screenshots/Part_6_2.png)
## Part 7. Installing and using text editors
* VIM usage:
- Create with saving the changes (:wq)
![Part_7](screenshots/Part_7_1.png)
- Update without saving (:q!)
![Part_7](screenshots/Part_7_2.png)
- Search(:/)
![Part_7](screenshots/Part_7_3.png)
- Search and Replace(:s/search str/replace str)
![Part_7](screenshots/Part_7_4.png)
* NANO usage:
- Create with saving the changes (^X+Y)
![Part_7](screenshots/Part_7_5.png)
- Update without saving (^X+N)
![Part_7](screenshots/Part_7_6.png)
- Search(^X)
![Part_7](screenshots/Part_7_7.png)
- Replace(^R)
![Part_7](screenshots/Part_7_8.png)
* MCEDIT usage:
- Create with saving the changes (F2)
![Part_7](screenshots/Part_7_9.png)
- Update without saving (F10)
![Part_7](screenshots/Part_7_10.png)
- Search(F7)
![Part_7](screenshots/Part_7_11.png)
- Search and Replace(F4)
![Part_7](screenshots/Part_7_12.png)
## Part 8. Installing and basic setup of the SSHD service
* Install the SSHd service "sudo apt install openssh-server"
![Part_8](screenshots/Part_8_1.png)
* Auto-start of the service whenever the system boots added
![Part_8](screenshots/Part_8_2.png)
* Reset the SSHd service to port 2022
![Part_8](screenshots/Part_8_3.png)
* Sshd process using the ps command
![Part_8](screenshots/Part_8_4.png)
* Netstat -tan command
-t - filter TCP protocol
-a - all ports
-n - shows ip instead of host, port number instead of name, UID instead of username.
Table explained:
The "Proto" column tells us whether the specified socket is TCP or UDP. These are network protocols.
The "Recv-Q" and "Send-Q" columns tell us how much data is queued for this socket, waiting to be read (Recv-Q) or sent (Send-Q).
The "Local Address" and "External Address" columns tell you which hosts and ports the listed sockets are connected to. The local end is always on the computer on which you run netstat (in the example, the computer is called "Trafalgar"), and the external end is on another computer (may be somewhere on the local network or somewhere on the Internet).
The Status column tells you what state the listed sockets are in. The TCP protocol defines states, including "LISTENING" (wait for some external computer to contact us)
![Part_8](screenshots/Part_8_5.png)
## Part 9. Installing and using the top, htop utilities






 