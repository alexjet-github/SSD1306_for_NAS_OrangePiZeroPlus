# OLED for OrangePI_OLED
Adding OLED for display system information of NAS based on Orange Pi Zero Plus (H5)

**connection Orange PI Zero Plus:**

| OLED |    Name   |  Pin  |
|:----:|:---------:|:-----:|
|`VDD` |    3.3 V  |   1   |
|`SDA` |   SDA.0   |   3   |
|`SCK` |   SCL.0   |   5   |
|`GND` |    0 V    |   9   |

May work on other H5, H3 and H2+ boards with Armbian.
Use I2C-0 pins. To change I2C bus make corresponding changes in main.c row 127 (`bus = i2c_init((char*)&"/dev/i2c-0", 0x3c);`)

To run app:
1. git clone https://github.com/alexjet-github/SSD1306_for_NAS_OrangePiZeroPlus.git
2. cd ~/SSD1306_for_NAS_OrangePiZeroPlus
3. make
4. sudo ./build/ArmbianOLED

To run app at boot time:
1. sudo crontab -e
2. Add row: @reboot /home/<your username here>/SSD1306/build/ArmbianOLED` ex `@reboot /home/orangepi/SSD1306/build/ArmbianOLED
3. Reboot the board and check the display of information on the OLED

Exellent work with Armbian image [Latest version in archive](https://k-space.ee.armbian.com/archive/orangepizeroplus/archive/) on the board - Orange PI Zero Plus (H5).
[![How it works](https://github.com/vadzimyatskevich/OrangePI_OLED/blob/master/img/pic_1.JPG)]
