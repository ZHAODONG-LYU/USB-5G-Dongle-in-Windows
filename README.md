# USB-5G-Dongle-in-Windows
This repo recorded the process when you get a 5g module, and want to set up in your windows PC through usb\
 material: quectel RM500U-CN, usb board for 5g module, four antenna 

## Process: 

 1. insert SIM card into the board.
 2. Plug it into the computer.
 3. Install driver called "1_Quectel_UNISOC_5G_Windows_USB_Driver_RNDIS_V1.0.7", which you can find on the Internet. Decompress, click on the "setup.exe".
 4. Install SSM software(any Serial port app), select the "comX USB AT XXX", sent the following commands:
    1. AT+CPIN?
    2. AT+QCFG="usbnet"=,3 
    3. AT+QNETDEVCTL=2,3,1
    4. AT+CFUN=1,1
  5. Wait for some "SMS DONE" feedback, and then replug the usb dongle. 

  `NOTE :  if you are using RM500U, please set 3, if RM500Q, you can set in both 3 and 2. RM500U's performance is a little bit low for 2 -- mbim model`

