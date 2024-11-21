# Manual de Usuario - LoRa APRS iGate

Este manual de uso e implementación de APRS LoRa ofrece una guía detallada para configurar y operar sistemas de rastreo de baja potencia y largo alcance. 
APRS LoRa combina el sistema de paquetes automáticos APRS con la tecnología de modulación Chirp Spread Spectrum (CSS) de LoRa, lo que permite la transmisión de datos a grandes distancias, incluso en áreas con infraestructura limitada. 
A lo largo del manual, se explican aspectos clave como la conexión a redes Wi-Fi, el uso de formatos de datos AX.25, y la verificación en plataformas como aprs.fi. Esta integración es ideal para aplicaciones de monitoreo de fauna y telemetría ambiental, 
garantizando una comunicación confiable y un consumo de energía optimizado para dispositivos en entornos remotos.

# Diagrama aplicacion

El monitoreo de especies en peligro de extinción es esencial para su preservación, ya que proporciona datos cruciales sobre su comportamiento, desplazamiento y condiciones ambientales. Esto permite tomar decisiones informadas para implementar medidas de conservación. Además, el seguimiento continuo facilita identificar amenazas como cambios en su hábitat o actividades humanas perjudiciales, lo que contribuye a proteger la biodiversidad y los ecosistemas.

El diagrama presentado describe un sistema de comunicación basado en APRS (Automatic Packet Reporting System) sobre la tecnología LoRa, diseñado específicamente para el monitoreo de estas especies. Este sistema tiene varias etapas que trabajan de manera conjunta para recolectar, procesar, transmitir y visualizar datos relevantes en tiempo real.
 ![image](https://github.com/user-attachments/assets/bf71abe4-f8af-4931-8160-c84500b36d66)

Fuente de energía y sensores:

- Batería externa:
Proporciona la energía necesaria para el funcionamiento del sistema. Incluye un controlador de carga, un circuito de protección, y una etapa DC-DC para regular la tensión. También cuenta con un indicador LED para el monitoreo del estado de la batería.
Sensores de temperatura y velocidad: Recopilan datos ambientales relevantes y de movimiento del animal monitorizado.
- Módulo GPS externo:
Este módulo calcula la posición utilizando las cadenas NMEA obtenidas de las señales satelitales. Esto permite conocer la ubicación precisa de la especie en cualquier momento.

- Unidad central de procesamiento (ESP32):
Filtra y analiza los datos provenientes del GPS y los sensores.
Decodifica las señales utilizando el protocolo AX.25, común en aplicaciones APRS.
Gestiona las interrupciones para optimizar el flujo de datos hacia el transmisor.

- Transmisión mediante LILYGO LoRa32:
Este módulo codifica los datos, los sincroniza en paquetes y los transmite mediante una antena. Su tecnología LoRa permite una comunicación de largo alcance con un bajo consumo de energía, ideal para aplicaciones remotas.

- Receptor y procesamiento en el iGate:
El iGate descodifica las señales recibidas, valida la información y filtra los datos para garantizar su precisión antes de retransmitirlos a un servidor.

- Servidor y aplicación:
Los datos se almacenan y procesan en un servidor, donde se actualizan en tiempo real.
Una aplicación visualiza la información recopilada, permitiendo su análisis y mapeo. Esto facilita la interpretación de la ubicación, temperatura y velocidad del animal, además del estado de la batería del dispositivo.
# Descripcion del modulo iGate y componentes

El módulo LILYGO TTGO LoRa32 es una plataforma de desarrollo que combina capacidades de Wi-Fi, Bluetooth y LoRa en un solo dispositivo basado en el chip ESP32 de Espressif. Este módulo es ideal para proyectos de IoT, ya que permite la transmisión de datos a largas distancias con un bajo consumo energético. Integra un microcontrolador ESP32 y un transceptor LoRa SX1276/SX1278,
 proporcionando una opción flexible y económica para aplicaciones de telemetría, comunicación de sensores y sistemas de seguimiento. También incluye una pantalla OLED para visualizar datos directamente en el dispositivo, facilitando la supervisión en tiempo real y opera en la banda de frecuencia de los 70 cm.
![image](https://github.com/user-attachments/assets/71423296-4cbb-4a8d-9151-fcc052028e19)

# Configuracion
- Paso 1: Hardware
1. Conecte la batería LP103454 al módulo LILYGO TTGO LoRa32.
2. Asegúrese de que todos los cables estén correctamente conectados.
- Paso 2: Software
1. Descargue el software desde el repositorio oficial [LoRa APRS iGate GitHub](https://github.com/richonguzman/LoRa_APRS_iGate).
2. Siga las instrucciones del repositorio para instalar las dependencias necesarias.
- Paso 3: Configuracion del iGate desde Platform IO
1. Defina el parametro de callsign
2. Ingrese las coordenadas de latitud y longitud del lugar de operación.
3. Configure los parametros para la conexion a red, SSID y la clave de acceso.
# Configuracion secundaria
1. Se ingresa al siguiente enlaces: https://riojanosporlaradio.com/lora-aprs-for-dummies/
2. Se siguen los pasos, esta configuracion se realiza haciendo uso del iGate como un router para conectarse por medio de un dispositivo movil a la red wifi del mismo.
3. Luego se ingresa a la direccion IP descrita en la pantalla configurar todos los parametros y cargarlos en el dispostivio, las instrucciones a detalle se encuentran en el enlace.
   Imagen de ejemplo:
   ![image](https://github.com/user-attachments/assets/a5f42b6b-1844-4088-8486-5fc969212b68)

# Uso del dispositivo
1. Una vez confiugurado el dispositivo, enciendalo y verifique la conexion a red y APRS.
2. Verifique la conexion en la plataforma https://aprs.fi/, se visualizara el signo escogido en la ubicacion determinada.
