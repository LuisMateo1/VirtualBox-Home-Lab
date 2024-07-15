# VBox-Home-Lab

<h>Creating a Home Lab using VirtualBox</h>

In this lab, I will create two virtual machines using VirtualBox, and configure the network settings to allow those two machines to communicate with each other only, and not connect to the internet.

After downloading all the necessary files I checked the file hashes and confirmed it matched the checksum on the website to make sure the file was not changed in transit.

Hash for VirtualBox
![Screenshot 2024-07-15 100539](https://github.com/user-attachments/assets/86260844-66f7-4a6a-b107-4f9b2d939d5f) 
![Screenshot 2024-07-15 105406](https://github.com/user-attachments/assets/6d9d2dd0-4e17-433e-8c9e-f7a3054070f9)

Hash for Kali
![Screenshot 2024-07-15 105301](https://github.com/user-attachments/assets/b469a36b-5c77-4110-9856-3424791691f7)

Hash for Mr.Robot vulnerable machine
![Screenshot 2024-07-15 110858](https://github.com/user-attachments/assets/9936502b-e9ae-4828-93cc-ac6f9ee17767)

It might be unnecessary in this case, but it is good practice to check file hashes to confirm the integrity of a downloaded file

The default Kali credentials are kali/kali

![Screenshot 2024-07-15 112121](https://github.com/user-attachments/assets/713d3ff7-0d2a-489e-8497-ba9f79b7cd77)

Before I isolate this VM from the internet I will make sure that all distribution files are up to date
![Screenshot 2024-07-15 113057](https://github.com/user-attachments/assets/2d8993c4-0b5c-4c3a-8121-a424db40045b)

sudo apt update will search for any new packages that can be updated, and sudo apt upgrade will install those new packages. 

In this case, I used dist-upgrade because I haven't yet made any changes to this VM so any distribution changes will not negatively affect any changes I could have made. In the future, I can just do 'sudo apt upgrade'

Now I can create a snapshot of the current state of this VM and return to it if I ever need to return to a stable state.
![Screenshot 2024-07-15 114848](https://github.com/user-attachments/assets/85d37e24-69e5-4788-b5b0-5436b5592564)


To isolate the VM's I need to create a DHCP server on the host machine whice will asign IP address to the VM's
