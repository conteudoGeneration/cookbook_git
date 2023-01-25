<h1>Comandos do Terminal</h1>



<h2>1. Comando pwd</h2>

Ao abrir o terminal, automaticamente o seu usuário é direcionado a algum pasta. Para saber qual é a sua localização atual, você poderá utilizar o comando **pwd**:

```bash
pwd
```



<h2>2. Comando clear</h2>

Limpa a tela do Terminal:

```bash
clear
```



<h2>3. Criando Pastas</h2>

O comando **mkdir** é utilizado para criar novas pastas.

**Sintaxe:**

```bash
mkdir nome_do_pasta
```

**Exemplo 01:**

Criar a pasta **primavera** na pasta do seu usuário:

```bash
mkdir primavera
```

**Exemplo 02:**

Criar as pastas **verao**, **outono** e **inverno** na pasta do seu usuário:

```bash
mkdir verao outono inverno python 
```

**Exemplo 03:**

Criar as pastas **verao/sol** e **inverno/frio** na pasta do seu usuário:

```bash
mkdir verao/sol inverno/frio 
```

 

<h2>4. Criando um Arquivo Vazio com o comando touch</h2>

O comando touch é utilizado para criar um ou mais arquivos vazios. 

**Sintaxe:**

```bash
touch nome_do_arquivo
```

**Exemplo 01:**

Criar o arquivo **verao.txt** na pasta do seu usuário:

```bash
touch primavera.txt
```

 **Exemplo 02:**

Criar o arquivo **verao.txt** na pasta do seu usuário:

```bash
touch verao.txt outono.txt inverno.txt python.txt django.txt
```

 **Exemplo 03:**

Criar os arquivos **java.txt** na pasta **verao/sol** e **portugol.txt** na pasta **inverno/frio**:

```bash
touch verao/sol/java.txt inverno/frio/portugol.txt
```

 

<h2>5. Listando arquivos e pastas</h2>

O comando **ls** é muito flexível e permite ao usuário listar arquivos e pastas de diversas maneiras.

**Sintaxe:**

```bash
ls <opções>
```

**Exemplos:**

Para listar os arquivos e pastas da sua pasta atual, digite o comando:

```bash
ls
```

Para listar todo o conteúdo da pasta atual, adicionando uma pasta e/ou arquivo em cada linha, digite o comando:

```bash
ls -1
```

Para listar todo o conteúdo da pasta atual, adicionando uma pasta e/ou arquivo em cada linha, exibindo as informações de cada arquivo e/ou pasta (permissões, dono, data de criação e/ou modificação, tamanho, entre outros), digite o comando:

```bash
ls -l
```

Para listar os detalhes da pasta atual, sem exibir o seu conteúdo, digite o comando:

```bash
ls -ld
```

Para listar os detalhes de uma determinada pasta, sem exibir o seu conteúdo, digite o comando:

```bash
ls -ld /dev
```

Para listar todo o conteúdo da pasta atual, incluindo os arquivos e pastas ocultas, digite o comando:

```bash
ls -a
```

> Um **arquivo ou pasta** é chamado de oculto, quando ele não é exibido pelo gerenciador de **arquivos**, mas ainda assim ele está na pasta. Para ocultar um **arquivo**, renomeie o arquivo adicionando um ponto "." no começo do seu nome. 
>
> **Exemplo:**
>
> **.ssh**

Para listar todo o conteúdo da pasta atual, exibindo o tamanho dos arquivos em Kb, Mb ou Tb, digite o comando:

```bash
ls -lh
```

Para listar apenas os arquivos do tipo **txt** salvos na pasta atual, digite o comando: 

```bash
ls *.txt
```

Para listar apenas os arquivos e pastas, cujo nome começam com a letra **p**, salvos na pasta atual, digite o comando: 

```bash
ls p*
```



<h2>6. Comando find</h2>

O comando **find** lista arquivos de acordo com o padrão enviado a ele.

**Exemplo:**

Listar todos os arquivos do tipo **txt**, que começam com a letra **p** na pasta do seu usuário:

```bash
find p*.txt
```



<h2>7. Editar arquivo de texto com o Nano</h2>

O comando **nano** abre um editor de textos, que permite editar o conteúdo dos arquivos **txt**.

**Exemplo:**

**Passo 01:** Edite o arquivo **primavera.txt** localizado na pasta do seu usuário:

```bash
nano primavera.txt
```

**Passo 02:** O arquivo **primavera.txt** (vazio), será aberto no Editor de Textos **Nano**, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/NH9FmEK.png" title="source: imgur.com" /></div>

**Passo 03:** Digite o texto: *A Primavera é a estação das flores!*, como mostra a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/s6N9jmm.png" title="source: imgur.com" /></div>

**Passo 04:** Para **Sair e Salvar o arquivo**, utilize o atalho **^ + x**. Na sequência pressione as teclas **y** e **enter** para confirmar, no Menu inferior do Nano, como mostra a figura abaixo:

<div align="center"><img src="https://i.imgur.com/dei4N4Y.png" title="source: imgur.com" /></div>

> O **^** é equivalente a tecla **control do teclado**.

<h2>8. Comando cat</h2>

O comando cat é utilizado para apresentar no terminal o conteúdo de um arquivo texto e pode ser utilizado em conjunto
com outros comandos.

**Exemplo:**

Exibir o conteudo do arquivo **primavera.txt**:

```bash
cat primavera.txt
```

Resultado do comando:

```bash
A primavera é a estação das flores!
```



<h2>9. Comando Grep</h2>

O comando grep pode ser utilizado para procurar padrões em arquivos texto. Ele pode ser utilizado sozinho ou em
conjunto com outros comandos.

**Exemplo cat + grep:**

Procurar a palavra **flores** se ela for encontrada dentro do conteudo do arquivo **primavera.txt**:

```bash
cat primavera.txt | grep flores
```

Resultado do comando:

<div align="left"><img src="https://i.imgur.com/OEFRUwT.png" title="source: imgur.com" /></div>

Observe que a palavra **flores** está destacada em vermelho.

| <img src="https://i.imgur.com/L338M2G.png" title="source: imgur.com" width="100px"/> | **DESAFIO:** *Edite o arquivo primavera.txt com o nano e adicione a palavra flores nas linhas abaixo. Adicione algumas iniciando com a letra maiúscula também. Execute o comando cat primavera.txt novamente e veja o resultado!* |
| ------------------------------------------------------------ | :----------------------------------------------------------- |



<h2>10. Navegar pelas pastas</h2>

O comando **cd** permite ao usuário acessar pastas (abrir) de diversas maneiras.

**Sintaxe:**

```bash
cd <opções>
```

**Exemplos:**

Para acessar a pasta **primavera**, digite o comando:

```bash
cd primavera
```

Para acessar a pasta raiz, o **/**, digite o comando:

```bash
cd /
```

Para acessar a pasta do usuário (home directory), utilize o comando:

```bash
cd ~
```

Para acessar uma pasta localizada dentro da pasta do usuário (primavera, por exemplo), utilize o comando:

```bash
cd ~/primavera
```

Para voltar para a pasta anterior a pasta primavera (no exemplo, a pasta do usuário), digite o comando:

```bash
cd ..
```



<h2>11. Copiar Arquivos</h2>

Para efetuar a cópia de um arquivo ou um grupo de arquivos e pastas inteiras, utilize o comando **cp**.

**Sintaxe:**

```bash
cp arquivo_original pasta_destino_da_cópia
```

**Exemplo:**

Copie o arquivo **primavera.txt** localizado na pasta do seu usuário, para a pasta **primavera**, também localizada na pasta do seu usuário:

```bash
cp primavera.txt ~/primavera/
```

Na sequência, digite o comando abaixo, para checar se o arquivo foi copiado:

```bash
ls primavera
```


| <img src="https://i.imgur.com/vVDBDG0.png" title="source: imgur.com" width="150px"/> | <div align="left"> **ALERTA DE BSM:** *Mantenha a Atenção aos Detalhes. A barra final no pasta de destino do comando cp é essencial. Caso não seja colocada, o sistema interpretará o último elemento do caminho de destino como sendo um nome de arquivo e não como um pasta.** </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |



<h2>12. Copiar Múltiplos Arquivos</h2>

Para efetuar a cópia de múltiplos arquivos, utilize o comando **cp**, indicando todos os arquivos que você deseja copiar, separados por espaço.

**Sintaxe:**

```bash
cp arquivo_original_1 arquivo_original_2 arquivo_original_3 pasta_destino_da_cópia
```

**Exemplo:**

Copie os arquivos **python.txt** localizado na pasta do seu usuário, para a pasta **inverno/frio**, também localizada na pasta do seu usuário:

```bash
cp verao.txt outono.txt inverno.txt ~/verao/sol/
```
Na sequência, digite o comando abaixo, para checar se o arquivo foi copiado:

```bash
ls verao/sol
```

| <img src="https://i.imgur.com/vVDBDG0.png" title="source: imgur.com" width="150px"/> | <div align="left"> **ALERTA DE BSM:** *Mantenha a Atenção aos Detalhes. A barra final no pasta de destino é essencial. Caso não seja colocada, o sistema interpretará o último elemento do caminho de destino como sendo um nome de arquivo e não como um pasta.** </div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |



<h2>13. Copiar Pastas e Sub-pastas</h2>

Para efetuar a cópia de pastas e os seus sub-pastas, inclusive os arquivos, utilize o comando **cp -r**.

**Sintaxe:**

```bash
cp -r /pasta_origem/ /pasta_destino/
```

**Exemplo:**

Copiar o pasta **~/documentos/generation/** no seu pasta **~/documentos/generation/temp**:

```bash
cp -r ~/verao/sol/ ~/inverno/frio/
```

Na sequência, digite o comando abaixo, para checar se o arquivo foi copiado:

```bash
ls inverno/frio
```

Observe que foi criada a pasta **sol**. Na sequência, digite o comando abaixo, para checar se todos os arquivos da pasta sol foram copiados:

```bash
ls inverno/frio/sol
```



<h2>14. Mover e Renomear Arquivos</h2>

Para mover e renomear um arquivo, utilize o comando **mv**, indicando o arquivo que você deseja mover.

**Sintaxe:**

```bash
mv arquivo_original pasta_destino
```

**Exemplo 01:**

Mover o arquivo **python.txt** localizado na pasta do seu usuário, para a pasta **python**, também localizada na pasta do seu usuário:

```bash
mv python.txt ~/python/
```

Na sequência, digite o comando abaixo, para checar se o arquivo **python.txt** foi movido:

```bash
ls
```

Observe que o arquivo **python.txt** não existe mais na pasta atual. Na sequência, digite o comando abaixo, para checar se o arquivo **python.txt** foi movido para a pasta **python**:

```bash
ls python
```

**Exemplo 02:**

Mover o arquivo **django.txt** localizado na pasta do seu usuário, para a pasta **python**, localizada na pasta do seu usuário,   renomeando o arquivo para **django_python.txt**:

```bash
mv django.txt ~/python/django_python.txt
```

Na sequência, digite o comando abaixo, para checar se o arquivo **django.txt** foi movido:

```bash
ls
```

Observe que o arquivo **django.txt** não existe mais na pasta atual. Na sequência, digite o comando abaixo, para checar se o arquivo **django.txt** foi movido para a pasta **python** e renomeado para **django_python.txt**:

```bash
ls python
```

**Exemplo 03:**

Renomear o arquivo **primavera.txt** localizado na pasta do seu usuário, para **primavera_chegou.txt**:

```bash
mv primavera.txt primavera_chegou.txt
```

Na sequência, digite o comando abaixo, para checar se o arquivo **primavera.txt** foi renomeado para **primavera_chegou.txt**:

```bash
ls
```



<h2>15. Apagando Arquivos</h2>

O comando **rm** é utilizado para apagar um ou mais arquivos. 

**Sintaxe:**

```bash
rm nome_do_arquivo
```

**Exemplo 01:**

Apagar o arquivo **primavera_chegou.txt** localizado na pasta do seu usuário:

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



<h2>16. Apagando Pastas</h2>

Os comandos **rm -Rf** e **rmdir** são utilizados para apagar pastas. A diferença é que o primeiro apaga todo o conteúdo da pasta (incluindo as subpastas), enquanto o segundo exige que a pasta esteja vazia.

**Sintaxe:**

```bash
rm -Rf nome_do_pasta
```

```bash
rmdir nome_do_pasta
```

**Exemplo 01:**

Apagar a pasta **inverno** localizada na pasta do seu usuário:

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

Apagar a pasta **python** localizada na pasta do seu usuário:

```bash
rmdir python
```

Na sequência, digite o comando abaixo, para checar se a pasta **python** foi apagada:

```bash
ls
```

No exemplo acima, o comando **rmdir** funcionou, porque a pasta **python** está vazia.

<br />

<h2>17. Comando date</h2>

Para ver a data e a hora do sistema, utilize o comando **date**:

```bash
date
```

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
