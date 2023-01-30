<h1>Terminal - Comandos para Redes de Computadores</h1>

1. Para visualizar o nome da sua máquina (Hostname), utilize o comando:

```bash
hostname
```

2. Para visualizar a lista de placas de rede e os respectivos Endereços IP, utilize o comando:

```bash
ipconfig
```

3. Para visualizar o Endereço MAC das placas de rede, utilize o comando:

```bash
arp -a
```

4. Para verificar se um computador está disponível em uma rede ou se um servidor está ativo, utilize o comando:

```bash
ping <endereço_destino>
```

**Exemplo 01 - Site na WEB:**

```bash
ping www.generation.org
```

*Para interromper o comando basta digitar **Ctrl + C**. Quando interromper o comando serão mostradas as estatísticas dos testes realizados.*

**Exemplo 02 - Sua máquina na rede:**

**Passo 01:** Visualize a lista de placas de rede do seu compuatdor, através do comando:

```bash
ipconfig
```

**Passo 02:** Identifique o endereço IP da sua máquina, como mostra a imagem abaixo (o IP está destacado em verde):

<div aling="center"><img src="https://i.imgur.com/XdKxwPv.png" title="source: imgur.com" /></div>

**Passo 03:** Execute o comando abaixo, indicando o endereço da sua placa de rede:

```bash
ping 192.168.0.114
```

Com o comando ping nós podemos medir o tempo de ida e volta (round time trip) que um pacote demora para ir do seu host para outro. Você pode usar tanto o endereço IP do host ou o endereço Web. Observe a imagem abaixo:

<div align="center"><img src="https://i.imgur.com/HUjguy3.png" title="source: imgur.com" /></div>

Observe que o tempo de resposta está excelente ( < 1ms) e nenhum pacote se perdeu.

**Endereços IP Privados**

A tabela de endereços abaixo, são exclusivos para uso interno, ou seja, sites da WEB não utilizam as faixas de endereço listadas na tabela abaixo:

| Nome            | Número de IPs | Faixa de **endereços** IP     |
| --------------- | ------------- | ----------------------------- |
| Classe A        | 16,777,216    | 10.0.0.0 – 10.255.255.255     |
| Classe B        | 1,048,576     | 172.16.0.0 – 172.31.255.255   |
| Classe C        | 65,536        | 192.168.0.0 – 192.168.255.255 |
| Classe Zeroconf | 65,536        | 169.254.0.0 – 169.254.255.255 |

5. Para visualizar os caminhos do seu host até um destino, utilize o comando:

```bash
tracert <endereço_destino>
```

**Exemplo:**

```bash
tracert www.uol.com.br
```

6. Para fazer o rastreamento das portas que são utilizadas no seu computador, utilize o comando:

```bash
netstat -s
```

7. Para visualizar a tabela de roteamento de um host, utilize o comando:

```bash
netstat -rn
```

<br /><br />

<div align="left"><a href="../README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>
