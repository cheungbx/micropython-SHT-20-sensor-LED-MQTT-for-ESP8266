# micropython-SHT-20-sensor-LED-MQTT-for-ESP8266
This is a micropython program written for ESP8266 Node MCU D1 mini to read SHT 20 temperature and humidity sensor and BH1750fvi lux meter.
and post to MQTT broker. Then receive on/off command from MQTT server to control LEDs.
The result is also displayed on the OLED i2C SSD1306

All OLED displya and sensors are connected using a single i2C interface.

* Here are the pin layouts
* led = Pin(14, Pin.OUT) 
* pump = Pin(13, Pin.OUT)
* btnLeft = Pin(12, Pin.IN, Pin.PULL_UP)
* btnDown = Pin(2, Pin.IN, Pin.PULL_UP)
* btnA = Pin(0, Pin.IN, Pin.PULL_UP)
* buzzer = Pin(15, Pin.OUT)


* i2c = I2C(-1, Pin(5), Pin(4))   # SCL, SDA
* display = ssd1306.SSD1306_I2C(128, 64, i2c)
