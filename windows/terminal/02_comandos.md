<h1>Comandos do Terminal</h1>



Antes de iniciarmos a sessão prática, siga as instruções abaixo:

1. Localize através do Menu Iniciar do Windows, o **Terminal - Prompt de Comando (CMD)**, como mostra a imagem abaixo: 

<div align="center"><img src="https://i.imgur.com/hHafDiQ.png" title="source: imgur.com" width="90%"/></div>

2. Abra o **Terminal - Prompt de Comando (CMD)**. Será aberta a janela abaixo:

<div align="center"><img src="https://i.imgur.com/1FB25fg.png" title="source: imgur.com" width="90%"/></div>

3. Observe que o Prompt de comando do terminal, indicará que você está na sua pasta pessoal (Home Directory), como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/RdZ4TJe.png" title="source: imgur.com" width="90%"/></div>

4. Na sequência, crie uma pasta chamada **aula_terminal**, na pasta **aula_terminal**, através do comando:

```bash
md aula_terminal
```

5. Acesse a pasta **aula_terminal**, através do comando:

```bash
cd aula_terminal
```

A maioria dos comandos, a partir deste ponto, serão executados dentro desta pasta.

<br />


<h2>1. Identificar a pasta atual</h2>

Ao abrir o Terminal CMD ou o Terminal PowerShell, automaticamente o prompt de comando indica a pasta atual. De qualquer forma, você pode utilizar o comando abaixo, para identificar a sua pasta atual: 

```bash
echo %cd%
```

<br />

<h2>2. Mostrar a data atual</h2>

Para ver a data do dia no Terminal, utilize o comando: 

```bash
date
```

Depois de executar este comando, será solicitada a alteração da data do sistema. Pressione **enter** para cancelar a alteração.

<br />

<h2>3. Mostrar a hora atual</h2>

Para ver a hora no Terminal, utilize o comando: 

```bash
time
```

Depois de executar este comando, será solicitada a alteração da hora do sistema. Pressione **enter** para cancelar a alteração.

<br />

<h2>4. Limpar a tela</h2>

Para limpar a tela do Terminal, utilize o comando: 

```bash
cls
```


<br />

<h2>5. Criar Pastas</h2>

Para criar novas pastas, utilize o comando: 

**Sintaxe:**

```bash
md nome_da_pasta
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 01:**

Criar a pasta **primavera** na pasta **aula_git**: 

```bash
md primavera
```


<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 02:**

Criar as pastas **verao**, **outono** e **inverno** na pasta **aula_git**: 

```bash
md verao outono inverno python 
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 03:**

Criar as pastas **sol** dentro da pasta **verao** e **frio** dentro da pasta **inverno**: 

```bash
md verao/sol & md inverno/frio
```

O operador **&** (E lógico), inserido entre 2 comandos, permite executar os 2 comandos de uma única vez. No exemplo acima, estamos executando 2 comandos. 

<br />

<h2>6. Navegar pelas pastas</h2>

O comando **cd** permite ao usuário acessar pastas (abrir) de diversas maneiras.

**Sintaxe:**


```bash
cd <opções>
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 01:**

Para acessar a pasta **primavera**, digite o comando: 

```bash
cd primavera
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 02:**

Para acessar a unidade principal (diretório raiz - C:), digite o comando: 

```bash
cd /
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 03:**

Para acessar a pasta do usuário (home directory), utilize o comando: 

```bash
cd %USERPROFILE%
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 04:**

Para acessar uma pasta localizada dentro da pasta do usuário (primavera, por exemplo), utilize o comando: 

```bash
cd %USERPROFILE%/aula_terminal/primavera
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 05:**

Para voltar para a pasta anterior a pasta primavera (no exemplo, a pasta **aula_terminal**), digite o comando: 

```bash
cd ..
```

<br />

<h2>7. Criando um Arquivo de texto</h2>

O comando **notepad (Bloco de Notas)** é utilizado para criar um arquivo de texto. 

**Sintaxe:**


```bash
notepad nome_do_arquivo
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 01:**

Criar o arquivo **verao.txt** na pasta **aula_git**: 

```bash
notepad primavera.txt
```

Depois de executar o comando acima, será aberto o Bloco de Notas (Notepad)  do Windows, perguntando se você deseja criar o arquivo, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/5Uz43m3.png" title="source: imgur.com" /></div>

Clique no botão **Sim**, para criar o arquivo. Na sequência, feche o arquivo.

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 02:**

Criar os arquivos **verao.txt, outono.txt, inverno.txt, python.txt e django.txt** na pasta **aula_git**: 

```bash
notepad verao.txt 
notepad outono.txt
notepad inverno.txt
notepad python.txt
notepad django.txt
```

Cada arquivo deve ser criado individualmente.

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 03:**

Criar os arquivos **java.txt** na pasta **verao\sol** e **sql.txt** na pasta **inverno\frio**: 

```bash
notepad verao\sol\java.txt
notepad inverno\frio\sql.txt
```

Cada arquivo deve ser criado individualmente. 

<br />

<h2>8. Listando arquivos e pastas</h2>

O comando **dir** é muito flexível e permite ao usuário listar arquivos e pastas de diversas maneiras.

 **Sintaxe:**

```bash
dir <opções>
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplos:**

Para listar os arquivos e pastas da sua pasta atual, digite o comando:

```bash
dir
```

 <br />

Para listar todas as pastas e arquivos organizados em uma visualização horizontal, digite o comando:

```bash
dir /w
```

 <br />

Para listar apenas os nomes dos arquivos, digite o comando:

```bash
dir /b
```

 <br />

Para listar todas as pastas com pausas, quando a quantidade de arquivos é grande o suficiente para que não possa ser exibida de uma só vez na tela, digite o comando:

```bash
dir /p
```

 <br />

Para listar o conteúdo de todas as pastas e subpastas, digite o comando:

```bash
dir /s
```

 <br />

Para listar apenas os arquivos do tipo **txt** salvos na pasta atual, digite o comando: 

```bash
dir *.txt
```

 <br />

Para listar apenas os arquivos e pastas, cujo nome começam com a letra **p**, salvos na pasta atual, digite o comando: 

```bash
dir p*
```

 <br />

Para listar os arquivos da pasta verao e suas subapastas, digite o comando: 

```bash
dir verao /s
```

 <br />

<h2>9. Obter ajuda</h2>

Para obter ajuda sobre qualquer comando, utilize a opção **/?**, como mostra o exemplo abaixo: 

 **Sintaxe:**

```bash
comando /?
```

 <br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo:**

Obter ajuda para o comando **dir**:

```bash
dir /?
```

Para descobrir a versão do Windows, digite o comando:  


```bash
ver
```

 <br />

<h2>10. Editar arquivo de texto com o Notepad</h2>

O comando **notepad**, além de criar um arquivo txt, ele também abre o arquivo no Bloco de Notas do Windows para edição, que permite alterar o conteúdo dos arquivos **txt**.

 **Sintaxe:**

```bash
notepad nome_do_arquivo.txt
```

 <br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo:**

**Passo 01:** Edite o arquivo **primavera.txt** localizado na pasta **aula_terminal**:

```bash
notepad primavera.txt
```

**Passo 02:** O arquivo **primavera.txt** (vazio), será aberto no **Bloco de Notas**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/hA7lwBd.png" title="source: imgur.com" width="90%"/></div>

**Passo 03:** Digite o texto: *Primavera! Muitas Flores!*, como mostra a imagem abaixo:

<div align="center"><img src="https://imgur.com/I39wRZ5.png" title="source: imgur.com" width="90%"/></div>

**Passo 04:** Salve e feche o arquivo.

<br />

<h2>11. Comando type</h2>

O comando **type** é utilizado para apresentar no terminal o conteúdo de um arquivo texto.

 **Sintaxe:**

```bash
type nome_do_arquivo
```

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo:**

Exibir o conteúdo do arquivo **primavera.txt**:

```bash
type primavera.txt
```

Resultado do comando:

```bash
Primavera! Muitas Flores!
```

<br />

<h2>12. Copiar Arquivos</h2>

Para efetuar a cópia de um arquivo ou um grupo de arquivos e pastas inteiras, utilize o comando **copy**.

**Sintaxe:**

```bash
copy arquivo_original pasta_destino_da_cópia
```

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 01:**

Copie o arquivo **primavera.txt** localizado na pasta **aula_terminal**, para a pasta **primavera**, também localizada na pasta  **aula_terminal**:

```bash
copy primavera.txt primavera
```

Na sequência, digite o comando abaixo, para checar se o arquivo foi copiado:

```bash
dir primavera
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 02:**

Copie o arquivo **primavera.txt** localizado na pasta **aula_terminal**, para a pasta **verao/sol**, também localizada na pasta  **aula_terminal**:

```bash
copy primavera.txt verao\sol
```

Na sequência, digite o comando abaixo, para checar se o arquivo foi copiado:

```bash
dir verao /s
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 03:**

Criar uma cópia do arquivo **primavera.txt** dentro da pasta **aula_terminal**. A cópia será criada com o nome **primavera_2023.txt**:

```bash
copy primavera.txt primavera_2023.txt
```

Na sequência, digite o comando abaixo, para checar se o arquivo foi copiado:

```bash
dir
```

<br />

<h2>13. Copiar Múltiplos Arquivos</h2>

Para efetuar a cópia de múltiplos arquivos, utilize o comando **copy**, indicando todos os arquivos que você deseja copiar, separados por espaço.

**Sintaxe:**

```bash
copy critério pasta_destino_da_cópia
```

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo:**

Copie todos os arquivos **.txt** localizados na pasta **aula_terminal**, para a pasta **inverno/frio**, também localizada na pasta **aula_terminal**:

```bash
copy *.txt inverno\frio
```
Na sequência, digite o comando abaixo, para checar se o arquivo foi copiado:

```bash
dir inverno /s
```

<br />

<h2>14. Copiar Pastas e Sub-pastas</h2>

Para efetuar a cópia de pastas e os seus sub-pastas, inclusive os arquivos, utilize o comando **xcopy**.

**Sintaxe:**

```bash
xcopy <opções> pasta_origem pasta_destino
```

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo:**

Crie uma nova pasta chamada **java**:

```bash
md java
```

Copie todos os arquivos e subpastas da pasta **inverno** na pasta **java**:

```bash
xcopy /e inverno java
```

*A opção **/e** copia todas as subpastas, inclusive as pastas vazias.*

Na sequência, digite o comando abaixo, para checar se os arquivos e as pastas foram copiados:

```bash
dir java /s
```

Observe que foi criada uma cópia da pasta **frio**, dentro da pasta java, com todos os seus arquivos.

<br />

<h2>15. Renomear arquivos e pastas</h2>

Para renomear um arquivo, utilize o comando **ren**, indicando o arquivo que você deseja renomear e o seu novo nome.

**Sintaxe:**

**Arquivo:**

```bash
ren arquivo_original novo_nome
```

**Pasta:**

```bash
ren pasta_original novo_nome
```

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 01:**

Renomear o arquivo **primavera_2023.txt** localizado na pasta **aula_terminal**, para **primavera_chegou.txt**:

```bash
ren primavera_2023.txt primavera_chegou.txt
```

Na sequência, digite o comando abaixo, para checar se o arquivo **primavera.txt** foi renomeado para **primavera_chegou.txt**:

```bash
dir
```

<br />

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 02:**

Renomear a pasta **java** localizada na pasta **aula_terminal**, para **java_2023**:

```bash
ren java java_2023
```

Na sequência, digite o comando abaixo, para checar se a pasta **java** foi renomeada para **java_2023**:

```bash
dir
```

<br />

<h2>16. Mover arquivos e pastas</h2>

Para mover um arquivo para outra pasta, utilize o comando **move**, indicando o arquivo que você deseja mover.

**Sintaxe:**

**Arquivo:**

```bash
move nome_do_arquivo pasta_destino
```

**Pasta:**

```bash
ren nome_da_pasta pasta_destino
```

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 01:**

Mover o arquivo **python.txt** localizado na pasta **aula_terminal**, para a pasta **python**, também localizada na pasta **aula_terminal**:

```bash
move python.txt python
```

Na sequência, digite o comando abaixo, para checar se o arquivo **python.txt** foi movido:

```bash
dir
```

Observe que o arquivo **python.txt** não existe mais na pasta atual. Na sequência, digite o comando abaixo, para checar se o arquivo **python.txt** foi movido para a pasta **python**:

```bash
dir python
```

<img src="https://i.imgur.com/4kDRTbu.png" title="source: imgur.com" width="3%"/>**Exemplo 02:**

Crie uma nova pasta chamada **linguagens**:

```bash
md linguagens
```

Mova a pasta **python**, localizada na pasta **aula_terminal**, para a pasta **linguagens**:

```bash
move python linguagens
```

Na sequência, digite o comando abaixo, para checar se a pasta **python** foi movida:

```bash
dir
```

Observe que a pasta **python** não existe mais na pasta atual. Na sequência, digite o comando abaixo, para checar se a pasta **python** foi movida para a pasta **linguagens**:

```bash
dir linguagens
```

<br />

<h2>17. Apagando Arquivos</h2>

O comando **rm** é utilizado para apagar um ou mais arquivos. 

**Sintaxe:**

```bash
rm nome_do_arquivo
```

**Exemplo 01:**

Apagar o arquivo **primavera_chegou.txt** localizado na pasta **aula_terminal**:

```bash
rm primavera_chegou.txt
```

Na sequência, digite o comando abaixo, para checar se o arquivo **primavera_chegou.txt** foi apagado:

```bash
ls
```

**Exemplo 02:**

Apagar todos os arquivos **.txt** da pasta **python**:

```bash
rm ~/python/*.txt
```

| <img src="https://i.imgur.com/vVDBDG0.png" title="source: imgur.com" width="150px"/> | <div align="left"> **ALERTA DE BSM:** *Mantenha a Atenção aos Detalhes. Observe no exemplo acima que o caminho da pasta veio antes do tipo do arquivo, porque estamos fora da pasta python.** </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

Na sequência, digite o comando abaixo, para checar se todos os arquivos **.txt** da pasta **python** foram apagados:

```bash
ls python
```



<h2>18. Apagando Pastas</h2>

Os comandos **rm -Rf** e **rmdir** são utilizados para apagar pastas. A diferença é que o primeiro apaga todo o conteúdo da pasta (incluindo as subpastas), enquanto o segundo exige que a pasta esteja vazia.

**Sintaxe:**

```bash
rm -Rf nome_do_pasta
```

```bash
rmdir nome_do_pasta
```

**Exemplo 01:**

Apagar a pasta **inverno** localizada na pasta **aula_terminal**:

Experimente apagar a pasta com o comando **rmdir**:

```bash
rmdir inverno
```

Será exibida a mensagem abaixo, indicando que a pasta **inverno** não pode ser apagada porquê não está vazia

<div align="left"><img src="https://i.imgur.com/NuxbQKT.png" title="source: imgur.com" /></div>

Experimente apagar a pasta com o comando **rm -Rf**:

```bash
rm -Rf inverno
```

Na sequência, digite o comando abaixo, para checar se a pasta **inverno** foi apagada:

```bash
ls
```

Observe que desta vez a pasta **inverno** e todo o seu conteúdo foi apagado.

**Exemplo 02:**

Apagar a pasta **python** localizada na pasta **aula_terminal**:

```bash
rmdir python
```

Na sequência, digite o comando abaixo, para checar se a pasta **python** foi apagada:

```bash
ls
```

No exemplo acima, o comando **rmdir** funcionou, porque a pasta **python** está vazia.

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
