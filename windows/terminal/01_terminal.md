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

Os computadores Windows mais atuais utilizam os processadores Intel.

Os Processadores Intel mais atuais, são baseados na **Arquitetura Hibrida**. O Processador I9 (mais rápido da família), da 13º geração, possui 24 núcleos (**sendo 12 p-cores e 12 e-cores**) de processamento e o chip tem “um dos núcleos mais rápidos do mundo”.

> **Arquitetura Hibrida**
>
> Os processadores Intel da 13ª Geração se adaptam à maneira como você utiliza o computador. Ao jogar, o processador impede que tarefas em segundo plano interrompam ou usem núcleos de alto  desempenho, resultando em uma jogabilidade mais estável. Quando você  está usando seu sistema para tarefas genéricas, ele oferece uma experiência mais suave no nível do  sistema.
>
> A Arquitetura hibrida possui dois tipos de  núcleos em um único processador: 
>
> - **Performance-cores (P-cores)** poderosos;
> - **Efficient-cores (E-cores)** flexíveis. 
>
> **Performance-cores são:**
>
> - Núcleos de alto desempenho e fisicamente maiores, projetados para velocidade enquanto mantêm a eficiência.
> - Ideal para processar o trabalho pesado exigido por muitos mecanismos de jogos.
>
> **Os Efficient-cores são:**
>
> - Fisicamente menores, com vários E-cores se encaixando no espaço físico de um P-core.
> - Ideais para desempenho escalável. Eles trabalham em  conjunto com os P-cores para acelerar tarefas que exigem muito do núcleo (como ao renderizar um vídeo, por exemplo).
> - Otimizado para executar tarefas em segundo plano com eficiência.  Tarefas menores podem ser transferidas para E-cores (por exemplo, lidar  com Discord ou software antivírus), deixando os P-cores livres para  impulsionar o desempenho dos jogos.

<br />

<table width="100%" align="center">  
  <tr>    
    <td width="25%"><div align="center"><img src="https://i.imgur.com/88JsuRM.png" title="source: imgur.com" width="80%"/></div></td>    
    <td width="25%"><div align="center"><img src="https://i.imgur.com/2zzoWY2.png" title="source: imgur.com" width="80%"/></div></td>
    <td width="25%"><div align="center"><img src="https://i.imgur.com/VmtmjAg.png" title="source: imgur.com" width="80%"/></div></td>    
    <td width="25%"><div align="center"><img src="https://i.imgur.com/J1KVFFW.png" title="source: imgur.com" width="80%"/></div></td>
  </tr>  
</table>

<br />

<h2>2. Software</h2>

Software é a parte virtual, lógica, imaterial do computador. Corresponde ao **conjunto de informações e instruções a serem executadas, a fim de se conseguir o resultado esperado**.

Quando pensamos em sistema, normalmente pensamos em uma interface visual, que é o elemento de interação com o ser humano, mas um software pode existir sem nada visual. Ele pode estar embutido em um micro-controlador que comanda um circuito eletrônico, mas não é ligado em um monitor. Ele pode ser simplesmente um software feito para computador, mas sem interface, como um programa robô que fica checando alguma atividade do computador. Existem diferentes tipos de software para diversas finalidades.

<div align="center"><img src="https://i.imgur.com/QKmo44o.png" title="source: imgur.com" width="60%"/></div>

<br />

<h2>3. Sistema Operacional</h2>

O **Sistema operacional** é um tipo especial de software. Ele é um software de base, que possui diferentes funções. Uma delas é controlar o equipamento, provendo uma interface de controle para o usuário realizar suas configurações e utilizar o equipamento. Outra é oferecer um protocolo para que outros softwares, software-aplicativos, sejam instalados sobre o sistema operacional, como um editor de texto ou um game, por exemplo.

<div align="center"><img src="https://i.imgur.com/Bw3Wsd8.png" title="source: imgur.com" width="60%"/></div>

Observe na imagem acima que o Sistema Operacional está localizado entre o Hardware e os Softwares aplicativos. Sem o sistema operacional, o computador não consegue realizar nenhuma tarefa.

<h3>3.1. Kernel Mode</h3>

O **kernel Mode é o componente principal de um sistema operacional e a interface central entre o hardware e os processos executados por um computador**. Ele estabelece a comunicação entre ambos, gerenciando recursos com a maior eficiência possível.

<h3>3.2. User Mode</h3>

O User Mode é composto por 2 subsistemas:

**Os subsistemas integrais** incluem processos de suporte de sistema fixo (como gerenciador de  sessão e processo de login), processos de serviço (como agendador de  tarefas e serviço de spooler de impressão), subsistema de segurança  (para tokens de segurança e gerenciamento de acesso) e aplicativos de  usuário.

**O subsistema de ambiente** atua como um link entre os aplicativos do modo de usuário e as funções do kernel do sistema operacional. Existem quatro subsistemas de ambiente primário, ou seja, Win32, POSIX, OS/2 e subsistema Windows para LINUX (WSL2).

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

<h2>4. Windows</h2>

O Windows é um sistema operacional desenvolvido, fabricado e comercializado pela Microsoft. Ele é projetado para funcionar em computadores Intel, AMD e alguns Macintosh. Ao comprar um computador atualmente, é quase certo que o Windows virá pré-instalado. O Windows é o sistema operacional desktop mais usado no mundo. Atualmente, ele está na versão 11.

<div align="center"><img src="https://i.imgur.com/V4YsorU.jpg" title="source: imgur.com" /></div>

<h3>4.1. Sistema de Arquivos</h3>

O sistema de arquivos do Windows é composto por diversas pastas, todas localizadas dentro da unidade de disco local c:, como mostra a tabela abaixo:

| Pasta                           | Descrição                                                    |
| ------------------------------- | ------------------------------------------------------------ |
| **Arquivos de Programas**       | Softwares e aplicativos globais - 64 bits.                   |
| **Arquivos de Programas (x86)** | Softwares e aplicativos globais - 32 bits.                   |
| **PerfLogs**                    | Pasta do sistema usada pelo Monitor de desempenho do Windows para armazenar logs / relatórios. |
| **Usuarios**                    | Pasta onde ficam armazenadas as pastas dos usuários (Home Directory). |
| **Windows**                     | Pasta onde fica armazenado o Sistema Operacional Windows.    |

<br />

<h3>4.3. Pasta do usuário - Home directory</h3>

Todas as pastas dos usuários possuem algumas pastas padrão, como mostra a tabela abaixo:

| Path               | Descrição                                       |
| ------------------ | ----------------------------------------------- |
| **Área de Trabalho**      | Área de trabalho do usuário                     |
| **Documentos**    | Documentos e arquivos do usuário                |
| **Downloads**    | Arquivos do usuário obtidos via download        |
| **Vídeos**       | Arquivos de vídeo do usuário                    |
| **Músicas**        | Arquivos de audio do usuário                    |
| **Imagens**        | Imagens do usuário                              |
| **Favoritos** | Links dos sites salvos no Favoritos do Edge |

<br />

<h2>5. Terminal do Windows</h2>

Todos os computadores pessoais hoje em dia vêm com uma interface gráfica de usuário (GUI - Graphical User Interface), embora nem sempre tenha sido assim. Antigamente os computadores eram inicializados em um terminal, somente texto. Tudo o que aparecia na tela era um cursor piscando. Sem um manual do usuário, não era possível saber quais comandos você deveria digitar, porquê o sistema não era nada intuitivo. 

O sistema operacional vem com muitos aplicativos pré-instalados. Alguns deles você conhece, tais como: Calendário, Fotos e Navegador de Internet. Outros, são mais comumente conhecidos como comandos do Terminal, tais como: **dir, copy, ren, entre outros**. Para ter acesso a estes comandos, utilizaremos o aplicativo que é chamado de **Prompt de Comando - CMD**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/1FB25fg.png" title="source: imgur.com" /></div>

O terminal ou Shell nada mais é do que um aplicativo que encaminha os comandos para o Sistema Operacional. Ele
interpreta os comandos enviados e retorna os resultados. Apesar de não possuir uma interface gráfica elaborada
ele possui uma infinidade de funcionalidades. O conhecimento dos comandos poderá auxiliá-lo para o aumento da
produtividade, pois muitas tarefas podem ser automatizadas.

<h3>5.1. Atalhos do Terminal</h3>

Dentro do Terminal do Mac, 99% dos comandos são inseridos via teclado. O mouse praticamente não possui funcionalidade dentro do Terminal, no máximo selecionar o texto para copiar ou colar comandos. Todo o resto é feito via teclado. Abaixo, temos uma tabela contendo os principais atalhos do Terminal do Mac:

| Atalho                           | Descrição                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| **🠈 / 🠊 / 🠉 / 🠋** |Mover o cursor.|
| **Ctrl + V ou Shift + Insert** | Cola o texto na posição do cursor.                           |
| **Ctrl + C ou Ctrl + Insert**   | Copia o texto selecionado para a área de transferência.      |
| **Ctrl + A**                    | Selecionar todo o texto na linha atual, se a linha contém texto. Se é  uma linha vazia, selecione todo o texto no prompt de comando. |
| **Shift + 🠈 / 🠊 / 🠉 / 🠋**       | Move o cursor para a esquerda ou direita de um caractere, para cima ou  para baixo de uma linha, selecionando o texto ao longo do caminho. |
| **Ctrl + Shift + 🠈 / 🠊**        | Move o cursor uma palavra para a esquerda ou para a direita, selecionando essa palavra ao longo do caminho. |
| **Shift + Home / End**          | Move o cursor para o início ou fim da linha atual, selecionando o texto ao longo do caminho. |
| **Shift + Page Up / Page Down** | Move o cursor para cima ou para baixo uma tela, selecionando o texto. |
| **Ctrl + Shift + Home / End**   | Move o cursor para o início ou fim do "buffer de tela", selecionando  todo o texto entre o cursor e o início ou o final do Prompt de Comando. |
| **Ctrl + 🠉 / 🠋**                | Move uma linha para cima ou para baixo no histórico do Prompt de Comando (é como usar a barra de rolagem). |
| **Ctrl + Page Up / Page Down**  | Move uma página para cima ou para baixo na história do Prompt de Comando (é como rolar ainda mais longe). |
| **Alt + F4**                    | Fecha a janela do prompt de comando.                         |

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
