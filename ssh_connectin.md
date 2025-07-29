# SSH CONNECTION
The reason for this project was to find a way I could control my windows laptop from my raspberrypi desktop.

First step was for me to open my command prompt on windows 
I followed the raspberypi documentation on how to to connect to a remote terminal, the command instructions `ssh <username>@<ip address>`
I took that literally, but after running through my diffculty through the youtbe search . I was able to interpret the command successfully.
<img width="960" height="502" alt="image" src="https://github.com/user-attachments/assets/76d291ff-3035-432a-a031-af880a2e0462" />
Unfortunately this was not enough as I kept hittng a barrier “connection refused” 
Going back to the Youtube video I realized I had to update my windows laptop on my new plans to access this feature
<img width="1325" height="719" alt="image" src="https://github.com/user-attachments/assets/d7d17d37-03f2-4801-b463-f38d467d0e5d" />
so I went to the settings window and clicked on he apps and features, once there I clicked on optional features like the video suggested.
<img width="966" height="648" alt="image" src="https://github.com/user-attachments/assets/b2a39129-2a20-48d9-9d52-c0fc6f4e9d1b" />
At the time of the process, the video instructed to search for SSH Cliens and install this feature, however, I only had the SSH server,
after installing it and moving forward in my project successfully, did I come back and find the SSH client, so if the client does not show up for you it only means this is your first time accessing that feature, windows is smart and will update that once you finalize your work.
Regardless of doing this, it still said connection refused, so I consulted the higher power, chatgpt.
Chatgpt gave me the requirements needed to to make sure I had my setup going properly. 
I had to change my configuration settings on raspberrypi, First I clicked the raspberry icon → preferences and Raspberrry pi configuration (see image below)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4eb8378f-fc2b-430d-a7e0-478a73affeb1" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ba5d6a0f-a6bc-43c1-8abf-851258b1e9d2" />
Once the configuration is page is open, you move from system to interfaces and toggle the SSH button to turn it on (mine currently shows the change) 
going back to the command prompt on windows 
<img width="962" height="499" alt="image" src="https://github.com/user-attachments/assets/65c99ed5-992c-466b-bf31-33eee7f884d3" />
Note: You can see I used a different IP address 192.168.0.109 when I was troubleshooting because I did not understand the process. 
You can also see that I hit another wall of connection closed from connection refused, running this problem through chatgpt, I realized it meant either my username or password is incorrect, which is why I changed my username to pi from basinuchi.
I also tried to use clear as a command that works on linux but command prompt does not care about linux commands.
The challenge was my password, first off all I was taken aback hat I could not see the password I typed, distracted me in typing it out correctly. 
So I figured I must be using the wrong password and switched to my Pi-hole password which was incorrect, after several tries, taking a break and going back. I was able to type the password correctly the one used to access my raspberry pi
<img width="977" height="506" alt="image" src="https://github.com/user-attachments/assets/4e55d2eb-e981-49e7-9190-f058d2265de5" />
My SSH connection was successful
