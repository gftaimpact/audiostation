# Documentação do Projeto Audiostation

Audiostation é um reprodutor de mídia de estilo antigo. O projeto contém várias classes, módulos, controles de usuário e formulários. As referências e objetos do projeto são listados abaixo:

## Referências:
1. OLE Automation
2. Microsoft Scripting Runtime
3. Windows Script Host Object Model
4. Microsoft XML, v6.0

## Objetos:
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

## Classes:
As classes do projeto incluem:
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

## Controles de Usuário:
Os controles de usuário incluem:
1. ButtonBig
2. Hyperlink
3. MixSlider

## Formulários:
Os formulários do projeto incluem:
1. Form_About
2. Form_Busy
3. Form_Main
4. Form_Midi
5. Form_OpenDialog
6. Form_Playlist
7. Form_Plugins
8. Form_Settings_Record
9. Form_Track_Properties

## Módulos:
Os módulos do projeto incluem:
1. AudiostationCDPlayer
2. AudiostationMIDIPlayer
3. AudiostationMP3Player
4. ModBass
5. ModBassCD
6. ModConvert
7. ModEnums
8. ModLanguage
9. ModMain
10. ModConstMidi
11. ModMidiUtils
12. ModBassNetRadio
13. ModPlaylist
14. ModBassSpectrum

# Detalhes Adicionais:
- O formulário inicial é "Form_Main".
- O nome do executável é "Audiostation.exe".
- A empresa da versão é "Sibra-Soft".
- O produto da versão é "Audiostation".

# Observações:
- A verificação de overflow, a verificação de ponto flutuante e a verificação FDIV estão desativadas.
- O projeto está configurado para iniciar no modo normal, não no modo desacompanhado.
- O projeto não retém a memória após o término.
- O projeto não suporta múltiplos segmentos de thread.