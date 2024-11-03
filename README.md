# APRS-LoRa - Proyecto
Debe descargar el comprimido y extraerlo para ver los archivos.

# Detalle del proyecto
Para el proyecto se va a utilizar la placa LILYGO LoRa con un ESP32 Version T3 1.6.1 para poder configurar un iGate utilizado APRS y LoRa para las comunicaciones con otros Trackers. El iGate permite a los Trackers poder transmitir informacion de ubicacion y telemetria sin necesidad de utilizar protocolos comunmente utilizados como WIFI o LTE celular. Mediante LoRa se puede transmitir a grandes distancias utilizando radiofrecuencia para poder tener una comunicacion en zonas rurales o de poco acceso a otros medios o inclusive para poder monitorear flotillas de vehiculos en ruta.
# iGate configurado y conectado
![image](https://github.com/user-attachments/assets/77538d54-f413-4023-8823-5dda2f805bb9)
# Configuracion de parametros en Visual SC/Platform IO
![image](https://github.com/user-attachments/assets/acc55404-9826-4aa1-9898-ce346679d2a6)
# Implementacion
- Hardware
Para implementar APRS con LoRa, es fundamental seleccionar un módulo adecuado como el LILYGO TTGO LoRa32, configurado para operar en la frecuencia de 433.755 MHz, la cual es adecuada para las aplicaciones de APRS. La antena, por su parte, debe estar sintonizada específicamente a esta frecuencia para optimizar el alcance y la calidad de la señal, asegurando transmisiones confiables. Además, se requiere una fuente de alimentación robusta, preferentemente una batería de larga duración, que garantice suficiente energía para un funcionamiento continuo en entornos remotos o de difícil acceso.
- Software
Para implementar correctamente el software para APRS, es fundamental mantener el firmware actualizado y contar con todas las bibliotecas necesarias instaladas, lo cual garantiza el funcionamiento óptimo del dispositivo. Asimismo, es crucial configurar con precisión los parámetros de operación, como la frecuencia, para asegurar la compatibilidad de transmisión. Además, deben establecerse las coordenadas GPS para la ubicación exacta del equipo y el indicativo (Call Sign) para la identificación única en la red de APRS. Estas configuraciones aseguran una comunicación precisa y efectiva en el sistema.
- Red APRS-IS
Para integrar APRS a un sistema con LoRa, es crucial conectar el dispositivo a una red Wi-Fi estable, ya que esto permite que los datos recopilados se envíen a la red APRS-IS para su visualización y análisis en tiempo real. Una vez que el sistema está operativo, plataformas como aprs.fi pueden utilizarse para verificar la recepción y el registro correcto de los datos transmitidos, asegurando que la información enviada desde los dispositivos de rastreo esté siendo registrada de manera precisa y accesible en la red APRS.
#Protocolo APRS LoRa
APRS (Automatic Packet Reporting System) en combinación con LoRa es una solución que permite la transmisión eficiente de datos de telemetría y ubicación en tiempo real para aplicaciones como el monitoreo ambiental y seguimiento de animales. Utiliza la modulación de espectro ensanchado LoRa, lo que permite enviar pequeñas cantidades de datos a largas distancias con bajo consumo energético. Al integrar LoRa con APRS, se facilita la recolección de información desde dispositivos en campo hacia una red central (APRS-IS), permitiendo visualizar y verificar datos mediante plataformas en línea como aprs.fi, sin necesidad de infraestructura compleja.
![image](https://github.com/user-attachments/assets/72afdb8d-7a70-4591-9bd5-6e981ab98f8d)

APRS LoRa utiliza la modulación Chirp Spread Spectrum (CSS), que es característica de LoRa, permitiendo una comunicación robusta y resistente a interferencias en entornos de largo alcance. Los datos se transmiten en paquetes cortos, generalmente en formato AX.25, el estándar de paquetes de datos en sistemas APRS. Este formato incluye información estructurada sobre la ubicación, velocidad, estado de sensores y otras telemetrías relevantes. La combinación de CSS y el formato AX.25 permite que APRS LoRa sea eficiente y adecuado para aplicaciones de rastreo y monitoreo en áreas extensas y remotas.
Estructura de datos AX.25: 
![image](https://github.com/user-attachments/assets/b9e4ac50-44ba-4102-bdd2-92328d3ea6d7)
