# sistemasprogramables-kamikaze
sistemasprogramables-kamikaze created by GitHub Classroom

 Sensores de sonido: micrófono

<a href="https://cooltext.com"><img src="https://images.cooltext.com/5387875.png" width="921" height="115" alt=" Sensores de sonido: micrófono" /></a>
<br />Image by <a href="https://cooltext.com">Cool Text: Free Logos and Buttons</a> - <a href="https://cooltext.com/Edit-Logo?LogoID=3509961347">Create An Image Just Like This</a>

| Nombre                               | Participacion                 | Calificación |
|--------------------------------------|-------------------------------|--------------|
| Acevedo Cardona Adelaid Lesdeymariet |                               |              | 
| Encarnacion Ocampo Gustavo           | KY-037 Módulo de sensor de micrófono |              | 
| Gallardo Dueñas Carlos Ivan          | KY-012 Sensor Zumbador Activo |              | 
| d                                    |                               |              | 

# KY-037 Módulo de sensor de micrófono (alta sensibilidad)

![alt text](http://sensorkit.en.joy-it.net/images/8/8e/ky-037.jpg "KY-037 Microphone sensor module (high sensitivity)")

## Datos técnicos 
**Salida digital:** Puede usar un potenciómetro para configurar un valor extremo para el sonic. Si el valor excede el valor extremo, enviará una señal a través de la salida digital.

**Salida analógica:** Señal directa del micrófono como valor de voltaje.

**LED1:** Muestra que el sensor recibe voltaje.
**LED2:** Muestra que se detectó un campo magnético.

## Pinout
![alt text](http://sensorkit.en.joy-it.net/images/d/d8/4_dig_V_G_An_eng.png "pinout")

## Funcionalidad del sensor.
El sensor tiene 3 componentes principales en su placa de circuito. Primero, la unidad de sensor en la parte frontal del módulo que mide el área físicamente y envía una señal analógica a la segunda unidad, el amplificador. El amplificador amplifica la señal, de acuerdo con el valor resistente del potenciómetro, y envía la señal a la salida analógica del módulo.
El tercer componente es un comparador que apaga la salida digital y el LED si la señal cae por debajo de un valor específico.
Puede controlar la sensibilidad ajustando el potenciómetro.
![alt text](http://sensorkit.en.joy-it.net/images/d/de/sens-poti.jpg "fun-sen")


# Modulo KY-012 Sensor Zumbador Activo

![alt text](https://ae01.alicdn.com/kf/Ha4027ff59c964f6395e5110879dd4ac7R.jpg "KY-012 Sensor Zumbador Activo")

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

| KY-012 | arduino |
|--------|---------|
| S      | pin 8   |
| -      | GND     |

![alt text](https://arduinomodules.info/wp-content/uploads/Arduino_KY-012_Keyes_Active_buzzer_module_connection_diagram.png "KY-012 diagrama de conexion")

## CÓDIGO DE EJEMPLO KY-012 EN ARDUINO 

El siguiente Arduino Sketch activará y desactivará continuamente el zumbador, generando una serie de pitidos cortos y agudos.

---

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
