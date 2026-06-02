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

<img width="1336" height="103" alt="image" src="https://github.com/user-attachments/assets/47fecd1b-cdb2-41bd-a081-adb1f4a253f3" />


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

# Now edit the second entry

<img width="1336" height="103" alt="image" src="https://github.com/user-attachments/assets/7fb7a1da-473a-4bb7-bc32-57fa1b63fc9c" />

sudo nano 20auto-upgrades

# Check both of these lines are present and set to 1

<img width="1252" height="174" alt="image" src="https://github.com/user-attachments/assets/0d9f9484-236e-4ad4-9e2b-c1dd7b73f1a4" />

CTRL + X 

# Restart server for changes to take effect
Sudo reboot

# Check if automatic upgrades are running okay
sudo systemctl status unattended-upgrades

# Make sure it's Active and running

<img width="1316" height="548" alt="image" src="https://github.com/user-attachments/assets/155c61e2-68ba-418b-a8d6-057ae840c96d" />

# Networking

# Check network connections

ip a

# To make changes
sudo nano /etc/netplan/00-installer-config.yaml

*If you are still following this tutorial, note that 00-installer-config.yaml (in the /etc/netplan/ folder) has been replaced by 50-cloud-init.yaml in the same folder

# Adding a Desktop To The Server
# Install a lightweight desktop environment (LXDE)

sudo apt install lxde-core lxappearance
Enter Y
Pick lightdm
sudo reboot

# Look into Installing Cockpit too for web management (not included here)



# Adding a new user
sudo adduser David
Enter password,full name etc.

# Enter Home Directory
cd /home
ls

# Make admin
sudo usermod -a -G sudo David
Password

# Switch users
su - David
Enter password
whoami
exit

# Switch to root (no longer need to enter sudo)
sudo su -
apt update

# List user accounts
compgen -u

# Removing a user
sudo del user david
password

# Enable the root account
sudo passwd root
create a new password

Exit and login as root.
Command pompt will chnage to # instead of usual $

# Disable the root account
sudo passwd -l root

# Rename the server
hostname
hostnamectl
sudo hostnamectl set-hostname newservername

hostname

# If name on CMD line hasn't updated
exec bash

# If you update name of the servers also work on updarting the IP -> Hostname
cat /etc/hosts
sudo nano /etc/hosts

-- update the hostname and enter the new name
ctrl + x






















