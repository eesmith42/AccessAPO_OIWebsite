<h1 align="center">Accessing the APO-OI Website for Updates</h1>

- add anchor tags to emails (example in chat saved from 3/10 meeting)

## Description

The APO-OI website uses WPI's user server to host a public-facing website containing information about the organization and Merit Badge University information. Merit Badge University (MBU) is an annual service done by APO-OI where members teach scouts badges. The MBU website is used for registration for the event, as well as information about the event.

This README is meant to aid the Web Chair & MBU Chair in accessing the website for updates and making the link live for MBU registration. **This README is a PRIVATE document, as there is a key to access the website that only the Web Chair & MBU Chair may have access too. This is in accordance with what Emma Smith, the Spring 2021 Web Chair, was told by ITS.**

**Note: The SSH Key for accessing the website will change about every year, so you will need to contact ITS in order to obtain that key. Contacting ITS can be done either by emailing one of the people listed below or by putting in a ticket via the WPI Hub.**

## Contact Information 

<a href=“mailto:apo-fellowship@wpi.edu>apo-fellowship@wpi.edu</a>

This document was written by Emma Smith, the Spring 2021 Web Chair for APO-OI. If you have questions, contact her at: eesmith@wpi.edu or eesmith42@outlook.com. 

The contacts at ITS that will be helpful in the transition from Web Chair to Web Chair or general questions about the process:

- John Eismeier at jpeismeier@wpi.edu (main contact)
- Carien van Gelder at cwvangelder@wpi.edu
- Mark Taylor at mtaylor@wpi.edu

## How To Access The Website

Prior to being able to access the APO-OI website, you need to download [PuTTY] (https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) and make sure that the master branch on the APO Website GitHub repository is fully updated (i.e. merge the branch created for the update to the master branch). **The master branch should be fully updated before you start this process; it must be fully updated for any updates to the website to go through.**

Following the installation of PuTTY & updating of the master branch, open up the program. Your window should look something like this (possibly without the linux.wpi.edu in the "Saved Sessions" box):

![PuTTY Initial Window](https://github.com/eesmith42/AccessAPO_OIWebsite/blob/main/PuTTyWindowInitial.jpg)

Enter **linux.wpi.edu** into the box under "Host Name (or IP address)".

Enter **22** into the box under "Port".

The "Connection type:" should be **ssh**.

"Close window on exit:" should be **Only on clean exit**.

![PuTTY Inputs](https://github.com/eesmith42/AccessAPO_OIWebsite/blob/main/PuTTyWindowInputs.jpg)

Click "Open". You will come across a window that looks like this:

![PuTTY Login Window](https://github.com/eesmith42/AccessAPO_OIWebsite/blob/main/PuTTyLoginWindow.jpg)

Log in using your WPI credentials (i.e. your username and password you use to access your email/bannerweb/etc). Enter your username, and your window should look like this:

![PuTTY Username](https://github.com/eesmith42/AccessAPO_OIWebsite/blob/main/PuTTyPasswordWindow.jpg)

After you type in your username, you will have to type in your password. The password will not show up on the screen, but type it in as you usually would. Your window should now look like this:

![PuTTY Password](https://github.com/eesmith42/AccessAPO_OIWebsite/blob/main/PuTTyAfterPass.jpg)

Next, you will access the APO-OI website using the ssh key.

In the terminal, type **insert ssh key here**. Where it says "(tab)", press the tab key on your keyboard. It should auto-complete the key, which will make your life easier. 

The window should now look like this:

![PuTTY SSH Key](https://github.com/eesmith42/AccessAPO_OIWebsite/blob/main/PuTTySSHKey.jpg)

Type in **ls** in order to look at what is currently in the APO-OI website on this end. 

Your window should now look like this:

![PuTTY APO Website Content](https://github.com/eesmith42/AccessAPO_OIWebsite/blob/main/PuTTyWebsiteContents.jpg)

Now, the next step is updating the website!

## Installing Updates

You've officially gotten into the website, woo woo! Now you'll run through how to install the updates to the website.

Your window should look like this:

image

In the window, type **Cd t/A(tab)**. Just like before, where it says "(tab)", press tab to auto-complete the line of code. The code should be "Cd t/APO_Website/".

Your window should now look like this:

image

Next, you will type **Git pull** into the window, which will make the window look like this:

image

Finally, you will type **./i(tab)**. The "(tab)" is where you press tab on your keyboard to auto-complete the line of code. The code should be "./install.sh". 

Your window should look like this:

image

## Final Steps

Check the website (https://users.wpi.edu/~apo/index.html) to make sure your updates have been pushed!

## Troubleshooting

When you update the website, it may only look like it is updated on WPI's end (i.e. the PuTTY window) and not on your end (i.e. when you open it in a browser on your computer). This isn't a problem with the process. **All you need to do is clear your cache for it to update on your end.**

This is a new process for updating the APO-OI website, so if you are having any issues with this process, please contact the contacts at ITS listed below the **Contact Information** section of this README.
