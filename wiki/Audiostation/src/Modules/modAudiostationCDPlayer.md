# Documentación del Código: AudiostationCDPlayer

### Módulo: AudiostationCDPlayer
Este módulo añade funcionalidad de reproductor de CD al programa Audiostation.

**Fecha de creación**: 04-10-2021  
**Fecha de modificación**: 13-10-2021  
**Autor**: Sibra-Soft - Alex van den Berg

## Variables Globales
- `CDPlaystate`: Representa el estado actual de reproducción del CD.
- `mode`: Representa el modo de reproducción actual del CD.
- `CurrentTrackCount`: Representa el número total de pistas en el CD.
- `CurrentTrackNr`: Representa el número de pista actual en reproducción.

## Subrutinas y Funciones
### EndSync
Esta subrutina se activa al final de la sincronización de una pista. Si hay más pistas en el CD, reproduce la siguiente.

### PlayTrackFromCD
Esta subrutina reproduce una pista específica desde el CD.

### StopPlay
Esta subrutina detiene la reproducción del CD.

### CheckIfCDRomDriveExists
Esta función verifica si existe una unidad de CD-ROM.

### Play
Esta subrutina inicia la reproducción del CD.

### Pause
Esta subrutina pausa la reproducción del CD.

### Forward
Esta subrutina avanza la reproducción del CD en 5 segundos.

### Rewind
Esta subrutina retrocede la reproducción del CD en 5 segundos.

### OpenOrCloseDriveDoor
Esta subrutina abre o cierra la puerta de la unidad de CD-ROM.

### NextTrack
Esta subrutina reproduce la siguiente pista del CD, dependiendo del modo de reproducción actual.

### PreviousTrack
Esta subrutina reproduce la pista anterior del CD.