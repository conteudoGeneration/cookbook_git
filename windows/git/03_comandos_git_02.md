<h1>Comandos Git - Parte 02</h1>



<h2>1. Clonando o Repositório Remoto</h2>

Antes de clonarmos o repositório remoto, vamos apagar o nosso repositório local, para simularmos um acidente de percurso.

1. Vamos retornar para a pasta do usuário, através do comando:

```bash
cd ~
```

2. Na sequência, vamos apagar a pasta **aulagit** através do comando:

```bash
rm -Rf aulagit
```

3. Para confirmar que a pasta foi apagada, utilize o comando abaixo:

```bash
ls
```

4. Volte para o repositório remoto **aulagit** no Github e copie o endereço **HTTPS** do repositório, como indicado na imagem abaixo:

<div align="center"><img src="https://i.imgur.com/VKmyqsN.png" title="source: imgur.com" /></div>

5. Para clonar o repositório, utilize o comando abaixo:

```bash
git clone https://github.com/rafaelq80/aulagit.git
```

*Observe que o endereço do repositório remoto foi adicionado depois do comando **git clone**.*

6. Ao efetuar a clonagem (cópia do repositório), será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/f2HWeaP.png" title="source: imgur.com" /></div>

7. Para confirmar que a clonagem foi bem sucedida, utilize o comando abaixo:

```bash
ls
```

*Observe que a pasta **aulagit** foi restaurada.*

8. Para acessar a pasta, utilize o comando:

```bash
cd aulagit
```

9. Para verificar se o repositório clonado está conectado com o repositório do Github, utilize o comando abaixo:

```bash
git remote -v
```

10. Ao executar o comando acima, será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/rURPm9E.png" title="source: imgur.com" /></div>

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-clone/pt_BR" target="_blank"><b>Documentação: <i>Git Clone</i></b></a></div>

<br />


<h2>2. Atualizando o Repositório Local</h2>

Vamos fazer uma alteração no Github e atualizar o repositório local:

1. Volte para o repositório remoto **aulagit** no Github, abra o arquivo **docker.txt** e clique no **ícone do lápis para editar o arquivo**, como mostra a imagem abaixo

<div align="left"><img src="https://i.imgur.com/2f7iCeA.png" title="source: imgur.com" /></div>

2. Adicione o texto indicado, como mostra imagem abaixo:

- **docker.txt:** *Esta linha foi inserida na branch ramo1.

<div align="left"><img src="https://i.imgur.com/iJHslsO.png" title="source: imgur.com" /></div>

3. Faça o **commit das alterações** clicando no botão **Commit changes**, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/f2hjRGH.png" title="source: imgur.com" /></div>

4. Volte para o Terminal. 
5. Para atualizar o repositório local com as alterações efetuadas no repositório remoto, utilize o comando abaixo:

```bash
git fetch
```

6. Ao executar o comando acima, será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/wmd3A23.png" title="source: imgur.com" /></div>

7. Para confirmar se as atualizações foram efetuadas, utilize o comando abaixo:

```bash
git status
```

8. Observe que as atualizações foram adicionadas no repositório, mas não foram aplicadas no repositório local, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/XCdixZF.png" title="source: imgur.com" /></div>

O comando **git fetch** é a opção de atualização segura. O **git fetch** baixa o conteúdo remoto e não altera o estado do repositório local. 

Para baixar o conteúdo remoto e, de imediato, tenta alterar o conteúdo do repositório local  para que ele corresponda àquele conteúdo, utilizamos o comando **git pull**. O comando **git pull** deve ser usado com cuidado, porque no processo de atualização ele pode gerar conflitos no repositório local.

9. Para aplicar as atualizações no repositório local, utilize o comando abaixo:

```bash
git pull origin main
```

*Observe que o comando **git pull** é semelhante ao comando **git push**.*

10. Ao executar o comando git pull, será exibida a mensagem abaixo:

<div align="left"><img src="https://i.imgur.com/CL3Mikh.png" title="source: imgur.com" /></div>

*Observe que as alterações foram confirmadas, como indicado (seta amarela), na imagem acima.*

11. Volte para o VSCode e observe que o arquivo **docker.txt** no repositório local foi atualizado, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/5bIRit7.png" title="source: imgur.com" /></div>

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-fetch/pt_BR" target="_blank"><b>Documentação: <i>Git Fetch</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-pull/pt_BR" target="_blank"><b>Documentação: <i>Git Pull</i></b></a></div>

<br />


<h2>3. Trabalhando com Branch</h2>

<h3>3.1. Criando uma nova branch</h3>

1. Crie uma nova branch, com o nome **ramo1**, através do comando:

```bash
git checkout -b ramo1
```

O comando **git checkout** troca de branch, ou seja, sai da branch atual e acessa outra branch indicada no comando. A **opção -b** cria uma nova branch com o nome indicado (em nosso exemplo **ramo1**), e acessa a nova branch.

2. A imagem abaixo mostra que a branch **ramo1** foi criada e passou a ser a branch ativa:

<div align="left"><img src="https://i.imgur.com/Z56xq1h.png" title="source: imgur.com" /></div>

3. Para checar se está na branch **ramo1**, utilize o comando:

```bash
git branch --show-current
```

4. Edite o arquivo **docker.txt** no **VSCode** e adicione o texto indicado, como mostra imagem abaixo:

- **docker.txt:** *Esta linha foi inserida na branch ramo1.*

<div align="left"><img src="https://i.imgur.com/QOAdYr5.png" title="source: imgur.com" /></div>

5. Confirme se os arquivos foram salvos, através do comando:

```bash
git status
```

6. Observe na imagem abaixo, que o arquivo docker.txt está pronto para ser adicionado na index e ser "commitado":

<div align="left"><img src="https://i.imgur.com/bcs7KDm.png" title="source: imgur.com" /></div>

7. Faça o Commit das alterações, através do comando:

```bash
git commit -a -m "Atualizar a branch ramo1"
```

8. Para enviar a branch **ramo1** para o Repositório Remoto no Github, utilize o comando:

```bash
git push origin ramo1
```

*Observe no comando acima, que foi indicada a branch **ramo1**, ao invés da branch **main**, depois da palavra origin, indicando que a **branch ramo1** será enviada para o repositório remoto*.

9. Volte para o Repositório Remoto **aulagit** no Github e observe que agora nós teremos 2 branches, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/qBvgTUV.png" title="source: imgur.com" /></div>

*As alterações feitas no arquivo **docker.txt** estão disponíveis apenas na branch ramo1. Se você abrir o arquivo docker.txt, que está na branch main, verá que o arquivo só tem 2 linhas.*

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-branch/pt_BR" target="_blank"><b>Documentação: <i>Git branch</i></b></a></div>

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-checkout/pt_BR" target="_blank"><b>Documentação: <i>Git Checkout</i></b></a></div>

<br />

<h3>3.2. Atualizando a branch main com o conteúdo da nova branch</h3>

1. Volte para a branch Main

```bash
git checkout main
```

2. Edite o arquivo **docker.txt** no VSCode e observe que o conteúdo do arquivo não foi modificado na branch Main, como mostra imagem abaixo:

<div align="left"><img src="https://i.imgur.com/5bIRit7.png" title="source: imgur.com" /></div>

3. Atualize a branch main com as alterações realizadas no arquivo **docker.txt** na branch **ramo1**, atravé do comando:

```bash
git merge ramo1
```

4. Abra o arquivo **docker.txt** no VSCode e observe que o arquivo foi atualizado:

<div align="left"><img src="https://i.imgur.com/QOAdYr5.png" title="source: imgur.com" /></div>

5. Envie as atualizações para a branch Main no Github, através do comando:

```bash
git push origin main
```

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-merge/pt_BR" target="_blank"><b>Documentação: <i>Git Merge</i></b></a></div>

<br />


<h2>4. Como funciona uma branch</h2>

Uma branch (ramo) representa uma linha independente de desenvolvimento. As ramificações servem como uma abstração para o processo de edição/estágio/commit. Você pode pensar neles como uma maneira de solicitar um novo diretório de trabalho, área de preparação e histórico do projeto. Novos commits são registrados no histórico do branch atual, o que resulta em uma bifurcação no histórico do projeto.

O `git branch`comando permite criar, listar, renomear e excluir ramificações. Ele não permite que você alterne entre as ramificações ou reúna um histórico bifurcado novamente. Por esta razão, `git branch`está fortemente integrado com os comandos `git checkout`e .`git merge`

Vamos analisar o que aconteceu no nosso exemplo:

<div align="left"><img src="https://i.imgur.com/jBH0Jjp.png" title="source: imgur.com" /></div>

1. A branch main recebeu 4 commits;
2. A partir do commit 4, foi criada a branch ramo1. Este commit será uma cópia do commit 3;
3. A branch ramo1 recebeu um commit contendo a atualização do arquivo docker.txt;
4. Esta atualização não está visível na Branch main
5. Ao efetuar o git merge, a branch main recebe as alterações que foram realizadas na branch ramo1.

A branch ramo1 é um universo paralelo até que o git merge seja executado na branch main.

<br />

<h2>5. Resolução de Conflitos</h2>

<h3>5.1. Criando o conflito no Github</h3>

1. Volte para o repositório remoto **aulagit** no Github, abra o arquivo **docker.txt** e clique no **ícone do lápis para editar o arquivo**, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/ImHvg8m.png" title="source: imgur.com" /></div>

2. Adicione o texto indicado, como mostra imagem abaixo:

- **docker.txt:** *Esta linha vai gerar um conflito.*

<div align="left"><img src="https://i.imgur.com/9VHkfpP.png" title="source: imgur.com" /></div>

3. Faça o , como mostra a imagem abaixo: clicando no botão **Commit changes**, como mostra a imagem abaixo:

<div align="left"><img src="https://i.imgur.com/InJtaN6.png" title="source: imgur.com" /></div>

<br />

<h3>5.2. Criando o Conflito no Git Local</h3>

1. Volte para o terminal

2. Edite o arquivo **docker.txt** no **VSCode** e adicione o texto indicado, como mostra imagem abaixo:

- **docker.txt:** *Esta linha vai criar um conflito local.*

<div align="left"><img src="https://i.imgur.com/PWkYhqZ.png" title="source: imgur.com" /></div>

3. Faça o **Commit das alterações**, através do comando:

```bash
git commit -a -m "Criar o conflito local!"
```

4. Para receber o conteúdo atualizado do Repositório Remoto no Github, utilize o comando:

```bash
git pull origin main
```

5. Após executar o comando acima, observe que no final da mensagem aparece a palavra **CONFLICT**, indicando que foi encontrado um conflito entre o conteúdo do repositório local e o conteúdo do repositório remoto:

<div align="left"><img src="https://i.imgur.com/A4sImKx.png" title="source: imgur.com" /></div>

6. Volte para o arquivo **docker.txt** no **VSCode** e verifique os conflitos encontrados:

<div align="left"><img src="https://i.imgur.com/Kf9F76j.png" title="source: imgur.com" /></div>

Observe na imagem acima, que as diferenças encontradas nos dois arquivos são exibidas indicando o que está no **repositório local** (destacado em verde) e no **repositório remoto** (destacado em azul).

7. O VSCode oferece 3 opções para resolver um conflito e mais uma para ajudar na decisão:

- **Accept Current Change:** Mantém a mudança local
- **Accept Incoming Change:** Mantém a mudança remota
- **Accept Both Changes:** Une as 2 mudanças
- **Compare Changes:** Exibe os 2 arquivos lado a lado, para que
  você possa comparar as diferenças.

8. Clique na opção que melhor se encaixa com o seu objetivo e salve o arquivo.

9. Faça o **Commit das alterações**, através do comando:

```bash
git commit -a -m "Resolver o conflito!"
```

10. Confirme se os arquivos foram “Commitados”

```bash
git status
```

11. Observe na imagem abaixo que os arquivos foram "commitados" e o conflito foi resolvido:

<div align="left"><img src="https://i.imgur.com/rkWMgw3.png" title="source: imgur.com" /></div>

12. Envie as atualizações para o repositório remoto no Github.

```bash
git push origin main
```

<br />

| <img src="https://i.imgur.com/RfjtOFi.png" title="source: imgur.com" width="120px"/> | <div align="left">**DICA:** Para evitar conflitos, uma boa prática é tentar fazer com que todos na equipe sempre estejam atualizados com o repositório remoto através da execução do comando git pull regularmente no Repositório Local.</div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

<br />

<h2>6. Comandos úteis</h2>

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

5. Forçar uma atualização no Repositório Remoto

```bash
git push -f origin main
```

6. Forçar uma atualização no Repositório Local

```bash
git pull -f origin main
```

7. Alterar a mensagem do ultimo commit

```bash
git commit --amend
```

*O Editor padrão do Git será aberto. Altere a mensagem e feche o editor.*

8. Renomear a Branch master para main

```bash
git branch -M master main
```

9. Remover arquivos e/ou pasta da árvore, sem remover da pasta de trabalho.

```bash
git rm --cached <nome da pasta ou arquivo>
```

Este comando é muito útil para resolver o problema da **"pasta presa"** no Github, ou seja, a pasta possui a pasta oculta .git, gerando uma duplicidade de repositório. Quando isto acontece, a pasta fica inacessível e o ícone muda para <img src="https://i.imgur.com/OzRhQuP.png" title="source: imgur.com" width="30px"/> uma pasta com uma seta. Veja a representação gráfica na imagem abaixo:

<div align="center"><img src="https://i.imgur.com/s7VnPfi.png" title="source: imgur.com" /></div>

O comando acima elimina a pasta oculta **.git** da subpasta e disponibiliza o conteúdo da pasta para ser "commitado" novamente.

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-rm/pt_BR" target="_blank"><b>Documentação: <i>Git rm</i></b></a></div>

<br /><br />


<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
