# Creating a Keylogger that sends keystrokes via email 
WARNING! only use this project on your home network and devices. this project is simply for educational purposes only!
The first step for me was to download the python version 3.11.2
<img width="1365" height="656" alt="python downloader caption" src="https://github.com/user-attachments/assets/89d050d7-05aa-4be5-ad50-0d73287e086f" />
i downloaded the one with 64bit, this version is recommended to be more reliable.
<img width="655" height="403" alt="Python admin message" src="https://github.com/user-attachments/assets/4690f329-de9a-4727-9ccb-8754f6f27762" />

once the file has been downloaded and opened, be sure to click, add python.exe to file PATH
You should also have admin priviledges, if  yours does not give you the option like mine does. you can simply follow the file path location from the download page
and right click on the python file to run admin priviledges.
i created an enviroment folder on my desktop and i called it keylogger creation, i will use this to store my files as we proceed there.

THE NEXT STEP - We have to think like hackers and when a hacker wants to corrupt your system, they disguise the medium as a legitimate software or file or mail etc.
Thats going to be our plot of this step; for that i searched for an icon, i used the gear icon that is usually used for the settings logo
i downloded the ICO format of this icon. i used this website https://icon-icons.com/  

<img width="1366" height="657" alt="download ico" src="https://github.com/user-attachments/assets/04ea7e74-b37c-48d6-b97a-03a9b65757c4" />

We will use this icon to mask the keylogger.

<img width="629" height="64" alt="previous settings icon name" src="https://github.com/user-attachments/assets/84c435d1-e589-4a5c-a2b8-144e15da0d98" />

i moved the image to the keylogger folder i created

<img width="839" height="259" alt="icon renamed" src="https://github.com/user-attachments/assets/c76e3313-ddbd-4628-8fd5-0684c779dc75" />

i renamed it to icon, above the file in the image you will see on the tool bar VIEW, i clicked on it which created a new pop up bar 
on the right of the pop up bar, i clicked, file name extensions.

Now on Command Prompt we are going to install the libraries we need. 
pip install pynput and later  pip install pyinstaller

<img width="977" height="507" alt="first two cp" src="https://github.com/user-attachments/assets/33f1f257-f56c-4dd7-8336-5b7456cb0b15" />

The next is to configure my gmail account that will send the keystrokes to me, for this i opened a new a Gmail account 
i went to manage my account, i had to make sure i had my two step verification turned on and searched app passwords

<img width="1314" height="539" alt="app passwords" src="https://github.com/user-attachments/assets/edf8f993-e0c4-4d38-9527-458c61527562" />

this is because i am seeting up a password for my keylogger app, so i create a random app name like project key
it gave me a temporary password and i copied and saved it in my notes because i will be using this information later

Now i went back to my keylogger creation folder, that i created earlier and moved the icon to, i will create a text document and then change the extenstion from
.txt to .py

<img width="876" height="493" alt="keylogger text file" src="https://github.com/user-attachments/assets/21977033-5971-42de-9f3f-0fa1f0ca0ef0" />

Now through my educational process, i have to make sure that my windows defender is turned off for this to work (i will show you something intresting toward the end about this)

<img width="796" height="630" alt="manage settings" src="https://github.com/user-attachments/assets/4ae0dcdf-dafa-415e-a50d-cec8ebcd91fd" />

go to manage settings

<img width="796" height="625" alt="defender off" src="https://github.com/user-attachments/assets/12a341c6-f10f-4d9a-a8ee-3453bd503847" />
toggle the defender button off.

Now for the coding part i openede IDLE text editor, which comes with the python package downloaded, i went to file and opened a new file and inputted a python code i got from
https://github.com/benjy-cyber
the code is really simple to follow, the temporary password i got earlier from google, i was able to put it inside the quotation of the code.
i was confused about the email part because i had to put my email in "From and To" I made only one gmail accountg and had no interest in putting my personal email in this

<img width="486" height="101" alt="new" src="https://github.com/user-attachments/assets/7fa2034d-c83c-4c59-a251-be1b25a70705" />

i added +reciepient, as i was going to use the same email regardless with From and To, i wanted to make sure it would be forwadinf the information back to my account. 
Then I saved the file in the keylogger.py, the file earlier that was changed from text to py in the folder

now in the file path type powershell, once powershell is open. Type in pyinstaller -w -F keylogger.py --icon.ico
this code makes sure that the code works on the background, it works fast +the name of the file and the icon, so i am able to mask it

<img width="1208" height="684" alt="powershell" src="https://github.com/user-attachments/assets/6288dda3-f125-4848-bfe6-8b76dfaf9390" />

powershell compiles this and if you go back to the file folder and click the dist folder

<img width="1125" height="357" alt="dist" src="https://github.com/user-attachments/assets/94285685-bb11-4595-ac23-bddb53ee90b4" />

copy the keylogger.exe file with the gear icon
now we will mask the file into something else like system_thread.exe once you double click it, it starts running but nothing opens. 
to test if its working, i will type random things and see if it triggers the email for me, from the code i set my traget to a 100 keystrokes, so i must reach
that number to recieve an email

<img width="877" height="259" alt="image" src="https://github.com/user-attachments/assets/7e42055f-49f1-4147-b825-93253e0a3af5" />

<img width="894" height="318" alt="image" src="https://github.com/user-attachments/assets/5d83b220-8cac-43c9-a542-f4e980f3b16d" />

Now the big question is if your windows defender is turned on will this work?
i restarted my windows laptop, made certain my windows defender was turned on and ran the program again.

<img width="990" height="319" alt="image" src="https://github.com/user-attachments/assets/5180f7fc-1ad6-4c70-a29a-1e8c6a30076e" />

so with my windows defender turned on it was still capable of copying my keystrokes, i went to the task manager and turned off the file that was running and it did stop. 
I learned that keylogging beyond a malicious file that will copy your keystrokes, you can also be targeted through social enginering. Devices should always be locked and guarded.
Nobody should have access to your device.


