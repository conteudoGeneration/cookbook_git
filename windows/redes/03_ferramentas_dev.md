<h1>Ferramentas de Desenvolvimento</h1>

Todo navegador web moderno inclui um poderoso conjunto de ferramentas  para desenvolvedores. Essas ferramentas fazem muitas coisas, desde  inspecionar o HTML, CSS e JavaScript recém carregado e quais recursos  foram requeridos até mostrar quanto tempo a página precisou para  carregar. Este artigo explica como usar as funções básicas  das ferramentas para desenvolvedores do seu navegador.

As Ferramentas de Desenvolvimento são muito utilizadas no Desenvolvimento do Frontend, pois permitem visualizar se os dados que o Frontend está enviando para o Backend estão corretos e checar o funcionamento de códigos Javascript/Typescript.

Neste tutorial, iremos utilizar as Ferramentas de Desenvolvimento para visualizarmos as **Requisições HTTP (Request)**, que são realizadas pelo Navegador da Internet ao abrir um site e as suas respectivas **Respostas (Response)**.

<div align="left"><img src="https://i.imgur.com/cDPH4tl.png" title="source: imgur.com" width="30px"/> <a href="https://developer.mozilla.org/pt-BR/docs/Learn/Common_questions/What_are_browser_developer_tools" target="_blank"><b>Documentação: Ferramentas de Desenvolvimento do Navegador</b></a></div>



<h2>Utilizando as Ferramentas de Desenvolvimento</h2>



Neste tutorial utilizaremos o Firefox, entretanto a forma de acessar é semelhante para os Navegadores  **Google Chrome** e  **Microsoft Edge**. 

1. Abra o seu Navegador favorito

<div align="center"><img src="https://i.imgur.com/5rlBjgf.png" title="source: imgur.com" width="90%"/></div>

2. Para abrir as Ferramentas do Desenvolvedor, pressione a Tecla **F12** do seu teclado (Firefox e Edge), ou a combinação de teclas **CTRL + SHIFT + I** (Chrome).

3. Clique na **Guia Rede (Network)** para Visualizar as Requisições HTTP.

<div align="center"><img src="https://i.imgur.com/oP1S25j.png" title="source: imgur.com" /></div>

4.  Abra o site do **Google**: **https://www.google.com**

<div align="center"><img src="https://i.imgur.com/nzxH422.png" title="source: imgur.com" /></div>

5.  Observe que na **Guia Rede** serão exibidas todas as Requisições realizadas pelo site.

<div align="center"><img src="https://i.imgur.com/FWPZ5HH.png" title="source: imgur.com" /></div>

6.  Clique sobre a primeira requisição da lista, como mostra a figura abaixo:

<div align="center"><img src="https://i.imgur.com/eJNGNCU.png" title="source: imgur.com" /></div>

7.  Observe que será aberto um painel do lado direito da lista. Clique na **Guia Cabeçalhos**. 

   <div align="center"><img src="https://i.imgur.com/yqyBXnK.png" title="source: imgur.com" /></div>

8.  Observe na imagem acima que é possível identificar o **Verbo (GET)**, o **Host (www.google.com)**, o **Caminho (/)**, o **Endereço IP com a porta (142.251.132.36:443)**, o **HTTP Status Code** da Resposta (**200 🡪 OK** ) e a **Versão do Protocolo HTTP (2.0)**.

9.  Experimente acessar outros sites e veja as requisições HTTP que são geradas por eles.

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
