# Documentação do Código

## Módulo: ModMain
Descrição: Módulo principal da aplicação do programa

### Variáveis e Objetos Públicos:

- `Public LanguageFile As String`: Representa o arquivo de idioma usado no aplicativo.
- `Public Const MAXDRIVES = 10`: Define o número máximo de unidades de disco que o programa pode gerenciar.
- `Public curdrive As Long`: Armazena a unidade de disco atualmente em uso.
- `Public stream(MAXDRIVES) As Long`: Array que armazena as informações de streaming de cada unidade de disco.
- `Public seeking As Long`: Variável usada para buscar uma posição específica na mídia atualmente em reprodução.
- `Public IsDebuggig As Boolean`: Indica se o modo de depuração está ativo.
- `Public PlayStateMediaMode As enumMediaMode`: Armazena o estado atual da reprodução da mídia.
- `Public Mp3Info As New Mp3Info`: Objeto que armazena informações sobre o arquivo MP3 atual.
- `Public WebRequest As New WebClient`: Objeto usado para fazer solicitações web.
- `Public Settings As New RegistrySettings`: Objeto usado para gerenciar as configurações do aplicativo no Registro do Windows.
- `Public Extensions As New SibraSoft`: Objeto que fornece funcionalidades adicionais.
- `Public AudioStaRecorder As New AudiostationRecorder`: Objeto usado para gravar áudio.
- `Public AudioStaStreamer As New AudiostationSteamer`: Objeto usado para transmitir áudio.

### Procedimentos e Funções:

1. `Sub Main()`: O procedimento principal que é chamado quando o aplicativo é iniciado. Ele chama o construtor da aplicação.

2. `Sub OpenFile(MediaFile As String)`: Este procedimento é chamado para abrir um arquivo de mídia. Ele verifica o tipo do arquivo e realiza ações correspondentes. 

3. `Sub ApplicationConstructor()`: Este procedimento é chamado quando a aplicação é iniciada. Ele verifica se a pasta temporária existe, define o idioma do aplicativo, verifica o arquivo carregado e chama `OpenFile` se um arquivo de mídia válido for fornecido.

4. `Sub ApplicationDestructor()`: Este procedimento é chamado quando a aplicação está prestes a ser encerrada. Ele libera os recursos usados pelo aplicativo.

*Data de Criação*: 04-10-2021

*Data de Alteração*: 25-06-2022

*Autor*: Sibra-Soft - Alex van den Berg
