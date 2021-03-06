# Quack4

![Quack4](Quack4.png)

A quacktrip v0.5 plugin that handles a 3 way connection.
Head to the [releases](https://github.com/fdch/Quack4/releases) pages to get the builds.

Version: 1.6
Author: ffddcchh

made with Camomile

Based on [quacktrip\~](http://msp.ucsd.edu/tools/quacktrip/) by Miller Puckette.

Many thanks to Miller Puckette and the Pure Data team, 
Marc Ainger for testing and support, 
and Pierre Guillot for Camomile.

---

# instructions (ver abajo para español)

## puredata

1. unzip the zip file
2. open with Pure Data the file `Quack4.pd` located in the folder` src / Quack4 / `

## plugin

1. unzip the zip file
2. load the VST (or AU in macos) from your DAW (Ableton, Max, Reaper, etc)

## how to use

- this system is managed with "calls" that are made between two people at the same time
- each call must have a unique name known to the two people who communicate
- up to 6 simultaneous calls can be made (always between one person and 6 other people on different IPs)
- each row corresponds to a call
- the name of the call must be entered in the "call-name" field, replacing the name "q1" (or "q2", "q3", etc.) with the name agreed between both parties
- after entering the name of the call, the call is started by clicking on the white toggle on the left corresponding to the call

## controls of each call

### onoff
turn the call on or off

### call-name
unique name of the call between two different IPs. Double-click on the graphic symbol object to type the name with the keyboard and then press Enter to correctly enter the name.

### status
- if the `bang` object blinks: it is communicating with the server
- if object `toggle` is on: connection established on call

### nchan
number of audio channels of the outgoing call: 0, 1 or 2 channels (default 2)

### fifo
amount in milliseconds to wait to send the audio packets (default 50). Low values ​​improve round-trip latency but the signal is affected depending on the transmission speed. High values ​​add latency to the transmission but guarantee fewer cuts in the audio.

### bufsize
block size of the signal sent and internal processing in Quack4.pd: 0 (64), 1 (128) or 2 (256) (default 0, that is, 64)

### 2x
repeat (see quacktrip\~)


## global controls

### onoff (green)
Turn on all calls (use carefully)

### get
local test audio signal output

### send
Send test audio signal (to all calls). Note: Only the person on the other end of the call hears it

### server (buttons)
These buttons allow you to choose between a server (default) from Miller Puckette and another one of my own. It is important that all people are using the same server.

### server (symbol)
can be added / changed to a ip from another server

### port (number)
you can add / change the port number of another server

---

# instrucciones:

## puredata

1. descomprimir el archivo zip
2. abrir con Pure Data el archivo `Quack4.pd` ubicado en la carpeta `src/Quack4/`

## plugin

- cargar el VST (o AU en macos) desde tu DAW (Ableton, Max, Reaper, etc)

## modo de uso

### una llamada

- este sistema se maneja con "llamadas" que se realizan entre dos personas a la vez
- la llamada debe tener un nombre único elegido por las dos personas que se comunican
- este nombre deben ingresarlo en el campo `call-name`
- es importatísimo reemplazar el nombre `q1` (o `q2`, `q3`, etc) por el nombre acordado entre ambas personas
- luego, apretar el toggle blanco de la izquierda para iniciar la llamada.

### múltiples llamadas

- cada hilera se corresponde a una llamada
- se pueden realizar hasta 6 llamadas simultáneas
- las llamadas son siempre entre una persona y otras 6 personas (en IPs distintas)

## controles de cada llamada

### onoff
enciende o apaga la llamada

### call-name
nombre único de la llamada entre dos IPs distintas. Hacer doble click en el objeto de símbolo gráfico para escribir el nombre con e teclado y luego apretar Enter para que se ingrese correctamente el nombre.

### status
- si el objeto `bang` titila: se está comunicando con el servidor
- si el objeto `toggle` está encendido: se estableció la conexión en la llamada 

### nchan
cantidad de canales de audio de la llamada saliente: 0, 1 ò 2 canales (default 2)

### fifo
cantidad en milisegundos de espera para enviar los paquetes de audio (default 50). Valores bajos mejoran la latencia de ida y vuelta pero la señal se ve afectada dependiendo de la velocidad de transmisión. Valores altos agregan latencia a la transmisión pero garantizan menos cortes en el audio. 

### bufsize
tamaño del bloque de la señal enviada y de procesamiento interno en Quack4.pd: 0 (64), 1 (128) ò 2 (256) (default 0, o sea, 64)

### 2x
repeat (ver quacktrip\~)


## controles globales

### onoff (verde)
enciende todas las llamadas (usar con cuidado)

### get
prueba local de señal de audio de salida

### send
envío de señal de audio de prueba (a todas las llamadas). Nota: solo lo oye la persona del otro lado de la llamada

### server (botones)
estos botones permiten elegir entre un servidor (default) de Miller Puckette y uno mío. Es importante que todas las personas estén usando el mismo servidor.

### server (symbol)
se puede agregar/cambiar a una ip de otro servidor

### port (numero)
se puede agregar/cambiar el número de puerto de otro servidor
