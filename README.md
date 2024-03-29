# RPIImageManger

# Imaging and Shrinking a Raspbian Image

This will go over how to take an image of a Raspberry Pi, shrink it and reimage it to another Pi. Exactly the same as the original. 

The image can be downloaded from the SharePoint within the 'Realeases' section.

---


## Prerequisites -


1.	Linux system
    -	Will need to have gzip installed
    -	This is for the shrinking script. It is written in bash.
    -    MacOS should also work.

2.	Windows 10
    -    Windows is needed as well as the disk imager used is Windows based. Others could work too, needs to be an .img file.

3.	Drewsif’s PiShrink Github
    -	https://github.com/Drewsif/PiShrink

4.	Win32DiskImager
    -   https://sourceforge.net/projects/win32diskimager/

5.	7zip
        -   https://www.7-zip.org/download.html
        -   To open the compressed image.



## Imaging - 


1.	Once you have completed the setup of the RaspberryPi OS, take the SD card out and use Win32DiskImager to read the card to a file.

2.	Once the image file is saved on the computer, either transfer the file to the Linux computer or open up the Linux subsystem and run the following command on the .img file (this will duplicate the file during the process, make sure there is enough space on the computer to accommodate)
    -	pishrink.sh -vpz /path/to/image.img
    -	This command will shrink the ‘image.img’ and the switches that are set also apply a gzip compression on the image.
    -   #### The 'v' switch can be removed to make the output a bit quieter.

3.	The image file will have a .gz extension added to it automatically.

4.	The shrunken and compressed image can be distributed!



## Decompressing and unshrinking the Image - 


1.	To decompress the file, open up the file in 7zip and extract the .img.

2.	With the decompressed .img file, then open Win32DiskImager and write the file to the SD card.

3.	Put the SD card into the RaspberryPi and boot it up.
    -	On first boot, the filesystem will expand to the original size.
    -   The size of new SD card should exceed the original image size

4.	All of the settings changes and apps that were installed are all available as last seen on the original image.

5.	That’s it!

---
# Installed Items


## Services Enabled 

1. SSH 
2. VNC

## Applications installed

1. MQTTT
2. iPython

