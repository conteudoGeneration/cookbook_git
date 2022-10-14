<h1>Terminal</h1>



Antes de falarmos sobre terminal, vamos definir alguns conceitos importantes

<h2>Hardware</h2>

Hardware **é a parte física do computador, ou seja, o conjunto de aparatos eletrônicos, peças e equipamentos que fazem o computador funcionar**. A palavra hardware pode se referir também como o conjunto de equipamentos acoplados em produtos que precisam de algum tipo de processamento computacional.

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

Os computadores da Apple mais atuais utilizam os processadores M1 e M2, baseado na Arquitetura ARM. Ele possui 8 núcleos de processamento e o chip tem “um dos núcleos mais rápidos do mundo” e “uma das melhores performances por watt”, consumindo pouquíssima energia. Em 2023, deve chegar ao mercado o processador M3.

<table width="100%" align="center">    
    <tr>        
        <td width="33%"><div align="center"><img src="https://i.imgur.com/j8d4MiZ.jpg" title="source: imgur.com" width="60%"/></div></td>        
        <td width="33%"><div align="center"><img src="https://i.imgur.com/horESg7.jpg" title="source: imgur.com" width="60%"/></div></td>
        <td width="33%"><div align="center"><img src="https://i.imgur.com/Vsp2Vl3.jpg" title="source: imgur.com" width="60%"/></div></td>
    </tr>   
</table>


> A sigla **ARM** quer dizer **Advanced RISC Machine** (Máquina RISC Avançada), e o termo RISC diz respeito a um conjunto de instruções de  processadores. Esse padrão é utilizado em todos os processadores ARM,  uma vez que é uma demanda da arquitetura.
>
> **RISC** é um conjunto de  instruções reduzido, mais limitado, fazendo as instruções serem mais  simples que o sistema CISC (conjunto de instruções complexas), utilizado nos PCs. O sistema RISC exige  menos do processador, assim o chip não precisa de tanta energia, o que é essencial em dispositivos móveis que possuem bateria.

<h2>Software</h2>

Software é a parte virtual, lógica, imaterial da Informática. Corresponde ao **conjunto de informações e instruções a serem executadas, a fim de se conseguir o resultado esperado**.

Quando pensamos em sistema, normalmente pensamos em uma interface visual, que é o elemento de interação com um ser humano, mas um software pode existir sem nada visual. Ele pode estar embutido em um micro-controlador que comanda um circuito eletrônico, mas não é ligado em um monitor. Ou ele pode ser simplesmente um software feito para computador, mas sem interface, como um programa robô que fica checando alguma atividade do computador. Existem diferentes tipos de software para diversas finalidades.

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

<h2>Sistema Operacional</h2>

O Sistema operacional é um tipo especial de software. Ele é um software de base que possui diferentes funções. Uma dela é controlar o equipamento, provendo uma interface de controle para o usuário realizar suas  configurações e utilizar o equipamento. Outra é permitir um protocolo  para que outros softwares, os software-aplicativos, sejam instalados  sobre o sistema operacional, como um editor de texto ou um game, por exemplo.

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

Observe na imagem acima que o Sistema Operacional está localizado entre o Hardware e os Softwares aplicativos.

<h3>Kernel</h3>

O **kernel é o  componente principal de um sistema operacional e a interface  central entre o hardware e os processos executados por um computador**. Ele estabelece a comunicação entre ambos, gerenciando recursos com a maior eficiência possível.

<h3>Aplicativos</h3>

Com exceção do sistema operacional, quase todo o software que você  pensar é um software-aplicativo. Editor de texto, de planilha, de  apresentação, ferramenta de e-mail, game, navegador.

Uma característica dos software-aplicativos é que eles são instalados sobre um sistema operacional, assim, um software-aplicativo depende mais do sistema  operacional do que hardware do equipamento. 

Os principais sistemas operacionais para computadores são: 

<table>
    <tr>
        <td><div align="center"><img src="https://i.imgur.com/za4tPUA.png" title="source: imgur.com" width="60%"/></div></td>
        <td><div align="center"><img src="https://i.imgur.com/PuWeuww.png" title="source: imgur.com" width="60%"/></div></td>
        <td><div align="center"><img src="https://i.imgur.com/9VM3pgl.png" title="source: imgur.com" width="60%"/></div></td>
    </tr>
    <tr>
    	<td><div align="center"><b>Windows</b></div></td>
        <td><div align="center"><b>Linux</b></div></td>
        <td><div align="center"><b>macOS</b></div></td>
    </tr>
</table>



<h2>macOS</h2>

O Mac OS é um sistema operacional desenvolvido, fabricado e comercializado pela Apple. Ele é projetado para funcionar em computadores Macintosh. Ao comprar um computador da Apple, o macOS vem pré-instalado desde 2002. O Mac OS é o segundo sistema operacional de desktop mais usado no mundo depois do Windows.

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

<h3>História</h3>

1. O seu surgimento ocorreu em 1984, junto ao lançamento do primeiro Macintosh. Esse computador tinha 128 KB de RAM e processadores da família 68000 da Motorola. Inicialmente, o seu sistema operacional era chamado apenas de System. … A partir da versão 7.6, o nome Mac OS começou a ser adotado.
2. Em 2001, a Apple lançou o Mac OS X  10.0. O sistema operacional, do qual os atuais mac OS são  descendentes. O macOS popularizou uma nova linguagem visual e revolucionou o mercado de  dispositivos móveis, entre outros feitos.

<h3>Sistema de Arquivos</h3>

O sistema de arquivos do Mac OS é composto por diversas pastas, como mostra a tabela abaixo:

| Pasta                       | Descrição                                                    |
| --------------------------- | ------------------------------------------------------------ |
| **/**                       | Raiz do Sistema de arquivos. O equivalente ao c:\ do Windows. |
| **/Applications**           | Softwares e aplicativos globais.                             |
| **/Applications/Utilities** | Aplicativos utilitários globais.                             |
| **/bin**                    | Pasta do Terminal. Nesta pasta ficam os principais comandos do Terminal do Mac OS. |
| **/dev**                    | Dispositivos do computador, como o HD por exemplo.           |
| **/Library**                | Bibliotecas essenciais compartilhadas pelos programas e módulos do kernel. |
| **/Network**                | Lista de computadores conectados na mesma rede.              |
| **/System**                 | Arquivos do Sistema Operacional - Mac OS                     |
| **/Users**                  | Pasta onde ficam armazenadas as pastas dos usuários (Home directory). |
| **/Users/name**             | Diretório privado do usuário (Home directory), onde name é o nome o usuário. |
| **/usr/local**              | Aplicativos Local                                            |
| **/Volumes**                | Ponto de montagem para montar um sistema de arquivos temporariamente, como um drive de DVD, por exemplo. |
| **/Volumes/name**           | Volume montado, identificado pelo nome, onde name é o nome do volume. |



<h3>Meta Directories</h3>

Existem alguns diretórios especiais, que embora não sejam diretórios reais, eles apontam para diretórios reais, funcionando como uma espécie de atalho. Veja na tabela abaixo:

| Path   | Descrição                       |
| ------ | ------------------------------- |
| **.**  | Pasta atual                     |
| **..** | Pasta anterior                  |
| **~**  | Home Directory do usuário atual |

<h3>Pasta do usuário - Home directory</h3>

Todas as pastas dos usuários possuem algumas pastas padrão, como mostra a tabela abaixo:

| Path               | Descrição                      |
| ------------------ | ------------------------------ |
| **~**              |                                |
| **Users/name**     | , onde name é o nome o usuário |
| **~/Applications** |                                |
| **~/Desktop**      |                                |
| **~/Documents**    |                                |
| **~/Downloads**    |                                |
| **~/Library**      |                                |
| **~/Movies**       |                                |
| **~/Music**        |                                |
| **~/Pictures**     |                                |
| **~/Public**       |                                |
| **~/Sites**        |                                |

<h2>Terminal do Mac</h2>

Todos os computadores pessoais hoje em dia vêm com uma interface gráfica de usuário (GUI - Graphical User Interface), embora nem sempre tenha sido assim. Antigamente os computadores eram inicializados em um terminal, somente texto. Tudo o que aparecia na tela era um cursor piscando. Sem um manual do usuário, não era possível saber quais comandos você deveria digitar, porquê o sistema não era nada intuitivo. 

O sistema operacional vem com muitos aplicativos pré-instalados. Alguns deles você conhece, tais como: Calendário, Mail, Fotos e Navegador de Internet. Outros, você não estará familiarizado, e eles são mais comumente conhecidos como comandos do Terminal, tais como: **cat, cp, df, echo e rm**. Um aplicativo foi empacotado com o macOS desde o primeiro lançamento, em 2001. Para ter acesso a estes comandos, utilizaremos o aplicativo que é chamado de “Terminal” como mostra a imagem abaixo:

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

O terminal ou Shell nada mais é do que um aplicativo que encaminha os comandos para o Sistema Operacional. Ele
interpreta os comandos enviados e retorna os resultados. Apesar de não possuir uma interface gráfica elaborada
ele possui uma infinidade de funcionalidades. O conhecimento dos comandos poderá auxiliá-lo para o aumento da
produtividade, pois muitas tarefas podem ser automatizadas.

O terminal do Mac OS X pode ser acessado através da interface gráfica, clicando no ícone do **Terminal**.



O macOS e o Linux têm muito em comum, e isso é evidente com o Terminal. O Linux e o macOS são baseados no sistema operacional UNIX. A maioria dos comandos do Terminal do Mac são os mesmos utilizados no Linux.

<h3>O teclado do MAC</h3>

O teclado dos computadores da Apple, são um pouco diferentes do teclado padrão Windows. Veja na imagem abaixo:

<div align="center"><img src="https://i.imgur.com/XjevLFE.jpg" title="source: imgur.com" /></div>

A principal diferença estão nas teclas modificadoras, que utilizam símbolos específicos, como mostra a figura abaixo:

| Tecla              | Símbolos |
| ------------------ | -------- |
| **Command (Cmd)**  | ⌘        |
| **Shift**          | ⇧        |
| **Option (Alt)**   | ⌥        |
| **Control (Ctrl)** | ⌃        |
| **Caps Lock**      | ⇪        |
| **Fn**             |          |



<h3>Atalhos do Terminal</h3>

Dentro do Terminal do Mac, 99% dos comandos são inseridos via teclado. O mouse praticamente não possui funcionalidade dentro do Terminal, no máximo selecionar o texto para copiar ou colar comandos. Todo o resto é feito via teclado. Abaixo, temos uma tabela contendo os principais atalhos do Terminal do Mac:

| Atalho                           | Descrição                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| setas direcionais                     |Mover  o cursor.|
|  ^ + a |Mover  o cursor para o início da linha de comandos.|
|  ^ + e |Mover  o cursor para o fim da linha de comandos.|
|  ^ + p                  |Busca  o comando anterior.|
|  ^ + n                   |Busca  o próximo comando.|
|  ^ + b |Mover  o cursor um caractere para a esquerda.|
|  ^ + f |Mover  o cursor um caractere para a direita.|
|  ^ + l                             |Apaga  a tela.|
|  ^ + u  |Apaga  os caracteres a esquerda do cursor.|
|  ^ + k   |Apaga  os caracteres a direita do cursor|
|  ^ + delete  |Apaga  o caractere abaixo do cursos.|
| backspace                  |Apaga  caractere a esquerda.|
|  ^ + h               |Apaga  caractere a esquerda.|
|  ^ + w           |Recorta  e copia para o clipboard.|
|  ^ + y              |Cola  o conteúdo do clipboard|
|  ^ + c       |Interrompe  a execução de um comando|
|  ^ + r               |Busca  comando no histórico.|
| ⌘ + "              |Navegação  entre comandos.|
| ⌘ + #              |Navegação  entre comandos.|



