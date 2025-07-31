# How to take screenshot on Raspberry PI
When trying to take a screenshot on RasperryPi, most of the information on youtube will convince you, to run a lot of commands to get it running on the terminal. 
All you need is a simple key on your raspberry keyboard PrtScrn
However, to activate this you have to open the linux tab and run the scrot command/ I also did the sudo apt-get scrot
<img width="1920" height="1040" alt="r1" src="https://github.com/user-attachments/assets/564bb815-1818-48c8-ab54-4f8f198edd57" />
One challenge that I had to overcome was not being able to view my scrot images or view the screenshot from the Prtscn key
<img width="928" height="663" alt="r2" src="https://github.com/user-attachments/assets/8b51a1ca-5a97-4ca1-9605-0b2821890011" />
 
 I found much later that my images were being saved directly to pictures
 
<img width="939" height="686" alt="r3" src="https://github.com/user-attachments/assets/d51869d1-961c-4d79-a20c-ba39d1c9cf1c" />

if you open and zoom in the picture you notice the first two photos are from the 24th and the rest are from the 25th. This is because I didn’t realize my PrtScn key was already active. 
So before running the scrot command, click the PrtScn and check your home directory in the pictures section.
If it’s available there, great! If not run the Scrot command and that should activate the PrtScn.
