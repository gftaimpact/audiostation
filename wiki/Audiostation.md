# Documentación del Código: VBGROUP 5.0

VBGROUP 5.0 es una herramienta para organizar y administrar proyectos relacionados en Visual Basic.

## Proyectos de inicio

```ini
StartupProject=Audiostation\Audiostation.vbp
```

La línea de código anterior especifica el proyecto que se iniciará por defecto cuando se ejecute el grupo de proyectos. En este caso, el proyecto de inicio es `Audiostation.vbp` que se encuentra en el directorio `Audiostation`.

## Proyectos incluidos en el grupo

```ini
Project=Projects\Recorder\Audiostation Recorder.vbp
```

Esta línea de código especifica uno de los proyectos que están incluidos en el grupo de proyectos. En este caso, el proyecto es `Audiostation Recorder.vbp` que se encuentra en el subdirectorio `Recorder` del directorio `Projects`.

Nota: Puede haber múltiples líneas de `Project=` en un archivo VBGROUP para incluir múltiples proyectos.

# Resumen

El archivo VBGROUP esencialmente sirve como una forma de agrupar y administrar proyectos relacionados en Visual Basic. Permite a los desarrolladores especificar un proyecto de inicio y listar otros proyectos que forman parte del grupo.