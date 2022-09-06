# How to add WIFI

1. Donwload flashing tools for ESP8266
    https://espressif.com/en/support/download/other-tools?keys=&field_type_tid%5B%5D=14
2. Download ESP-Link firmware 
    https://github.com/jeelabs/esp-link/releases
3. Flash the ESP (GPI0 <--> GND on connecting)

    |File |Addresses|
    |-----|---------|
    |blank.bin | 0xFE000|
    |esp_init_data_default.bin | 0XFC000|
    |boot_v1.6.bin | 0X0 |
    |user1.bin | 0X1000 |

    |Setting | Value|
    |-----|---------|
    |SPI SPEED | 26.7MHz|
    |SPI MODE | DOUT|
    |DoNotChgBin | Unchecked |
    |BAUD | 115200 |

    Actions:
    1) Erase
    2) START
    
4) Restart your ESP (CH_PD <--> VCC)
5) Connect to network ESP-*
6) Open 192.168.4.1 in the web browser
7) Configure WIFI SSID & Password
8) Wire ESP to DLC32 as showed on the diagram 
9) In LaserGRBL connect using Telnet (port 23)
