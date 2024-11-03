# Manual de Usuario - LoRa APRS iGate

Este manual de uso e implementación de APRS LoRa ofrece una guía detallada para configurar y operar sistemas de rastreo de baja potencia y largo alcance. 
APRS LoRa combina el sistema de paquetes automáticos APRS con la tecnología de modulación Chirp Spread Spectrum (CSS) de LoRa, lo que permite la transmisión de datos a grandes distancias, incluso en áreas con infraestructura limitada. 
A lo largo del manual, se explican aspectos clave como la conexión a redes Wi-Fi, el uso de formatos de datos AX.25, y la verificación en plataformas como aprs.fi. Esta integración es ideal para aplicaciones de monitoreo de fauna y telemetría ambiental, 
garantizando una comunicación confiable y un consumo de energía optimizado para dispositivos en entornos remotos.

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
# Uso del dispositivo
1. Una vez confiugurado el dispositivo, enciendalo y verifique la conexion a red y APRS.
2. 2. Verifique la conexion en la plataforma https://aprs.fi/, se visualizara el signo escogido en la ubicacion determinada.
