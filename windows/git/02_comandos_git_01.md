<h1>Comandos do Git - Parte 01</h1>

<br />

<h2>1.Criando o seu primeiro Repositório local</h2>



1. Vamos checar qual é a sua pasta atual. Digite o comando:

```bash
pwd
```

*Verifique se você está na pasta do seu usuário (Home Directory).* 

2. Caso não esteja na pasta do seu usuário, digite o comando:

```bash
cd ~
```

3. Vamos criar o nosso primeiro Repositório na pasta do usuário. Vamos criar a pasta **aulagit**, através do comando:

```bash
mkdir aula_git
```

4. Na sequência vamos acessar esta pasta através do comando:

```bash
cd aula_git
```

5. Dentro da pasta **aulagit**, vamos criar o nosso **Repositório Git Local**, através do comando:

```bash
git init
```

6. Para verificar se o Repositório foi criado, utilize o comando:

```bash
git status
```

O comando **git status** mostra se a pasta atual é um Repositório e qual é o status atual (vazio, possui arquivos aguardando para serem versionados, entre outros).

7. Observe na imagem abaixo, que o Repositório foi criado, não existe nenhum commit e não existe nenhuma pasta ou arquivo para ser "commitada" 

<div align="center"><img src="https://i.imgur.com/ZI8l3R8.png" title="source: imgur.com" width="90%"/></div>

8. Uma outra forma de verificar se o Repositório foi criado é através do comando:

```bash
ls -a
```

*Observe que dentro da pasta aula git, foi criada uma pasta oculta com chamada **.git***

O comando **git init** criou a pasta `.git` (oculta), contendo as subpastas `objects`, `refs/heads`, `refs/tags` e alguns arquivos modelo.  Também foi criado um arquivo inicial chamado `HEAD`, que guarda a referencia `HEAD` da branch principal. o Head funciona como um ponteiro, indicando qual é a branch atual. 

9. Para descobrir qual é a sua branch atual, utilize o  comando:

```bash
git branch --show-current
```

O comando acima exibirá que no momento, o **HEAD** do Repositório está apontando para a Branch **main**, ou seja, a Branch atual do Repositório.

<br />

> [!IMPORTANT]
>
> O arquivo **HEAD** é um arquivo interno do Git, portanto, não deve ser manipulado manualmente.

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-init/pt_BR" target="_blank"><b>Documentação: <i>Git Init</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-status/pt_BR" target="_blank"><b>Documentação: <i>Git Status</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-branch/pt_BR" target="_blank"><b>Documentação: <i>Git Branch</i></b></a></div>


<br />

<h2>2.Versionando os arquivos no Repositório local</h2>



1. Antes começarmos a versionar os nossos arquivos, precisamos criar alguns arquivos dentro do nosso Repositório Local, através do Visual Studio Code, digitando o comando:

```bash
code .
```

2. A pasta **aulagit** será aberta no **Visual Studio Code**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/z6LMMQn.png" title="source: imgur.com" width="90%"/></div>

3. No Visual Studio Code, crie os 3 arquivos indicados abaixo e adicione as seguintes frases em cada arquivo:

- **portugol.txt:** Portugol é uma pseudo linguagem.
- **java.txt:** Java é uma Linguagem de programação.
- **mysql.txt:** MySQL é um Sistema Gerenciador de Banco de dados.

4. Na sequência, vamos adicionar os arquivos no índice do Repositório Local (Staging), através do comando:

```bash
git add .
```

O comando **git add** atualiza o índice do Repositório Local com o conteúdo atual encontrado na árvore de trabalho para preparar o conteúdo para o próximo commit. O **ponto** após o comando git add, indica que será adicionado todo o conteúdo atual, incluindo os arquivos e pastas.

O conteúdo adicionado é enviado para o **Staging**, que é um espaço temporário onde você determina quais mudanças serão adicionadas ao Repositório Local. Utilizar o staging é muito simples com o comando **git add** você adiciona os arquivos para o staging, e quando estiver satisfeito com as alterações efetua um commit, que veremos na sequência.

<br />

> [!TIP]
>
> O git **não versiona pastas vazias**. Para versionar uma pasta é necessário adicionar arquivos dentro dela.

<br />

5. Para verificar as alterações no Repositório Local, utilize o comando:

```bash
git status
```

6. O comando **git status** retornará que existem arquivos aguardando para serem "commitados" no índice do Repositório Local, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/WpqHlSQ.png" title="source: imgur.com" /></div>

7. Para "commitar" os arquivos, utilize o comando:

```bash
git commit -m "Meu primeiro commit"
```

O comando **git commit** cria um novo commit com todos os conteúdos atuais do índice e a mensagem informada entre aspas no registro log descrevendo todas as alterações que foram realizadas. Um novo commit é um herdeiro direto do `HEAD` que em geral é o topo do branch atual e o branch é atualizado para apontar para este novo commit.

> Os **commits** são as principais unidades de bloco de construção de uma linha do tempo do projeto Git. Os commits podem ser considerados instantâneos ou marcos ao longo da linha do tempo de um projeto Git. Os commits são criados com o comando **git commit** para capturar o estado de um projeto naquele momento.

8. Após executar o comando, será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/F5lijPS.png" title="source: imgur.com" /></div>

9. Para verificar se os arquivos e pastas foram "commitados", utilize o comando:

```bash
git status
```

10. O comando **git status** retornará que não existem arquivos aguardando para serem "commitados", como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/BOIgZ5Y.png" title="source: imgur.com" /></div>

11. Para visualizar as informações do histórico de commits, utilize o comando:

```bash
git log
```

Para sair da listagem do comando **git log**, caso seja necessário, pressione a letra **q** do seu teclado.

12. Observe na imagem abaixo, que serão exibidos todos os detalhes do commit:

<div align="left"><img src="https://i.imgur.com/IxI238Z.png" title="source: imgur.com" /></div>

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-add/pt_BR" target="_blank"><b>Documentação: <i>Git Add</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-status/pt_BR" target="_blank"><b>Documentação: <i>Git Status</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-commit/pt_BR" target="_blank"><b>Documentação: <i>Git Commit</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-log/pt_BR" target="_blank"><b>Documentação: <i>Git log</i></b></a></div>


<br />

<h2>3.Entendendo o fluxo de trabalho do Git</h2>



Os seus repositórios locais consistem em três "árvores" mantidas pelo git:

- A primeira é o seu **Working Directory** (pasta de trabalho), ou seja, a pasta onde você criou o seu Repositório Local e estão armazenados todos os arquivos do Repositório Local (independente de estarem commitados). No nosso exemplo é a pasta **aulagit**, que foi criada na pasta do seu usuário (home directory) e inicializada como um Repositório Local git.
- A segunda é a **Index** (índice) ou Staging Area, que funciona como uma área temporária onde ficam armazenados os arquivos que foram criados, atualizados ou apagados, desde o ultimo commit. As alterações no Stage são simplesmente alterações no **working Directory**, em que se pretende “avisar” ao Repositório Local sobre essas alterações que foram realizadas. 
- A terceira é a **HEAD**, que funciona como uma espécie de ponteiro, possui a função de apontar para o último *commit* (confirmação) que você fez.        

<div align="left"><img src="https://i.imgur.com/GKHWuOW.png" title="source: imgur.com" /></div>

A **HEAD** aponta para o **último commit**, que foi realizado no Repositório Local, logo quando você executa o comando **git commit você está dizendo para a HEAD que este novo commit é o mais atual e será a nova HEAD** do seu Repositório Local.

Vamos entender o fluxo na prática! 

1. Crie mais 2 arquivos dentro do nosso Repositório Local, através do **Visual Studio Code** e adicione as seguintes frases em cada arquivo:

- **spring.txt:** Spring é um framework.
- **docker.txt:** Docker é um gerenciador de containers.

2. Para verificar as alterações no Repositório Local, utilize o comando:

```bash
git status
```

3. O comando **git status** retornará que existem arquivos que não foram adicionados no índice do Repositório Local, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/JIpTtvE.png" title="source: imgur.com" /></div>

4. Na sequência, vamos adicionar os arquivos no índice do Repositório Local, através do comando:

```bash
git add .
```

5. Para verificar as alterações no Repositório Local, utilize o comando:

```bash
git status
```

6. O comando **git status** retornará que existem arquivos aguardando para serem "commitados" no índice do Repositório Local, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/kAbUDmf.png" title="source: imgur.com" /></div>

7. Para "commitar" os arquivos, utilize o comando:

```bash
git commit -m "Meu segundo commit"
```

8. Para verificar as alterações no Repositório Local, utilize o comando:

```bash
git status
```

9. O comando **git status** retornará que não existem arquivos aguardando para serem "commitados", como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/BOIgZ5Y.png" title="source: imgur.com" /></div>

10. Para visualizar as informações do histórico de commits, utilize o comando:

```bash
git log
```

11. Observe na imagem abaixo, que serão exibidos todos os detalhes do commit:

<div align="left"><img src="https://i.imgur.com/esS7wBR.png" title="source: imgur.com" /></div>

*Observe que o **HEAD** do Repositório Local passou a ser o **"Meu segundo commit"**.*

<br />

<h2>4.Atualizar o conteúdo de um arquivo</h2>



1. Volte para **Visual Studio Code**, abra o arquivo **spring.txt** e atualize o seu conteúdo:

- **spring.txt:** Spring é um framework Java.

2. Para checar as mudanças que aconteceram no arquivo **spring.txt**, utilize o comando:

```bash
git diff
```

3. O comando **git diff** retornará que o arquivo **spring.txt** foi modificado e indica quais foram as alterações, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/bw6Sewy.png" title="source: imgur.com" /></div>

4. Para verificar as alterações no Repositório Local, utilize o comando:

```bash
git status
```

5. O comando **git status** retornará que o arquivo **spring.txt** foi atualizado e ainda não foi adicionado no índice do Repositório Local, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/xETINlK.png" title="source: imgur.com" /></div>

6. Na sequência, vamos adicionar **apenas o arquivo spring.txt** no índice do Repositório Local, através do comando:

```bash
git add spring.txt
```

7. Para verificar as alterações no Repositório Local, utilize o comando:

```bash
git status
```

8. O comando **git status** retornará que o arquivo **spring.txt** está aguardando para ser "commitado" no índice do Repositório Local, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/XC8uxsD.png" title="source: imgur.com" /></div>

9. Para "commitar" o arquivo **spring.txt**, utilize o comando:

```bash
git commit -m "Meu terceiro commit"
```

10. Para verificar as alterações no Repositório Local, utilize o comando:

```bash
git status
```

11. O comando **git status** retornará que não existem arquivos aguardando para serem "commitados", como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/BOIgZ5Y.png" title="source: imgur.com" /></div>

12. Para visualizar o histórico de commits, utilize o comando:

```bash
git log
```

13. Observe na imagem abaixo, que serão exibidos todos os detalhes do commit:

<div align="left"><img src="https://i.imgur.com/RtYyCxQ.png" title="source: imgur.com" /></div>

14. Observe que o **HEAD** do Repositório Local passou a ser o **"Meu terceiro commit"**.

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-diff/pt_BR" target="_blank"><b>Documentação: <i>Git Diff</i></b></a></div>


<br />

<h2>5.Desfazendo um commit</h2>



Existem 2 comandos no Git para desfazer um Commit:

- O **git reset**, que desfaz commit, alterando o histórico do Repositório. Em outras palavras, além de desfazer o commit, ele também remove a existência dele do histórico do Repositório. Ao utilizar este comando, deve-se tomar cuidado porque você vai modificar todo o histórico de commits, por isso o seu uso não é recomendado em branches compartilhadas com outros usuários.
- O **git revert**, que desfaz as alterações de um commit e assim que ele for desfeito, o comando criará um novo commit, com os dados revertidos, ou seja, ele não modifica o histórico de nenhum dos commits anteriores. Ao utilizar este comando, recomenda-se indicar o commit que será revertido através do SHA (Código de identificação do commit).

1. Vamos desfazer o commit **Meu terceiro commit**, através do comando **git reset**:

```bash
git reset HEAD~1
```

2. Para checar o status do Repositório Local, utilize o comando:

```bash
git status
```

3. O comando **git status** retornará que o arquivo **spring.txt** voltou a ficar disponível para ser adicionado, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/xETINlK.png" title="source: imgur.com" /></div>

4. Para visualizar o histórico dos commits, utilize o comando:

```bash
git log
```

5. Observe na imagem abaixo, que o **HEAD** do Repositório Local passou a ser o **"Meu segundo commit"**, após o **Meu terceiro commit** ser desfeito:

<div align="left"><img src="https://i.imgur.com/esS7wBR.png" title="source: imgur.com" /></div>

*O comando **git reset HEAD~1** redefiniu o `HEAD` atual para um commit anterior (~1) ao commit atual, desfazendo o commit atual.*

<br />

> [!TIP]
>
> Para desfazer o commit e apagar todos os arquivos e pastas que foram commitados, utilize o comando **git reset HEAD~1 -- hard**.

<br />

6. Vamos refazer o commit **Meu terceiro commit**, através do comando:

```bash
git commit -a -m "Meu terceiro commit"
```

*A opção **-a** é o equivalente a fazer o **git add** . junto com o comando **git commit**.*

<br />

> [!TIP]
>
> A opção **-a** funciona apenas se for um commit de atualização do arquivo. Para arquivos novos é necessário usar os comandos git add e na sequência o git commit.

<br />

7. Vamos desfazer o commit **Meu terceiro commit** novamente, só que desta vez através do comando **git revert**:

```bash
git revert 1866
```

8. O código **1866** são os 4 primeiros caracteres do **SHA** do commit que será revertido, como vemos na imagem abaixo:

<div align="left"><img src="https://i.imgur.com/zs7XYaE.png" title="source: imgur.com" /></div>

9. Em seguida o **Git** abrirá o Visual Studio Code (Editor que foi selecionado como padrão do Git), para editar a mensagem do **commit** de reversão.
10. Feche o arquivo que contém a mensagem no **Visual Studio Code** e volte par o Terminal.
11. Será exibida uma mensagem semelhante a imagem abaixo, confirmando a reversão do commit:

<div align="left"><img src="https://i.imgur.com/ntpTuRp.png" title="source: imgur.com" width="60%"/></div>

12. Para checar o status do Repositório Local, utilize o comando:

```bash
git status
```

13. O comando **git status** retornará que não existem arquivos aguardando para serem "commitados", como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/BOIgZ5Y.png" title="source: imgur.com" /></div>

<br />

> [!IMPORTANT]
>
> Diferente do **git reset**, o **git revert** desfaz todas as alterações do commit desfeito. Por este motivo, que o comando git status informa que não existem novos arquivos ou arquivos modificados para serem "commitados".

<br />

14. Para visualizar o histórico dos commits, utilize o comando:

```bash
git log
```

15. Observe na imagem abaixo, que o **HEAD** do Repositório Local passou a ser o **Revert Meu terceiro commit**, ou seja, o commit criado pelo comando **git revert**, que indica que o commit **Meu terceiro commit** foi desfeito:

<div align="left"><img src="https://i.imgur.com/zRolqwV.png" title="source: imgur.com" /></div>

<br/>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-reset/pt_BR" target="_blank"><b>Documentação: <i>Git Reset</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-revert/pt_BR" target="_blank"><b>Documentação: <i>Git Revert</i></b></a></div>

<br />

<h2>6.Publicando o Repositório Local no Github</h2>



<h3>6.1.Criar o Repositório Remoto no Github</h3>




Vamos criar o Repositório no Github:

1. Acesse a sua conta do Github

2. Na Barra de Navegação superior da Conta do Github, clique no botão **+** e no menu que será aberto, clique na opção **New repository**.

<div align="center"><img src="https://i.imgur.com/JBoiJv1.png" title="source: imgur.com" /></div>

3. Crie um **Repositório Público**, chamado **aulagit**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/8qxr1c4.png" title="source: imgur.com" /></div>

4. Em seguida clique no botão **Create Repository** no final da tela.
4. Será aberta uma tela semelhante a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/BnhGA2n.png" title="source: imgur.com" /></div>

6. Copie o endereço do Repositório indicado pela seta amarela. Observe que foi copiado o endereço **HTTPS**.

<br />

<h3>6.2.Conectar o Repositório Local com o Repositório Remoto</h3>



1. Crie a conexão do Repositório Local com o Repositório Remoto, através do comando:

```bash
git remote add origin https://github.com/rafaelq80/aulagit.git
```

*Observe que depois da palavra origin foi inserido o **endereço HTTPS do Repositório Remoto** que foi copiado do Github.*

<br />

> [!TIP]
>
> Para colar um conteúdo no Terminal do Windows, utilize o botão direito do mouse ou a combinação de teclas `SHIFT + INSERT` do seu teclado.

<br />

2. Para confirmar se o Repositório Local está conectado com o Repositório Remoto, utilize o comando:

```bash
git remote -v
```

3. Observe na imagem abaixo, que será exibido o endereço do Repositório Remoto, confirmando a conexão:

<div align="left"><img src="https://i.imgur.com/rURPm9E.png" title="source: imgur.com" /></div>

<br />

<h3>6.3.Enviar o conteúdo do Repositório Local para o Github</h3>



1. Envie o conteúdo do Repositório Local para o Repositório Remoto, através do comando:

```bash
git push origin main
```

Observe que no comando **git push** foram adicionados 2 parâmetros:

- **origin:** O Repositório Remoto;
- **main:** A Branch do Repositório Local, que será enviada para o Repositório Remoto.

2. Volte para o Github e verifique se os arquivos estão disponíveis no Repositório Remoto, no Github, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/5ou5Nhd.png" title="source: imgur.com" /></div>

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-remote/pt_BR" target="_blank"><b>Documentação: <i>Git Remote</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-push/pt_BR" target="_blank"><b>Documentação: <i>Git Push</i></b></a></div>


<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
