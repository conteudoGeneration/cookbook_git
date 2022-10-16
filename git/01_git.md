<h1>Versionamento de código com o Git</h1>



O controle de versão, também conhecido como versionamento de código, é a prática de rastrear e gerenciar as alterações em um código de software. **É uma forma de administrar as mudanças que são feitas no código fonte do projeto e garantir mais segurança na transição de uma versão para a outra**. 

<h2>Sistemas de Controle de Versão - VCS</h2>

Os **Sistemas de Controle de Versão (Version Control System - VCS)** são ferramentas de software que ajudam as equipes de pessoas desenvolvedoras a gerenciar as alterações no código-fonte ao longo do tempo, criando um histórico da evolução do projeto. Como os ambientes de desenvolvimento são muito dinâmicos, os sistemas de controle de versão ajudam as equipes a trabalharem de forma rápida e inteligente. Atualmente, a grande maioria das empresas trabalham dentro da cultura **DevOps**, e neste contexto, os Sistemas de Controle de Versão auxiliam a reduzir o tempo de desenvolvimento e aumentar as implementações bem-sucedidas.

> **DevOps** é um composto de **Dev** (desenvolvimento) e **Ops** (operações), que na prática é a  união de pessoas, processos e tecnologias para fornecer continuamente  valor aos clientes.
>
> Equipes que adotam a cultura, as práticas e as ferramentas de DevOps  apresentam alto desempenho, criando produtos melhores, com mais rapidez, para maior satisfação do cliente.

O software de controle de versão mantém o registro de todas as modificações efetuadas no código em um tipo especial de banco de dados. Se um erro for cometido, as pessoas desenvolvedoras podem **voltar no tempo** e **comparar versões anteriores do código para ajudar a corrigir o erro**, sem a necessidade de interromper o trabalhos dos demais colaboradores da equipe.

Antes dos sistemas de controle de versão, o processo de versionamento era manual e cada pessoa desenvolvedora tinha a sua forma de fazer, ou seja, não havia um padrão formal. A maioria utilizava a prática de fazer uma cópia da pasta do projeto e renomear a pasta acrescentando o  numero da versão, como mostra a imagem abaixo:

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

O grande problema desta estratégia é que a pessoa desenvolvedora e o seu time não mantinham um histórico sobre até que ponto do desenvolvimento do projeto cada pasta contemplava, além de ter que lidar com um grande numero de pastas e arquivos repetidos. A única forma de saber o conteúdo de cada uma era abrindo uma por uma, até encontrar o que se procurava. Um processo lento, desgastante e que muitas vezes gerava mais retrabalho, principalmente quando uma das pastas eram alteradas ou apagadas acidentalmente. O controle de versão protege o código-fonte contra catástrofes e erro humano.

Outro ponto importante é que as pessoas desenvolvedoras atualmente trabalham em equipes e estão sempre  escrevendo novas versões do código-fonte e modificando o código-fonte existente. Uma pessoa desenvolvedora pode estar trabalhando em um novo recurso, enquanto outra pessoa desenvolvedora corrige um bug não relacionado, e desta forma cada pessoa desenvolvedora pode fazer alterações em várias partes e em vários arquivos do projeto, inclusive alterações simultâneas em um mesmo arquivo.

O controle de versão ajuda as equipes a solucionarem esses tipos de  problemas, rastreando cada alteração individual feita por cada  pessoa desenvolvedora, ajudando a evitar conflitos com trabalhos simultâneos. O software de controle de versão é uma parte essencial no dia a dia das  práticas profissionais para qualquer equipe de pessoas desenvolvedoras nos dias de hoje. 

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

Observe que cada versão do código (commit) é um marco no processo de desenvolvimento, ou seja, um commit adiciona as alterações mais recentes do código-fonte no repositório, tornando essas alterações parte da revisão principal do  repositório. Cada bolinha na imagem acima, representa uma versão consolidada do sistema, que já foi testada e validada.

É importante ressaltar que os commits nos sistemas de controle de versão são mantidos no repositório **indefinidamente**. Assim, quando outros usuários fizerem uma atualização ou check-out no repositório, eles receberão a última versão da aplicação. Os sistemas de controle de versão permitem reverter facilmente para versões anteriores. Nesse contexto, **um commit dentro de um sistema de controle de versão é protegido**, pois é facilmente revertido, mesmo após o commit ter sido aplicado.

<h3>Benefícios do Sistema de Controle de Versão</h3>



1. **Um histórico de alterações completo e a longo prazo de  todos os arquivos.** Esse histórico mantém as alterações realizadas no código e também inclui o autor, a data e as notas escritas sobre o objetivo de cada  alteração. Ter o histórico completo permite voltar às versões anteriores para ajudar na análise da causa raiz de bugs e é crucial para corrigir  problemas nas versões mais antigas do software. Se o software estiver  sempre sendo trabalhado, quase tudo poderá ser considerado uma "versão  mais antiga" do software.
2. **Ramificação e mescla**. O  trabalho simultâneo da equipe é certo, mas mesmo os indivíduos que  trabalham sozinhos podem se beneficiar da capacidade de trabalhar em  fluxos independentes de mudanças. Criar uma "ramificação" nas  ferramentas do VCS mantém vários fluxos de trabalho independentes uns  dos outros, além de oferecer a facilidade de mesclar esse trabalho de  novo, permitindo que os desenvolvedores verifiquem se as alterações em  cada ramificação não estão em conflito. 
3. **Rastreabilidade**. Ser capaz de rastrear cada alteração feita no software e conectar ao software de  gestão de projetos e rastreamento de bugs, além de ser capaz de anotar cada alteração com uma mensagem descrevendo o  objetivo da mudança.



https://azure.microsoft.com/pt-br/resources/cloud-computing-dictionary/what-is-devops/#devops-overview



<h2>O que é o Git?</h2>



O **Git** é o Sistema de Controle de Versões mais popular e utilizado no mundo do Desenvolvimento, que possui a capacidade de documentar e armazenar todas as alterações que são feitas no código durante o processo de desenvolvimento e atualização do projeto.

O Git é um projeto de código aberto, maduro e com manutenção ativa e constante, que foi desenvolvido em 2005 por Linus Torvalds, o famoso criador do kernel do  sistema operacional Linux. Um número impressionante de projetos de  software depende do Git para controle de versão, incluindo projetos  comerciais e de código-fonte aberto. 

Tendo uma arquitetura distribuída, o Git é um exemplo de DVCS  (portanto, Sistema de Controle de Versão Distribuído). Em vez de ter  apenas um único local para o histórico completo da versão do software,  como é comum em sistemas de controle de versão outrora populares como CVS ou Subversion, no Git, a cópia de  trabalho de todo desenvolvedor do código também é um repositório que  pode conter o histórico completo de todas as alterações.

<h3>Fluxo de trabalho de ramificação de recurso</h3>

Uma das maiores vantagens do Git são seus recursos de **branch (ramificação)**. Ao  contrário dos sistemas de controle de versão centralizados, os branches  do Git são simples e o merge (fusão) entre branches é fácil. Essas características facilitam o fluxo de trabalho e é um dos principais motivos da popularidade do Git.

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

Os branches de recursos oferecem um ambiente isolado para cada  alteração na base de código. Quando um desenvolvedor quer começar a  trabalhar em algo, não importa o tamanho da empreitada, ele cria um novo branch. Assim, é garantido que o branch principal sempre contenha  código de qualidade de produção.

Uma branch de recurso é como se fosse um universo paralelo, que caminha de forma independente, sem interferir no ramo principal, a branch main. O merge, seria um commit onde a branch de recurso passa a fazer parte da branch principal, criando uma fusão entre as duas, como vemos na imagem abaixo:

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

Observe que...

<h3>Desenvolvimento distribuído</h3>

No Sistemas de  controle de versão centralizados, cada desenvolvedor recebe uma cópia de trabalho que aponta  para um único repositório central. O Git, por sua vez, é um sistema de  controle de versão distribuído. Em vez de uma cópia de trabalho, cada  desenvolvedor obtém seu próprio repositório local, com um histórico  completo de commits.

![Desenvolvimento distribuído](https://wac-cdn.atlassian.com/dam/jcr:9d51f0ee-5946-4be2-886c-ff040ef8c1a1/03.svg?cdnVersion=582)

Ter um histórico local completo torna o Git rápido, já que você não  precisa de uma conexão de rede para criar commits, inspecionar versões  anteriores de um arquivo entre commits.

O desenvolvimento distribuído também facilita a escalabilidade da  equipe de engenharia. Se alguém quebrar o branch de produção no sistema centralizado,  ninguém consegue inserir suas alterações até a  correção. Com o Git, esse tipo de bloqueio não existe. Todos podem  continuar trabalhando em seus próprios repositórios locais e depois enviar as alterações para o repositório remoto.

E, semelhante aos branches de recursos, o desenvolvimento distribuído cria um ambiente mais confiável. Mesmo que um desenvolvedor destrua seu repositório local, ele pode simplesmente clonar (copiar) o de outra pessoa e  começar de novo.

<h3>Solicitações pull</h3>

Muitas ferramentas de gerenciamento de código-fonte, aprimoram a funcionalidade principal do Git com pull requests. Uma pull request é uma forma de pedir a outro desenvolvedor para fazer o merge  de um dos seus branches no repositório dele. Esse recurso não só  facilita o acompanhamento das alterações para os líderes de projeto, mas também permite que os desenvolvedores iniciem discussões sobre seu  trabalho antes de integrá-lo com o resto da base de código.

![Solicitações pull](https://wac-cdn.atlassian.com/dam/jcr:ada8f4c4-22b1-486c-872b-df83484e288b/02%20Pull%20Requests.svg?cdnVersion=582)

Como são essencialmente um tópico de comentários anexado a um branch  de recurso, as pull requests são extremamente versáteis. Quando um  desenvolvedor fica preso a um problema difícil, ele pode abrir uma pull  request para pedir ajuda ao resto da equipe. 

Site Git --> https://git-scm.com



<h2>O que é o Github?</h2>


O GitHub é um serviço baseado em nuvem que hospeda um sistema de  controle de versão distribuído (DVCS) chamado Git. Ele permite que os desenvolvedores colaborem e façam mudanças em projetos compartilhados enquanto mantêm  um registro detalhado do seu progresso. O Github é uma espécie de rede social de projetos e código fonte, que permite hospedar e compartilhar os seus projetos.

Além do Github, existem outras alternativas como o GitLab, o Bitbucket e o Subversion:

<div align="center"><img src="mudar" title="source: imgur.com" width="60%"/></div>

O GitHub é uma excelente ferramenta para o trabalho em equipe,  porque a plataforma online facilita a gestão do  projeto. Essa ferramenta também está disponível para empresas: é conhecida  como GitHub Enterprise. Nela você encontra uma forma inteligente de  gerenciar o trabalho de uma equipe.

Além disso, a segurança é levada muito a sério, algo fundamental  quando se trata de projetos digitais. Porém, o que chama realmente a  atenção é o fato da equipe poder trabalhar ao mesmo tempo, de diversos lugares do mundo. Hoje em dia, para qualquer negócio, a automatização dos fluxos de  trabalho é fundamental e o GitHub faz isso possível. Os recursos  encontrados na plataforma auxiliam no desenvolvimento dos projetos,  facilitando o crescimento da empresa como um todo.

Site Git Hub --> https://github.com

<h3>Portfólio no Github</h3>


Uma das formas de mostrar o seu trabalho para outras pessoas, em  especial, empresas, é pelo seu portfólio. Pelo Github, você pode montar o seu portfólio com projetos que demonstrem as suas habilidades com  código. 

**Não há nada melhor do que provar suas habilidades através do código**. É como diria Linus Torvalds, criador do Linux: *“falar é fácil, me mostre o código”.*

