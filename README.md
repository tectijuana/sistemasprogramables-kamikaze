# sistemasprogramables-kamikaze
sistemasprogramables-kamikaze created by GitHub Classroom

 Sensores de sonido: micrófono

<a href="https://cooltext.com"><img src="https://images.cooltext.com/5387875.png" width="921" height="115" alt=" Sensores de sonido: micrófono" /></a>
<br />Image by <a href="https://cooltext.com">Cool Text: Free Logos and Buttons</a> - <a href="https://cooltext.com/Edit-Logo?LogoID=3509961347">Create An Image Just Like This</a>

| Nombre                               | Participacion                 | Calificación |
|--------------------------------------|-------------------------------|--------------|
| Acevedo Cardona Adelaid Lesdeymariet | Modulo KY-038 Sensor de Micrófono/Sonido |              | 
| Encarnacion Ocampo Gustavo           | Modulo KY-037 Sensor de Micrófono/Sonido (Alta Sensibilidad) |              | 
| Gallardo Dueñas Carlos Ivan          | Modulo KY-012 Sensor Zumbador Activo |              | 
| Portilla Amparan Josue               | Modulo KY-006 Sensor Zumbador Pasivo |              | 

# Módulo KY-037 Sensor de Micrófono (Alta Sensibilidad)

![alt text](http://sensorkit.en.joy-it.net/images/8/8e/ky-037.jpg "KY-037 Microphone sensor module (high sensitivity)")

## ¿Qué es el sensor KY-037?
Este módulo Ky-037 Sensor De Sonido permite detectar cualquier tipo de sonido superior al rango ajustado por el potenciómetro que lleva este. También permite obtener dos salidas, una análoga, que lleva toda la información que está detectando el micrófono y una digital que es una salida de encendido o apagado que se activa cuando el sonido supera un cierto volumen establecido por el potenciómetro.

## Datos técnicos 
**Salida digital:** Puede usar un potenciómetro para configurar un valor extremo para el sonic. Si el valor excede el valor extremo, enviará una señal a través de la salida digital.

**Salida analógica:** Señal directa del micrófono como valor de voltaje.

**LED1:** Muestra que el sensor recibe voltaje.
**LED2:** Muestra que se detectó un campo magnético.

## ESPECIFICACIONES TÉCNICAS.

1. Modelo: KY-037
2. Voltaje de funcionamiento: 5 Volts
3. Salidas: Analógica y digital
4. Permite ajustar un nivel de umbral de salida
5. Usa el Micrófono Gao Gan grado, de alta sensibilidad.
6. Tiene un indicador LED de encendido
7. Tiene un LED que indica la salida del comparador
8. Interruptor digital salida (0 / 1)
9. Temperatura: -40 a +85 °C
10. Dimensiones: 35 x 15 x 14 mm
11. Peso: 4 gr

## Pinout
![alt text](http://sensorkit.en.joy-it.net/images/d/d8/4_dig_V_G_An_eng.png "pinout")

## Funcionalidad del sensor.
El sensor tiene 3 componentes principales en su placa de circuito. Primero, la unidad de sensor en la parte frontal del módulo que mide el área físicamente y envía una señal analógica a la segunda unidad, el amplificador. El amplificador amplifica la señal, de acuerdo con el valor resistente del potenciómetro, y envía la señal a la salida analógica del módulo.
El tercer componente es un comparador que apaga la salida digital y el LED si la señal cae por debajo de un valor específico.
Puede controlar la sensibilidad ajustando el potenciómetro.
![alt text](http://sensorkit.en.joy-it.net/images/d/de/sens-poti.jpg "fun-sen")

## Codigo Ejemplo en Arduino
El programa lee el valor de voltaje actual que se medirá en el pin de salida y lo muestra a través de la interfaz en serie.
Además de eso, el estado del pin digital se mostrará en el terminal, lo que significa si se superó o no el valor extremo.
```C++
// Declaration and initialization of the input pin
int Analog_Eingang = A0; // X-axis-signal
int Digital_Eingang = 3; // Button
  
void setup ()
{
  pinMode (Analog_Eingang, INPUT);
  pinMode (Digital_Eingang, INPUT);
       
  Serial.begin (9600); // Serial output with 9600 bps
}
  
// The program reads the current value of the input pins
// and outputs it via serial out
void loop ()
{
  float Analog;
  int Digital;
    
  // Current value will be read and converted to voltage
  Analog = analogRead (Analog_Eingang) * (5.0 / 1023.0); 
  Digital = digitalRead (Digital_Eingang);
    
  //... and outputted here
  Serial.print ("Analog voltage value: "); Serial.print (Analog, 4);  Serial.print ("V, ");
  Serial.print ("Extreme value: ");
  
  if(Digital==1)
  {
      Serial.println (" reached");
  }
  else
  {
      Serial.println (" not reached yet");
  }
  Serial.println ("----------------------------------------------------------------");
  delay (200);
}
```
**Conecciones al Arduino.**
| KY-037      | Arduino |  
|-----------------|---------|
|  Señal digital  |  Pin 3  |
|        +V       |  Pin 5V |   
|       GND       | Pin GND |   
| Señal analógica |  Pin 0  |  

## Codigo Ejemplo en Raspberry Pi
El programa lee los valores actuales de los pines de entrada y los emite en el terminal en [mV].
Además de eso, el estado del pin digital se mostrará en la terminal para mostrar si se superó o no el valor extremo.
```Python
#############################################################################################################
### Copyright by Joy-IT
### Published under Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License
### Commercial use only after permission is requested and granted
###
### KY-053 Analog Digital Converter - Raspberry Pi Python Code Example
###
#############################################################################################################
 
 
# This code is using the ADS1115 and the I2C Python Library for Raspberry Pi
# This was published on the following link under the BSD license
# [https://github.com/adafruit/Adafruit-Raspberry-Pi-Python-Code]
from Adafruit_ADS1x15 import ADS1x15
from time import sleep
 
# import needed modules
import math, signal, sys, os
import RPi.GPIO as GPIO
GPIO.setmode(GPIO.BCM)
GPIO.setwarnings(False)
 
# initialise variables
delayTime = 0.5 # in Sekunden
 
# assigning the ADS1x15 ADC
 
ADS1015 = 0x00  # 12-bit ADC
ADS1115 = 0x01  # 16-bit
 
# choosing the amplifing gain
gain = 4096  # +/- 4.096V
# gain = 2048  # +/- 2.048V
# gain = 1024  # +/- 1.024V
# gain = 512   # +/- 0.512V
# gain = 256   # +/- 0.256V
 
# choosing the sampling rate
# sps = 8    # 8 Samples per second
# sps = 16   # 16 Samples per second
# sps = 32   # 32 Samples per second
sps = 64   # 64 Samples per second
# sps = 128  # 128 Samples per second
# sps = 250  # 250 Samples per second
# sps = 475  # 475 Samples per second
# sps = 860  # 860 Samples per second
 
# assigning the ADC-Channel (1-4)
adc_channel_0 = 0    # Channel 0
adc_channel_1 = 1    # Channel 1
adc_channel_2 = 2    # Channel 2
adc_channel_3 = 3    # Channel 3
 
# initialise ADC (ADS1115)
adc = ADS1x15(ic=ADS1115)
 
# Input pin for the digital signal will be picked here
Digital_PIN = 24
GPIO.setup(Digital_PIN, GPIO.IN, pull_up_down = GPIO.PUD_OFF)
  
#############################################################################################################
  
# ########
# main program loop
# ########
# The program reads the current value of the input pin
# and shows it at the terminal
  
try:
        while True:
                #Current values will be recorded
                analog = adc.readADCSingleEnded(adc_channel_0, gain, sps)
  
                # Output at the terminal
                if GPIO.input(Digital_PIN) == False:
                        print "Analog voltage value:", analog,"mV, ","extreme value: not reached"
                else:
                        print "Analog voltage value:", analog, "mV, ", "extreme value: reached"
                print "---------------------------------------"
  
                sleep(delayTime)
  
  
  
except KeyboardInterrupt:
        GPIO.cleanup()
```
**Conecciones al Raspberry Pi.**
| KY-037      |  | Raspberry Pi                      |   
|-----------------|----------|---------------------------|
| Señal digital   | GPIO24   | Pin 18 (RPi)              |   
| +V              | 3,3V     | Pin 1 (RPi)               |   
| GND             | GND      | Pin 06 (RPi)              |   
| Señal analógica | Analog 0 | Pin A0 (ADS1115 - KY-053) |  


# Modulo KY-012 Sensor Zumbador Activo

![alt text](https://images-na.ssl-images-amazon.com/images/I/71Fu2Fr4f6L._SX425_.jpg "KY-012 Sensor Zumbador Activo")

El módulo KY-012 Active Buzzer consta de un zumbador piezoeléctrico activo, que genera un sonido de aproximadamente 2,5 kHz cuando la señal es alta. 

| Tensión de funcionamiento      | 3.5V ~ 5.5V                       |
|--------------------------------|-----------------------------------|
| Corriente máxima               | 30mA / 5VDC                       |
| Frecuencia de resonancia       | 2500Hz ± 300Hz                    |
| Salida de sonido mínima        | 85Db @ 10cm                       |
| Temperatura de trabajo         | -20°C ~ 70°C [-4°F ~ 158°F]       |
| Temperatura de almacenamiento  | -30°C ~ 105°C [-22°F ~ 221°F]     |
| Dimensiones                    | 18.5mm x 15mm [0.728in x 0.591in] |


## DIAGRAMA DE CONEXIÓN KY-012
Conecte la señal (S) al pin 8 del Arduino y tierra (-) a GND. Tenga en cuenta que algunas placas están mal etiquetadas, intente invertir los cables si no puede escuchar ningún sonido al ejecutar el boceto.

### arduino
| KY-012 | arduino |
|--------|---------|
| S      | pin 8   |
| -      | GND     |

![alt text](https://arduinomodules.info/wp-content/uploads/Arduino_KY-012_Keyes_Active_buzzer_module_connection_diagram.png "KY-012 diagrama de conexion")
### raspberry pi
| Sensor Signal | = GPIO24 | Pin 18 |
|---------------|----------|--------|
| Sensor [+V]   | = 3.3V   | Pin 1  |
| Sensor GND    | = GND    | Pin 6  |

![alt text](https://cdn.thegeekpub.com/wp-content/uploads/2019/05/KY-012-Active-Piezo-Buzzer-Module-wiring-diagram-raspberry-pi.jpg "KY-012 diagrama de conexion")

## ¿Qué es un buzzer o zumbador?

El zumbador o buzzer es un dispositivo electrónico que permite producir diferentes sonidos ya sea de manera continua o de forma intermitente puede ser del mismo tono, este dispositivo lo puedes encontrar en tarjetas electrónicas, computadoras, multimetros, etc.

El modulo KY-012 integra un zumbador activo, este incorpora un oscilador simple por lo que únicamente es necesario suministrar corriente al dispositivo para que emita sonido. La diferencia de un buzzer activo a un pasivo es que el pasivo necesita recibir una onda de frecuencia.

## ¿Como funciona un buzzer?

Para entender como funciona el KY-012 debes tener encenta como esta construido, este consta de dos elementos, un electroimán o disco piezoeléctrico y una lámina metálica de acero.

Cuando se acciona, la corriente pasa por la bobina del electroimán y produce un campo magnético variable que hace vibrar la lámina de acero sobre la armadura, o bien, la corriente pasa por el disco piezoeléctrico haciéndolo entrar en resonancia eléctrica y produciendo ultrasonidos que son amplificados por la lámina de acero.

Para lograr obtener diferentes sonidos debes elaborar un circuito electrónico o bien programarlo con un microcontrolador, este modulo es compatible con la placa Arduino uno el cual te permitirá lograr distintos tonos.

## CÓDIGO DE EJEMPLO KY-012 EN ARDUINO 

El siguiente Arduino Sketch activará y desactivará continuamente el zumbador, generando una serie de pitidos cortos y agudos.


```c++
 int buzzerPin = 8;   
 void setup ()  
   {  pinMode (buzzerPin, OUTPUT);  }  
 void loop ()  
   {  
   digitalWrite (buzzerPin, HIGH);  
   delay (500);  
   digitalWrite (buzzerPin, LOW);  
   delay (500);  
   } 
 ```
## CÓDIGO DE EJEMPLO KY-012 EN RASPBERRY PI
En este ejemplo, verá cómo, con un pin de salida definido, el zumbador estará encendido durante 4 segundos y luego estará apagado durante 2 segundos.

```python
import RPi.GPIO as GPIO
import time
    
GPIO.setmode(GPIO.BCM)
    
# Output pin declaration for the Buzzer.
Buzzer_PIN = 24
GPIO.setup(Buzzer_PIN, GPIO.OUT, initial= GPIO.LOW)
    
print ("Buzzer-test [press ctrl+c to end the test]")
   
# Main program loop
try:
        while True:
            print("Buzzer will be on for 4 seconds")
            GPIO.output(Buzzer_PIN,GPIO.HIGH) #Buzzer will be switched on
            time.sleep(4) #Waitmode for 4 seconds
            print("Buzzer wil be off for 4 seconds") 
            GPIO.output(Buzzer_PIN,GPIO.LOW) #Buzzer will be switched off 
            time.sleep(2) #Waitmode for another 2 seconds in which the buzzer will be off
    
# Scavenging work after the end of the program
except KeyboardInterrupt:
        GPIO.cleanup()
 ```
# Modulo KY-006 Sensor Zumbador Pasivo
![alt text](https://arduinomodules.info/wp-content/uploads/KY-006_passive_buzzer_arduino_module.jpg)

Este modulo consiste en un zumbador piezoeléctrico pasivo, puede generar tonos entre 1.5 a 2.5 kHz al encenderlo y apagarlo a diferentes frecuencias, ya sea mediante retardos o PWM

| Tensión de funcionamiento      | 1.5V ~ 15V DC                       |
|--------------------------------|-----------------------------------|
| Rango de generacion de tonos   | 1.5 ~ 2.5kHz                      |
| Dimensiones                    | 18.5mm x 15mm [0.728in x 0.591in] |

## Diagrama de conexión KY-006
Conecte la señal (S) al pin 8 en el Arduino y la tierra (-) a GND. El pin central no se usa.

![alt text](http://arduinomodules.info/wp-content/uploads/Arduino_KY-006_Keyes_Passive_buzzer_module_connection_diagram.png)

## Raspberry Pi

| Modulo Signal | Pin 18 |
|---------------|--------|
| Modulo Vcc+   | Pin 1  |
| Sensor GND    |  GND   |

![alt text](https://cdn.thegeekpub.com/wp-content/uploads/2019/05/KY-006-passive-piezo-buzzer-wiring-diagram-Raspberry-Pi.jpg)

## CÓDIGO DE EJEMPLO KY-006 EN ARDUINO 

El siguiente boceto Arduino generará dos tonos diferentes encendiendo y apagando el zumbador KY-006 a diferentes frecuencias


```c++
 int buzzer = 8; 
 // set the buzzer control digital IO pin    
 void setup() {  pinMode(buzzer, OUTPUT); // set pin 8 as output  }   
 void loop() {  for (int i = 0; i < 80; i++) 
 {  // make a sound   
 digitalWrite(buzzer, HIGH); 
 // send high signal to buzzer   
 delay(1); 
 // delay 1ms   
 digitalWrite(buzzer, LOW); 
 // send low signal to buzzer   
 delay(1);  }  
 delay(50);  
 for (int j = 0; j < 100; j++) { //make another sound   
 digitalWrite(buzzer, HIGH);
 delay(2); // delay 2ms   
 digitalWrite(buzzer, LOW); 
 delay(2); 
 }  delay(100);  }  
 ```
 
 ## CÓDIGO DE EJEMPLO KY-006 EN RASPBERRY PI
 El siguiente codigo de ejmplo crea una señal de alarma clasica en el buzzer ciclando los tonos arriba y abajo. 
 
 ```python
# import modules
import RPi.GPIO as GPIO
GPIO.setmode(GPIO.BCM)
  
# define the pin we will attach to
GPIO_PIN = 18
GPIO.setup(GPIO_PIN, GPIO.OUT)
 
# start at 50 hertz 
GPFrequency = 50
pwm = GPIO.PWM(GPIO_PIN, GPFrequency)
pwm.start(50)
 
    while(True):
        for GPFrequency in range(5000):
            pwm.ChangeFrequency(GPFrequency)
 ```
