<h1>1.Configurando o Git</h1>

Vamos configurar o Git local, antes de iniciarmos o uso da ferramenta:

1. Para verificar se o Git está instalado no sistema e a versão, digite o comando:

```bash
git version
```

2. Para listar todas as configurações do Git, digite o comando:

```bash
git config --list 
```

Para sair da listagem do comando, caso seja necessário, pressione a letra **q** do seu teclado.

*Caso não apareça nenhuma configuração, você ainda não configurou o seu Git.*

3. Para configurar o seu **nome** no Git, digite o comando:

```bash
git config --global user.name "Seu_Nome"
```

*Substitua Seu_Nome, pelo seu nome. Exemplo: João*

4. Para verificar se o seu **nome** foi configurado corretamente no Git, digite o comando:

```bash
git config user.name
```

5. Para configurar o seu **e-mail** no Git, digite o comando:

```bash
git config --global user.email "seu_email@email.com"
```

*Substitua seu_email, pelo seu e-mail cadastrado no Github. Exemplo: joao@email.com*

6. Para verificar se o seu **e-mail** foi configurado corretamente no Git, digite o comando:

```bash
git config user.email
```

7. Para configurar o **Editor de Código padrão** do Git, digite o comando:

**Configurar o VSCode:**

```bash
git config --global core.editor "code --wait"
```

**Caso o VSCode não esteja abrindo, utilize o comando abaixo, para atualizar o editor:**

```bash
git config --global --replace-all core.editor "code --wait"
```

8. Para verificar se o seu **Editor de Código** foi configurado corretamente no Git, digite o comando:

```bash
git config core.editor
```

9. Para configurar o **nome padrão da branch principal** do repositório Git, digite o comando:

```bash
git config --global init.defaultBranch main
```

> Esta configuração é importante para que todes os seus repositórios, a branch principal seja definida como **main**.

10. Para verificar se o **nome padrão da branch principal** foi configurado como main, digite o comando:

```bash
git config init.defaultBranch
```

11. Para listar todas as configurações do Git, digite o comando:

```bash
git config --list 
```

*Observe que desta vez será exibida uma lista com todas as configurações você fez no seu Git.*

12. Para utilizar a estratégia de mesclagem de repositórios padrão ao invés de usar a estratégia de mesclagem rebase, digite o comando:

```bash
git config --global pull.rebase false
```

*Como a estratégia rebase pode afetar os commits do repositório remoto de outros usuários, aumentando a probabilidade de conflitos, é recomendado utilizar a estratégia padrão. O comando acima desativa a estratégia rebase como estratégia padrão.*

<br />

<div align="left"><img src="https://i.imgur.com/fu9QxlT.png" title="source: imgur.com" width="25px"/> <a href="https://git-scm.com/docs/git-config/pt_BR" target="_blank"><b>Documentação: <i>Git Config</i></b></a></div>

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
