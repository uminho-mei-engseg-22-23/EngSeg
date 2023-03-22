# Avaliação prática 2 - Projeto de análise de um tema (PA)

De seguida são apresentados os vários projetos de análise de um tema. O relatório final deverá ser colocado na área do Grupo no github até ao dia 20/03/2022, na subdiretoria "AP2-PA".


## 1. Data e horário de apresentação do trabalho

Data: Os trabalhos serão apresentados durante a segunda parte da aula de 3ª feira, de acordo com as datas indicadas abaixo. Os grupos terão 15 minutos para fazer a apresentação, seguida de 5 - 10 minutos de questões.

+ Grupo 1 - 28/03/2023
+ Grupo 2 - 28/03/2023
+ Grupo 3 - 11/04/2023
+ Grupo 4 - 11/04/2023
+ Grupo 5 - 18/04/2023
+ Grupo 6 - 11/04/2023
+ Grupo 7 - 28/03/2023
+ Grupo 8 - 18/04/2023
+ Grupo 9 - 18/04/2023

## 2. Avaliação do PA

A avaliação do PA será efetuada entre 0 e 20 valores. Quem entregar antes da data limite tem uma valorização de 1% na sua nota por cada dia de antecipação.

Exemplificando:

+ o Grupo A entrega o PA no dia 10/03/2021 e tem uma avaliação de 15 valores. Como entregou 10 dias antes terá 10% de valorização, sendo a sua nota final de 16,5 valores.
+ o Grupo B entrega o PA no dia 15/03/2021 e tem uma avaliação de 15 valores. Como entregou 5 dias antes terá 5% de valorização, sendo a sua nota final de 15,75 valores.

## 3. Projeto

A European Identity Digital Wallet (EUDIW) é uma iniciativa da Comissão Europeia para, entre outros, fornecer aos cidadãos europeus um meio seguro e conveniente de armazenar e gerir os seus documentos de identificação (e outros atributos do cidadão, como por exemplo percurso académico, profissão, ...), em formato digital (por exemplo, através de uma app no dispositivo móvel do cidadão). A EUDIW tem como objetivo principal ajudar a simplificar e proteger a identidade digital (em formato digital) dos cidadãos europeus e promover a interoperabilidade entre serviços digitais em toda a UE.

O cidadão poderá utilizar a sua EUDIW para se identificar online (na web) e offline (no Mundo físico).

### 3.1 EUDIW - ponto de vista jurídico

A EUDIW irá estar definida, do ponto de vista jurídico, na nova versão do Regulamento (UE) eIDAS (Regulamento eIDAS 2.0), que deverá ser aprovado e entrar em vigor até final do ano de 2023.

O Regulamento (UE) eIDAS atualmente em vigor é o [REGULAMENTO (UE) N.o 910/2014 DO PARLAMENTO EUROPEU E DO CONSELHO de 23 de julho de 2014 relativo à identificação eletrónica e aos serviços de confiança para as transações eletrónicas no mercado interno e que revoga a Diretiva 1999/93/CE](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=uriserv:OJ.L_.2014.257.01.0073.01.ENG), encontrando-se as alterações aprovadas pela Comissão Europeia a 6 de Dezembro (e que darão origem ao Regulamento eIDAS 2.0) em <https://data.consilium.europa.eu/doc/document/ST-14959-2022-INIT/en/pdf> (em especial no anexo, a partir da página 7, sendo relevante os considerandos iniciais que se referem à EUDIW, o artigo 3 e os artigos 6a, 6b, 6c, 6d, 6da e 6db).

Podem encontrar mais informação em <https://www.consilium.europa.eu/en/press/press-releases/2022/12/06/european-digital-identity-eid-council-adopts-its-position-on-a-new-regulation-for-a-digital-wallet-at-eu-level/?utm_source=dsms-auto&utm_medium=email&utm_campaign=European+digital+identity+(eID)%3a+Council+makes+headway+towards+EU+digital+wallet%2c+a+paradigm+shift+for+digital+identity+in+Europe>.

### 3.2 EUDIW - ponto de vista técnico

Do ponto de vista técnico, a EUDIW está definida na [European Digital Identity Wallet Architecture and Reference Framework (ARF)](https://digital-strategy.ec.europa.eu/en/library/european-digital-identity-wallet-architecture-and-reference-framework)

### 3.3 Análise à EUDIW

O trabalho de todos os grupos é dividido em duas partes:

+ parte A - **análise resumida** da EUDIW na sua globalidade,
+ parte B - **análise detalhada** (e seu enquadramento na EUDIW) de um componente/protocolo/standard utilizado na EUDIW (diferente por cada Grupo, e indicado abaixo).

Nota:

+ Nesta UC, todos os trabalhos da parte *Prática 2* irão estar relacionados direta ou indiretamente com a EUDIW, pelo que se espera que utilizem este PA para ficarem com um bom conhecimento base da mesma quer do ponto de vista técnico como jurídico;
+ O **relatório** deverá conter as duas partes referidas em cima (A e B), esperando-se que a  parte B tenha detalhe adequado à análise pedida. O relatório tem de ser escrito em português de Portugal - se existirem palavras ou expressões que são melhor compreendidas em inglês, deixem-nas em inglês e escrevam-nas em itálico.
  + Em grupos com mais de três elementos, espera-se também que a parte A tenha um maior detalhe.
+ A **apresentação**, e dado que todos os grupos tiveram que fazer uma análise resumida da EUDIW, deve apenas refletir a análise detalhada que lhe foi pedida para a parte B (com um máximo de dois slides iniciais referente ao enquadramento da parte B na parte A).
  + Em grupos com mais de três elementos, a parte A deverá ser apresentada com mais algum detalhe (com um máximo de cinco slides).

#### 3.3.1 Parte B

Para a parte B, são os seguintes os componentes/protocolos/standards a analisar, conforme o número do seu grupo:

+ Grupo 1 - Na página 24 (requisito 6) do ARF é indicado *"PID attestation MUST be issued to be presented in accordance with both the data model specified in ISO/IEC 18013-5:2021 and the W3C Verifiable Credentials Data Model 1.1."*. Analise o que significa o PID ser emitido de acordo com o modelo de dados do ISO/IEC 18013-5:2021, e apresente um modelo de dados que satisfaça este requisito.
+ Grupo 2 - Na página 24 (requisito 6) do ARF é indicado *"PID attestation MUST be issued to be presented in accordance with both the data model specified in ISO/IEC 18013-5:2021 and the W3C Verifiable Credentials Data Model 1.1."*. Analise o que significa o PID ser emitido de acordo com o modelo de dados do *W3C Verifiable Credentials Data Model 1.1*, e apresente um modelo de dados que satisfaça este requisito.
+ Grupo 3 -  Na página 24 (requisito 7) do ARF é indicado *"PID attestation MUST be encoded as CBOR and JSON format."*. Analise o que são estes formatos, que tipo de bibliotecas existem para a sua utilização (em várias linguagens de programação) e dê exemplos da sua utilização.
+ Grupo 4 - Na página 24 (requisito 8) do ARF é indicado *"PID attestation MUST enable Selective Disclosure of attributes by using Selective Disclosure for JWTs (SD-JWT) and Mobile Security Object (ISO/IEC 18013-5) scheme accordingly to the data model."*. Analise o que significa os atributos do PID poderem ser divulgados seletivamente utilizando o *Selective Disclosure for JWTs (SD-JWT)* e apresente exemplos de como tal poderia ser feito.
+ Grupo 5 - Na página 24 (requisito 8) do ARF é indicado *"PID attestation MUST use signatures and encryptions formats as detailed in JOSE RFCs and COSE RFCs."*. Analise o que são estes formatos, que tipo de bibliotecas existem para a sua utilização (em várias linguagens de programação) e dê exemplos da sua utilização.
+ Grupo 6 - Na página 26 (requisito 9) do ARF é indicado *"EAA MAY be encoded as JSON-LD."*. Analise o que é este formato, que tipo de bibliotecas existem para a sua utilização (em várias linguagens de programação) e dê exemplos da sua utilização.
+ Grupo 7 - Na página 26 (requisito 13) do ARF é indicado *"(Q)EAA SHOULD be issued accordingly to OpenID4VCI protocol."*. Analise o que é este protocolo, que tipo de bibliotecas existem para a sua utilização (em várias linguagens de programação) e dê exemplos da sua utilização.
+ Grupo 8 - Na página 35 (componente "*Attestation exchange Protocol - 1*") do ARF é indicado *"EUDI Wallet Solution [...] support OpenID4VP as attestation exchange protocol for remote flows. When pseudonymous authentication is requested, request parameters SHOULD be specified in accordance with OpenID SIOPv2"*. Analise o que é o protocolo OpenID4VP, que tipo de bibliotecas existem para a sua utilização (em várias linguagens de programação) e dê exemplos da sua utilização.
+ Grupo 9 - Na página 35 (componente "*Attestation exchange Protocol - 1*") do ARF é indicado *"EUDI Wallet Solution [...] support OpenID4VP as attestation exchange protocol for remote flows. When pseudonymous authentication is requested, request parameters SHOULD be specified in accordance with OpenID SIOPv2"*. Analise o que é o protocolo OpenID SIOPv2, que tipo de bibliotecas existem para a sua utilização (em várias linguagens de programação) e dê exemplos da sua utilização.
+ Grupo 10 - Na página 37 (componente "*Signature formats - 3*") do ARF é indicado *"EUDI Wallet Solution [...] support signatures and encryptions in accordance with LD-Proof specifications."*. Analise o que é a *LD-Proof specifications*, que tipo de bibliotecas existem para a sua utilização (em várias linguagens de programação) e dê exemplos da sua utilização.

Note que a secção 9 do ARF identifica um conjunto de bibliografia que pode ser relevante para a sua análise. O ISO/IEC 18013-5:2021 pode ser encontrado [aqui](ISO_IEC_FDIS_18013-5_(E).pdf).
