# My Raspberry Pi

> A short record of my first Raspverry Pi

---
### Receive my package

![rasppi](https://raw.githubusercontent.com/wq-peng/repo_image/master/raspberrypi/package.jpg)

---
## 1. Download the system image
Cause I am going to use Rospberry Pi with SSH, I just choose the Lite version iamge.

![image](https://raw.githubusercontent.com/wq-peng/repo_image/master/raspberrypi/image.png)

## 2. Move the image to the SD card
Fisrtly check the location of the SD card.  
`diskutil list`

![disk](https://raw.githubusercontent.com/wq-peng/repo_image/master/raspberrypi/disk.png)

Then unmount the SD card  
`diskutil unmountDisk "location"`

![umount](https://raw.githubusercontent.com/wq-peng/repo_image/master/raspberrypi/umount.png)

Finally move using `dd`  
`sudo dd if="image location" of="SD location" bs=1m`

![dd](https://raw.githubusercontent.com/wq-peng/repo_image/master/raspberrypi/dd.png)

Creat an empty file `"SSH"` to allow ssh connection initially.

## 3. Start up 
1. Insert the SD card into Raspberry Pi
2. Connect the Ehernet cable
3. Plug the USB power line

![pi](https://raw.githubusercontent.com/wq-peng/repo_image/master/raspberrypi/1.jpg)

connect to Raspberry Pi with SSH  
`ssh pi@raspberrypi.local`

![ssh](https://raw.githubusercontent.com/wq-peng/repo_image/master/raspberrypi/ssh.png)

`Hello, Raspberry Pi`

![hello](https://raw.githubusercontent.com/wq-peng/repo_image/master/raspberrypi/hello.png)