# Documentación del módulo ModBassCD

Este módulo se utiliza para interactuar con un CD utilizando la biblioteca BASSCD. Contiene constantes, tipos y funciones globales para leer y manipular CDs.

## Constantes globales

Las constantes globales definen valores que son utilizados en todo el módulo. Estos incluyen códigos de error, opciones de configuración, opciones de interfaz, banderas y más.

## Tipos

El tipo `BASS_CD_INFO` se utiliza para almacenar información sobre el CD y el dispositivo de CD. Contiene campos como el fabricante, el modelo, la revisión, la letra de la unidad, las banderas de capacidad de lectura/escritura, la capacidad de abrir/cerrar la puerta del CD, la capacidad de bloquear/desbloquear la puerta del CD, la velocidad máxima de lectura, el tamaño de la caché, y la capacidad de leer el CD-TEXT.

Los tipos `BASS_CD_TOC_TRACK` y `BASS_CD_TOC` se utilizan para representar la Tabla de Contenidos (TOC) de un CD.

## Funciones

Las funciones en este módulo se utilizan para interactuar con un CD o el dispositivo de CD. Estas incluyen funciones para obtener información sobre el CD o el dispositivo de CD, abrir y cerrar la puerta del CD, comprobar si la puerta del CD está abierta o cerrada, comprobar si el CD está listo, obtener el número de pistas en el CD, obtener la longitud de una pista, crear una secuencia de CD, reproducir una pista, detener la reproducción, y obtener la posición actual en la pista.

## Funciones de devolución de llamada

La función `CDDATAPROC` es una función de devolución de llamada que se llama cuando se lee el sub-canal o los datos C2 de un CD. Los parámetros de esta función incluyen el manejador de la secuencia de CD, la posición de los datos, el tipo de datos, el búfer que contiene los datos, la longitud del búfer y el valor del parámetro de usuario proporcionado cuando se llamó a `BASS_CD_StreamCreate/FileEx`.

Por favor, consulte el archivo BASSCD.CHM para obtener una documentación más detallada.