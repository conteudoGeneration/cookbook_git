<h1>Atualizando o Repositório Java no Github</h1>

O que veremos por aqui:

- Visualizar a pasta Workspace
- Atualizar o Repositório Git Local
- Atualizar o Repositório Remoto no Github

<h2>1. Visualizar a pasta Workspace</h2>

1. No Eclipse/STS, clique com o botão direito do mouse sobre a pasta do projeto (no exemplo abaixo, **helloworld**). No menu que será aberto, clique na opção **Show in 🡒 System Explorer**, para exibir a pasta no Windows Explorer.

<div align="center"><img src="https://i.imgur.com/cR65mhl.png" title="source: imgur.com" /></div>

2. Será aberta a janela do Windows Explorer, mostrando todas as pastas, com todos os projetos criados até o momento.

<div align="center"><img src="https://i.imgur.com/iWE0EAX.png" title="source: imgur.com" /></div>

<br />

| <img src="https://i.imgur.com/vVDBDG0.png" title="source: imgur.com" width="100px"/> | <div align="left"> **ALERTA DE BSM:** *Mantenha a Atenção aos Detalhes. A sua pasta Workspace pode conter outras pastas, diferentes da imagem acima.* </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

<br />

3. Caso esta pasta **.git** não esteja sendo exibida, na janela do Windows Explorer, clique na **Guia Exibir** e na sequência no botão **Opções**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/4Bh3jii.png" title="source: imgur.com" /></div>

4. Na janela **Opções de Pasta**, na **Guia Modo de Exibição**, no item **Configurações avançadas**, localize a opção: **Pastas e arquivos ocultos** e marque a opção **Mostrar arquivos, pastas e unidades ocultas** (como mostra a figura abaixo). Em seguida clique em **OK** para concluir.

<div align="center"><img src="https://i.imgur.com/n8hQu12.png" title="source: imgur.com" /></div>

<br />

| <img src="https://i.imgur.com/oScAYGc.png" title="source: imgur.com" width="80px"/> | <div align="left"> **ATENÇÃO:** *A alteração da visualização de arquivos ocultos será mantida pelo Windows, logo você não vai precisar fazer novamente.* </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

<br />

5. Na imagem abaixo, encontramos a seguintes pastas e arquivos:

<div align="center"><img src="https://i.imgur.com/iWE0EAX.png" title="source: imgur.com" /></div>

<br />

| Pasta / Arquivo | Conteúdo                                                     |
| --------------- | ------------------------------------------------------------ |
| **.git**        | Pasta do Git, responsável por criar o versionamento do código. Esta pasta é oculta (repare que ela está debotada) e sempre será ignorada pelo Git, entretanto ela não pode ser apagada, senão você perderá todo o histórico do seu Repositório. |
| **.metadata**   | Pasta que contém as configurações do Eclipse / STS. Esta pasta não pode ser apagada, senão você perderá todas as configurações do seu Eclipse / STS |
| **aula_01**     | Pasta que contém os códigos da sessão de hoje                |
| **helloworld**  | Pasta que contém o código do Projeto Hello World             |
| **.gitignore**  | Arquivo que contém as pastas e arquivos que não serão versionados (ignorados) pelo Git. Na sessão anterior, adicionamos a pasta **.metadata** neste arquivo. |

<br />

<h2>2. Atualizar o Repositório Git Local</h2>



1. Dentro da pasta Workspace, clique com o botão direito do mouse em qualquer ponto da janela do Windows Explorer, que não tenha nenhuma pasta ou arquivo. No menu que será aberto, clique na opção **Git Bash Here**, para abrir o **Terminal do Git** nesta pasta.

<div align="center"><img src="https://i.imgur.com/zbTy7xM.png" title="source: imgur.com" /></div>

2. Será aberto o Git Bash, como mostra a imagem abaixo, já na pasta da Workspace do Eclipse/STS.

<div align="center"><img src="https://i.imgur.com/To5Ttfc.png" title="source: imgur.com" /></div>

<br />

| <img src="https://i.imgur.com/vVDBDG0.png" title="source: imgur.com" width="100px"/> | <div align="left"> **ALERTA DE BSM:** *Mantenha a Atenção aos Detalhes. A nome da sua pasta Workspace pode ser diferente da imagem acima.* </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

<br />

3. Digite o comando abaixo para checar se o seu  **Repositório Local** está conectado com o seu **Repositório Remoto**:

```bash
git remote -v
```

4. Se estiver conectado, será exibida uma mensagem, **semelhante** a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/XWee1oq.png" title="source: imgur.com" /></div>

5. Digite o comando abaixo para adicionar os novos arquivos na **Stage Area** do Git:


```bash
git add .
```

6. Na sequência, digite o comando **git status** e observe que todos os arquivos criados na sessão de hoje, foram adicionados na **Stage**, como mostra a imagem abaixo, e estão aguardando para serem "comitados":

```bash
git status
```

<br />

<div align="center"><img src="https://i.imgur.com/upNNUCw.png" title="source: imgur.com" /></div>

7. Na sequência, faça o commit dos arquivos através do comando abaixo:

```bash
git commit -m "Aula 01 - Variáveis e Operadores"
```

8. Para confirmar que o commit foi realizado com sucesso, digite o comando **git log** e observe que agora você terá 2 commits:

```bash
git log
```

<br />

<div align="center"><img src="https://i.imgur.com/oC9rtv2.png" title="source: imgur.com" /></div>

9. Observe que o commit que você acabou de fazer, foi realizado apenas no Repositório Local (seta amarela). No Repositório Remoto (seta verde), continua existindo apenas o commit feito na sessão anterior (Hello World).
10. Acesse o Repositório Remoto **java** no seu Github e verifique que ele continua com apenas 1 commit (Hello World), semelhante a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/HQANKTE.png" title="source: imgur.com" /></div>

<br />

<h2>2. Atualizar o Repositório Remoto no Github</h2>



1. Volte para o Terminal - Git Bash
2. Na sequência, utilize o comando abaixo, para sincronizar o conteúdo do **Repositório Local** com o seu **Repositório Remoto**:

```bash
git push origin main
```

3. Para confirmar que a sincronização foi realizada com sucesso, digite o comando **git log** e observe que agora você terá os 2 commits nos 2 Repositórios:

```bash
git log
```

<br />

<div align="center"><img src="https://i.imgur.com/g6V8HHk.png" title="source: imgur.com" /></div>

4. Observe que o commit que você acabou de fazer, foi enviado para o Repositório Remoto (seta verde).

5. Acesse o Repositório Remoto **java** no seu Github, atualize a página e verifique que ele agora possui 2 commits, semelhante a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/XFJwo0f.png" title="source: imgur.com" /></div>

<br />

| <img src="https://i.imgur.com/vVDBDG0.png" title="source: imgur.com" width="100px"/> | <div align="left"> **ALERTA DE BSM:** *Mantenha a Atenção aos Detalhes. Repita estes passos a cada novo projeto que for criado ou a cada alteração que você realizar em um projeto existente.* </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
