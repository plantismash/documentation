## Setting Up plantiSMASH on Windows Without Linux 

For users who do not have a Linux system installed, follow this guide to set up a Linux environment on Windows .

---

## Create a Linux Environment in Windows

Skip this step if using a Linux server. Refer to the [WSL setup guide](https://medium.com/@larysha.rothmann/getting-started-with-wsl-for-bioinformatics-setting-up-a-fully-functional-and-pretty-53b9c79b5380).

1. Open the Windows command prompt: Press `Win Key`, search for ‘command prompt’, and select ‘Run as administrator’. Click ‘Yes’ when prompted by Windows to allow the app to make changes.
2. Type in the command prompt: 
   ```bash
   wsl.exe --install
   ```
3. Wait for the installation to finish, and type ‘Yes’ if prompted.
4. Restart your computer.
5. Click on Ubuntu.exe to register Ubuntu.
6. To have root as the administrator every time you start, use:
   ```bash
   sudo -s
   ```
7. If any issues arise, unregister Ubuntu in PowerShell with:
   ```bash
   wsl --unregister Ubuntu
   ```
   Then click Ubuntu.exe to register Ubuntu again or visit your Linux server terminal. 

