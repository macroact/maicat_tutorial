# Maicat Tutorial
## Setting up the Network:

### (Omitt in case of institutional pre-setting) Bluetooth Connection 
When Robot Maicat is turned on and you log in to the Maicat App, the App will search for a nearby Maicat. 
Select the MyCat that appears on the app screen to proceed with the Bluetooth connection. Pairing

### (Omitt in case of institutional pre-setting) Wi-Fi Setting 
From the list of detected networks on the app screen select the network to which you want Maicat to connect to. Enter the correct Wi-Fi password. After a few moments, Maicat will connect to that network and no further settings are required after that.

https://github.com/macroact/maicat_tutorial/assets/103547322/32a52cf4-bc47-4de6-a12d-e5fdab67b557


### Verify Maicat's IP Address
After checking the IP address on the app screen, use it for block-coding or SSH connection.
![ip_address](https://github.com/user-attachments/assets/ea20e087-247a-4dfb-9ae8-8320393a7b24)

#### [For Block-Coding]
Enter the IP address found on the app screen into the IP address field on the block-coding screen. 
![textField](https://github.com/user-attachments/assets/20c33dc7-2284-4e19-b7bb-1ace59cf2284)

If the IP address is entered correctly, you will be connected to Maicat as shown below. 
![textField-connect](https://github.com/user-attachments/assets/331add9d-9f82-4235-b7fc-38cf413181a4)

Then enter the serial number (UUID) of your Maicat into the ID field on the block-coding screen.
![textField-connect](https://github.com/user-attachments/assets/331add9d-9f82-4235-b7fc-38cf413181a4)
![textField-id](https://github.com/user-attachments/assets/cca81aec-3836-4188-b3ce-5b24489ae279)

#### [For Ubuntu]
Open a terminal window and enter the corresponding IP address "ssh maicat@IPaddress" as well as the host name "ssh maicat@maibot1.local" and press enter.<br/>
In general, the hostname is the last digit of the serial number (UUID) you received and set to "maibot(last digit).local".
```
ssh maicat@192.168.0.1
```
and
```
ssh maicat@maibot1.local
```

&nbsp;
[Next - The eyes of maicat](../02_maicat_eyes/README.md)
