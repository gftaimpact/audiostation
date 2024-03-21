# Documentación del Código

El siguiente módulo, llamado `ModConvert`, se encarga de la conversión de archivos de audio de un formato a otro.

## Enumeraciones

El módulo contiene dos enumeraciones públicas: `ConvertFrom` y `convertto`. 

### ConvertFrom

Esta enumeración define los formatos de audio desde los cuales se puede convertir un archivo. Incluye los siguientes formatos:
- Real Media
- Real Audio
- Voice File Format
- Apple Core Format
- Sony Wave64
- OGG
- Westwood Studios Audio
- Sony OpenMG Audio
- Raw Flac
- Creative Voice
- Windows Media
- Media4A

### convertto

Esta enumeración define los formatos de audio a los que se puede convertir un archivo. Incluye los siguientes formatos:
- MP3
- WAV

## Función Convert

La función `Convert` es una función pública que toma tres parámetros: 

- `ConvFilename`: es una cadena que representa el nombre del archivo a convertir.
- `ConvFrom`: es un valor de la enumeración `ConvertFrom` que representa el formato del archivo a convertir.
- `convTo`: es un valor de la enumeración `convertto` que representa el formato al que se convertirá el archivo.

La función utiliza la herramienta de línea de comandos `ffmpeg` para convertir el archivo. El archivo convertido se guarda en el directorio temporal de la aplicación con la extensión `.mp3`.

Además, la función escribe la ruta del archivo convertido en la configuración de la aplicación bajo las claves "Sibra-Soft", "Audiostation" y "CheckFile".