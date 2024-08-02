# USB-5G-Dongle-in-Windows 
This repo recorded the process when you get a 5g module, and want to set up in your windows PC (windows 10 and 11) through usb\
 material: quectel RM500U-CN, usb board for 5g module, four antenna 

## Process

 1. insert SIM card into the board.
<p align="center">
    <img src="https://github.com/user-attachments/assets/16680a3f-cec9-44d4-8958-581b6489f6f6" alt="3c692c26950ceb1801e6f5a4a923d5e" width="500" height="300">
</p>
    
<p align="center">
    <img src="https://github.com/user-attachments/assets/ac0e3d16-809e-4e3e-bcfd-1dd1131c134b" alt="30c23b753dee50292f86613765af468" width="500" height="300">
</p>

 2. Plug it into the computer.
 3. Install driver called "1_Quectel_UNISOC_5G_Windows_USB_Driver_RNDIS_V1.0.7", which you can find on the Internet. Decompress, click on the "setup.exe".
 4. Install SSM software(any Serial port app), select the "comX USB AT XXX", sent the following commands:
    1. AT+CPIN?
    2. AT+QCFG="usbnet"=,3 
    3. AT+QNETDEVCTL=2,3,1
    4. AT+CFUN=1,1
  5. Wait for some "SMS DONE" feedback, and then replug the usb dongle. 

  `NOTE :  if you are using RM500U, please set 3, if RM500Q, you can set in both 3 and 2. RM500U's performance is a little bit low for 2 -- mbim model`
## Reference
[1] [Chinese doc](https://www.waveshare.net/wiki/RM500U-CN_5G_HAT#Windows_.E7.B3.BB.E7.BB.9FRNDIS_.E6.8B.A8.E5.8F.B7.E4.B8.8A.E7.BD.91)
