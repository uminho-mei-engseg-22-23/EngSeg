# Aula TP - 28/Fev/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 14/Mar/23. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios

### Parte III: Segurança da informação

#### Experiência III.1

Durante a aula teórica desta semana, no âmbito das cifras simétricas, falámos de vários tipos de _stream ciphers_ e, vários modos de operação das _block ciphers_.

Identifique e explique quais das propriedades de segurança é que são fornecidas por essas cifras.

### Parte IV: Cifras simétricas

#### IV.1 _Stream cipher_

##### Experiência IV.1.1

O RC4 já foi uma cifra muito utilizada, nomeadamente no âmbito dos protocolos SSL/TLS e WEP, mas desde 2003 foram sendo encontradas várias vulnerabilidades pelo que na prática já é hoje pouco utilizado.

1. Desenvolva, em python, uma aplicação linha de comando que utilize o RC4 para cifrar um ficheiro. No interface da linha de comando (CLI - _command line interface_) deve poder indicar o comprimento da chave (40, 56, 64, 80, 128, 192, ou 256 bits), a operação a efetuar (cifra/decifra), ficheiro de input e ficheiro de output.

2. Porque é que pode dizer que esta cifra não tem a propriedade de autenticidade?

##### Pergunta P.IV.1.1

O ChaCha20 é uma das duas cifras simétricas escolhidas para a encriptação dos novos protocolos de transporte, nomeadamente o TLS 1.3 (cf. [IETF RFC 8446](https://datatracker.ietf.org/doc/html/rfc8446)), embora a sua utilização seja opcional.

Desenvolva em python (utilizando a biblioteca [PyCryptodome](https://pycryptodome.readthedocs.io/en/latest/src/introduction.html)) uma aplicação linha de comando (CLI - _command line interface_) que utilize o Chacha20 para cifrar um ficheiro.

1. Indique o  tamanho do nonce que vai utilizar, conforme boas práticas definidas no [IETF RFC 7539](https://datatracker.ietf.org/doc/html/rfc7539).
2. A aplicação desenvolvida **só** pode obter os parâmteros necessários como argumentos da linha de comando. Por exemplo:

``chacha20 -operação chave input_file output_file``
> em que operação pode ser cifra ou decifra, chave é a chave a utilizar para a operação,
> input_file o ficheiro sobre o qual aplicar a operação, e output_file é o ficheiro resultante
> da aplicação da operação sobre input_file.

3. No caso de existir algum erro nos parâmetros ou com a execução da operação, a aplicação deverá fornecer uma mensagem adequada de erro.

#### IV.2 _Block cipher_

##### Pergunta P.IV.2.1

O AES é uma das duas cifras simétricas escolhidas para a encriptação dos novos protocolos de transporte, nomeadamente o TLS 1.3 (cf. [IETF RFC 8446](https://datatracker.ietf.org/doc/html/rfc8446)), sendo a sua utilização obrigatória, nomeadamente com tamanho de chave de 128 bits e no modo de operação GCM (i.e., AES-128-GCM).

O modo de operação GCM (_Galois Counter Mode_) é cada vez mais utilizado devido à sua performance, e combina o CTR (_Counter Mode_, visto na aula teórica) com a autenticação de Galois. O resultado do modo de operação GCM é uma sequência de bytes que contém o _IV_, _ciphertext_, e uma _authentication tag_ (utilizada para verificar a autenticação e integridade da restante sequência de bytes).

1. Desenvolva em java (utilizando os _providers_ do _Bouncy Castle_) uma aplicação linha de comando que utilize o AES-128-GCM (com IV de 12 bytes aleatório e diferente em cada utilização, e Tag de 128 bits) para cifrar um ficheiro.
2. A aplicação desenvolvida **só** pode obter os parâmteros necessários como argumentos da linha de comando. Por exemplo:

``aes -operação chave input_file output_file``
> em que operação pode ser cifra ou decifra, chave é a chave a utilizar para a operação,
> input_file o ficheiro sobre o qual aplicar a operação, e output_file é o ficheiro resultante
> da aplicação da operação sobre input_file.

3. No caso de existir algum erro nos parâmetros ou com a execução da operação, a aplicação deverá fornecer uma mensagem adequada de erro.

##### Experiência IV.2.1

Utilizando o openssl indique qual é o comando linha que utiliza para cifrar e decifrar um ficheiro com AES-256-CBC.
