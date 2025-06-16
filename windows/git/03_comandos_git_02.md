<h1>Comandos Git - Parte 02</h1>



<h2>1. Clonando um Repositório Remoto na sua máquina</h2>



Antes de clonarmos o Repositório Remoto, vamos apagar o nosso Repositório Local, para simularmos um acidente de percurso.

1. Feche o **Visual Studio Code**, caso esteja aberto
1. Volte para a pasta do usuário, através do comando:

```bash
cd ~
```

3. Na sequência, vamos apagar a pasta **aulagit** através do comando:

```bash
rm -rf aulagit
```

Será questionado se você tem certeza que deseja excluir a pasta? Responda SIM (**s**).

4. Para confirmar que a pasta foi apagada, utilize o comando abaixo:

```bash
ls
```

5. Volte para o Repositório Remoto **aulagit** no Github e copie o endereço **HTTPS** do Repositório, como indicado na imagem abaixo:

<div align="center"><img src="https://i.imgur.com/VKmyqsN.png" title="source: imgur.com" /></div>

6. Para clonar o Repositório, utilize o comando abaixo:

```bash
git clone https://github.com/rafaelq80/aulagit.git
```

*Observe que o endereço do Repositório Remoto foi adicionado depois do comando **git clone**.*

7. Ao efetuar a clonagem (cópia do Repositório), será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/f2HWeaP.png" title="source: imgur.com" /></div>

8. Para confirmar que a clonagem foi bem sucedida, utilize o comando abaixo:

```bash
ls
```

*Observe que a pasta **aulagit** foi restaurada.*

9. Para acessar a pasta, utilize o comando:

```bash
cd aulagit
```

10. Para verificar se o Repositório clonado está conectado com o Repositório do Github, utilize o comando abaixo:

```bash
git remote -v
```

11. Ao executar o comando acima, será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/rURPm9E.png" title="source: imgur.com" /></div>

<br />

> O Comando **git clone** faz uma cópia exata do Repositório Remoto na sua máquina, incluindo o histórico e todas as branches.

<br />

> [!IMPORTANT]
>
> Caso você esteja o clonando um Repositório de uma conta do Github de terceiros e deseje enviar o Repositório clonado para um Repositório Remoto na sua conta pessoal do Github, será necessário conectar o Repositório clonado com o seu Repositório Remoto.

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="4%"/> <a href="https://git-scm.com/docs/git-clone/pt_BR" target="_blank"><b>Documentação: <i>Git Clone</i></b></a></div>

<br />

<h2>2. Recebendo as atualizações do Repositório Remoto no Repositório Local</h2>



Vamos fazer uma alteração no conteúdo do arquivo **docker.txt**, hospedado no Repositório Remoto do Github e na sequência vamos atualizar o Repositório Local:

1. Volte para o Repositório Remoto **aulagit** no Github, abra o arquivo **docker.txt** e clique no **ícone do lápis para editar o arquivo**, como mostra a imagem abaixo

<div align="left"><img src="https://i.imgur.com/2f7iCeA.png" title="source: imgur.com" /></div>

2. Adicione o texto indicado, como mostra imagem abaixo:

- **docker.txt:** Esta linha foi inserida na branch ramo1.

<div align="left"><img src="https://i.imgur.com/iJHslsO.png" title="source: imgur.com" /></div>

3. Faça o **commit das alterações** clicando no botão **Commit changes**, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/f2hjRGH.png" title="source: imgur.com" /></div>

4. Volte para o Terminal. 
5. Para atualizar o Repositório Local com as alterações efetuadas no Repositório Remoto, utilize o comando abaixo:

```bash
git fetch
```

6. Ao executar o comando acima, será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/wmd3A23.png" title="source: imgur.com" /></div>

7. Para confirmar se as atualizações foram efetuadas, utilize o comando abaixo:

```bash
git status
```

8. Observe que as atualizações foram adicionadas no Repositório, mas não foram aplicadas no Repositório Local, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/XCdixZF.png" title="source: imgur.com" /></div>

<br/>

> O comando **git fetch** é que chamamos de opção de atualização segura. O comando `git fetch` baixa os dados do repositório remoto, como branches e histórico de commits, mas **não os mescla automaticamente** com sua branch atual. Isso permite revisar as mudanças antes de aplicá-las com um `merge` ou `rebase`.
>
> Para atualizar o conteúdo e alterar o estado do Repositório Local de forma imediata, utilizaremos o comando **git pull**. O comando **git pull** deve ser usado com cuidado, porque no processo de atualização pode gerar conflitos no Repositório Local, como veremos adiante.

<br />

9. Para aplicar as atualizações no Repositório Local, utilize o comando abaixo:

```bash
git pull origin main
```

*Observe que a sintaxe do comando **git pull** é muito semelhante a sintaxe do comando **git push**.*

10. Ao executar o comando **git pull**, será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/CL3Mikh.png" title="source: imgur.com" /></div>

*Observe que as alterações foram confirmadas, como indicado (seta amarela), na imagem acima.*

11. Volte para o Visual Studio Code e observe que o arquivo **docker.txt** do Repositório Local foi atualizado, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/5bIRit7.png" title="source: imgur.com" /></div>

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="4%"/> <a href="https://git-scm.com/docs/git-fetch/pt_BR" target="_blank"><b>Documentação: <i>Git Fetch</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="4%"/> <a href="https://git-scm.com/docs/git-pull/pt_BR" target="_blank"><b>Documentação: <i>Git Pull</i></b></a></div>

<br />

<h2>3. Trabalhando com Branches</h2>



Uma Branch no Git é como se fosse um ramo ou uma ramificação do código. Ela permite que você tenha versões diferentes do código em desenvolvimento ao mesmo tempo, sem afetar a versão principal (geralmente mantido na Branch main). Cada branch é uma cópia isolada de um commit específico, que pode receber novos commits de forma independente da branch de origem.

<br />

> [!NOTE]
>
> Todo Repositório Git possui uma branch padrão, geralmente chamada de **main**.

<br />

Vamos ver na prática como criar e trabalhar com mais de uma branch:

<br />

<h3>3.1. Criando uma nova branch</h3>



1. Crie uma nova branch, com o nome **ramo1**, através do comando:

```bash
git checkout -b ramo1
```

<br />

> O comando **git checkout** troca de branch, ou seja, sai da branch atual e acessa outra branch indicada no comando. A **opção -b** cria uma nova branch com o nome indicado (em nosso exemplo **ramo1**). Na prática, o comando acima cria e acessa a nova branch.

<br />

2. A imagem abaixo mostra que a branch **ramo1** foi criada e passou a ser a branch ativa:

<div align="left"><img src="https://i.imgur.com/Z56xq1h.png" title="source: imgur.com" /></div>

3. Para checar se está na branch **ramo1**, utilize o comando:

```bash
git branch --show-current
```

<br />

> O comando **git branch** permite criar, listar, renomear e excluir branches. Entretanto ele não permite que você alterne entre as branches ou faça a fusão do histórico de duas branches em uma.

<br />

4. Edite o arquivo **docker.txt** no **Visual Studio Code** e adicione o texto indicado, como mostra imagem abaixo:

- **docker.txt:** *Esta linha foi inserida na branch ramo1.*

<div align="left"><img src="https://i.imgur.com/QOAdYr5.png" title="source: imgur.com" /></div>

5. Confirme se os arquivos foram atualizados, através do comando:

```bash
git status
```

6. Observe na imagem abaixo, que o arquivo **docker.txt** está pronto para ser adicionado na index e ser "commitado":

<div align="left"><img src="https://i.imgur.com/bcs7KDm.png" title="source: imgur.com" /></div>

7. Faça o Commit das alterações, através dos comandos abaixo:

```bash
git add .
```

```bash
git commit -m "Atualizar a branch ramo1"
```

8. Para enviar a branch **ramo1** para o Repositório Remoto no Github, utilize o comando:

```bash
git push origin ramo1
```

<br />

> [!IMPORTANT]
>
> Observe no comando acima, que foi indicada a branch **ramo1**, ao invés da branch **main**, depois da palavra origin, indicando que a **branch ramo1** será enviada para o Repositório Remoto.

<br />

> [!TIP]
>
> Ao utilizar os comandos **git push** e **git pull**, sempre indique qual branch será enviada ou atualizada com o conteúdo e histórico do Repositório Remoto.

<br />

9. Volte para o Repositório Remoto **aulagit** no Github e observe que agora nós teremos 2 branches, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/qBvgTUV.png" title="source: imgur.com" /></div>

<br />

> [!IMPORTANT]
>
> As alterações feitas no arquivo **docker.txt** estão disponíveis apenas na branch ramo1. Se você abrir o arquivo docker.txt, que está na branch main, verá que o arquivo só tem 2 linhas.

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="4%"/> <a href="https://git-scm.com/docs/git-branch/pt_BR" target="_blank"><b>Documentação: <i>Git branch</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="4%"/> <a href="https://git-scm.com/docs/git-checkout/pt_BR" target="_blank"><b>Documentação: <i>Git Checkout</i></b></a></div>

<br />

<h3>3.2. Unindo o conteúdo da branch main, com o conteúdo da branch ramo1</h3>



1. Volte para a branch **main**

```bash
git checkout main
```

<br />

> [!NOTE]
>
> Note que como queremos apenas trocar de branch, não utilizaremos a opção **-b**, que é utilizada para criar uma nova branch.

<br />

2. Edite o arquivo **docker.txt** no Visual Studio Code e observe que o conteúdo do arquivo não foi modificado na branch main, como mostra imagem abaixo:

<div align="left"><img src="https://i.imgur.com/5bIRit7.png" title="source: imgur.com" /></div>

3. Vamos unir o conteúdo da branch **ramo1** com o conteúdo da branch **main**, atualizando o arquivo **docker.txt** do Repositório Local, com as alterações realizadas no mesmo arquivo, só que na branch **ramo1**, através do comando:

```bash
git merge ramo1
```

4. Abra o arquivo **docker.txt** no Visual Studio Code e observe que o arquivo foi atualizado:

<div align="left"><img src="https://i.imgur.com/QOAdYr5.png" title="source: imgur.com" /></div>

5. Envie as atualizações para a branch main no Github, através do comando:

```bash
git push origin main
```

<br />

> O Comando **git merge** é responsável por fazer a fusão (união) dos conteúdo e do histórico de 2 branches, em dentro de uma delas. 
>
> No exemplo acima, como a branch ativa é a branch **main**, ela receberá todo o conteúdo e o histórico da branch **ramo1**. Observe que a branch **ramo1** não terá o seu conteúdo e histórico alterados, enquanto a branch **main** terá o seu conteúdo e histórico modificados, porque recebeu o conteúdo e o histórico da branch **ramo1**.

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="4%"/> <a href="https://git-scm.com/docs/git-merge/pt_BR" target="_blank"><b>Documentação: <i>Git Merge</i></b></a></div>

<br />

<h2>4. Como funciona uma branch?</h2>



Como vimos anteriormente, uma branch (ramo ou ramificação) representa uma linha independente de desenvolvimento. As branches funcionam como se fosse um universo paralelo, onde você pode desenvolver uma nova funcionalidade (feature) para o seu projeto, em uma cópia, sem modificar o projeto original e com benefício de manter o histórico com todas as mudanças efetuadas nesta branch, independente do histórico da branch original. 

Vamos analisar o que aconteceu no nosso exemplo:

<div align="left"><img src="https://i.imgur.com/jBH0Jjp.png" title="source: imgur.com" /></div>

1. No exemplo acima, a branch **main** recebeu inicialmente 4 commits;
2. No commit 4 da branch **main**, foi criada uma nova branch, chamada **ramo1**. A branch **ramo1** será uma cópia exata do conteúdo e do histórico da branch **main**, até o **commit 4**;
3. A branch **ramo1** recebeu um novo commit contendo a atualização, que foi realizada no arquivo **docker.txt**;
4. Neste momento, o novo commit efetuado na branch **ramo1** não está disponível na Branch **main**;
5. Ao executar o comando **git merge**, na branch **main**, ela receberá todas as atualizações e o histórico da branch **ramo1**

O processo de fusão das branches exemplificado acima, fará com que a Branch main unifique os conteúdos e o histórico das duas branches, permitindo que o time de desenvolvimento visualize todas as alterações de ambas as branches, em ordem cronológica, mantendo o histórico completo do projeto.

Neste processo de fusão, podem acontecer alguns erros, entre eles podemos destacar 2:

- **Conflitos (conflicts):** Ocorrem quando o sistema não consegue resolver as diferenças entre duas confirmações. Isso pode acontecer quando duas pessoas alteram as mesmas linhas no mesmo arquivo ou quando um desenvolvedor exclui arquivos enquanto outro faz alterações. O Git marca os arquivos em conflito e interrompe o processo de merge. A partir daí, é responsabilidade dos desenvolvedores resolver o conflito. 
- **Histórias não Relacionadas (Unrelated Histories):** Referem-se a situações em que duas branches não compartilham um ancestral comum em seu histórico de commits. Essencialmente, são linhas de desenvolvimento separadas, que não têm conexão até que você as mescle explicitamente ou crie uma nova ramificação a partir de uma existente. Quando você encontra o erro *“fatal: refusing to merge unrelated histories”*, significa que você está tentando mesclar branches com diferentes históricos de commits.

<br />

<h2>5. Resolução de Conflitos</h2>



Vamos simular um conflito e vermos na prática como resolver:

<br />

<h3>5.1. Criando um conflito no Repositório Remoto</h3>



1. Volte para o Repositório Remoto **aulagit** no Github, abra o arquivo **docker.txt** e clique no **ícone do lápis para editar o arquivo**, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/ImHvg8m.png" title="source: imgur.com" /></div>

2. Adicione o texto indicado, como mostra imagem abaixo:

- **docker.txt:** *Esta linha vai gerar um conflito.*

<div align="left"><img src="https://i.imgur.com/9VHkfpP.png" title="source: imgur.com" /></div>

3. Faça o commit clicando no botão **Commit changes**, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/InJtaN6.png" title="source: imgur.com" /></div>

<br />

<h3>5.2. Criando um Conflito no Repositório Local</h3>



1. Volte para o terminal

2. Edite o arquivo **docker.txt** no **Visual Studio Code** e adicione o texto indicado, como mostra imagem abaixo:

- **docker.txt:** *Esta linha vai criar um conflito local.*

<div align="left"><img src="https://i.imgur.com/PWkYhqZ.png" title="source: imgur.com" /></div>

3. Faça o **Commit das alterações**, através dos comandos abaixo:

```bash
git add .
```

```bash
git commit -m "Criar o conflito local!"
```

4. Para receber o conteúdo atualizado do Repositório Remoto no Github, utilize o comando:

```bash
git pull origin main
```

5. Após executar o comando acima, observe que no final da mensagem aparece a palavra **CONFLICT**, indicando que foi encontrado um conflito entre o conteúdo do Repositório Local e o conteúdo do Repositório Remoto:

<div align="left"><img src="https://i.imgur.com/A4sImKx.png" title="source: imgur.com" /></div>

6. Volte para o arquivo **docker.txt** no **Visual Studio Code** e verifique os conflitos encontrados:

<div align="left"><img src="https://i.imgur.com/Kf9F76j.png" title="source: imgur.com" /></div>

Observe na imagem acima, que as diferenças encontradas nos dois arquivos são exibidas indicando o conteúdo da linha que gerou o conflito no **Repositório Local** (destacado em verde) e o conteúdo da linha que gerou o conflito no **Repositório Remoto** (destacado em azul).

Neste exemplo temos o conflito em apenas uma linha, entretanto, em um projeto podemos ter várias linhas em conflito, em vários arquivos. No Visual Studio Code, todas as linha que estão gerando conflito serão indicadas da mesma forma.

7. O Visual Studio Code oferece 3 opções para resolver um conflito e mais uma para ajudar na decisão:

- **Accept Current Change:** Mantém a mudança local
- **Accept Incoming Change:** Mantém a mudança remota
- **Accept Both Changes:** Une as 2 mudanças
- **Compare Changes:** Exibe os 2 arquivos lado a lado, para que
  você possa comparar as diferenças.

8. Clique na opção que melhor se encaixa com o seu objetivo e salve o arquivo.

9. Faça o **Commit das alterações**, através dos comandos abaixo:

```bash
git add .
```

```bash
git commit -m "Resolver o conflito!"
```

10. Confirme se os arquivos foram “Commitados”

```bash
git status
```

11. Observe na imagem abaixo que os arquivos foram "commitados" e o conflito foi resolvido:

<div align="left"><img src="https://i.imgur.com/rkWMgw3.png" title="source: imgur.com" /></div>

12. Envie as atualizações para o Repositório Remoto no Github.

```bash
git push origin main
```

<br />

> [!TIP]
>
> Para evitar conflitos, uma boa prática é manter o Repositório Local sincronizado com o Repositório Remoto, ou seja, sempre atualizado, através da execução do comando **git pull** no Repositório Local, sempre que ocorrer uma atualização no Repositório Remoto.

<br />

<h2>6. Histórias não Relacionadas (Unrelated Histories)</h2>



O erro **fatal: refusing to merge unrelated histories** ocorre quando dois projetos *não relacionados* são mesclados (ou seja, projetos que não estão cientes da existência um do outro e têm históricos de confirmação incompatíveis).

Este erro costuma acontecer nos casos a seguir:

- Você clonou um projeto e, de alguma forma, a pasta `.git foi deletada ou corrompida. Isso faz com que o Git desconheça seu histórico local e, portanto, fará com que ele lance esse erro quando você tentar fazer *push* ou *pull do* repositório remoto.
- Você criou um novo repositório, adicionou alguns *commits* a ele e agora está tentando *extrair* de um repositório remoto que já possui alguns commits próprios. O Git também lançará o erro neste caso, pois não tem ideia de como os dois projetos estão relacionados.

Para resolver este erro utilize o comando abaixo para permitir que os históricos sejam unidos:

```bash
git pull origin main --allow-unrelated-histories
```

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="4%"/> <a href="https://git-scm.com/docs/git-pull/pt_BR" target="_blank"><b>Documentação: <i>Git Pull</i></b></a></div>

<br />

<h2>7. Comandos úteis</h2>



  1. Criar uma Branch no Github
```bash
git push origin task3:nova_branch
```

 2. Apagar uma Branch no github
```bash
git push origin:nome_branch
```

 3. Renomear uma Branch
```bash
git branch -m novo_nome
```
4. Apagar uma Branch no Repositório Local

```bash
git branch -d nome_branch
```

5. Alterar a mensagem do ultimo commit

```bash
git commit --amend
```

*O Editor padrão do Git (em nosso exemplo o Visual Studio Code), será aberto. Altere a mensagem e feche o editor.*

Outra opção, para não utilizar o editor, é utilizar o comando:

```bash
git commit --amend -m "Mensagem nova"
```

6. Renomear a Branch master para main

```bash
git branch -M master main
```

7. Renomear uma pasta do repsitório local:

```bash
git mv nome_antigo_da_past> novo_nome_da_pasta
```

*O comando `git mv` mantém o histórico do arquivo, garante que o Git rastreie as mudanças corretamente e atualiza o repositório remoto corretamente.*

8. Remover arquivos e/ou pasta da árvore, sem remover da pasta de trabalho.

```bash
git rm --cached <nome da pasta ou arquivo>
```

O comando `git rm --cached` remove o arquivo ou pasta do controle do Git (do índice), mas o mantém no diretório local. Se houver um `.git` dentro de uma subpasta, é necessário remover esse `.git` manualmente, pois isso caracteriza um repositório Git separado (submódulo ou pasta "presa").

Este comando é especialmente útil para resolver o problema conhecido como **“pasta presa”** no GitHub. Esse problema ocorre quando uma subpasta contém um diretório oculto `.git`, o que a transforma, inadvertidamente, em um repositório Git separado. Isso gera uma duplicidade de repositórios dentro da mesma estrutura, tornando a pasta inacessível para operações no repositório principal. Nessa situação, o ícone da pasta muda para <img src="https://i.imgur.com/OzRhQuP.png" title="source: imgur.com" width="30px"/> — indicando que ela está vinculada como um sub-repositório. Veja a ilustração abaixo para entender visualmente o problema:

<div align="center"><img src="https://i.imgur.com/s7VnPfi.png" title="source: imgur.com" /></div>

O comando acima elimina a pasta oculta **.git** da subpasta e disponibiliza o conteúdo da pasta para ser "commitado" novamente.

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="4%"/> <a href="https://git-scm.com/docs/git-rm/pt_BR" target="_blank"><b>Documentação: <i>Git rm</i></b></a></div>

<br /><br />


<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
