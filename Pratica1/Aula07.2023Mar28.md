# Aula TP - 28/Mar/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 11/Abr/23. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios - Parte IX: Criptografia aplicada

### 1\. Números aleatórios/pseudoaleatórios

#### Experiência 1.1

1. Execute o seguinte comando, que gera 1024 bytes pseudoaleatórios: `openssl rand -base64 1024`

2. Teste os seguintes comandos, que vão obter 1024 bytes pseudoaleatórios do sistema e os apresentam em base64:

- `head -c 32 /dev/random | openssl enc -base64`
- `head -c 64 /dev/random | openssl enc -base64`
- `head -c 1024 /dev/random | openssl enc -base64`
- `head -c 1024 /dev/urandom | openssl enc -base64`

Que conclusões pode tirar? Em que se baseia para essas conclusões ?

> **Nota:** Em kernels de Linux mais antigos, o `head -c 1024 /dev/random | openssl enc -base64` bloqueia até existir entropia suficiente.
>
> - Desde 2020, Linux kernel version 5.6 e superior, o /dev/random só bloqueia quando (ou enquanto) o CPRNG (_cryptographic pseudorandom number generator_) não foi inicializado. Após ter sido inicializado, o [/dev/random e /dev/urandom têm o mesmo comportamento](https://www.phoronix.com/scan.php?page=news_item&px=Linux-5.6-Random-Rework).
> - Discussão sobre a remoção do bloqueio ao /dev/random pode ser lida [aqui](https://lwn.net/Articles/808575/).

#### Experiência 1.2

**Nota:** Esta experiência é apenas para kernel Linux inferior ao 5.6. Nos que são posteriores, não notará nenhuma diferença pelo motivvo já indicado na experiência anterior.

O haveged - <http://www.issihosts.com/haveged/index.html> - é um daemon de entropia adaptado do algoritmo HAVEGE (_Hardware Volatile Entropy Gathering and Expansion_) - <http://www.irisa.fr/caps/projects/hipsor/> -.

Instale a package haveged na sua máquina com o seguinte comando: `sudo apt-get install haveged` (ou comando similar de instalação do seu _flavor_ Linux).

Teste novamente os seguintes comandos, que vão obter 1024 bytes pseudoaleatórios do sistema e os apresentam em base64:

- `head -c 1024 /dev/random | openssl enc -base64`
- `head -c 1024 /dev/urandom | openssl enc -base64`

Que conclusões pode tirar? Em que se baseia para essas conclusões ?

#### Experiência 1.3

O exemplo utilizando o _java.security.SecureRandom_ visto na aula, encontra-se na diretoria das aulas (Aula7/PseudoAleatorio), no ficheiro _RandomBytes.java_.

Analise, compile e execute este exemplo.

#### Pergunta P1.1

Na diretoria das aulas (Aula7/PseudoAleatorio) encontra o ficheiro _generateSecret-app.py_ baseado no módulo eVotUM.Cripto (<https://gitlab.com/eVotUM/Cripto-py>) - siga as instruções de instalação na [branch develop](https://gitlab.com/eVotUM/Cripto-py/-/tree/develop) que já é _compliant_ com o Python 3 -. Para instalar o módulo eVotUM.Cripto poderá efetuar o comando `git clone -b develop git@gitlab.com:eVotUM/Cripto-py.git`.

1. Analise e execute esse programa de geração de segredo aleatório e indique o motivo do output apenas conter letras e dígitos (não contendo por exemplo caracteres de pontuação ou outros).
2. O que teria de fazer para não limitar o output a vogais e dígitos? Altere o código.

### 2\. Partilha/Divisão de segredo (Secret Sharing/Splitting)

#### Experiência 2.1

O exemplo utilizando o _genSharedSecret.php_ visto na aula, encontra-se na diretoria das aulas (Aula7/SecretSharing), no ficheiro com o mesmo nome.

Analise e execute este exemplo. Verifique o que acontece se tentar reconstruir o segredo (_reconstroiSecret.php_) com mais ou menos componentes do que as esperadas.

#### Experiência 2.2

O exemplo utilizando o _shares.pl_ visto na aula, encontra-se na diretoria das aulas (Aula7/ShamirSharing), no ficheiro com o mesmo nome.

Analise e execute este exemplo. Verifique o que acontece se tentar reconstruir o segredo (_reconstruct.pl_) com mais ou menos componentes do que as esperadas.

#### Pergunta P2.1

Na diretoria das aulas (Aula7/ShamirSharing) encontra os ficheiros _createSharedSecret-app.py_, _recoverSecretFromComponents-app.py_ e _recoverSecretFromAllComponents-app.py_ baseado no módulo eVotUM.Cripto (<https://gitlab.com/eVotUM/Cripto-py>) - siga as instruções de instalação na [branch develop](https://gitlab.com/eVotUM/Cripto-py/-/tree/develop) que já é _compliant_ com o Python 3 -.

A. Analise e execute esses programas, indicando o que teve que efectuar para dividir o segredo "Agora temos um segredo extremamente confidencial" em 5 partes, com quorom de 3 para reconstruir o segredo, assim como posteriormente para o reconstruir.

Note que a utilização deste programa é ``python createSharedSecret-app.py number_of_shares quorum uid private-key.pem`` em que:

- number_of_shares - partes em que quer dividir o segredo
- quorum - número de partes necessárias para reconstruir o segredo
- uid - identificador do segredo (de modo a garantir que quando reconstruir o segredo, está a fornecer as partes do mesmo segredo)
- private-key.pem - chave privada, já que cada parte do segredo é devolvida num objeto JWT assinado, em base 64

B. Indique também qual a diferença entre _recoverSecretFromComponents-app.py_ e _recoverSecretFromAllComponents-app.py_, e em que situações poderá ser necessário utilizar _recoverSecretFromAllComponents-app.py_ em vez de _recoverSecretFromComponents-app.py_.

Nota: Relembre-se que a geração do par de chaves pode ser efetuada com o comando ``openssl genrsa -aes128 -out mykey.pem 1024``. O correspondente certificado pode ser gerado com o comando ``openssl req -key mykey.pem -new -x509 -days 365 -out mykey.crt``

### 3\. Authenticated Encryption

#### Pergunta 3.1

Utilizando o conhecimento de técnicas criptográficas, implemente um programa que permita

1. cifrar um ficheiro com uma técnica de _Authenticated encryption_;
2. validar um ficheiro que tenha sido cifrado com uma técnica de _Authenticated encryption_;
3. decifrar um ficheiro que tenha sido cifrado com uma técnica de _Authenticated encryption_.

A técnica de _Authenticated encryption_ a utilizar é a seguinte, consoante o número do seu grupo:

- Grupo 1 e 4 - EtM (Encrypt-then-MAC) em Java;
- Grupo 3 e 6 - EtM (Encrypt-then-MAC) em Python;
- Grupo 5 e 8 - E&M (Encrypt-and-MAC) em Java;
- Grupo 7 - E&M (Encrypt-and-MAC) em Python;
- Grupo 9 - MtE (MAC-then-Encrypt) em Java;
- Grupo 2 - MtE (MAC-then-Encrypt) em Python.

### 4\. Algoritmos e tamanhos de chaves

O site <https://eidas.ec.europa.eu/efda/tl-browser/#/screen/home> disponibiliza a lista de Entidades com serviços qualificados de confiança, de acordo com o Regulamento EU 910/2014 (eIDAS) - Regulamento de que falámos em aula anterior -.

Entre esses serviços encontra-se o serviço de emissão de certificados digitais qualificados para pessoa coletiva, designado por "QCert for ESeal".

#### Pergunta P4.1

Cada grupo indicado abaixo deve identificar os algoritmos e tamanhos de chave utilizados nos certificados das Entidades de Certificação (EC) que emitem certificados digitais qualificados, e verificar se são os mais adequados (e se não forem, propor os que considerar mais adequados):

- Grupo 1 - Austria, para a EC "e-commerce monitoring GmbH";
- Grupo 2 - Croácia, para a EC "Zagrebačka banka dioničko društvo";
- Grupo 3 - França, para a EC "Gendarmerie Nationale";
- Grupo 4 - Hungria, para a EC "NISZ National Infocommunications Services Company Limited by Shares";
- Grupo 5 - Itália, para a EC "Notartel S.p.A";
- Grupo 6 - Lituania, para a EC "State Enterprise Centre of Registers";
- Grupo 7 - Holanda, para a EC "Digidentity B.V.";
- Grupo 8 - Portugal, para a EC "CEGER - Centro de Gestão da Rede Informática do Governo";
- Grupo 9 - Eslovénia, para a EC "POŠTA SLOVENIJE d.o.o.".

Nota 1: Para Entidades de Certificação que já tenham vários certificados de EC, considere apenas o último certificado emitido.

Nota 2: Para obter o tamanho das chaves e algoritmos utilizados, deverá:

1. escolher o certificado da EC,
2. selecionar _Base 64-encoded_,
3. copiar o conteúdo do _Base 64-encoded_ e gravar em ficheiro (por ex., cert.crt),
4. inserir -----BEGIN CERTIFICATE----- no inicio do ficheiro,
5. inserir -----END CERTIFICATE----- no final do ficheiro,
6. executar o seguinte comando ``openssl x509 -in cert.crt -text -noout`` (substitua cert.crt pelo nome que deu ao ficheiro no passo 3.)

Nota 3: Na sua resposta inclua o resultado do comando ``openssl x509 -in cert.crt -text -noout``, referido na nota anterior.

### 5\. Assinaturas cegas (_Blind signatures_) baseadas no Elliptic Curve Discrete Logarithm Problem (ECDLP)

Para este ponto necessita de:

- Instalar o módulo eVotUM.Cripto a partir da [branch develop](https://gitlab.com/eVotUM/Cripto-py/-/tree/develop) - este _branch_ já é _compliant_ com o Python 3 -. Para o instalar poderá efetuar o comando `git clone -b develop git@gitlab.com:eVotUM/Cripto-py.git`.
- Copiar os ficheiros em [Aula7/BlindSignature](Aula7/BlindSignature) para a sua máquina.

Nota: A descrição detalhada da técnica de assinatura cega que é utilizada neste exercício encontra-se neste [paper](Aula7/ECDLP.blind_signature.pdf)

#### Experiência 5.1

Como estamos a falar em assinatura cega baseada em curvas elípticas, comecemos por gerar um par de chaves e certificado, utilizando o openssl.

Para isso, efetue os seguintes comandos:

- `openssl ecparam -name prime256v1 -genkey -noout -out key.pem`

  - gera o par de chaves para o ficheiro key.pem, utilizando uma curva elíptica do tipo prime256v1

- `openssl req -key key.pem -new -x509 -days 365 -out key.crt`

  - gera o certificado x509 com uma validade de 365 dias para o ficheiro key.crt

#### Experiência 5.2

Execute a assinatura cega, de acordo com as fases identificados na aula teórica (cf. slides 12 a 14 da aula teórica):

- Inicialização
- Ofuscação
- Assinatura
- Desofuscação
- Verificação

#### Pergunta P5.1

Como foi visto na aula teórica, a assinatura cega tem três participantes que participam em fases diferentes:

- Requerente - efetua a fase de ofuscação e desofuscação,
- Assinante - efetua a fase de Inicialização e Assinatura,
- Verificador - efetua a fase de Verificação.

Pretende-se que altere o código fornecido para a experiência 5.2, de forma a simplificar o input e output, do seguinte modo (pode adicionar outras opções, se assim o desejar):

- Assinante:

  - `init-app.py`

    - devolve o R' (i.e., pRDashComponents)

  - `init-app.py -init`

    - inicializa as várias componentes (InitComponents e pRDashComponents) e guarda-as (por exemplo, em ficheiro do assinante)

  - `blindSignature-app.py -key <chave privada> -bmsg <Blind message>`

    - devolve s (i.e., Blind Signature)

- Requerente:

  - `ofusca-app.py -msg <mensagem a assinar> -RDash <pRDashComponents>`

    - devolve m' (i.e., Blind message) e guarda as restantes componentes (Blind components e pRComponents) em ficheiro do requerente

  - `desofusca-app.py -s <Blind Signature> -RDash <pRDashComponents>`

    - devolve s' (i.e., Signature)

- Verificador:

  - `verify-app.py -cert <certificado do assinante> -msg <mensagem original a assinar> -sDash <Signature> -f <ficheiro do requerente>`

    - devolve informação sobre se a assinatura sDash sobre a mensagem msg é ou não válida.

### 6\. Criptografia homomórfica

#### Experiência 6.1

Utilize a biblioteca phe em python da criptografia homomórfica de Pallier (Partially homomorphic encryption) vista nas aulas teóricas, e efetue alguns exemplos.

#### Pergunta P6.1

Foi contratado para ajudar uma conhecida empresa de análises a guardar todos os dados das análises dos seus clientes em ambiente cloud.
O que a empresa pretende guardar é um ficheiro com a seguinte estrutura por cada linha: NIC do cliente, seguido de uma lista de tuplos (tipo de análise, valor). Por exemplo, uma linha pode ser: "123456789, (A23, 12,2), (B4, 32,1), (A2, 102), (CAA2, 34,5)". Adicionalmente foi-lhe indicado que poderá ser necessário obter a média de uma ou mais tipos de análise.

O seu trabalho é:

1. Indicar o modo mais adequado de guardar estes ficheiros em ambiente cloud;
2. Indicar o modo mais adequado de calcular as médias em ambiente cloud, sem que os dados sejam decifrados;
3. Desenvolver dois programas que permitam à empresa de análise testar, localmente, a solução que propõe.
