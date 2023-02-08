<h1>Enviando o primeiro Projeto Java para o Github</h1>



1. No Eclipse/STS, clique com o botão direito do mouse sobre a pasta do projeto (no exemplo abaixo, **helloworld**). No menu que será averto, clique na opção **Show in 🡒 System Explorer**, para exibir a pasta no Windows Explorer.

<div align="center"><img src="https://i.imgur.com/cR65mhl.png" title="source: imgur.com" /></div>

2. Será aberta a janela do Windows Explorer, mostrando todas as pastas, com todos os projetos criados até o momento.

<div align="center"><img src="https://i.imgur.com/jgdxc43.png" title="source: imgur.com" /></div>

3. Clique com o botão direito do mouse em qualquer ponto da janela do Windows Explorer, que não tenha nenhuma pasta. No menu que será aberto, clique na opção **Git Bash Here**, para abrir o **Terminal do Git** nesta pasta.

<div align="center"><img src="https://i.imgur.com/h34v3yG.png" title="source: imgur.com" /></div>

4. Será aberto o Git Bash, como mostra a imagem abaixo, já na pasta da Workspace do Eclipse/STS.

<div align="center"><img src="https://i.imgur.com/To5Ttfc.png" title="source: imgur.com" /></div>

5. Crie o arquivo **.gitignore**, através do comando abaixo:

```bash
notepad .gitignore
```

6. Será aberta a janela do **Notepad (Bloco de Notas)**, solicitando a criação do arquivo. Clique no botão **Sim**, para continuar.
<div align="center"><img src="https://i.imgur.com/IkFtVpL.png" title="source: imgur.com" /></div>

<br />

> O Git enxerga cada arquivo no seu Repositório Remoto com um dos três estados abaixo:
>
> 1. **Rastreado** – Um arquivo que já passou pelo staging ou commit;
> 2. **Não Rastreado** – Um arquivo que *não* passou pelo staging ou commit;
> 3. **Ignorado** – Um arquivo que o Git foi forçado a ignorar.
>
> Os arquivos ignorados costumam ser artefatos de desenvolvimento e  arquivos gerados por máquina que podem ser derivados da fonte do seu  repositório ou que não devem passar por commit. Exemplos comuns incluem:
>
> - caches de dependência, como o conteúdo de `/node_modules` ou `/packages`
> - código compilado, como arquivos `.o`, `.pyc` e `.class`
> - diretórios de saída de build, como `/bin`, `/out` ou `/target`
> - arquivos gerados no período de execução, como `.log`, `.lock` ou `.tmp`
> - arquivos de sistema ocultos, como `.DS_Store` ou `Thumbs.db`
> - arquivos pessoais de configuração do IDE, como `.idea/workspace.xml`
>
> Os arquivos ignorados são rastreados em um arquivo especial chamado `.gitignore`, que é verificado na origem do seu repositório. Não há nenhum comando git ignore explícito: é preciso editar e fazer commit do arquivo `.gitignore` à mão quando você tiver novos arquivos que quer ignorar. Os arquivos `.gitignore` contêm padrões que são comparados com nomes de arquivos em seu repositório para determinar se devem ou não ser ignorados. Por isso adicionamos o arquivo .gitignore manualmente.

<br />

7. No arquivo **.gitignore**, adicione a linha **.metadata** e na sequência salve e feche o arquivo.

<div align="center"><img src="https://i.imgur.com/AKTNixM.png" title="source: imgur.com" /></div>

**.metadata** é a pasta que será ignorada pelo Git na hora de versionar o código.

8. De volta ao **Git Bash**, digite o comando abaixo para criar o Repositório Local dentro da pasta **Worskspace do Eclipse/STS**.

```bash
git init
```

9. Digite o comando abaixo para adicionar o Projeto na **Stage Area** do Git:


```bash
git add .
```

10. Na sequência, faça o commit do Projeto, através do comando abaixo:

```bash
git commit -m "Projeto Hello World"
```

11. Acesse o seu **Github** e crie um novo **Repositório**, através da opção **New repository**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/GncQ1uf.png" title="source: imgur.com" /></div>

12. Crie o **Repositório Remoto** chamado **java**:

<div align="center"><img src="https://i.imgur.com/zp1RlIP.png" title="source: imgur.com" /></div>

13. Clique no botão **Create Repository**, para criar o Repositório:

<div align="center"><img src="https://i.imgur.com/d9cRI9m.png" title="source: imgur.com" /></div>

14. Na próxima janela, copie o endereço **HTTPS do Repositório Remoto**, indicado na imagem abaixo:

<div align="center"><img src="https://i.imgur.com/pIfU6Sx.png" title="source: imgur.com" /></div>

15. Volte para o Git Bash e execute o comando abaixo para conectar o seu **Repositório Local** com o seu **Repositório Remoto**, onde o endereço **https**, será o endereço do seu **Repositório Remoto**.

```bash
git remote add origin https://github.com/rafaelq80/java.git
```

16. Digite o comando abaixo para checar se o seu  **Repositório Local** está conectado com o seu **Repositório Remoto**:

```bash
git remote -v
```

17. Se estiver conectado, será exibida uma mensagem, semelhante a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/XWee1oq.png" title="source: imgur.com" /></div>

18. Na sequência, utilize o comando abaixo, para sincronizar o conteúdo do **Repositório Local** com o seu **Repositório Remoto**:

```bash
git push origin main
```

19. Volte para o Github, atualize a página do seu **Repositório Remoto** e verifique se ele está semelhante a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/HQANKTE.png" title="source: imgur.com" /></div>

<br />

<h1>Esqueci de criar o .gitignore</h1>



1. Caso você tenha esquecido de criar o **.gitignore**, o seu **Repositório Remoto** estará  semelhante a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/jlFcxIT.png" title="source: imgur.com" /></div>

A pasta **.metadata**, é utilizada para guardar as configurações da Workspace que você está desenvolvendo o seu projeto. Estas configurações são específicas do Eclipse e não é necessário enviar para o Github, além de ocupar espaço desnecessário no Repositório Remoto. Por isso vamos retirar esta pasta do versionamento.

2. Abra o Gitbash e acesse a pasta do seu **Repositório Local** (em nosso exemplo, a pasta **Workspace do Eclipse/STS**)
3. Crie o arquivo **.gitignore**, através do comando abaixo:

```bash
notepad .gitignore
```

4. Será aberta a janela do **Notepad (Bloco de Notas)**, solicitando a criação do arquivo. Clique no botão **Sim**, para continuar.

<div align="center"><img src="https://i.imgur.com/IkFtVpL.png" title="source: imgur.com" /></div>

5. No arquivo **.gitignore**, adicione a linha **.metadata** e na sequência salve e feche o arquivo.

<div align="center"><img src="https://i.imgur.com/AKTNixM.png" title="source: imgur.com" /></div>

**.metadata** é a pasta que será ignorada pelo Git na hora de versionar o código.

6. Digite o comando abaixo para adicionar o arquivo na **Stage Area** do Git:


```bash
git add .
```

7. Na sequência, faça o commit do arquivo, através do comando abaixo:

```bash
git commit -m "Adicionar .gitignore"
```

8. Na sequência, utilize o comando abaixo, para sincronizar o conteúdo do **Repositório Local** com o seu **Repositório Remoto**:

```bash
git push origin main
```

9. Volte para o Github, atualize a página do seu **Repositório Remoto** e verifique se ele está semelhante a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/fCIzUUz.png" title="source: imgur.com" /></div>

Observe que o arquivo **.gitignore** foi enviado para o Repositório Remoto, entretanto a pasta **.metadata** não foi excluída. Isso aconteceu porquê o .gitignore irá ignorar a pasta (não irá versionar), mas não irá excluir a pasta já versionada anteriormente.

10. Para excluir a pasta, utilize o comando abaixo:

```bash
git rm -rf --cached .metadata/
```

**IMPORTANTE:** O comando acima exclui a pasta do **Repositório Local**, mas não exclui a pasta do seu computador, ou seja, ao abrir a pasta Workspace no Windows Explorer, você verá que a pasta **.metadata** continua lá, apenas não será mais versionada.

<div align="center"><img src="https://i.imgur.com/Qxxd9qX.png" title="source: imgur.com" /></div>

11. Digite o comando abaixo para adicionar a exclusão da pasta **.metadata** na **Stage Area** do Git:


```bash
git add .
```

12. Na sequência, faça o commit para confirmar a exclusão da pasta **.metadata** do Repositório Local, através do comando abaixo:

```bash
git commit -m "Excluir a pasta .metadata"
```

13. Na sequência, utilize o comando abaixo, para sincronizar o conteúdo do **Repositório Local** com o seu **Repositório Remoto**:

```bash
git push origin main
```

14. Volte para o Github, atualize a página do seu **Repositório Remoto** e verifique se ele está semelhante a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/LgMjaZA.png" title="source: imgur.com" /></div>

Observe que a pasta **.metadata** foi excluída do **Repositório Remoto**.

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-rm/pt_BR" target="_blank"><b>Documentação: <i>Git RM</i></b></a></div>

<br />



<h1>Criei um novo Projeto na Workspace</h1>



No decorrer das aulas, serão criados vários projetos dentro da pasta Workspace. Para atualizar os Repositórios Local e Remoto, não será necessário criar um novo Repositório e fazer todo o processo acima. Para atualizar o Repositório atual, siga os passos abaixo:

1. Digite o comando abaixo para adicionar os novos Projetos na **Stage Area** do Git:


```bash
git add .
```

2. Na sequência, faça o commit do arquivo, através do comando abaixo:

```bash
git commit -m "Nome do Projeto"
```

3. Na sequência, utilize o comando abaixo, para sincronizar o conteúdo do **Repositório Local** com o seu **Repositório Remoto**:

```bash
git push origin main
```

4. Volte para o Github, atualize a página do seu **Repositório Remoto** e verifique se ele foi atualizado.
