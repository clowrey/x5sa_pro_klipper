# x5sa_pro_klipper
Edit: the printer.cfg firmware in the "archive" folder is for the original Tronxy board, new one is for the BTT Octopus Pro I am currently using. 
This firmware is only for the V6-191121 motherboard - based on instructions here: https://tronxy.fandom.com/wiki/Installing_Klipper

To install firmware place the "update" folder on an SD card and power on the printer, it should update and the screen will stop working. It now will work with Klipper!

Install Mainsail OS https://docs.mainsail.xyz/setup/ on your raspberry pi or other SBC

Use basic Klipper guide's to help you get familiar with how Klipper works... 

Copy the "printer.cfg" file contents into Mainsail OS klipper config either through the web interface or through SSH, SFTP etc.. 

I am currently using Bambulabs Studio fork Softfever with the Tronxy with good results, you can import the config for that from the folder in this repository.
https://github.com/SoftFever/BambuStudio-SoftFever

Old:
Install super slicer https://github.com/supermerill/SuperSlicer/releases

File - Import - Import Config Bundle - and use the bundle in this repository

Video of my nozzle + linear rail + lower endstop contact bed leveling setup:
https://youtu.be/urmSgkl6vnU

Video of it printing before attaching accelerometer and motion shaper:
https://youtu.be/9MZbLJ6z8Nc

