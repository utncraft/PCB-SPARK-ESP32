# PCB-SPARK-ESP32
Contiene el microcontrolador ESP32 Mini de 3.3V y funciona como el centro de procesamiento de bajo nivel para el subsistema motriz y como interfaz primaria de comunicación con el computador host (Raspberry Pi 4).

<img width="997" height="735" alt="image" src="https://github.com/user-attachments/assets/3fbf4616-99da-41e2-988c-0dcf98e7f0c0" />


## Funciones Principales del PCB:

* Interfaz de Comunicación Host: Proporciona la conexión física USB-C para establecer el enlace serial (USB-CDC) sobre el cual opera el stack de transporte de micro-ROS, permitiendo el intercambio bidireccional de mensajes con el sistema de alto nivel.

* Control de Actuadores Motrices: Enruta las señales GPIO necesarias para la generación de PWM (Modulación por Ancho de Pulso) hacia los drivers de potencia externos, controlando la velocidad y dirección de los dos motores DC de tracción.

* Interfaz de Retroalimentación de Velocidad: Integra los conectores y el filtrado básico para la captura de señales digitales provenientes de los encoders de cuadratura, permitiendo el cálculo de la odometría.

* Adquisición de Sensores de Navegación Local: Proporciona puertos de conexión para la lectura directa (ADC) de los sensores infrarrojos de seguimiento de línea.

* Controlador del Bus de Datos Interno: Implementa la topología física del bus I2C, actuando como el dispositivo iniciador de transacciones para solicitar datos a la PCB secundaria.

* Distribución de Energía Lógica (3.3V): Recibe alimentación regulada de 5V y gestiona la distribución de energía de 3.3V para el microcontrolador ESP32 y los sensores conectados directamente a esta placa.

## Schematics

<img width="909" height="485" alt="PCB-SPARK-ESP32-0 1-SCHEMA" src="https://github.com/user-attachments/assets/46c544f0-1815-4c67-bac7-14f6a24b55f5" />


## PCB

<img width="463" height="664" alt="PCB-SPARK-ESP32-0 1" src="https://github.com/user-attachments/assets/cb4da42c-c439-4d4d-b430-bf239d2e0c5e" />
