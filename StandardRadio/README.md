# StandardRadio

    dtc -@ -H epapr -O dtb -o "./rpi-receiver.dtbo" './rpi-receiver-overlay.dts'
    ./eepmake eeprom_settings.txt rpi-receiver.eep ./rpi-receiver.dtbo

set dtparam=i2c_vc=on (rpi3) in /boot/config.txt

    sudo reboot

set the jumper for WP

    sudo ./eepflash.sh -w -f=rpi-receiver.eep -t=24c64
