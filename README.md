# Traffic_Light
Esta pequeña porción de código permite visualizar una simulación de un semáforo, y una interacción en tiempon real con él, en donde el usuario hace un papel de peatón en el cruce peatonal al presionar el botón que acorta el tiempo de la luz verde, permitiendole pasar de acera de forma más rápida.

## Tabla de Contenidos
1. [Introducción](#introducción)
2. [Requisitos](#requisitos)
3. [Instalación](#instalación)
4. [Uso](#uso)
5. [Estructura de Archivos](#estructura-de-archivos)
6. [Problemas Conocidos](#Problemas-Conocidos)

## Introducción
El proyecto Traffic Light permite al usuario visualizar e interactuar con un semáforo, el cual podemos controlar a través de un software tercero, Arduino IoT Cloud, qué través de WIFI conecta en tiempo real una placa ESP32, la que a la vez está conectada a una protoboard con un circuito básico el cual contiene los leds necesarios para simular el funcionamiento de un semáforo.

## Requisitos

Para utilizar y/o contribuir a este proyecto, necesitarás los siguientes componentes y recursos:

- Memoria ESP32: Se requiere una memoria ESP32 compatible para ejecutar la aplicación. En este caso se tiene una ESP32 DEVKIT-V1.1

- Protoboard: Un protoboard es necesario para conectar y montar los componentes electrónicos. Asegúrate de tener uno disponible.

- LED: Se necesita al menos tres LED´s para ciertas funcionalidades de la aplicación.

- Resistencias: Las resistencias pueden ser necesarias para limitar la corriente a los LEDs u otros componentes, dependiendo de la configuración.

- Cables: Los cables de conexión son esenciales para conectar los componentes al protoboard y a la memoria ESP32.

- Acceso a Arduino IoT Cloud: Esta aplicación se integra con Arduino IoT Cloud. Asegúrate de tener acceso a una cuenta de Arduino IoT Cloud y estar familiarizado con su plataforma. Puedes registrarte en [https://cloud.arduino.cc/] si aún no tienes una cuenta.

## Instalación

### Configuración de Hardware
- Conexión de los componentes físicos:
- Conecta los LEDs al protoboard con las resistencias necesarias.
- Conecta los cables desde el protoboard a los pines GPIO del ESP32 para cada LED. Registra los pines utilizados.

### Configuración de Arduino IoT Cloud

- Inicia sesión en tu cuenta de Arduino IoT Cloud o regístrate si aún no tienes una cuenta.
- Crea un nuevo proyecto para tu semáforo.
- Define las variables utilizadas en la interfaz de Arduino IoT Cloud.

## Uso
Para hacer uso del aplicativo teniendo todas las dependencias instaladas, solo necesitamos cargar nuestro código a la memoria ESP32, una vez hecho esto podemos ir al apartado dashboard en Arduino IoT Cloud en donde tendremos una variable en forma de botón que hace referencia al botón encontrado en las aceras para agilizar el cambio del semáforo a rojo.

## Estructura de Archivos
Encontramos en el main este proyecto lo que es simplemente el Readme y el código en c++ en un archivo .ino.

## Problemas Conocidos
- Debido a que el funcionamiento del botón requiere de una actulización continua de su estado a través de wifi, en pocas ocasiones no encontramos la respuesta deseada.
