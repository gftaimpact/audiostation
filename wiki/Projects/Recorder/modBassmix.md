# Documentación del módulo modBassMix

Este módulo es parte de BASSmix, una extensión de la biblioteca de audio BASS. Esta extensión proporciona la capacidad de mezclar múltiples flujos y/o canales de muestra en un solo flujo, con opciones de mezcla y procesamiento de efectos opcionales.

## Variables Globales

Las constantes globales en este módulo se utilizan para establecer configuraciones, atributos y banderas para la creación de flujos, adición de canales y otras funciones de BASSmix.

## Estructuras

`BASS_MIXER_NODE` es una estructura utilizada para definir un nodo en una envolvente. Esta estructura contiene la posición y el valor del nodo.

## Funciones

Las funciones en este módulo son para la creación de flujos, adición de canales, configuración de atributos y otras funciones de mezcla y división de audio. Algunas funciones son envoltorios de 32 bits para las funciones de BASS de 64 bits.

### Ejemplos de funciones

- `BASS_Mixer_GetVersion` - Esta función devuelve la versión de BASSmix.
- `BASS_Mixer_StreamCreate` - Esta función se utiliza para crear un nuevo flujo de mezcla.
- `BASS_Mixer_ChannelGetMixer` - Esta función obtiene el manejador del flujo de mezcla al que está asignado un canal.
- `BASS_Mixer_ChannelIsActive` - Esta función verifica si un canal está activo.
- `BASS_Mixer_ChannelSetPosition` - Esta función cambia la posición de reproducción de un canal en el flujo de mezcla.

Por favor, consulte la documentación BASSMIX.CHM para más detalles.

Nota: Este módulo requiere la biblioteca bassmix.dll para funcionar correctamente.

## Licencia

Este módulo es propiedad de Un4seen Developments Ltd. y está protegido por las leyes de derechos de autor.