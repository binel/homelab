# Pi Setup 

These are setup instructions for configuring a new Raspberry pi 

- Flash SD card using the [Raspberry Pi Imager](https://www.raspberrypi.com/software/)
- During the setup process choose to enable ssh 
- During the setup process configure a default user with the name "isaac"
- Once the pi is running, copy pi connection key from laptop to the pi with `ssh-copy-id -i ~/.ssh/pi_ssh_key.pub isaac@ip-address 
- Attempt to ssh in to verify connectivity with `ssh -i ~/.ssh/pi_ssh_key isaac@ip-address
- Add the ip address to ansible/inventory.ini 
- Update the pi using the ansible command `ansible-playbook -i inventory.ini update-pis.yaml
