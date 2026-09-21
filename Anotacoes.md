# Anotações da disciplina

REVISAO PROVA 01

Diferença entre o modelo P2P e o modelo Cliente-Servidor -> No modelo P2P, cada user tem seu próprio Banco de Dados local e atua tanto como cliente quanto como servidor. No P2P, os computadores da rede podem solicitar e fornecer 
recursos, logo, cada máquina pode atuar como cliente e servidor. 

. Redes MANs não são projetadas para abranger grandes áreas geográficas (como continentes), mas sim para cidades. 
. Redes PANs abrangem dispositivos próximos a uma pessoa, como smartwatch + celular.
. A internet é formada pela conexão de milhares de redes diferentes, pertencentes a empresas, governos, etc.
. LANs normalmente abrangem ambientes pequenos, como casas, escolas e escritórios.

Exemplos práticos do uso de redes de computadores: 
1. Amazon vendendo um produto diretamente para um consumidor -> B2C (Business to Consumer).
2. Uma pessoa vendendo um celular usado para outra pessoa na OLX -> C2C (Consumer to Consumer).

O HFC (Hybrid Fiber-Coaxial) utiliza Fibra Óptica e cabos coaxiais para transimitir sinais.

. O modelo OSI tem 7 camadas, e a aplicação é a camada mais alta.
. O modelo TCP;IP possui 4 camadas com nomes diferetes das do OSI. 
. A interface define os serviços e primitivas que uma camada oferece para a camada imediatamente superior. 
. Um protocolo estabelece regras para a comunicação entre camadas pares, definindo como as mensagens são formatadas e interpretadas. 

Fibra Óptica vs Cabos de cobre (Pares Trançados)
1. Maior velocidade e largura da banda.
2. Maior distância e menor interferência.

Modos de comunicação:
. Simplex permite comunicação em apenas um direção (rádio)
. Half-duplex permite duas direções, mas uma por vez (walkie-talkie)
. Full-duplex permite duas direções ao mesmo tempo (ligação telefônica)

Teorema de Nyquist-Shannon
Ele determina a taxa mínima de amostragem necessária para representar e reconstruir corretamente um sinal, sendo essa taxa pelo menos duas vezes a maior frequência do sinal. Ou seja, a taxa de dados máxima (capacidade de transmissão) de um canall físico de comunicação.

. A fibra monomodo tem um núcleo menor que a multimodo, alcança distâncias maiores e geralmente tem custo menor. 
. O cabo coaxial tem boa blindagem, e em geral suporta maior largura de bandas que cabo de par trançado. 
. A fibra óptica funciona com base na reflexão total interna da luz dentro do núcleo. 

Reflextores: Fazem o sinal do wifi mudar de direção, criando vários caminhos para que ele chegue ao receptor. Esses sinais podem sofrer interferência entre si e se cancelar parcialmente, enfraquecendo o sinal.

A camada de ENLACE: 
. Enquadramento (frames) e adição de redundância
. Controle de fluxo
. Detecção e, em certos protocolos, correção de erros

Detecção de erros na camada de enlace:
. O CRC Cyclic Redundancy Check usa aritmética polinomial para verificar a integridade do quadro. 
. Na paridade par, se houver 3 bits 1, adiocionamos um bit 1, ficando com 4 bits 1, q é par.
. Esxquemas simples de bit de pariedade podem detectar erros em blocos, mas não conseguem detectar todos.
. O Checksum realiza operações de soma sobre os dados para gerar um valor de verificação de integridade. 

Ao encontrar cinco bits 1 consecutivos nos dados, a camada de enlace adiciona um bit 0 apos eles para evitar q a sequência seja confundida com a flag de delimitação. 

A camada de REDE:
. Roteamento entre redes

. ICMP é o protocolo q define o controle de erros e mensagens operacionais

. O serviço n orientado a conexões sem confirmacao pode ser usado em canais com baixa taxa de erros.
. Rede wifi sao mais suscetiveis a interferencias e colisoes, por isso usam confirmacoes ACKs para garantir a entrega de quadros.
. O servico orientado a conexoes com confirmacao estabelece uma conexão logica e busca entregar quadros em ordem, sem duplicacoes. 
. Em rede ethernet, usa-se servico orientado a conexoes. 

Enquadramento de rede por Contagem de Caracteres caso haja um erro de transmissão no primeiro byte (contador): o receptor calculará o tamanho do quadro incorretamente, causando a perda de sicronização e interpretar incorretamente os quadros seguintes. 

CRC calcula o resto de divisao para garantir q o quadro chegoou sem corrupçao. 

SERVICO DE REDES
Datagramas -> envia cada pacote individualmente, podendo seguir caminhos diferentes. 
Circuitos virtuais -> estabelecem uma conexão logica previa, logo os pacotes segguem um caminho definido. 

TTL time to live -> quantidade de hops um pacote tem ate ser descartado

PROTOCOLO IPv4
Ocupa 32 bits quando completo. 

2ⁿ − 2 === n = qtde de bits, resultado = qtde de hosts. 
O ipv4 tem 32 bits, para saber a mascara tem q fazer 32 - n (qtde bts), ai da /22, /24 etx






----------------------------------------------------

<pre>
192.168.23.54 - /28
- R: 192.168.23.48
- B: 192.168.23.63
- 
10.190.2.34 - /26
- R: 10.190.2.0
- B: 10.190.2.63
- 
200.3.120.222 - /29
- R: 200.3.120.216
- B: 200.3.120.223
- 
244.30.103.67 - /27
- R: 244.30.103.64
- B: 244.30.103.95
- 
172.0.21.17 - /28
- R: 172.0.21.16
- B: 172.0.21.31
- 
208.54.21.16 - /23
- R: 200.54.20.0
- B: 200.54.21.255  -> no .20 cabem 256 IP's e no 21 também, então seria como somar 256 + 256 que fecharia os 512 da /23 

/27 - Cabem 32 computadores nas /27
Mascarade de rede tm 32 bits, na 27 tirei 5 bits na host, 
192.168.25.0
</pre>

Camada de Enlace  
Camada de Rede    

Rede 
Broadcast

### Artigo IEEE
<pre>
Resumo
Introdução
  -> História
  -> Problema
  -> Forma como resolve
  -> Exemplo
Conclusão
Referências

Temas
  -> Protocolo aloha (original e sloted)
  -> Cssa 

REDE: é uma conexão entre vários pontos. 
Endereço de rede = primeiro ip
Endereço de broadkast = ultimo ip
  toda vez q tirar o bit dobra o valor de ips possiveis 

TOPOLOGIA: maneira em que a rede esta ligada
  - SÉRIE     :
  - BARRAMENTO:
  - ESTRELA   :

LAN: Local Area Network 
WAN: Wide  Area Network

SWITCH X HUB X ROTEADOR

Modelo OSI x TCP/IP:
</pre>
<img width="838" height="550" alt="image" src="https://github.com/user-attachments/assets/d77aaed3-5a6a-40c0-bc6b-986ee2fe0d5f" />

Atividade:
IP: 200.30.128.0 
255.255.248.0 - 8 salto.

LAB1(150 PC)

LAB2(500 PC)

LAB3(50 PC)

LAB4(1030 PC)

LAB5(15 PC)

Respostas: 

LAB1: Rede 200.30.130.0 — Broadcast 200.30.130.255

LAB2: Rede 200.30.128.0 — Broadcast 200.30.129.255

LAB3: Rede 200.30.131.0 — Broadcast 200.30.131.63

LAB5: Rede 200.30.131.64 — Broadcast 200.30.131.95

LAB4: não cabe na rede restante


