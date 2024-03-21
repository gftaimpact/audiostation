# Documentación de Código: VBGROUP 5.0

El archivo VBGROUP es un archivo de grupo de proyecto para Visual Basic 6.0. Este archivo contiene información sobre los proyectos que se incluyen en el grupo. En este caso, se incluyen dos proyectos en el grupo: Audiostation y Audiostation Recorder.

## Sección de Código

```bash
StartupProject=Audiostation\Audiostation.vbp
Project=Projects\Recorder\Audiostation Recorder.vbp
```

## Descripción

### Línea 1: StartupProject=Audiostation\Audiostation.vbp

Esta línea especifica el proyecto de inicio del grupo. Cuando se abre el grupo, este es el proyecto que se cargará y estará listo para ejecutarse. En este caso, el proyecto de inicio es "Audiostation".

El valor `Audiostation\Audiostation.vbp` es una ruta relativa al archivo .vbp (Visual Basic Project) para el proyecto de inicio.

### Línea 2: Project=Projects\Recorder\Audiostation Recorder.vbp

Esta línea especifica un proyecto adicional que se incluye en el grupo. Este proyecto no se cargará automáticamente al abrir el grupo, pero está disponible para ser cargado y ejecutado.

El valor `Projects\Recorder\Audiostation Recorder.vbp` es una ruta relativa al archivo .vbp para este proyecto adicional.

## Resumen

Este archivo de grupo de proyecto enlaza dos proyectos: Audiostation y Audiostation Recorder. Audiostation se configura como el proyecto de inicio y se cargará automáticamente al abrir el grupo. Audiostation Recorder es un proyecto adicional que se puede cargar y ejecutar según sea necesario.