# Setup OpenMediaVault in Raspberry Pi

1. Download and flash Raspberry Pi OS Lite to the MicroSD card, I've used Raspberry Pi Imager for this, you can use other imager like Balena Etcher
https://www.raspberrypi.org/downloads/raspberry-pi-os/

2. Before plugging in the MicroSD card to the Raspberry Pi, it is recommended to enable SSH by creating a file named "ssh" on the drive.

3. Plug in the MicroSD card, Lan Cable, power supply to the Pi and connect to it via SSH (I'm using Putty)

4. Update the Pi and run raspi-config
sudo apt-get update && sudo apt-get upgrade -y
sudo raspi-config
> change password, change hostname, connect to wifi, change timezone
> reboot

5. Install log2ram
https://github.com/azlux/log2ram

echo "deb http://packages.azlux.fr/debian/ buster main" | sudo tee /etc/apt/sources.list.d/azlux.list
wget -qO - https://azlux.fr/repo.gpg.key | sudo apt-key add -
apt update
apt install log2ram

sudo reboot

6. Install OMV
https://pimylifeup.com/raspberry-pi-openmediavault/



