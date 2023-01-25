<h1>Terminal</h1>

Antes de falarmos sobre terminal, vamos definir alguns conceitos importantes relacionados ao computador.

<h2>1. Hardware</h2>

Hardware **é a parte física do computador, ou seja, o conjunto de componentes eletrônicos, peças e equipamentos que fazem o computador funcionar**. A palavra hardware pode se referir também ao conjunto de equipamentos acoplados em produtos que precisam de algum tipo de processamento computacional.

Na imagem abaixo, temos os principais componentes de um computador:

<div align="center"><img src="https://i.imgur.com/M6BJRdi.png" title="source: imgur.com" width="60%"/></div>

- **Processador (CPU):** O processador é a unidade central de processamento de um computador (CPU), que funciona como o cérebro do computador, pois interage e faz as conexões necessárias entre todos os programas instalados.
- **Memória RAM:** Permite a leitura e a escrita de arquivos. Ou seja, a sua função é possibilitar que o processador tenha acesso imediato aos dados que deseja, contribuindo para uma maior rapidez e capacidade de resposta das solicitações;
- **HD - SSD:** Responsável por armazenar os dados, programas e o Sistema Operacional;
- **Monitor:** Dispositivo de saída;
- **Teclado e Mouse:** Dispositivos de entrada.

Os computadores da Apple mais atuais utilizam os processadores M1 e M2, baseado na **Arquitetura ARM**. Ele possui 8 núcleos de processamento e o chip tem “um dos núcleos mais rápidos do mundo” e “uma das melhores performances por watt”, consumindo pouquíssima energia. Em 2023, deve chegar ao mercado o processador M3.

<table width="100%" align="center">  
  <tr>    
    <td width="33%"><div align="center"><img src="https://i.imgur.com/j8d4MiZ.jpg" title="source: imgur.com" width="60%"/></div></td>    
    <td width="33%"><div align="center"><img src="https://i.imgur.com/horESg7.jpg" title="source: imgur.com" width="60%"/></div></td>
    <td width="33%"><div align="center"><img src="https://i.imgur.com/Vsp2Vl3.jpg" title="source: imgur.com" width="60%"/></div></td>
  </tr>  
</table>


> A sigla **ARM** quer dizer **Advanced RISC Machine** (Máquina RISC Avançada), e o termo RISC diz respeito a um conjunto de instruções de processadores. Esse padrão é utilizado em todos os processadores ARM, uma vez que é uma demanda da arquitetura.
>
> **RISC** é um conjunto de instruções reduzido, mais limitado, fazendo as instruções serem mais simples que o sistema CISC (conjunto de instruções complexas), utilizado nos PCs. O sistema RISC exige menos do processador, assim o chip não precisa de tanta energia, o que é essencial em dispositivos móveis que possuem bateria.

<h2>2. Software</h2>

Software é a parte virtual, lógica, imaterial do computador. Corresponde ao **conjunto de informações e instruções a serem executadas, a fim de se conseguir o resultado esperado**.

Quando pensamos em sistema, normalmente pensamos em uma interface visual, que é o elemento de interação com o ser humano, mas um software pode existir sem nada visual. Ele pode estar embutido em um micro-controlador que comanda um circuito eletrônico, mas não é ligado em um monitor. Ele pode ser simplesmente um software feito para computador, mas sem interface, como um programa robô que fica checando alguma atividade do computador. Existem diferentes tipos de software para diversas finalidades.

<div align="center"><img src="https://i.imgur.com/QKmo44o.png" title="source: imgur.com" width="60%"/></div>

<h2>3. Sistema Operacional</h2>

O **Sistema operacional** é um tipo especial de software. Ele é um software de base, que possui diferentes funções. Uma delas é controlar o equipamento, provendo uma interface de controle para o usuário realizar suas configurações e utilizar o equipamento. Outra é oferecer um protocolo para que outros softwares, software-aplicativos, sejam instalados sobre o sistema operacional, como um editor de texto ou um game, por exemplo.

<div align="center"><img src="https://i.imgur.com/4uvIv9K.png" title="source: imgur.com" width="60%"/></div>

Observe na imagem acima que o Sistema Operacional está localizado entre o Hardware e os Softwares aplicativos. Sem o sistema operacional, o computador não consegue realizar nenhuma tarefa.

<h3>3.1. Kernel</h3>

O **kernel é o componente principal de um sistema operacional e a interface central entre o hardware e os processos executados por um computador**. Ele estabelece a comunicação entre ambos, gerenciando recursos com a maior eficiência possível.

<h3>3.2. Utilitários do Sistema</h3>

São os aplicativos auxiliares, que complementam o Sistema Operacional, oferecendo recursos adicionais para um melhor funcionamento do sistema.

<h3>3.3. Principais Sistemas Operacionais</h3>

Os principais sistemas operacionais para computadores disponíveis no mercado são: 

<table>
  <tr>
    <td><div align="center"><img src="https://i.imgur.com/za4tPUA.png" title="source: imgur.com" width="60%"/></div></td>
    <td><div align="center"><img src="https://i.imgur.com/PuWeuww.png" title="source: imgur.com" width="60%"/></div></td>
    <td><div align="center"><img src="https://i.imgur.com/9VM3pgl.png" title="source: imgur.com" width="60%"/></div></td>
  </tr>
  <tr>
  	<td><div align="center"><b>Windows</b></div></td>
    <td><div align="center"><b>Linux</b></div></td>
    <td><div align="center"><b>MacOS</b></div></td>
  </tr>
</table>

<br />

<h2>4. MacOS</h2>

O Mac OS é um sistema operacional desenvolvido, fabricado e comercializado pela Apple. Ele é projetado para funcionar em computadores Macintosh. Ao comprar um computador da Apple, o macOS vem pré-instalado desde 2002. O Mac OS é o segundo sistema operacional de desktop mais usado no mundo depois do Windows.

<div align="center"><img src="https://i.imgur.com/pVKLEnp.png" title="source: imgur.com" /></div>

<h3>4.1. Sistema de Arquivos</h3>

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

<br />

<h3>4.2. Meta Directories</h3>

Existem alguns diretórios especiais, que embora não sejam diretórios reais, eles apontam para diretórios reais, funcionando como uma espécie de atalho. Veja na tabela abaixo:

| Path   | Descrição                       |
| ------ | ------------------------------- |
| **.**  | Pasta atual                     |
| **..** | Pasta anterior                  |
| **~**  | Home Directory do usuário atual |

<br />

<h3>4.3. Pasta do usuário - Home directory</h3>

Todas as pastas dos usuários possuem algumas pastas padrão, como mostra a tabela abaixo:

| Path               | Descrição                                                 |
| ------------------ | --------------------------------------------------------- |
| **~/Applications** | Aplicativos do usuário                                    |
| **~/Desktop**      | Área de trabalho do usuário                               |
| **~/Documents**    | Documentos e arquivos do usuário                          |
| **~/Downloads**    | Arquivos do usuário obtidos via download                  |
| **~/Library**      | Arquivos específicos dos aplicativos do usuário           |
| **~/Movies**       | Arquivos de vídeo do usuário                              |
| **~/Music**        | Arquivos de audio do usuário                              |
| **~/Pictures**     | Imagens do usuário                                        |
| **~/Public**       | Arquivos que o usuário deseja compartilhar sem restrições |
| **~/Sites**        | Páginas da Web, usadas para compartilhamento na Web       |

<br />

<h2>5. Terminal do Mac</h2>

Todos os computadores pessoais hoje em dia vêm com uma interface gráfica de usuário (GUI - Graphical User Interface), embora nem sempre tenha sido assim. Antigamente os computadores eram inicializados em um terminal, somente texto. Tudo o que aparecia na tela era um cursor piscando. Sem um manual do usuário, não era possível saber quais comandos você deveria digitar, porquê o sistema não era nada intuitivo. 

O sistema operacional vem com muitos aplicativos pré-instalados. Alguns deles você conhece, tais como: Calendário, Mail, Fotos e Navegador de Internet. Outros, são mais comumente conhecidos como comandos do Terminal, tais como: **cat, cp, rm, entre outros**. Para ter acesso a estes comandos, utilizaremos o aplicativo que é chamado de **Terminal**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/fcldjTw.png" title="source: imgur.com" /></div>

O terminal ou Shell nada mais é do que um aplicativo que encaminha os comandos para o Sistema Operacional. Ele
interpreta os comandos enviados e retorna os resultados. Apesar de não possuir uma interface gráfica elaborada
ele possui uma infinidade de funcionalidades. O conhecimento dos comandos poderá auxiliá-lo para o aumento da
produtividade, pois muitas tarefas podem ser automatizadas.

O terminal do Mac OS X pode ser acessado através da interface gráfica através do **Finder**, em **Applications 🡲 utilities**, clicando no ícone do **Terminal**.

<div align="center"><img src="https://i.imgur.com/uuFWeAt.png" title="source: imgur.com" /></div>

O macOS e o Linux têm muito em comum, e isso é evidente com o Terminal. O Linux e o macOS são baseados no sistema operacional UNIX. A maioria dos comandos do Terminal do Mac são os mesmos utilizados no Linux.

<h3>5.1. O teclado do MAC</h3>

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

<br />

<h3>5.2. Atalhos do Terminal</h3>

Dentro do Terminal do Mac, 99% dos comandos são inseridos via teclado. O mouse praticamente não possui funcionalidade dentro do Terminal, no máximo selecionar o texto para copiar ou colar comandos. Todo o resto é feito via teclado. Abaixo, temos uma tabela contendo os principais atalhos do Terminal do Mac:

| Atalho                           | Descrição                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| **setas direcionais**                 |Mover o cursor.|
| **^ + a** |Mover o cursor para o início da linha de comandos.|
| **^ + e** |Mover o cursor para o fim da linha de comandos.|
|  **^ + p**              |Busca o comando anterior.|
|  **^ + n**               |Busca o próximo comando.|
| **^ + b** |Mover o cursor um caractere para a esquerda.|
| **^ + f** |Mover o cursor um caractere para a direita.|
|  **^ + l**                         |Apaga a tela.|
|  **^ + u**  |Apaga os caracteres a esquerda do cursor.|
| **^ + k** |Apaga os caracteres a direita do cursor|
|  **^ + delete**  |Apaga o caractere abaixo do cursos.|
| **backspace**              |Apaga caractere a esquerda.|
|  **^ + h**           |Apaga caractere a esquerda.|
|  **^ + w**       |Recorta e copia para o clipboard.|
|  **^ + y**          |Cola o conteúdo do clipboard|
|  **^ + c**   |Interrompe a execução de um comando|
|  **^ + r**           |Busca comando no histórico.|
| **⌘ + "**          |Navegação entre comandos.|
| **⌘ + #**          |Navegação entre comandos.|

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
