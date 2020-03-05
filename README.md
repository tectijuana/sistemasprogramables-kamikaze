# sistemasprogramables-kamikaze
sistemasprogramables-kamikaze created by GitHub Classroom

 Sensores de sonido: micrófono

<a href="https://cooltext.com"><img src="https://images.cooltext.com/5387875.png" width="921" height="115" alt=" Sensores de sonido: micrófono" /></a>
<br />Image by <a href="https://cooltext.com">Cool Text: Free Logos and Buttons</a> - <a href="https://cooltext.com/Edit-Logo?LogoID=3509961347">Create An Image Just Like This</a>

| Nombre                               | Participacion                 | Calificación |
|--------------------------------------|-------------------------------|--------------|
| Acevedo Cardona Adelaid Lesdeymariet |                               |              | 
| Encarnacion Ocampo Gustavo           | Módulo de sensor de micrófono |              | 
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

## CÓDIGO DE EJEMPLO KY-012
El siguiente Arduino Sketch activará y desactivará continuamente el zumbador, generando una serie de pitidos cortos y agudos.

| int buzzerPin = 8;   void setup ()  {  pinMode (buzzerPin, OUTPUT);  }   void loop ()  {  digitalWrite (buzzerPin, HIGH);  delay (500);  digitalWrite (buzzerPin, LOW);  delay (500);  } |
