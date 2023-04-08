# Aula TP - 11/Abr/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 26/Abr/23. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios - Parte X: Aplicações e protocolos

### 1\. Protocolo TLS

#### Experiência 1.1

Vá ao site [www.ssllabs.com](https://www.ssllabs.com/ssltest/) e efetue o _SSL Server test_ para o site do Governo Português (<https://www.portugal.gov.pt/>).

Analise o resultado.

#### Pergunta P1.1

Cada grupo indicado abaixo deve efetuar o teste _SSL Server test_ aos sites indicados (que têm de obrigatoriamente funcionar sobre HTTPS) e responder às respetivas perguntas:

- Grupo 1 - Escolha dois sites de Universidades Portuguesas.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. O que significa, para efeitos práticos, o "_Zombie POODLE_" indicado nos detalhes do protocolo?

- Grupo 2 - Escolha dois sites de Universidades Europeias, não Portuguesas.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. O que significa, para efeitos práticos, o "_BEAST attack_" indicado nos detalhes do protocolo?

- Grupo 3 - Escolha dois sites de Universidades não Europeias.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha visto a seguinte informação: "_DNS CAA_". O que significa, para efeitos práticos?

- Grupo 4 - Escolha dois sites de Ministérios do Governo Português.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_DROWN_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 5 - Escolha dois sites de Ministérios de Governos Europeus, não portugueses.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_GOLDENDOODLE_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 6 - Escolha dois sites de Ministérios de Governos não Europeus.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_POODLE (SSLv3)_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 7 - Escolha dois sites de Câmaras Municipais Portuguesas.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_Downgrade attack prevention_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 8 - Escolha dois sites de Bancos Portugueses (ou sites de Bancos estrangeiros em .pt).

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_Public Key Pinning (HPKP)_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 9 - Escolha dois sites de Bancos a operar na Europa (i.e., sites com domínios europeus, desde que não .pt).

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_Heartbleed (vulnerability)_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 10 - Escolha dois sites de Bancos a operar fora da Europa (i.e., sites com domínios não europeus).

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_Ticketbleed (vulnerability)_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 11 - Escolha dois sites de empresas não bancárias cotadas na Bolsa Portuguesa e pertencentes ao PSI 20.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_OpenSSL CCS vuln. (CVE-2014-0224)_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 12 - Escolha dois sites de empresas não bancárias e não portuguesas cotadas na Euronext.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_ROBOT (vulnerability)_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

- Grupo 13 - Escolha dois sites de empresas cotadas no NASDAQ.

  1. Anexe os resultados do _SSL Server test_ à sua resposta.
  2. Analise o resultado do _SSL Server test_ relativo ao site escolhido com pior rating. Que comentários pode fazer sobre a sua segurança. Porquê?
  3. É natural que tenha reparado na seguinte informação: "_OpenSSL Padding Oracle vuln. (CVE-2016-2107)_" na secção de detalhe do protocolo. O que significa, para efeitos práticos?

### 2\. Protocolo SSH

Para este ponto necessita de instalar o **ssh-audit** na sua máquina, devendo obtê-lo a partir de <https://github.com/jtesta/ssh-audit> ou através de `pip3 install ssh-audit`.

#### Experiência 2.1

Utilize o ssh-audit para efetuar um teste ao servidor gitlab.inesctec.pt, i.e.

> `ssh-audit gitlab.inesctec.pt`

Analise o resultado.

#### Pergunta P2.1

Cada grupo indicado abaixo deve utilizar o ssh-audit para efetuar teste aos sites indicados, que têm de obrigatoriamente ter o ssh (usualmente, na porta 22) ativo.

**Nota 1:** Para simplificar a resposta a esta pergunta deverá configurar uma conta em <https://www.shodan.io/>, já que após login pode fazer pesquisas fáceis sobre serviços disponíveis na Web. Por exemplo, para pesquisar por servidores ssh em Braga, poderá pesquisar por `port:22 country:pt city:braga`. Se quiser saber os servidores ssh da Universidade do Minho, pode pesquisar por `port:22 org:"Universidade do Minho"`.

**Nota 2:** Para pesquisar as vulnerabilidades de um produto software pode utilizar a pesquisa no site [CVE details](https://www.cvedetails.com/index.php), inserindo o nome do produto e a versão a pesquisar.

Cada Grupo deve escolher:

- Grupo 1 - Escolha dois servidores ssh de Universidades Portuguesas.
- Grupo 2 - Escolha dois servidores ssh de Universidades Europeias, não Portuguesas.
- Grupo 3 - Escolha dois servidores ssh de Universidades não Europeias.
- Grupo 4 - Escolha dois servidores ssh de empresas comerciais em Braga.
- Grupo 5 - Escolha dois servidores ssh de empresas comerciais no Porto.
- Grupo 6 - Escolha dois servidores ssh de empresas comerciais em Lisboa.
- Grupo 7 - Escolha dois servidores ssh de empresas comerciais em Madrid.
- Grupo 8 - Escolha dois servidores ssh de empresas comerciais em Paris.
- Grupo 9 - Escolha dois servidores ssh de empresas comerciais em Londres.
- Grupo 10 - Escolha dois servidores ssh de empresas comerciais em San Francisco.
- Grupo 11 - Escolha dois servidores ssh de empresas cotadas na Bolsa Portuguesa.
- Grupo 12 - Escolha dois servidores ssh de empresas não portuguesas cotadas na Euronext.
- Grupo 13 - Escolha dois servidores ssh de empresas cotadas no NASDAQ.

Responda aos seguintes pontos:

1. Anexe os resultados do ssh-audit à sua resposta.
2. Indique o software e versão utilizada pelos servidores ssh.
3. Qual dessas versões de software tem mais vulnerabilidades?
4. E qual tem a vulnerabilidade mais grave (de acordo com o _CVSS score_ identificado no CVE details)?
5. Para efeitos práticos, a vulnerabilidade indicada no ponto anterior é grave? Porquê?

### 3\. TOR (The Onion Router)

Para este ponto necessita de instalar o **tor**, **secure-delete**, **curl** e **anonsurf** na sua máquina ou (**preferencialmente**) numa máquina virtual Linux. Sugere-se que efetue a seguinte sequência de comandos (supondo máquina Debian Linux):

> `sudo apt-get install tor secure-delete curl`

> `git clone https://github.com/Und3rf10w/kali-anonsurf.git`

> `cd kali-anonsurf`

> `sudo ./installer.sh`

#### Experiência 3.1

Vamos utilizar o TOR (através do comando linha `anonsurf`) para mudarmos a nossa localização geográfica.

1. Abra o browser (o que tiver instalado na sua máquina) e vá a <https://iplocation.com/>

    - Aponte o seu endereço IP e localização (também o pode obter através do comando `sudo anonsurf myip`)

2. Na linha de comando execute `sudo anonsurf start`
3. Faça reload (shift-reload) da página web onde se encontrava

    - Aponte o seu endereço IP e localização (note que se não mudou, é porque existiu algum erro)

4. Na linha de comando execute `sudo anonsurf change`
5. Faça reload (shift-reload) da página web onde se encontrava

    - Aponte o seu endereço IP e localização (note que se não mudou, é porque existiu algum erro)

6. Na linha de comando execute `sudo anonsurf stop`
7. Faça reload (shift-reload) da página web onde se encontrava

    - Aponte o seu endereço IP e localização (note que se não é o inicial, é porque existiu algum erro)

#### Pergunta P3.1

Para aceder a alguns sites nos EUA tem que estar localizado nos EUA.

1. Efetuando o comando `sudo anonsurf start` consegue garantir que está localizado nos EUA?
2. Porquê? Utilize características do protocolo TOR para justificar.

#### Experiência 3.2

Vamos utilizar o "TOR Browser" para navegarmos anonimamente na rede. Para isso necessita de instalar o Browser TOR (veja como em <https://www.torproject.org/download/>).

Sugere-se que efetue a seguinte sequência de comandos:

A. No browser TOR aceda à página <https://www.theregister.com/2022/03/04/russia_splinternet_tor_rumours/>.
Clique no lado esquerdo da barra de URL (no cadeado) e verifique qual é o circuito para esse site.

B. Abra outro tab/pestana no browser TOR e aceda à página <https://www.cyberghostvpn.com/privacyhub/what-are-onion-sites/>. Clique no lado esquerdo da barra de URL e verifique qual é o circuito para esse site.

Tire as suas conclusões.

#### Pergunta P3.2

No seguimento da experiência anterior, aceda a <https://www.bbcweb3hytmzhn5d532owbu6oqadra5z3ar726vq5kgwwn6aucdccrad.onion/>, <http://ciadotgov4sjwlzihbbgxnqg3xiyrg7so2r2o3lt5wz5ypk4sxyjstad.onion> ou <https://www.facebookwkhpilnemxj7asaniu7vnjjbiltxjqhye3mhbshg7kx5tfyd.onion/>.

1. Clique no lado esquerdo da barra de URL (no símbolo do _onion_) e verifique qual é o circuito para esse site.

2. Porque existem 6 "saltos" até ao site Onion, sendo que 3 deles são "_relay_"? Utilize características do protocolo TOR para justificar.

3. Qual é o _Rendez-vous Point_?

### 4. Blockchain

#### Experiência 4.1

Neste exemplo siga o artigo [Building a blockchain](https://medium.com/@akshaykore/building-a-blockchain-7579c53962dd) e os vários passos indicados no mesmo.

Notas:

1. Se tiver que instalar o node.js e o npm numa máquina linux siga os passos indicados em <https://github.com/nodesource/distributions>.

2. O código em javascript encontra-se na diretoria [Aula8/koreCoin](Aula8/koreCoin), no ficheiro main.experiencia1.1.js .

#### Pergunta 4.1

Na experiência anterior, altere o método que cria o Genesis Block, de modo a que o timestamp seja a data do dia de hoje e o dado incluído nesse Bloco seja "Bloco inicial da koreCoin".

#### Pergunta 4.2

Na experiência anterior, adicione alguns blocos simulando várias transações em cada um deles.

#### Experiência 4.2

Neste exemplo siga o artigo [Let’s Build the Tiniest Blockchain in Less Than 50 Lines of Python](https://medium.com/crypto-currently/lets-build-the-tiniest-blockchain-e70965a248b) e os vários passos indicados no mesmo.

Nota:

1. O código em python encontra-se na diretoria [Aula8/snakeCoin](Aula8/snakeCoin), no ficheiro snakecoin.experiencia1.2.py .

#### Experiência 4.3 - Proof of Work Consensus Model

Esta experiência tem por base a Experiência 4.1.

Neste exemplo siga o artigo [Implementing a simple ‘proof of work’ algorithm for the Blockchain](https://cryptocurrencyhub.io/implementing-a-simple-proof-of-work-algorithm-for-the-blockchain-bdcd50faac18) e os vários passos indicados no mesmo.

Nota:

1. O código em javascript encontra-se na diretoria [Aula8/koreCoin](Aula8/koreCoin), no ficheiro main.experiencia2.1.js .

#### Pergunta 4.3

Na experiência anterior, altere a dificuldade de minerar para 2 e veja qual o tempo que demora, utilizando o comando time do Linux (ou similar no seu sistema operativo), por exemplo `time node main.experiencia2.1.js`.
Repita o exemplo para dificuldade de minerar 3, 4 e 5.

Apresente os tempos e conclua sobre os mesmos.

#### Experiência 4.4

Esta experiência tem por base a Experiência 4.2.

Neste exemplo siga o artigo [Let’s Make the Tiniest Blockchain Bigger - Part 2: With More Lines of Python](https://medium.com/crypto-currently/lets-make-the-tiniest-blockchain-bigger-ac360a328f4d) e os vários passos indicados no mesmo.

Nota:

1. Para instalar o flask numa máquina linux (debian ou similar) execute os seguintes comandos:

- `sudo apt-get install python-pip`
- `pip install flask`

2. O código em python encontra-se na diretoria [Aula8/snakeCoin](Aula8/snakeCoin), no ficheiro snakecoin-server.experiencia2.2.py .

3. Para arrancar com o servidor snakeCoin execute o seguinte comando: `python snakecoin-server.experiencia2.2.py &`

4. Para adicionar uma transação (pending transaction) na snakeCoin blockchain, execute o seguinte comando:
`curl "localhost:5000/txion"
     -H "Content-Type: application/json"
     -d '{"from": "akjflw", "to":"fjlakdj", "amount": 3}'`

5. Para minerar a transação (pending transaction), execute o seguinte comando:
`curl localhost:5000/mine`

#### Pergunta 4.4

1. Na experiência anterior, qual é o algoritmo de 'proof of work' ?
2. Parece-lhe um algoritmo adequado para minerar? Porquê?

#### Experiência 4.5 - Aprender a programa em Solidity

O Solidity é uma linguagem de programação orientada a objetos, utilizada para implementar _smart contracts_ em várias plataformas _blockchain_, entre as quais a Ethereum.

Pode aprender solidity e a desenvolver DApps fazendo os tutoriais em <https://cryptozombies.io/en/course/>.
