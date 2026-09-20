# Escáner de Puertos TCP en Python

## Descripción

Este proyecto consiste en el desarrollo de un escáner de puertos de red utilizando Python.

La aplicación permite ingresar una dirección IP y seleccionar un rango de puertos para comprobar cuáles se encuentran abiertos mediante conexiones TCP.

El programa cuenta con una interfaz gráfica desarrollada con Tkinter y utiliza la biblioteca `socket` para realizar las conexiones de red.

## Herramientas utilizadas

- Python
- Visual Studio Code
- GitHub
- Biblioteca socket
- Tkinter
- PyInstaller

## Funcionalidades

La aplicación permite:

1. Ingresar una dirección IP.
2. Ingresar un puerto inicial.
3. Ingresar un puerto final.
4. Realizar el escaneo del rango seleccionado.
5. Mostrar los puertos abiertos encontrados.
6. Mostrar el progreso del escaneo.
7. Mostrar un resumen de los resultados.
8. Mostrar el tiempo utilizado para realizar el escaneo.
9. Limpiar los datos para realizar un nuevo escaneo.

## Funcionamiento

El programa utiliza la biblioteca `socket` de Python para intentar establecer una conexión TCP con cada puerto dentro del rango seleccionado.

Se utiliza:

- `socket.AF_INET` para trabajar con direcciones IPv4.
- `socket.SOCK_STREAM` para utilizar el protocolo TCP.
- `connect_ex()` para intentar establecer la conexión.

Cuando `connect_ex()` devuelve el valor `0`, significa que la conexión TCP fue establecida correctamente y el puerto se considera abierto.

## Ejemplo

Datos ingresados:

Dirección IP:

    127.0.0.1

Puerto inicial:

    7995

Puerto final:

    8005

Resultado de ejemplo:

    Puerto 8000 - ABIERTO

Al finalizar, la aplicación muestra un resumen con:

- Dirección IP analizada.
- Rango de puertos.
- Cantidad de puertos escaneados.
- Cantidad de puertos abiertos.
- Puertos encontrados.
- Tiempo de escaneo.

## Interfaz gráfica

La interfaz fue desarrollada utilizando Tkinter y contiene:

- Campo para dirección IP.
- Campo para puerto inicial.
- Campo para puerto final.
- Botón para iniciar el escaneo.
- Botón para limpiar.
- Botón para salir.
- Barra de progreso.
- Área de resultados.
- Resumen del escaneo.

## Ejecutar desde Python

Para ejecutar el programa desde Visual Studio Code:

    python scanner.py

## Ejecutable de Windows

El proyecto también cuenta con una versión ejecutable para Windows creada utilizando PyInstaller.

El archivo se encuentra en:

    dist/EscanerPuertos.exe

Esto permite ejecutar la aplicación sin necesidad de abrir Visual Studio Code.


## Autor

Tito Vega
