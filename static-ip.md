# Making A static IP 
This is a project I have done before, I was able to document most of my challenges with a back and forth on Chatgpt
As a tip if you are following a script like me to properly put in commands properly its safe to do a copy and paste, which doesn’t happen like the normal way we would do it on a word file instead use the these keys Ctrl+Shift+V to properly paste on Linux.

The process of getting started with this project, Is discovering what your local IP address is, You can do this by opening your Linux terminal and typing out the command hostname -I
<img width="795" height="447" alt="image" src="https://github.com/user-attachments/assets/f184de64-d207-40cb-bbc6-911e51ff3dad" />

In this case my local address is 192.168.0.17 (note  that this is the static IP I created previously)
Now you can set the static IP address from your router admin page but doing this through the PI is much more fun for me and I also do not have admin rights to my home WiFi
So the next step on the PI is to open the DHCP configuration file – Dynamic Host Configuration Protocol; DHCP is used on internet protocol networks for automatically assigning IP addresses and other communication parameters to devices connected to the network using a client-server architecture. (just like I am using)
On your Pi put in the command: sudo nano /etc/dhcpcd.conf 
