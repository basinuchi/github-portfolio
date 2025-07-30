# Making A static IP 
This is a project I have done before, I was able to document most of my challenges with a back and forth on Chatgpt
As a tip if you are following a script like me to properly put in commands properly its safe to do a copy and paste, which doesn’t happen like the normal way we would do it on a word file instead use the these keys Ctrl+Shift+V to properly paste on Linux.

The process of getting started with this project, Is discovering what your local IP address is, You can do this by opening your Linux terminal and typing out the command hostname -I
<img width="795" height="447" alt="image" src="https://github.com/user-attachments/assets/f184de64-d207-40cb-bbc6-911e51ff3dad" />

In this case my local address is 192.168.0.17 (note  that this is the static IP I created previously)
Now you can set the static IP address from your router admin page but doing this through the PI is much more fun for me and I also do not have admin rights to my home WiFi
So the next step on the PI is to open the DHCP configuration file – Dynamic Host Configuration Protocol; DHCP is used on internet protocol networks for automatically assigning IP addresses and other communication parameters to devices connected to the network using a client-server architecture. (just like I am using)
On your Pi put in the command: sudo nano /etc/dhcpcd.conf 

<img width="1920" height="1042" alt="dhcp" src="https://github.com/user-attachments/assets/5a71700d-21ca-4383-a40e-fe055e811c55" />
If you see this when you put in this command, you made a very simple yet unrecognizable mistake. This was one of my first challenges when I was trying to do such a simple project. Usually more information should be available in that blank space
The biggest headache in this is, most youtubers don’t think to cover this and chatgpt is unable to process why this is a problem and would most likely tell you the command you inputted is wrong.
I had to change my course of direction, from consulting a diffeent Youtbe video I found an  easier way that I could work with using NMTUI: NetworkManager Text User interace is a tool in linux used for configuring and managing network connectiond through a text-based interface

using the command nmtui
<img width="1920" height="1047" alt="nmtui" src="https://github.com/user-attachments/assets/0f2c446d-2473-4b04-bc2f-6f89dcdf5f8d" />
You get the prompt
<img width="1916" height="1040" alt="edit promp" src="https://github.com/user-attachments/assets/b83477ee-d666-45f7-8c39-758045a0fc4e" />

asking you to edit a connection, hit the enter key
<img width="1920" height="1040" alt="tplink" src="https://github.com/user-attachments/assets/e6374d62-1027-4403-bb90-696abc245bb6" />
In my case I clicked the Tp link as the option where I want to make my changes
<img width="1916" height="1043" alt="pic1" src="https://github.com/user-attachments/assets/f93e3279-fb67-46b2-bc16-1a0fc1f05c3b" />
I used my arrow keys to navigate to IPV4 CONFIGURATION, clicking enter and used my arrow keys to pick manual. it will originally be on automatic (note in the drop down menu, you will see DHCP only, I am hypothesizing that clicking that will make our previous DHCP command work properly.
Now using my arrow key, I will navigate to show and press enter
<img width="1920" height="1040" alt="pic2" src="https://github.com/user-attachments/assets/93e7fee3-8c8d-4914-bd05-08dd02dec122" />
<img width="1916" height="1047" alt="pic3" src="https://github.com/user-attachments/assets/7b472559-40fc-4216-9bfd-9a0a8c2b2a7e" />
<img width="1916" height="1047" alt="address 1" src="https://github.com/user-attachments/assets/66590ce9-3620-4347-8e28-ce9322e851cb" />
Now navigate your arrow key to Addresses and click add. You want to add the address you are sure no device is using in your home network. 
This is where the practical understanding of sub netting comes in. do not close this page but open a new terminal and input the command ifconfig 
This will show you your IP information
My current IP address is 192.168.0.17/24, 17 being the number I chose for my static IP, how was I able to know and choose this number?
From the command inputted in my terminal, it showed a subnet mask of 255.255.255.0 which is represented by the /24 you see (CIDR block), this meant that I have access to 256 possible ip addresses in picking for a static IP. From the range of (network address-192.168.0.1- 192.168.0.255-broadcast address) They are unavailable. So I selected the ip within the usable range.

Back to the project once you have picked your IP navigate your arrow key to gateway and enter the routers IP address, you can add the Ip address to the DNS servers but I used Cloudfares DNS servers instead.
<img width="1916" height="1047" alt="end 1" src="https://github.com/user-attachments/assets/0560ffea-2da2-4a0c-98b5-6f2f41a51d46" />
Once done you can navigate back to OK
<img width="1920" height="1040" alt="end2" src="https://github.com/user-attachments/assets/702c0477-186c-41c7-aacf-bc53448ac199" />
and click quit
<img width="1916" height="1040" alt="end4" src="https://github.com/user-attachments/assets/98716f59-11e3-438e-82b4-42e90b3cc676" />
  To check if it works put in the command on linux: sudo systemctl restart NetworkManager
  <img width="1920" height="1047" alt="finale" src="https://github.com/user-attachments/assets/582991e5-4833-4aae-9bd7-a715f429b365" />
once this is done go to new terminal and type in hostname -I
Congratulations!! you have successfully set up a static wifi
