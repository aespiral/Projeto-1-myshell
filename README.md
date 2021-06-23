# Projeto-1-myshell


## Objetivo
Desenvolver um shell Unix básico e, dessa forma, fixar conceitos de programação Unix tais como processos, sinais, pipes.

## Formato
Trabalho em equipe de até 3 membros.

## Especificação
* ~Prompt~. O ~prompt~ deve mostrar o usuário, nome da máquina e o diretório de trabalho. O diretório home deve ser abreviado pelo sinal `~`. (Dica: existe uma variável de ambiente HOME, usem-na para determinar o diretório home.)
* Finalização. O comando `exit` encerra a execução do shell.
* Sinais. Os sinais disparados no teclado pelas combinações `CTRL+C` e `CTRL+Z` não devem interferir no shell.
* Invocação de comandos. Todos os programas executáveis que estiverem no caminho (~path~) devem ser executados em primeiro plano. Se o comando não está no caminho, isso deve ser indicado. Processos zumbis e processos bloqueados devem ser tratados. Ao final da execução do comando, o controle retorna ao shell.
* Navegação. Implemente o comando `cd` para mudança de diretório. Quando invocado sem parâmetros, subentende-se o diretório home como destino (equivalente a `cd ~`). Diretórios inválidos devem gerar algum tipo de erro a ser exibido para o usuário.
* Redirecionamentos. Implemente os redirecionamentos: saída para arquivo (indicado com `>`); arquivo para entrada (indicado com `<`); saída de erro para arquivo (indicado com `2>`).
* Composição de comandos com ~pipes~. Vários comandos podem ser executados simultaneamente, encadeando a saída de um com a entrada do próximo através de um ~pipe~. A sintaxe `cmd1 | cmd2 | cmd3 | ... | cmdn` é usada para realizar a composição.
Dicas. Algumas ~syscalls~ e funções que podem ser úteis: `fork`, `execvp`, `wait`, `signal`, `sigaction`, `getcwd`, `getenv`, `gethostname`, `strlen`, `strtok`, `strcmp`,  `chdir`,  `fgets`, `strerror`,  `exit`, `feof`, `pipe`, `close`.