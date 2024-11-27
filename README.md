# Nombres-en-la-pantalla-LCDI2C-

import machine
import time
import lcd
from machine import Pin, I2C

# Inicializar I2C
i2c = I2C(0, scl=Pin(22), sda=Pin(21), freq=400000)  # GPIO22 para SCL, GPIO21 para SDA

# Inicializar pantalla LCD (en este caso una LCD 16x2)
lcd = lcd.LCD(i2c)

# Configurar el LCD
lcd.clear()  # Limpiar la pantalla
lcd.putstr("Hola Mundo!")  # Mostrar un mensaje

# Mostrar nombres en la pantalla
time.sleep(2)  # Espera 2 segundos antes de cambiar el texto
lcd.clear()
lcd.putstr("Nombre 1: mateo g")  # Primer nombre
time.sleep(2)  # Espera 2 segundos
lcd.clear()
lcd.putstr("Nombre 2: luis naula)  # Segundo nombre
time.sleep(2)  # Espera 2 segundos
lcd.clear()

