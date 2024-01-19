# Documentação do Código

## Nome do Módulo: modMain

Este módulo contém o procedimento principal (Main) para a execução do programa. Ele também tem uma variável pública chamada "Settings" que é uma nova instância da classe RegistrySettings.

### Atributos

#### Settings
Tipo: RegistrySettings

Este é uma instância da classe RegistrySettings que será usada para ler e escrever configurações no Registro do sistema.

### Sub Main()

Este é o procedimento principal que é executado quando o programa é iniciado.

#### Funcionamento

Se houver uma instância anterior do aplicativo em execução, ele irá verificar qual é o comando de entrada (obtido através do método `Command`). De acordo com o comando, ele irá escrever uma configuração específica no Registro através do objeto `Settings`:

- "-stop": escreve a configuração "stop" no Registro.
- "-save": escreve a configuração "save" no Registro.

Se não houver uma instância anterior em execução, o programa também verificará o comando de entrada:

- "-settings": mostra o formulário de configurações.
- "-record": esconde o formulário principal e inicia a gravação.
- Outros comandos: finaliza a execução do programa.

#### Observações

A função `Trim` é usada para remover espaços em branco extras no início e no fim do comando de entrada. O método `End` é usado para finalizar a execução do programa.

### Dependências

Este módulo depende das seguintes classes/formulários:

- RegistrySettings: Para a manipulação das configurações no Registro.
- Form_Settings: Formulário de configurações do programa.
- Form_Main: Formulário principal do programa.

### Exceções

Este módulo não trata explicitamente nenhuma exceção. Portanto, qualquer erro ocorrido durante a execução do código neste módulo resultará em um erro não tratado.