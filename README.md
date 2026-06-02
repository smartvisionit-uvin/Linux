# While in the CLI
~$ represents the directory we're currently accessing

# Identify the directory that you're in
PWD

# To log out of the server
Exit
Enter

# Update Server (apt-update tells your computer what updates are available/ apt-upgrade installs said updates)
sudo apt update
Enter

Sudo apt upgrade
Enter

# Restart the VM
Sudo reboot

# Automatic updates
sudo apt install unattended-upgrades
-- Once entered, check if the server already has the newest version of the package

# As a part of the above automation, it would be useful to set up the server to restart to complete the installation automatically
# To do this we need to install another package
sudo apt install update-notifier-common

# Check the configuration in the APT config directory. APT is a powerful tool handling the installation and removal of oftware
cd /etc/apt/apt.conf.d

#To list contents
LS

# Open 50 unattended Updates file
sudo nano 50unattended-upgrades

# Make sure the below 3 lines are not commented out (remove forward slashes if highlighted)

<img width="1221" height="366" alt="image" src="https://github.com/user-attachments/assets/c022a9d4-3b00-45fa-9dc0-34549a82c197" />

# To search and look for automatic updates
Press CTRL + W
Search automatic-reboot 

# Check and uncomment the code
<img width="856" height="84" alt="image" src="https://github.com/user-attachments/assets/bf4b3f8f-a209-40b4-9334-9d4dff7a7f67" />

# Also replace False with true. We have now told the server to restart automatically following an unattended upgrade

<img width="1092" height="121" alt="image" src="https://github.com/user-attachments/assets/bd23b7d4-3f65-40d4-b277-0fea51ea45ed" />

# Scroll down and uncomment this entry 
<img width="1223" height="295" alt="image" src="https://github.com/user-attachments/assets/afc952b2-35f6-47bf-8b0d-6f44ec1de42a" />

# To save changes
Press CTRL + X
Y




