# Avaliação prática 2 - Projeto de desenvolvimento 1 (PD1)

De seguida são apresentados os vários projetos para consolidação dos conceitos básicos de criptografia. O relatório final e o código fonte deverá ser colocado na área do Grupo no github até ao dia 24/04/2023, na subdiretoria "AP2-PD1" (**Note que no relatório tem de indicar os passos necessários para se poder testar o código fonte, incluindo o ambiente (que se espera que seja preferencialmente Linux)**).
A apresentação e discussão do trabalho será posteriormente marcada em data/hora a indicar.

## 1. Data e horário de apresentação do trabalho

Data: A indicar

+ Grupo 1 -
+ Grupo 2 -
+ Grupo 3 -
+ Grupo 4 -
+ Grupo 5 -
+ Grupo 6 -
+ Grupo 7 -
+ Grupo 8 -
+ Grupo 9 -
+ Grupo 10 -
+ Grupo 11 -
+ Grupo 12 -
+ Grupo 13 -
+ Grupo 14 -

## 2. Avaliação do PD1

A avaliação do PD1 será efetuada entre 0 e 20 valores. Quem entregar antes da data limite tem uma valorização de 1% na sua nota por cada dia de antecipação.

### 2.1 Grupos com mais de 3 alunos

Os grupos com mais de 3 alunos devem apresentar no seu relatório, as funcionalidades/componentes/outros que efetuaram para além do que lhes era pedido no enunciado.

----

## 3. Projeto

Tal como referido no Projeto de Análise de um tema ([PA](PA.md)), nesta UC todos os trabalhos da parte *Prática 2* irão estar relacionados direta ou indiretamente com a EUDIW.

### 3.1. Projetos com utilização de HSM (Hardware Security Module)

O HSM (*Hardware Security Module*) é um dispositivo físico que atua como um cofre eletrónico para proteger chaves criptográficas e outros dados sensíveis, sendo normalmente credenciados de acordo com standards de segurança, como os definidos pelo FIPS (e.g., FIPS 140-2 Level 3) ou pelo *Common Criteria* (e.g., CC *Evaluation Assurance Level* 4+ com *Protection Profile* EN 419 221-5 “*Cryptographic Module for Trust Services*”).

Os HSMs são usados em diversas aplicações que exigem a mais alta segurança, onde se inclui o ecossistema EUDIW, em que serão utilizados para várias funções de segurança:

+ geração de chaves criptográficas;
+ armazenamento seguro de chaves e dados sensíveis;
+ geração de números aleatórios seguros e criptograficamente fortes;
+ garantia de integridade dos dados armazenados e processados;
+ realização de funções criptográficas em tempo real e em grande escala;
+ gestão de várias chaves criptográficas e políticas de segurança.

A comunicação com um HSM efetua-se usualmente através de uma API PKCS#11, que permite aceder às funções criptográficas disponibilizadas pelo HSM (sendo as mais comuns a geração de chaves, assinatura digital, cifra, e decifra). Esta interface/API PKCS#11 tem ainda a vantagem de fornecer uma camada de abstração que permite que as aplicações comuniquem com diferentes dispositivos criptográficos, incluindo HSMs, sem a necessidade de conhecer detalhes de implementação de cada dispositivo.

Neste projeto, o objetivo é desenvolver uma aplicação de comando linha (CLI - *command line interface*) que permita utilizar as funcionalidades criptográficas do seu HSM, em especial:

+ a criação de par de chaves, utilizando algoritmos RSA e curvas elípticas,
+ a criação de chaves simétricas,
+ a assinatura, cifra, decifra e verificação de assinatura com par de chaves,
+ a cifra e decifra com chaves simétricas,
+ a listagem das chaves existentes no HSM.

Note que a chave privada e a chave simétrica nunca podem sair do HSM.

Sugere-se a utilização da interface Java para PKCS#11, jacknji11, que pode encontrar em <https://github.com/joelhockey/jacknji11> ou <https://github.com/devisefutures/jacknji11>

#### 3.1.1 Grupo 4

O Grupo 1 efetuará este projecto recorrendo ao emulador de HSM [SoftHSM v2](https://github.com/opendnssec/SoftHSMv2), disponibilizando a seguinte funcionalidade mínima:

+ a criação de par de chaves, utilizando algoritmos RSA;
+ a criação de chaves simétricas, utilizando algoritmo AES;
+ a assinatura, cifra, decifra e verificação de assinatura com par de chaves,
+ a cifra e decifra com chaves simétricas,
+ a listagem das chaves existentes no HSM.

#### 3.1.2 Grupo 3

O Grupo 1 efetuará este projecto recorrendo ao emulador de HSM Utimaco HSM simulator. O simulador pode ser obtido gratuitamente a partir de <https://support.hsm.utimaco.com/hsm-simulator>, disponibilizando a seguinte funcionalidade mínima:

+ a criação de par de chaves, utilizando algoritmos RSA;
+ a criação de chaves simétricas, utilizando algoritmo AES;
+ a assinatura, cifra, decifra e verificação de assinatura com par de chaves,
+ a cifra e decifra com chaves simétricas,
+ a listagem das chaves existentes no HSM.

#### 3.1.3 Grupo 5

O Grupo 1 efetuará este projecto recorrendo ao emulador de HSM [SoftHSM v2](https://github.com/opendnssec/SoftHSMv2), disponibilizando a seguinte funcionalidade mínima:

+ a criação de par de chaves, utilizando algoritmos ECDSA;
+ a criação de chaves simétricas, utilizando algoritmo Triple-DES (3DES);
+ a assinatura, cifra, decifra e verificação de assinatura com par de chaves,
+ a cifra e decifra com chaves simétricas,
+ a listagem das chaves existentes no HSM.

#### 3.1.4 Grupo 9

O Grupo 1 efetuará este projecto recorrendo ao emulador de HSM Utimaco HSM simulator. O simulador pode ser obtido gratuitamente a partir de <https://support.hsm.utimaco.com/hsm-simulator>, disponibilizando a seguinte funcionalidade mínima:

+ a criação de par de chaves, utilizando algoritmos ECDSA;
+ a criação de chaves simétricas, utilizando algoritmo Triple-DES (3DES);
+ a assinatura, cifra, decifra e verificação de assinatura com par de chaves,
+ a cifra e decifra com chaves simétricas,
+ a listagem das chaves existentes no HSM..

### 3.2. Projetos de criação de dados do tipo 1 (cf. ARF)

O EUDIW ARF indica que os dados do tipo 1 devem ser criados nos formatos a seguir identificados:

+ VC em JSON e JWT
+ ISO 18013-5:2021 em CBOR

#### 3.2.1 Grupo 2

Proponha estrutura de dados para PID, de acordo com os requisitos do ARF, e através de uma aplicação de comando linha (CLI - *command line interface*):

+ crie PID no formato VC em JSON e JWT;
+ valide PID criados no formato VC em JSON e JWT.

#### 3.2.2 Grupo 1

Proponha estrutura de dados para PID, de acordo com os requisitos do ARF, e através de uma aplicação de comando linha (CLI - *command line interface*):

+ crie PID no formato ISO 18013-5:2021 em CBOR;
+ valide PID criados no formato ISO 18013-5:2021 em CBOR.

### 3.3. Projetos de criação de dados do tipo 2 (cf. ARF)

O EUDIW ARF indica que os dados do tipo 2 devem ser criados nos formatos a seguir identificados:

+ JSON/JSON-LD + JWT
+ JSON-LD + LD-Proofs
+ ISO 18013-5:2021 em CBOR

#### 3.3.1 Grupo 6

Proponha estrutura de dados para EAA, de acordo com os requisitos do ARF, e através de uma aplicação de comando linha (CLI - *command line interface*):

+ crie EAA no formato JSON/JSON-LD + JWT;
+ valide EAA criados no formato JSON/JSON-LD + JWT.

#### 3.3.2 Grupo 7

Proponha estrutura de dados para EAA, de acordo com os requisitos do ARF, e através de uma aplicação de comando linha (CLI - *command line interface*):

+ crie EAA no formato JSON-LD + LD-Proofs;
+ valide EAA criados no formato JSON-LD + LD-Proofs.

#### 3.3.3 Grupo 8

Proponha estrutura de dados para EAA, de acordo com os requisitos do ARF, e através de uma aplicação de comando linha (CLI - *command line interface*):

+ crie EAA no formato ISO 18013-5:2021 em CBOR;
+ valide EAA criados no formato ISO 18013-5:2021 em CBOR.
