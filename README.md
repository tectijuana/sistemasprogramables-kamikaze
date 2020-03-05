# sistemasprogramables-kamikaze
sistemasprogramables-kamikaze created by GitHub Classroom

 Sensores de sonido: micrófono

<a href="https://cooltext.com"><img src="https://images.cooltext.com/5387875.png" width="921" height="115" alt=" Sensores de sonido: micrófono" /></a>
<br />Image by <a href="https://cooltext.com">Cool Text: Free Logos and Buttons</a> - <a href="https://cooltext.com/Edit-Logo?LogoID=3509961347">Create An Image Just Like This</a>

| Nombre                               | Participacion                 | Calificación |
|--------------------------------------|-------------------------------|--------------|
| Acevedo Cardona Adelaid Lesdeymariet | Módulo KY-038 Sensor de Micrófono/Sonido |              | 
| Encarnacion Ocampo Gustavo           | Módulo KY-037 Sensor de Micrófono/Sonido (Alta Sensibilidad) |              | 
| Gallardo Dueñas Carlos Ivan          | Módulo KY-012 Sensor Zumbador Activo |              | 
| Portilla Amparan Josue               | Módulo KY-006 Sensor Zumbador Pasivo |              | 

# ¿Qué es un Micrófono?
Un micrófono es un transductor que convierte las ondas sonoras en señales eléctricas. Podemos conectar un micrófono a un microcontrolador como Arduino o un microprocesador como Raspberry Pi para detectar sonidos.

La salida producida por un micrófono es una señal eléctrica analógica que representa el sonido recibido. Sin embargo, en general, esta señal es demasiado baja para ser medida y tiene que ser amplificada.

![](https://www.luisllamas.es/wp-content/uploads/2016/11/arduino-microfono-ky-038-funcionamiento.png)

Existen placas como la **KY-038** que incorporan un micrófono junto con un comparador **LM393**, que permite obtener la lectura **tanto como un valor analógico como de forma digital.**

El uso habitual de este tipo de sensores no amplificados es emplear la salida digital para detectar el sonido cuando este supera un cierto umbral, regulado a través de un potenciómetro ubicado en la placa.

La salida analógica permite obtener una estimación del volumen registrado. Sin embargo, como hemos comentado, este tipo de módulos con micrófono no resultan adecuados para medir el sonido de forma analógica ya que carecen de amplificación.

Si solo queremos detectar el sonido, y no medirlo, este tipo de sensores son más apropiados ya que únicamente requieren la lectura de una señal digital, sin necesitar realizar más cálculos.

Este tipo de sensores pueden ser útiles, por ejemplo, para encender un dispositivo cuando se detecte sonido, encender una lámpara con una palmada, o incluso orientar un robot o una torre con servos mediante sonido.

# Precio

Este tipo de sensores son muy baratos. Podemos encontrar módulos con micrófono como los **KY-037** o **KY-038** por unos **0.80€** o **25.00 MXN**, buscando en vendedores internacionales de **eBay** o **AliExpress.**

Según el modelo el micrófono puede estar instalado apuntando hacia el frente o hacia arriba, pero la electrónica es la misma. Elegiremos uno u otro según resulta más conveniente para nuestro proyecto.

![](https://www.luisllamas.es/wp-content/uploads/2016/11/arduino-microfono-ky-038-componete.png)

El precio de este tipo de sensores es muy reducido, pero debemos tener en cuenta que por un precio similar podemos encontrar sensores amplificados como el **MAX9812.**

Escoger entre uno u otro, como hemos comentado, depende de únicamente si queremos detectar sonido o si queremos medirlo, en cuyo caso optaríamos por módulo amplificado. Ante la duda, los módulos amplificados son más versátiles e interesantes.

# Módulo KY-038 Sensor de Micrófono/Sonido

![](https://cdn-global-hk.hobbyking.com/media/catalog/product/cache/4/image/660x415/17f82f742ffe127f42dca9de82fb58b1/legacy/catalog/84763_high.jpg)

## ¿Qué es el Sensor KY-038?
El sensor KY-038 tiene como característica que es altamente sensible, por lo que su sensor de micrófono de condensador electret (EC) permite detectar un mínimo ruido producido en el ambiente, cuenta con un LED indicador de suministro de energía y por el otro extremo cuenta con otro que indica la salida. También permite obtener dos salidas, una análoga, que lleva toda la información que está detectando el micrófono y una digital que es una salida de encendido o apagado que se activa cuando el sonido supera un cierto volumen establecido por el potenciómetro.
## ¿Cómo Funciona el Sensor KY-038?
Este Sensor puede detectar sonido, consiste en el funcionamiento de un detector de ondas sonoras, dichas ondas son recibidas en forma de energía y son enviadas mediante señales eléctricas hacia un aparato receptor/codificador.

Este sensor la señal que nos entrega es digital y analógica, lo cual nos permite decidir cuál utilizar según nuestras necesidades. Si necesitamos saber el valor del sensor, podremos utilizar directamente la salida analógica para conseguir los datos. Sino, podemos utilizar la salida digital, la cual se activa o se desactiva según si el sensor llega a medir la intensidad del sonido que le configuremos, mediante la definición de la sensibilidad del sensor.
## Especificaciones Técnicas
* **Modelo:** KY-038
* **Voltaje de Funcionamiento:** 4 a 6 V DC
* **Distancia Máxima de Inducción:** 0.5 metros.
* **Chip Principal:** LM393
* **Micrófono:** Electret
* **Gama de Frecuencias:** 100 – 10.000 Hz.
* **Sensibilidad:** – 46 ± 2,0, (0dB = 1V / Pa) a 1K Hz.
* **La Sensibilidad Mínima a Ruido:** 58 dB
* **Dimensiones:** 36 x 15 x 15 mm
* **Peso:** 4 gr
## Esquemático
![](https://www.cdmxelectronica.com/wp-content/uploads/ky-037-1.png)
## Footprint
![](https://image.easyeda.com/histories/38502a05c3184a8d8013fc684f3c1b41.png)
### BOM
| ID |         Name         | Designator | Footprint | Quantity |
|:--:|:--------------------:|:----------:|:---------:|:--------:|
|  1 | Header-Male-2.54_1x4 |     P1     |     [	HDR-4X1/2.54](https://easyeda.com/component/b73ecc946600486997b70f149e556e90)      |     1    |
|  2 |         100k         |     VR1    |      [	TRIMMER_DIPLOHM_P94	](https://easyeda.com/component/92c24b29f73742238d4068ca2042695c)     |     1    |
|  3 |         100k         |    R2,R6   |      [	0603-RES](https://easyeda.com/component/ee9454430f3e424ca64697f854490218)     |     2    |
|  4 |          150         |     R3     |      [	0603-RES](https://easyeda.com/component/ee9454430f3e424ca64697f854490218)     |     1    |
|  5 |          1k          |     R5     |      [	0603-RES](https://easyeda.com/component/ee9454430f3e424ca64697f854490218)     |     1    |
|  6 |          10K         |    R1,R4   |      [0603-RES](https://easyeda.com/component/ee9454430f3e424ca64697f854490218)     |     2    |
|  7 |       ELECTRET       |     Q1     |      [	9.7ELECTRET](https://easyeda.com/component/94f13822d23544388e27c09f91158287)     |     1    |
|  8 |    LEDCHIPLED_0603   |    L2,L1   |      [	CHIPLED_0603](https://easyeda.com/component/4739d2832cee4e328e7eef0e9eae99b6)     |     2    |
|  9 |         LM393        |     U1     |      [	SO08](https://easyeda.com/component/008cfe86cc5d4e94ad9fffdb083aa72a)     |     1    |
## Esquema de Montaje
El esquema eléctrico es sencillo. Alimentamos el módulo conectando GND y 5V a los pines correspondientes de Arduino.

Ahora si queremos usar la lectura digital, conectamos la salida DO a una de las [entradas digitales](https://www.luisllamas.es/entradas-digitales-en-arduino/) de Arduino.

![](https://www.luisllamas.es/wp-content/uploads/2016/11/arduino-microfono-montaje.png)

Deberemos calibrar el umbral de disparo de la salida digital con el potenciómetro instalado en el módulo para el nivel de sonido deseado.

Mientras que la conexión vista desde Arduino quedaría así:

![](https://www.luisllamas.es/wp-content/uploads/2016/11/arduino-microfono-montaje-esquema.png)

Si quisiéramos emplear el valor analógico, simplemente conectaríamos la salida AO del sensor a una [entrada analógica](https://www.luisllamas.es/entradas-analogicas-en-arduino/) de Arduino. Aunque, como hemos dicho, en este caso sería mejor optar por un modelo amplificado.
## Ejemplos de Código en Arduino 
En el primer ejemplo de código, empleamos la señal digital del sensor para encender el LED integrado en Arduino si se detecta sonido, y apagarlo en caso contrario.
```c++
const int pinLED = 13;
const int pinMicrophone = 9;
 
void setup ()
{
  pinMode (pinLED, OUTPUT);
  pinMode (pinMicrophone, INPUT);
}
 
void loop ()
{
  bool soundDetected = digitalRead(pinMicrophone);
  if (soundDetected)
  {
    digitalWrite (pinLED, HIGH);
    delay(1000);
  }
  else
  {
    digitalWrite (pinLED, LOW);
    delay(10);
  }
}
```
En el siguiente ejemplo almacenamos un estado (ON/OFF) y hacemos que varíe cada vez que se detecte un sonido. En el ejemplo empleamos el estado para encender o apagar el LED integrado, pero en un caso real realizaríamos las acciones oportunas como activar un relé.
```c++
const int pinLED = 13; 
const int pinMicrophone = 9;
bool state;
 
void setup()
{
  pinMode(pinLED, OUTPUT);
  pinMode(pinMicrophone, INPUT_PULLUP);
}
 
void loop()
{
  bool soundDetected = digitalRead(pinMicrophone); 
  if (soundDetected == true)
  {
    state = ! state;    
    digitalWrite(pinLED , state);
    delay (1000);
  }
  delay(10);
}
```
Este último ejemplo lee el valor de voltaje actual que se medirá en el pin de salida y lo muestra a través de la interfaz en serie.

Además de eso, el estado del pin digital se mostrará en el terminal, indicándonos si se superó o no el valor extremo.
```c++
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
  Serial.print ("Analog voltage value:"); Serial.print (Analog, 4);  Serial.print ("V, ");
  Serial.print ("Extreme value:");
  
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
### Conexiones Arduino 
**Señal Digital** = Pin 3<br/>
**+V**            = Pin 5V<br/>
**GND**           = Pin GND<br/>
**Señal Análoga** = Pin 0
### Descargar Programa de Ejemplo
[ARD_Analog-Sensor](http://sensorkit.en.joy-it.net/images/3/34/ARD_Analog-Sensor.zip)
## Ejemplo de Código en Raspberry Pi 
_**!! Atención !!**  Sensor Análogo  **!! Atención !!**_

A diferencia de Arduino, el Raspberry Pi no proporciona un ADC (Convertidor Digital Analógico) en su chip. Esto limita al Raspbery Pi si desea utilizar un sensor no digital.

Para evadir esto, es importante utilizar el **Sensorkit x40** con el módulo **KY-053**, que proporciona un ADC de 16 bits que se puede usar con el Raspberry Pi para actualizarlo con 4 pines de entrada analógica adicionales. Este módulo está conectado a través de I2C al Raspberry Pi. Mide los datos analógicos y los convierte en una señal digital adecuada para Raspberry Pi.

Por lo tanto, recomendamos utilizar el **ADC KY-053** si desea utilizar sensores analógicos junto con Raspberry Pi.
Para obtener más información, consulte el infosite: [Convertidor Digital Analógico KY-053](http://sensorkit.en.joy-it.net/index.php?title=KY-053_Analog_Digital_Converter&action=view) 

_**!! Atención !!**  Sensor Análogo  **!! Atención !!**_

El programa utiliza las bibliotecas de python ADS1x15 e I2C específicas de la empresa Adafruit para controlar el ADS1115 ADC. Puede encontrarlos aquí: [Adafruit-Raspberry-Pi-Python-Code](https://github.com/adafruit/Adafruit-Raspberry-Pi-Python-Code) publicado bajo [BSD License](https://opensource.org/licenses/BSD-3-Clause). Puede encontrar las bibliotecas necesarias en el paquete de descarga inferior.

El programa lee los valores actuales de los pines de entrada y los emite en el terminal en [mV].

Además de eso, el estado del pin digital se mostrará en la terminal para mostrar si se superó o no el valor extremo.
```python
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
### Conexiones Raspberry Pi
**Sensor:**<br/>

* **Señal Digital**	=	GPIO 24	[Pin 18 (RPi)]<br/>
* **+ V**	                =	3,3V	[Pin 1 (RPi)]<br/>
* **GND**	                =	GND	[Pin 06 (RPi)]<br/>
* **Señal Análoga**	=	0 Análogo	[Pin A0 (ADS1115 - KY-053)]<br/>

**ADS1115 - KY-053:**<br/>

* **VDD**	=	3,3V	[Pin 01]<br/>
* **GND**	=	GND	[Pin 09]<br/>
* **SCL**	=	GPIO03 / SCL	[Pin 05]<br/>
* **SDA**	=	GPIO02 / SDA	[Pin 03]<br/>
* **A0**	=	Mira Arriba	[Sensor: Señal Analógica]
### Descargar Programa de Ejemplo
[KY-038_Microphone_sensor_module_RPi](http://sensorkit.en.joy-it.net/images/4/4d/KY-038_Microphone_sensor_module_RPi.zip)

Para comenzar, ingrese el comando: ```sudo python KY-038_Microphone_sensor_module_RPir.py```

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
