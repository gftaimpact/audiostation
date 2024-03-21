# Documentación del código del proyecto Audiostation

Este proyecto llamado "Audiostation" es un reproductor de medios de estilo antiguo desarrollado por Sibra-Soft. Este documento detalla las referencias, objetos, clases, controles de usuario, formularios y módulos utilizados en el proyecto.

## Referencias

Las siguientes son las referencias de bibliotecas y componentes utilizados en el proyecto:

1. OLE Automation
2. Microsoft Scripting Runtime
3. Windows Script Host Object Model
4. Microsoft XML, v6.0

## Objetos

Los siguientes son los objetos utilizados en el proyecto:

1. isDigitalLibrary.ocx
2. isAnalogLibrary.ocx
3. MSCOMCTL.OCX
4. COMDLG32.OCX
5. MBPrgBar.ocx
6. TABCTL32.OCX
7. midifl2k.ocx
8. Comctl32.ocx
9. midiio2k.ocx
10. LaVolpeAlphaImg2.ocx
11. iProfessionalLibrary.ocx

## Clases

Las siguientes son las clases utilizadas en el proyecto:

1. AudioVolume
2. AudiostationSteamer
3. BaseTime
4. FileIO
5. AudioMeter
6. LocalStorage
7. Mp3Info
8. Nest
9. RegistrySettings
10. SibraSoft
11. StringBuilder
12. WebClient
13. AudiostationRecorder

## Controles de usuario

Los siguientes son los controles de usuario utilizados en el proyecto:

1. ButtonBig.ctl
2. Hyperlink.ctl
3. MixSlider.ctl

## Formularios

Los siguientes son los formularios utilizados en el proyecto:

1. Form_About.frm
2. Form_Busy.frm
3. Form_Main.frm
4. Form_Midi.frm
5. Form_OpenDialog.frm
6. Form_Playlist.frm
7. Form_Plugins.frm
8. Form_Settings_Record.frm
9. Form_Track_Properties.frm

## Módulos

Los siguientes son los módulos utilizados en el proyecto:

1. AudiostationCDPlayer.bas
2. AudiostationMIDIPlayer.bas
3. AudiostationMP3Player.bas
4. ModBass.bas
5. ModBassCD.bas
6. ModConvert.bas
7. ModEnums.bas
8. ModLanguage.bas
9. ModMain.bas
10. ModConstMidi.bas
11. ModMidiUtils.bas
12. ModBassNetRadio.bas
13. ModPlaylist.bas
14. ModBassSpectrum.bas

El programa se inicia desde el módulo `Sub Main`. El formulario principal del proyecto es `Form_Main`. El archivo de ayuda y el contexto de ayuda están actualmente vacíos. El proyecto se compila en una aplicación ejecutable llamada "Audiostation.exe" sin ninguna opción de línea de comando.