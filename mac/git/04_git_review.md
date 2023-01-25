<h1>Fluxo de Trabalho no Git - Prática</h1>


<h2>1. Configurando o Git Local</h2>

<h3>1.1. Criando repositório Central no Github</h3>


Vamos configurar o repositório Central no Github:

  1.  Acesse a Organização do projeto.

  2.  Clique na opção **Repositories**.

  3.  Na sequência, clique no botão **New**.

  4.  Crie um **Repositório Público**, chamado **revisao**.
<div align="center"><img src="https://i.imgur.com/Ctt17Fj.png" title="source: imgur.com" /></div>

5. Marque a opção **Add a README file** e clique no botão **Create repository**.

<div align="center"><img src="https://i.imgur.com/yerirgA.png" title="source: imgur.com" /></div>

<br />

<h3>1.2. Adicionando o Time no Repositório</h3>

Neste passo, vamos adicionar o time nos Repositórios do Projeto.

1. Na tela inicial do Repositório **revisao**, clique no link **Settings**.

<div align="center"><img src="https://i.imgur.com/9HH5L8Y.png" title="source: imgur.com" /></div>

2. Na próxima tela, no menu lateral do lado esquerdo da tela, clique na opção **Collaborators & teams**.

<div align="center"><img src="https://i.imgur.com/ovPFtJI.png" title="source: imgur.com" /></div>

3. Ainda nesta tela, clique no botão **Add teams**.

<div align="center"><img src="https://i.imgur.com/JEPc6NG.png?1" title="source: imgur.com" /></div>

4. Na próxima tela, selecione o **Time** e na opção **Choose role**, vamos deixar com **Administrador** (indicado em vermelho na imagem abaixo). Desta forma, todos os Integrantes do Grupo terão acesso total ao Repositório.

<div align="center"><img src="https://i.imgur.com/zsQkHaf.png" title="source: imgur.com" width="55%"/></div>

5. Clique no botão **Add** (botão verde), para concluir.

<h2>2. Atividade Prática</h2>

**Siga as instruções:**

1. Clone o repositório na sua máquina

```bash
git clone <endereço_do_repositório>
```

2. Crie uma Branch no seu Repositório local com o seu nome

```bash
git checkout -b <seu_nome>
```

3. Edite o arquivo **README.md** e adicione o seu nome

4. Execute os comando abaixo, para atualizar a sua Branch local

```bash
git add .

git commit -m "Meu nome"
```

5. Envie a sua Branch local para o Repositório remoto (revisao)

```bash
git push -u origin <seu_nome>
```

6. Após todes enviarem as suas respectivas Branches, atualize o seu repositório local e baixe a Branch remota de um membro do seu grupo no seu Repositório local. 

```bash
git fetch origin

git checkout --track -b <nome_branch> origin/<nome_branch>

git branch
```

7. Volte para a sua Branch local

```bash
git checkout <nome_branch_local>
```
8. Edite o arquivo **README.md** e adicione o seu sobrenome
9. Atualize a Branch local com o seu nome

```bash
git add .

git commit -m "Meu Sobrenome"
```

10. Volte para o Repositório remoto e acesse a sua Branch remota
11. Edite o arquivo **README.md** e adicione o nome da sua turma
12. Faça o Commit da atualização no Github, adicionando a mensagem: "Minha turma"
13. Execute o comando git pull na sua Branch local

```bash
git pull origin <nome_branch_local>
```

14. Será gerado um conflito. Resolva o conflito aceitando as duas alterações.
14. Atualize a sua Branch local 

```bash
git add .

git commit -m "Conflito resolvido"
```

16. Faça um merge entre a sua Branch e a Branch main

```bash
git checkout main

git merge <nome_branch_local>
```

17. Peça para um participante do grupo executa o comando git push

```bash
git push origin main
```

18. Na sequencia outro participante do grupo executa o comando git pull

```bash
git pull origin main
```

19. Será gerado um conflito. Resolva o conflito aceitando as duas alterações.

20. Atualize a Branch main remota, com os comandos abaixo:

```bash
git add .

git commit -m "Conflito resolvido - Seu nome"

git push origin main
```

21. Repita o processo a partir do passo 18 até que todes os integrantes do grupo tenham feito.

22. Ao finalizar, todes os integrantes do grupo, exceto o ultimo participante, farão o git pull para atualizar o repositório local.

```bash
git pull origin main
```

23. Execute o comando abaixo, para visualizar o histórico do Repositório:

```bash
git log
```

24. Para sair do git log, pressione a tecla **q** do seu teclado.
25. Envie um Print do Repositório no canal do Spring.


<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
