# Raspiducky

A Keyboard emulator like Rubber Ducky build over Raspberry Pi Zero W

### Features:

* Keyboard emulation
* USB Flash Drive emulation
* Expose configuration files over USB Flash disk emulation
* Run payloads over bluetooth

### Configuration

* Flash Raspbian 
* Login as pi, use a screen over HDMI and a keyboard over usb port
* Connect the raspberry to internet over wifi
* Clone the repository

      git clone https://github.com/arrase/Raspiducky.git
 
* Run install script

      cd Raspiducky
      chmod 777 install.sh
      ./install.sh

* Delete the install folder and reboot

      cd ..
      rm -rf Raspiducky
      sudo reboot

### First boot

When Raspiducky boots for first time the configuration is exposed over usb emulation

* Run a payload on boot

      cat payloads-db/open_terminal/open_mint_terminal.dd payloads-db/backdoor/bind_shell.dd > onboot_payload/payload.dd

* Flash drive options

      vim etc/raspiducky.conf
      
### Help

      # raspiducky.py 
      
      usage: raspiducky.py [-h] [--payload PAYLOAD] [--remote] [--address ADDRESS]
                     [--daemon {start,stop,restart}]

      optional arguments:
          -h, --help            show this help message and exit
          --payload PAYLOAD, -p PAYLOAD
                                Path to payload file
          --remote, -r          Run payload on remote device
          --address ADDRESS, -a ADDRESS
                                Remote device address
          --daemon {start,stop,restart}, -d {start,stop,restart}
                                Run as daemon


### Resources:

* Premade Ducky Scripts: https://github.com/hak5darren/USB-Rubber-Ducky/wiki
* Original USB Rubber Ducky: http://usbrubberducky.com/#!index.md

### Credits:

* Duckberry Pi: Jeff L. (Renegade_R - renegade_r65@hotmail.com)
* DroidDucky by Andrej Budincevic (https://github.com/anbud/DroidDucky)
* hardpass by girst (https://github.com/girst/hardpass)
