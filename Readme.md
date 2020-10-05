sudo ./build.sh wifisocket_x4

esptool.py --port /dev/ttyUSB0 --baud 115200 write_flash --flash_mode dout --flash_freq 40m -fs 4MB 0x00000 blank_1MB.bin

esptool.py --port /dev/ttyUSB0 --baud 115200 write_flash --flash_mode dout --flash_freq 40m -fs 4MB 0x00000 sdk/Espressif/ESP8266_BIN154/eagle.flash.bin 0x40000 sdk/Espressif/ESP8266_BIN154/eagle.irom0text.bin 0x3FC000 sdk/Espressif/ESP8266_NONOS_SDK154/bin/esp_init_data_default.bin
