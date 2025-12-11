# account-pirate
A basic tool that uses a vulnerability in Windows that's there since the beginning of time. Using this you can get admin CMD in the login screen directly.

**Just remember:** Don't do this on a machine that isn't yours, that includes your **school computers**. if you face cybercriminal charges, that's not my problem :) 
                   If you do something like this at least do it properly, and I'm not responsbile for it. This tool is for demonstration and educational purposes only.

Requirements:

- A Windows PE USB (Windows 8 or newer) [you can also use windows recovery enviorement if the target pc can't boot off of usb or smth, it needs to be windows pe 8 or newer still tho)
- But it defeats the entire purpose of this software since you need a password to go into WinRE:

<img width="474" height="201" alt="image" src="https://github.com/user-attachments/assets/f12e65cc-f5ae-4921-b234-63f9e584a107" />

- The tool itself (put it in c:\ or wherever you want, easily accessible and run it from windows pe, just a path where it's easily accessible for you. For secrecy, just put it in the root of your installation media if it isn't a CD/DVD drive.)

**THIS WILL NOT WORK IF THE TARGET INSTALLATION HAS BITLOCKER ENABLED ON THE C DRIVE.**

**ANOTHER NOTE: SETCH.EXE WILL BE ADDED TO EXCLUSIONS AND TAMPER PROTECTION WILL BE DISABLED BECAUSE WINDOWS 10 DETECTED THE EXPLOIT IN TESTING**

**Pro tip: To get file explorer in windows PE, press shift f10 to open command prompt (if you didn't already) and type notepad. Go to File > Open and select "All files".

# How does it work?

When you press SHIFT 5 times, the accesibility popup triggers which is [sethc.exe]. You can also do this in the login screen, and there's a huge security flaw.

![OIP-1815658149](https://github.com/user-attachments/assets/0a26391c-5d15-437d-a2cd-ed07f577ec77)

The user can just rename cmd.exe to sethc.exe, and **boom**. When you press SHIFT 5 times, CMD launches instead of that popup. But you have no admin priviliges.

**To fix that** I made a little executable called [cmd-m]. It's a batch script compiled to EXE so it can request admin priviliges and imitates command prompt. It basically asks for user input and executes it as a command, and this is why you need to type cmd-m in the command prompt when you're in the login screen to get **admin priviliges**.

<img width="979" height="512" alt="image" src="https://github.com/user-attachments/assets/c6c7a1ab-ed68-4a51-a3f7-df74636fa1ed" />

**Don't worry, you won't get any UAC. In the logon screen you're insolated from users altogether. If you need a full desktop with admin priviliges activate the administrator account:**

Type: **net user Administrator /active:yes**

To disable it, instead of yes just type no at the end: **net user Administrator /active:no**

<img width="979" height="512" alt="image" src="https://github.com/user-attachments/assets/73d5b57c-598f-4031-80a4-f82d129bf6ae" />

This is what the user interface looks like:
<img width="972" height="514" alt="program" src="https://github.com/user-attachments/assets/c20c09bb-1efd-4e52-b07c-148776652809" />

# How do I use this?

You press the number on your keyboard cooresponding to the number of the option you want to select. For example press [1] to inject the exploit.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/23d55a73-c156-4388-9f96-633bde0982c0" />

- Once you're in the logon screen (on the target installation) press SHIFT 5 times and a command prompt window will pop up.

After that type cmd-m and press ENTER. You will then have administrator priviliges directly on the logon screen.

**Note: The exploit works on both virtual machines and real computers. But please be aware of the legal risks of using this tool, and DO NOT use it unauthorized**

You will see a legal disclaimer when you launch the tool:

<img width="989" height="516" alt="image" src="https://github.com/user-attachments/assets/fdf2ec8b-da6b-4187-86c6-2183e7eee6f2" />

# Use responsibly, and enjoy!
