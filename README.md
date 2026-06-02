**# While in the CLI**
~$ represents the directory we're currently accessing

**#Identify the directory that you're in**
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

# As a part of the above automation, it would be useful to set up the server to automatically restart to complete the installation
# To do this we need to install another package
sudo apt install update-notifier-common
