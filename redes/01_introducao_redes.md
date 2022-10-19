<h1>Introdução a Redes de Computadores e Internet</h1>

**Rede de computadores** é um conjunto de equipamentos interligados de maneira a se comunicarem, trocarem informações e compartilharem recursos, como arquivos de dados gravados, impressoras, modems, softwares e outros equipamentos.

Quando falamos em Redes de Computadores, um outro conceito fundamental, que não pode ser ignorado é a Comunicação de dados, que é a troca de informação entre dois dispositivos através de algum meio de comunicação como, por exemplo, um par de fios:

<div align="center"><img src="https://i.imgur.com/allVfc3.png" title="source: imgur.com" width="90%"/></div>

Um sistema básico de comunicação de dados é composto por cinco elementos:

1. **Mensagem:** é a informação a ser transmitida; 
2. **Transmissor:** é o dispositivo que envia a mensagem de dados;
3. **Receptor:** é o dispositivo que recebe a mensagem;
4. **Meio:** é o caminho físico por onde viaja uma mensagem dirigida ao receptor;
5. **Protocolo:** é um conjunto de regras que governa a comunicação de dados. Ele representa um acordo entre os dispositivos que se comunicam.

Estes 5 elementos são a base de qualquer Rede de computadores, como veremos na sequência.

<h2>1. Modelo OSI</h2>

Para facilitar e unificar a interconexão de sistemas de computadores, a ISO (International Standards Organization) desenvolveu um modelo de referência chamado OSI (Open Systems Interconnection), para que os fabricantes pudessem criar protocolos de comunicação a partir desse modelo.

O modelo OSI tenta explicar o funcionamento da rede, dividindo-a em 7 camadas. Embora seja apenas um modelo teórico, que não precisa necessariamente ser seguido à risca pelos protocolos de rede, o modelo OSI é interessante, pois é muito útil para explicar diversos aspectos teóricos do funcionamento de uma rede de computadores. 

> Em Redes de computadores, **protocolo** é a “linguagem” usada pelos dispositivos de uma rede de modo que eles consigam se entender, isto é, trocar informações entre si. Um protocolo é um conjunto de regras que governa a comunicação de dados.

<h2>1.1. Por que o modelo OSI é importante?</h2>

Embora a internet moderna não siga estritamente o modelo OSI, o  modelo continua sendo muito útil para solucionar problemas de Rede. Seja uma pessoa que não consegue colocar seu notebook na internet ou um site que esteja inativo para milhares de usuários, o modelo OSI pode ajudar a resolver e isolar a fonte do problema. Se o problema puder ser reduzido a uma camada específica do modelo, muito trabalho desnecessário poderá  ser evitado.

<h3>1.2. Camadas do modelo OSI</h3>

O modelo de referência OSI é o método para descrever como os conjuntos interconectados de hardware e software de rede podem ser organizados para trabalhem em conjunto no mundo das redes. Com efeito, o modelo OSI oferece um modo de dividir arbitrariamente a tarefa da rede em camadas separadas, que estão sujeitos ao processo formal de padronização.
O modelo de referência OSI descreve sete camadas de funções de rede, descritas na imagem abaixo:

<div align="center"><img src="https://i.imgur.com/FAwRS0y.png" title="source: imgur.com" width="75%"/></div>

<h4>1.2.1. Camada de Aplicação</h4>

Essa é a única camada que interage diretamente com os dados do usuário. Os softwares aplicativos, como navegadores web e clientes de e-mail, dependem da camada de aplicação para iniciar as comunicações. Os softwares aplicativos clientes não fazem parte da camada de aplicação, a camada de aplicação é responsável pelos protocolos e manipulação de dados dos quais o software depende para apresentar dados significativos ao usuário. Os protocolos da camada de aplicação incluem o **HTTP** (**Hypertext Transfer Protocol**) e o **SMTP** (**Simple Mail Transfer Protocol**).

<h4>1.2.2. Camada de Apresentação</h4>

A camada de apresentação converte o formato do dado recebido pela camada de aplicação em um formato comum
a ser usado na transmissão desse dado. A camada de apresentação é responsável pela tradução, criptografia e compactação dos dados.

Dois dispositivos de comunicação que se comunicam podem usar métodos de codificação diferentes; por isso, a camada 6 é responsável pela tradução dos dados de entrada em uma sintaxe que a camada de aplicação do dispositivo receptor possa entender.

Se os dispositivos se comunicarem por meio de uma conexão criptografada, a camada 6 será responsável por adicionar a criptografia na extremidade do remetente e decodificar a criptografia na extremidade do destinatário, podendo, assim, apresentar dados não criptografados e legíveis à camada de aplicação.

Finalmente, a camada de apresentação também é responsável por compactar os dados recebidos da camada de aplicação antes de entregá-los à camada 5. Isso ajuda a aumentar a velocidade e a eficiência da comunicação ao minimizar a quantidade de dados que serão transferidos.

<h4>1.2.3. Camada de Sessão</h4>

A camada de sessão permite que duas aplicações em computadores diferentes estabeleçam uma sessão de
comunicação. O tempo decorrido entre o momento em que a comunicação é aberta e fechada é conhecido como "**sessão**". A camada de sessão garante que a sessão permaneça aberta pelo tempo necessário para transferir todos os dados que estão sendo trocados e, em seguida, fecha imediatamente a sessão para evitar o desperdício de recursos.

<h4>1.2.4. Camada de Transporte</h4>

A camada de transporte é responsável pela comunicação de ponta a ponta entre os dois dispositivos. Isso inclui receber os dados da camada de sessão e  dividi-los em porções menores chamadas **segmentos** antes de enviá-los para a  camada de rede. A camada de transporte no dispositivo receptor é responsável  por remontar os segmentos em dados, que a camada de sessão possa  consumir.

<h4>1.2.5. Camada de Rede</h4>

É responsável pelo endereçamento lógico dos pacotes (IP), convertendo endereços lógicos em endereços físicos, de
forma que os pacotes consigam chegar corretamente ao destino.  A camada de rede divide os segmentos da camada de transporte em  unidades menores denominadas **pacotes** no dispositivo remetente e remonta  esses pacotes no dispositivo receptor. A camada de rede também encontra o melhor caminho físico para que os dados cheguem ao seu destino, o que é conhecido como "**roteamento**".

<h4>1.2.6. Camada de Enlace de Dados</h4>

A camada de enlace recebe os pacotes de dados recebidos da camada de rede e os transforma em quadros que
trafegarão pela rede, adicionando informações como o endereço (MAC) da placa de rede de origem, o endereço (MAC) da placa de rede de destino, os dados de controle, os dados em si e a checagem de redundância cíclica (CRC).

<h4>1.2.7. Camada Física</h4>

Essa camada inclui o equipamento físico envolvido na transferência de  dados, como cabos e switches. Essa também é a camada em que os dados  são convertidos em um fluxo de bits, que é uma sequência de 1s e 0s. A  camada física de ambos os dispositivos também precisa aceitar de comum  acordo uma convenção de sinal para que se possa distinguir os 1s dos 0s  em ambos os dispositivos.

<br />

<h2>2. O que é a Internet?</h2>

A Internet é uma rede global de computadores. Imagine um sistema postal que entrega e que recebe pacotes em velocidades extremamente rápidas. 

Este sistema utiliza os Protocolos TCP/IP e HTTP para se comunicar. Qualquer indivíduo com permissão é capaz de obter informações de outro computador.

<h3>2.2 Protocolo</h3>

Um <b>protocolo</b> é um sistema de regras que define como o dado é trafegado dentro ou entre computadores. Comunicações entre dispositivos requer que estes concordem com o formato do dado que estiver sendo trafegado. O conjunto de regras que define esse formato é chamado de protocolo.

<h2>3. Protocolo TCP/IP</h2>

O TCP/IP é um conjunto de protocolos de comunicação. O nome vem de dois protocolos **TCP** (*Transmission Control Protocol*) e o **IP** (*Internet Protocol*). Ele tem por objetivo padronizar todas as comunicações de rede, principalmente as comunicações na web. O TCP/IP é o Protocolo que define a Internet.

<h3>3.1 Modelo TCP/IP</h3>

<div align="center"><img width="70%" src="https://i.imgur.com/PhKzoIu.png" title="source: imgur.com" />
<br /><i>O Modelo TCP/IP</i></div>

O modelo TCP/IP possui 4 camadas:

 <h4>3.1.1. Camada 4: Aplicação</h4>

Nesta camada encontra-se todos os protocolos de serviço que efetuam a comunicação direta com o software para identificar o tipo de requisição que está sendo realizada. O protocolo mais popular é o HTTP.

<h4>3.1.2. Camada 3: Transporte </h4>

Esta camada é Responsável pela comunicação entre hosts (Clientes e Servidores) envolvidos. Ela tem como função principal verificar se o pacote de dados alcançou seu destino e se os dados nele contidos chegaram de maneira integra. O protocolo mais popular é o TCP.

<h4>Pacote</h4>

Pacote é o formato no qual os dados são enviados do servidor para o cliente e vice e versa. Basicamente, quando os dados são enviados pela web, eles são enviados como milhares de pequenos blocos, para agilizar e simplificar o tráfico de dados pela Internet.

<div align="center"><img width="600px" src="https://i.imgur.com/zt1ekXp.png" title="source: imgur.com" />
<br /><i>Em azul temos o grande bloco de dados e logo abaixo, na cor amarela, o bloco dividido em pacotes menores que serão identificados e enviados para o seu destino</i></div>


<h4>Portas</h4>

A camada de transporte utiliza portas lógicas para garantir que a aplicação que iniciou a conversação encontrará no seu destino a aplicação desejada. 
Essas portas lógicas são canais virtuais, geralmente definidos pelo Sistema Operacional, que se abrem conforme o tipo de aplicação que se está executando. 
O **HTTP** utiliza as **portas 8080** (Localmente, ou seja, no seu Computador) e a **porta 80** (Internet).

<div align="center"><img src="https://i.imgur.com/Kc23EQ2.png" title="source: imgur.com" /></div>

No Exemplo acima, o pacote que chegou na Camada de Aplicação contém a informação **Porta: 8080**. Observe que neste cenário o Spring está utilizando a porta 8080, logo o TCP irá redirecionar o pacote para a nossa aplicação Spring. Se a Porta, por exemplo, estivesse com o valor 3306 o TCP redirecionaria para o MySQL.

<div align="left"><img src="https://i.imgur.com/cDPH4tl.png" title="source: imgur.com" width="30px"/> <a href="https://pt.wikipedia.org/wiki/Lista_de_portas_dos_protocolos_TCP_e_UDP" target="_blank"><b>Lista de portas - Protocolo HTTP</b></a></div>

<h4>3.1.3. Camada 2: Internet</h4>

Nesta camada encontramos os endereços IP de origem e destino de uma conexão. O IP também é conhecido como o endereço lógico (pode ser alterado).

<h4>3.1.4. Camada 1: Acesso a Rede</h4>

Nesta camada encontramos a conexão física da rede pela qual o pacote trafega. Cada equipamento conectado na rede carrega consigo a identidade do hardware que deu origem ao envio do pacote, armazenando o seu endereço MAC (Media Access Control). O MAC também é conhecido como Endereço físico (não pode ser alterado).

**Como funciona o Protocolo TCP/IP?**

<img width="30px" src="https://i.imgur.com/4gupQvJ.png" title="source: imgur.com" />  Assista ao vídeo *Warriors of the NET - IP for Peace* no link: <a href="https://youtu.be/Iqcp3k8DgGw" target="_blank">https://youtu.be/Iqcp3k8DgGw</a>

<br />

<h3>3.2 TCP/IP x OSI</h3>

O modelo OSI e o modelo TCP/IP possuem muitas características em  comum, pois ambos tratam de vários protocolos que são independentes.

Assim eles possuem também uma divisão de funções por camadas, e elas  são muito parecidas. Apesar disso, há algumas diferenças fundamentais  entre os modelos, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/TwhLZrk.png" title="source: imgur.com" /></div>

As principais diferenças entre TCP/IP e OSI são:

- O OSI possui 7 camadas e o TCP/IP possui apenas 4.
- O TCP/IP mesclou as camadas 5 e 6 do OSI para a camada 7 - Aplicação.
- Há uma camada chamada de Internet em TCP/IP enquanto que a mesma é chamada de Redes em OSI.
- O TCP/IP mesclou as camadas 1 e 2 do OSI para a camada Acesso a Rede.

<h2>4. Protocolo HTTP</h2>

O **HTTP (Hypertext Transfer Protocol / Protocolo de Transferência de Hipertexto)** é um protocolo que permite a obtenção de recursos, como documentos HTML. É a base de qualquer troca de dados na Web e um protocolo cliente-servidor, o que significa que as requisições são iniciadas pelo destinatário, geralmente um navegador da Web. 
Um documento completo é reconstruído a partir dos diferentes sub documentos obtidos, como por exemplo texto, descrição do layout, imagens, vídeos, scripts e muito mais.

<div align="center"><img src="https://i.imgur.com/tJ0MQZX.png" title="source: imgur.com" width="80%"/>
<br /><i>Página WEB composta por vários elementos</i></div>


O HTTP também possui uma outra versão chamada de **HTTPS ( Hyper Text Transfer Protocol Secure / Protocolo de Transferência de Hipertexto Seguro)**, que se trata de uma versão do protocolo criptografado, geralmente utilizado em transações bancárias. Ao utilizar o protocolo HTTPS, um cadeado <img width="20px"  src="https://i.imgur.com/kzxGaLT.png" title="source: imgur.com" /> é exibido no Navegador para indicar que a conexão é segura. 

<h3>4.1. O modelo Cliente Servidor</h3>

<div align="center"><img src="https://i.imgur.com/dEiN087.png" title="source: imgur.com" width="80%"/>
<br /><i>Os Clientes acessando o servidor via Internet</i></div>
<h4>3.1.1. Cliente</h4>

O Cliente é qualquer ferramenta que age em nome do usuário. Essa função é predominantemente realizada pelo navegador Web, salvo  algumas poucas exceções, são programas usados por pessoas  Desenvolvedoras Web para testar as suas aplicações (Exemplo: [Insomnia](https://insomnia.rest/)).

<h4>4.1.2. Servidor</h4>

O servidor é a "máquina" que serve o documento requisitado pelo usuário através do endereço www. Um servidor se apresenta virtualmente apenas como uma máquina, porém ele pode ser uma coleção de servidores dividindo a carga ou  um programa complexo que acessa outros servidores gerando toda ou parte do documento solicitado.

<h3>4.2. Fluxo HTTP</h3>

O HTTP funciona como um protocolo **Request-Response** (Solicitação-Resposta), entre um Cliente e um Servidor.

<div align="center"><img src="https://i.imgur.com/3lUSIhM.png" title="source: imgur.com" width="80%"/>
<br /><i>Fluxo de Funcionamento HTTP</i></div>


**<u>Exemplo</u>:** Um cliente (Navegador da Internet) envia uma **Request** HTTP ao servidor e o servidor retorna uma **Response** ao cliente. 

Para o cliente se comunicar com um servidor, ele realiza os seguintes passos:

1.  Abre uma conexão TCP, que será usada para enviar uma requisição, ou várias, e receber uma resposta. 
2.  Envia uma mensagem HTTP (Request).
3.  Lê a resposta do servidor (Response).
4.  Fecha ou reutiliza a conexão para requisições futuras.

<h3>4.3. Request</h3>

<div align="center"><img src="https://i.imgur.com/ryWicc4.png" title="source: imgur.com" />
<br /><i>Request Message Header HTTP</i></div>

As requisições consistem dos seguintes elementos:

1) Um **Método HTTP**, geralmente é um verbo como GET, POST, DELETE e PUT. 
2) O **caminho do recurso (Path)**, ou seja a **URL** do recurso sem os elementos que são de contexto, como o protocolo (http://). 
3) **versão do protocolo HTTP**. 
4) Cabeçalhos opcionais que contém informações adicionais para os servidores. 
5) Body (corpo) para alguns Métodos como o POST e o PUT, que enviam dados para o recurso solicitado dentro da requisição.

<div align="center"><img src="https://i.imgur.com/BD8gfge.png" title="source: imgur.com" />
<br /><i>Request HTTP</i></div>

<br />

<h4>4.3.1. Métodos HTTP (Verbos)</h4>

O protocolo HTTP define um conjunto de **Métodos de requisição** responsáveis por indicar a ação a ser executada para um dado recurso. Estes Métodos são referenciados como <b>Verbos HTTP</b>.  

<b>Principais Verbos HTTP</b>

<table width=100%>
	<tr>
		<td width=30%><b>Verbo
		<td width=70%><b>Descrição
	</tr>
	<tr>
		<td><i>GET
		<td>O Método GET solicita a representação de um recurso específico. Requisições utilizando o Método GET devem retornar apenas dados. Exemplo: Consultar um registro no Banco de Dados.
	</tr>
	<tr>
		<td><i>POST
		<td>O Método POST é utilizado para submeter uma entidade a um recurso específico para o servidor. Exemplo: Inserir um novo registro no Banco de Dados.
	</tr>
	<tr>
		<td><i>PUT
		<td>O Método PUT substitui todas as atuais representações do recurso de destino pela carga de dados da requisição. Exemplo: Atualizar os Atributos de um registro no Banco de Dados.
	</tr>
	<tr>
		<td><i>DELETE
		<td>O Método DELETE remove um recurso específico. Exemplo: Apagar um registro no Banco de Dados.
	</tr>
</table>
<div align="left"><img src="https://i.imgur.com/cDPH4tl.png" title="source: imgur.com" width="30px"/> <a href="https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods" target="_blank"><b>Documentação: HTTP Methods</b></a></div>

<h4/>4.3.2. URL</h4>

Quando acessamos um determinado site a partir do nosso computador, informamos para o navegador o endereço do site, também conhecido como **URL (Uniform Resource Locator)**. O Navegador da Internet se encarrega de descobrir qual o endereço do servidor que armazena o site.

A comunicação com uma aplicação WEB é realizada através de URL's, que são enviadas através da requisições, contendo principalmente o caminho do Recurso (também chamados de endpoints) e os Parâmetros. Veja os Exemplos abaixo:

**Requisição Local (seu computador)**

<div align="center"><img src="https://i.imgur.com/U9SM7Ci.png" title="source: imgur.com" /></div>

**Requisição Remota (servidor na Nuvem)**

<div align="center"><img src="https://i.imgur.com/gMCFUUr.png" title="source: imgur.com" /></div>

| Item           | Descrição                                                    |
| -------------- | ------------------------------------------------------------ |
| **Protocolo**  | Informa ao navegador qual o protocolo de comunicação do endereço (http ou https). Observe que na nuvem (Heroku), utiliza-se o protocolo **https**, enquanto localmente utiliza-se o protocolo **http**. |
| **Domínio**    | É o nome (identificador) do site. Este item é Obrigatório. Observe que localmente o seu computador é identificado como **localhost**, enquanto na Nuvem o endereço vai depender do nome da sua aplicação. |
| **Porta**      | Identifica a porta em que o site está disponível no servidor. Quando não é informada o Navegador preenche internamente com a porta padrão de acordo com o protocolo utilizado. Observe que localmente, a porta deve ser informada e porta padrão do Servidor WEB local é a **8080**, enquanto na Nuvem, mesmo sem informar o numero da porta, por se tratar do protocolo https utiliza-se a porta **443**. |
| **Recurso**    | Identifica qual o recurso o navegador vai buscar no servidor, quando não é informado pelo usuário o próprio navegador preenche com uma "/", que significa página inicial do site. <br />No contexto de uma aplicação WEB, um recurso é um CRUD (Create, Read, Update e Delete) completo de uma tabela no Banco de dados, desenvolvido em uma Linguagem Backend. <br />No exemplo acima, localmente está sendo procurado o recurso Postagens enquanto na Nuvem está sendo procurado o recurso Temas. |
| **Parâmetros** | Utilizado para enviar dados para a aplicação através da URL. <br />No exemplo Local, 12345 é o valor do id (identificador único) de uma Postagem que está sendo procurada. <br />No exemplo na Nuvem, java é a palavra que está sendo procurada no campo (Atributo) descricao, de um Tema. |

| <img src="https://i.imgur.com/hOgWvSc.png" title="source: imgur.com" width="150px"/> | <div align="left"> **ATENÇÃO:** *Na Requisição http, no item Path, não é enviado o endereço completo (URL). É enviado apenas o Recurso e os Parâmetros da URL.* </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

| <img src="https://i.imgur.com/hOgWvSc.png" title="source: imgur.com" width="250px"/> | <div align="left"> **IMPORTANTE:** *Os conceitos apresentados na formação da URL, em especial Recurso e Parâmetros serão estudados com mais detalhes no decorrer do Bloco 02. O mais importante neste momento é compreender quais são as partes que compõem a URL.* </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

<h3>4.4. Response</h3>

A Response (resposta) é a resposta que o servidor envia ao cliente depois de processar a Requisição. Essa resposta pode conter os dados que realmente o cliente esperava receber ou uma resposta informando que alguma coisa deu errado.

<div align="center"><img src="https://i.imgur.com/SkGiIId.png" title="source: imgur.com" />
<br /><i>Response HTTP</i></div>

O protocolo HTTP também define um conjunto de **Códigos de Status de respostas** responsáveis por indicar se a ação executada para um dado recurso foi executada corretamente ou não. Estes Métodos são comumente referenciados como **HTTP  Status Code**.
As respostas são agrupadas em cinco Classes:

1.  Respostas de informação (`100`-`199`),
2.  Respostas de sucesso (`200`-`299`),
3.  Redirecionamentos (`300`-`399`)
4.  Erros do cliente (`400`-`499`)
5.  Erros do servidor (`500`-`599`).

<h4>4.4.1. Principais HTTP Status Code</h4>

<img width="25px" src="https://i.imgur.com/WqsuztO.png" title="source: imgur.com" /><b> Respostas de Sucesso</b>

<table width=100%>
	<tr>
		<td width=15%><b>Código
		<td width=15%><b>Resposta	
		<td width=70%><b>Descrição
	</tr>
	<tr>
		<td align="center"><b>200
		<td align="center"><i>OK
		<td>Estas requisição foi bem sucedida. O significado do sucesso varia de acordo com o Método HTTP.
	</tr>
	<tr>
		<td align="center"><b>201
		<td align="center"><i>CREATED
		<td>A requisição foi bem sucedida e um novo recurso foi criado como resultado. Esta é uma típica resposta enviada após uma requisição POST.
	</tr>
	<tr>
		<td align="center"><b>204
		<td align="center"><i>NO CONTENT
		<td>Não há conteúdo para enviar para esta solicitação, mas os cabeçalhos podem ser úteis. O user-agent pode atualizar seus cabeçalhos em cache para este recurso com os novos. Essa resposta é muito comum após uma Requisição DELETE.
	</tr>
</table>

<img width="25px" src="https://i.imgur.com/NqT8xrC.png" title="source: imgur.com" /><b> Respostas de Erro do Cliente</b>

<table width=100%>
	<tr>
		<td width=15%><b>Código
		<td width=15%><b>Resposta	
		<td width=70%><b>Descrição
	</tr>
	<tr>
		<td align="center"><b>400
		<td align="center"><i>BAD REQUEST
		<td>Essa resposta significa que o servidor não entendeu a requisição pois está com uma sintaxe inválida.
	</tr>
	<tr>
		<td align="center"><b>401
		<td align="center"><i>UNAUTHORIZED
		<td>Embora o padrão HTTP especifique "unauthorized", semanticamente, essa resposta significa "unauthenticated". Ou seja, o cliente deve se autenticar para obter a resposta solicitada. Esta resposta é muito comum quando habilitamos a Segurança na API (Login, Senha e Token).
	</tr>
	<tr>
		<td align="center"><b>403
		<td align="center"><i>FORBIDDEN
		<td>O cliente não tem direitos de acesso ao conteúdo portanto o servidor está rejeitando dar a resposta. Diferente do código 401, aqui a identidade do cliente é conhecida.
	</tr>
	<tr>
		<td align="center"><b>404
		<td align="center"><i>NOT FOUND
		<td>O servidor não pode encontrar o recurso solicitado. Este código de resposta acontece com frequência na web.
	</tr>
	<tr>
		<td align="center"><b>405
		<td align="center"><i>METHOD NOT ALLOWED
		<td>O servidor não pode encontrar o Método solicitado. 
	</tr>
</table>

<img width="25px" src="https://i.imgur.com/p5sO5z7.png" title="source: imgur.com" /><b> Respostas de Erro do Servidor</b>

<table width=100%>
	<tr>
		<td width=10%><b>Código
		<td width=25%><b>Resposta	
		<td width=65%><b>Descrição
	</tr>
	<tr>
		<td align="center"><b>500
		<td align="center"><i>INTERNAL SERVER ERROR
		<td>O servidor encontrou uma situação com a qual não sabe lidar.
	</tr>
	<tr>
		<td align="center"><b>501
		<td align="center"><i>NOT IMPLEMETED
		<td>O Método da requisição não é suportado pelo servidor e não pode ser manipulado.
	</tr>
	<tr>
		<td align="center"><b>502
		<td align="center"><i>BAD GATEWAY
		<td>O servidor, ao trabalhar como um gateway a fim de obter uma resposta necessária para manipular a requisição, obteve uma resposta inválida.
	</tr>
	<tr>
		<td align="center"><b>503
		<td align="center"><i>SERVICE UNAVAILABLE
		<td>O servidor não está pronto para a requisição. Causas comuns são um servidor em manutenção ou sobrecarregado.
	</tr>
</table>

<br />

<div align="left"><img src="https://i.imgur.com/cDPH4tl.png" title="source: imgur.com" width="30px"/> <a href="https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status" target="_blank"><b>Documentação: HTTP Status Code</b></a></div>

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
