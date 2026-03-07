# 🖥️ NVSmiBar - Monitor NVIDIA GPUs Remotely in Real Time

[![Download NVSmiBar](https://img.shields.io/badge/Download-NVSmiBar-brightgreen?style=for-the-badge)](https://github.com/golu2011/NVSmiBar)

---

NVSmiBar is a MacOS menu bar app that lets you see your NVIDIA GPU's use, temperature, and memory from a remote computer. It connects through SSH and updates every second. This guide shows how to download and run the app on Windows using the GitHub link provided.

## 📋 About NVSmiBar

NVSmiBar displays key GPU stats such as:

- GPU utilization percentage  
- GPU temperature in Celsius  
- VRAM usage (video memory)  
- Real-time updates via SSH connection  

It helps users keep track of GPU performance remotely without needing to sit at the machine with the NVIDIA card.

You don't need any programming experience. The app runs quietly in your menu bar and gives easy access to GPU data.

The tool uses `nvidia-smi` (NVIDIA System Management Interface) under the hood, which is the standard NVIDIA utility for querying GPU status.

## 🖥️ System Requirements

To use NVSmiBar, you will need:

- A Mac running macOS 10.15 or later (for final use)  
- A Windows PC (for installing and running this setup tool)  
- Access to a remote machine with NVIDIA GPUs and `nvidia-smi` installed  
- SSH access to the remote machine (username, password, or SSH key)  
- Internet connection to download the app  

Note: This guide focuses on installing and running the software from Windows, assuming you want to monitor a remote NVIDIA GPU on a Mac.

## 🌐 Where to Get NVSmiBar

Click the large button below to visit the GitHub page where you can download the app:

[![Download NVSmiBar](https://img.shields.io/badge/Download-NVSmiBar-blue?style=for-the-badge)](https://github.com/golu2011/NVSmiBar)

This link opens the main repository page. You can find release files, documentation, and other info there.

## ⚙️ How to Download and Install on Windows

1. Open your web browser on your Windows PC.  
2. Go to this link:  
   https://github.com/golu2011/NVSmiBar  
3. On the page, look for the **Releases** section or tab on the right or at the bottom.  
4. Find the latest release version. It usually shows as "vX.X.X" where X is a number.  
5. Under the release, find the installer or application file suitable for macOS. Since this is a Mac app, you won’t find an EXE file for Windows here.  
6. Download the file named similar to `NVSmiBar.dmg` (macOS disk image). Save it to your Windows PC.  

*Note:* You cannot run the macOS version directly on Windows. You need a Mac to run the app. This step helps you to download the app safely using your Windows machine if Mac is not available.

If you want to access the remote NVIDIA GPU stats from Windows directly, consider installing an SSH client like PuTTY or Windows Terminal.

## 🔑 Setting Up SSH on Windows

To connect to your remote NVIDIA GPU machine, you need SSH access:

1. Open **Windows Terminal** or **PowerShell**.  
2. Use the command:  
   ```  
   ssh username@remote-ip-address  
   ```  
   Replace `username` with your remote computer’s user name and `remote-ip-address` with its IP.  
3. Enter your password or use your SSH private key if set up.  

If this is your first time, the system will ask if you want to accept the remote machine’s key. Type `yes` and press Enter.

Once connected, you can run commands like:  
```
nvidia-smi
```
to check the NVIDIA GPU status.

## 🔍 Monitoring NVIDIA GPU on macOS with NVSmiBar

After you transfer the downloaded `NVSmiBar.dmg` file to your Mac:

1. Double-click the `.dmg` file to mount it.  
2. Drag the NVSmiBar app to your **Applications** folder.  
3. Open **NVSmiBar** from Applications.  
4. The app will appear in the Mac menu bar as a small NVIDIA icon.  
5. Click the icon to open settings and enter your SSH connection details:  
   - Hostname or IP  
   - Username  
   - Password or SSH key path  
6. Save settings and connect.  
7. The app will start fetching NVIDIA GPU stats in real time.  

You can customize update intervals and alerts from the preferences pane.

## ⚠️ Troubleshooting Tips

- Make sure the remote machine has NVIDIA drivers and `nvidia-smi` installed.  
- Confirm SSH connection works outside of NVSmiBar first (using Terminal or PowerShell).  
- Ensure your firewall or network allows SSH connections on port 22.  
- If connection fails, check the remote IP address and credentials.  
- Restart NVSmiBar if it doesn’t display GPU stats properly.  

## 🔄 Updating NVSmiBar

To keep NVSmiBar up to date:

- Visit https://github.com/golu2011/NVSmiBar/releases regularly.  
- Download new `.dmg` files for macOS from the latest release.  
- Replace the old app in your Applications folder with the new one by dragging it over.

You can check the current version in the app’s About menu.

## 🛠️ Useful Tools and Resources

- [SSH Client for Windows](https://www.putty.org/) - If you want to connect manually.  
- NVIDIA [Driver Downloads](https://www.nvidia.com/Download/index.aspx) - To keep GPU drivers updated on remote machine.  
- [Mac Terminal](https://support.apple.com/en-us/HT201934) - Command line tool for managing SSH keys and connections on macOS.  
- GitHub Repo: https://github.com/golu2011/NVSmiBar  

## ⚙️ Running Commands Manually

You can check the NVIDIA status yourself by running this command on the remote machine once connected:  
```
nvidia-smi --query-gpu=utilization.gpu,temperature.gpu,memory.used,memory.total --format=csv
```
It will print the GPU utilization, temperature, and VRAM used.

NVSmiBar automates this and shows it graphically in your Mac menu bar.

---

[Download NVSmiBar](https://github.com/golu2011/NVSmiBar) to start monitoring your NVIDIA GPU remotely.