# SimpleRadio
this hat uses buttons to control the rpt-Receiver hat

    dtc -@ -H epapr -O dtb -o "./SimpleRadio.dtbo" './SimpleRadio-overlay.dts'
    ./eepmake eeprom_settings.txt SimpleRadio.eep ./SimpleRadio.dtbo
set dtparam=i2c_vc=on (rpi3) in /boot/config.txt
    sudo reboot
set the jumper for WP
    sudo ./eepflash.sh -w -f=SimpleRadio.eep -t=24c64