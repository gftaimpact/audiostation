# Módulo BASS 2.4 para Visual Basic
Este módulo contiene la definición de constantes, tipos y funciones para interactuar con la biblioteca de audio BASS 2.4.

Primero, se definen las constantes globales para la versión de la API y para representar los valores de verdadero y falso. También se definen códigos de error que pueden ser retornados por la función `BASS_ErrorGetCode`.

Además, se definen constantes para varias opciones y parámetros utilizados en las funciones de la biblioteca BASS.

Se definen tipos de datos para estructuras de información de dispositivos, muestras, canales, entre otros.

Se definen las funciones de la biblioteca BASS para la configuración de la biblioteca, manejo de dispositivos, manejo de canales, manejo de muestras, manejo de música, manejo de grabación, manejo de efectos, entre otros. Estas funciones están declaradas para ser llamadas desde el código de Visual Basic.

Se incluyen algunas funciones auxiliares para trabajar con valores de bytes y palabras.

Finalmente, se proporciona una función para convertir un puntero a una cadena ANSI en una cadena de Visual Basic.

Notas:
- VB no soporta enteros de 64 bits, por lo tanto, los usuarios de VB solo tienen acceso a los 32 bits bajos de los valores de retorno de 64 bits. Sin embargo, se pueden especificar parámetros de 64 bits utilizando la versión "64" de la función.
- Para pasar un nombre de archivo a las funciones `BASS_MusicLoad`, `BASS_SampleLoad` y `BASS_StreamCreateFile`, use `StrPtr(filename)`.
- Use la función `VBStrFromAnsiPtr` para convertir "char *" a "String" de VB.