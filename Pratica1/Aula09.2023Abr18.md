
# Aula TP - 18/Abr/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 02/Mai/23. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

A resposta às perguntas da secção 2, devem ser adicionadas como anexo ao relatório do seu projeto de desenvolvimento 2 (PD2, no âmbito da avaliação prática 2), e respondidas e efetuadas nesse âmbito, sendo entregues como anexo ao relatório do PD2.

## Exercícios

### 1. Secure Software Development Lifecycle (S-SDLC)

#### Experiência 1.1

Em que fase do modelo em cascata deve ser levada em linha de conta o regulamento europeu RGPD?

#### Pergunta P1.1

Em que fase do modelo _Microsoft Security Development Lifecycle_ deve ser levada em linha de conta o regulamento europeu RGPD?

#### Pergunta P1.2

1. Em que função de negócio, prática de segurança e actividade do SAMM deve ser levada em linha de conta o regulamento europeu eIDAS?

2. Em que nível de maturidade dessa prática de segurança tem de estar a empresa, para levar em conta o regulamento europeu eIDAS nos seus projetos? Justifique.

#### Experiência 1.2

No seu projeto de desenvolvimento 1 (PD1, no âmbito da avaliação prática 2) utiliza certamente componentes, bibliotecas ou APIs _open source_.

1. Quais são as que utiliza, que versão, e que licenciamento é que têm?
2. Face ao licenciamento que têm, que restrições/permissões impõem sobre a utilização das mesmas no seu código?
3. Que boas práticas considera importantes para a utilização de código _open source_ no seu programa?

#### Pergunta P1.3

De acordo com o OWASP (<https://owasp.org/www-project-application-security-verification-standard/>) e com a versão 4.0.3 do [_Application Security Verification Standard_](Aula9/OWASP%20Application%20Security%20Verification%20Standard%204.0.3-en.pdf):

+ The OWASP **Application Security Verification Standard** (**ASVS**) Project provides a basis for testing web application technical security controls and also provides developers with a list of requirements for secure development.
+ The primary aim of the OWASP Application Security Verification Standard (ASVS) Project is to normalize the range in the coverage and level of rigor available in the market when it comes to performing Web application security verification using a commercially-workable open standard.
+ The ASVS is a community-driven effort to establish a **framework of security requirements and controls that focus on defining the functional and non-functional security controls required when designing, developing and testing modern web applications and web services**.
+ The Application Security Verification Standard defines **three security verification levels**, with each level increasing in depth.
  + ASVS **Level 1** is for low assurance levels, and is completely penetration testable
  + ASVS **Level 2** is for applications that contain sensitive data, which requires protection and is the recommended level for most apps
  + ASVS **Level 3** is for the most critical applications - applications that perform high value transactions, contain sensitive medical data, or any application that requires the highest level of trust.

  Each ASVS level contains a list of security requirements. Each of these requirements can also be mapped to security-specific features and capabilities that must be built into software by developers.

1. Qual o nível de verificação de segurança (_security verification level_) que deve ser adoptado para o serviço que emite PIDs (_PID Issuer_) no ecossistema da EUDI Wallet? Justifique.
2. Dos requisitos identificados no OWASP ASVS, identifique, explique e justifique quais e como se devem aplicar ao _PID Issuer_, de acordo com o número do seu Grupo:
    + Grupo 1: _V1.1 Secure Software Development Lifecycle_
    + Grupo 2: _V1.6 Cryptographic Architecture_
    + Grupo 3: _V2.5 Credential Recovery_
    + Grupo 4: _V3.5 Token-based Session Management_
    + Grupo 5: _V4.1 General Access Control Design_
    + Grupo 6: _V5.1 Input Validation_
    + Grupo 7: _V5.3 Output Encoding and Injection Prevention_
    + Grupo 8: _V6.2 Algorithms_
    + Grupo 9: _V7.1 Log Content_
    + Grupo 10: _V8.1 General Data Protection_
    + Grupo 11: _V8.3 Sensitive Private Data_
    + Grupo 12: _V9.2 Server Communication Security_
    + Grupo 13: _V10.2 Malicious Code Search_
    + Grupo 14: _V11.1 Business Logic Security_
    + Grupo 15: _V13.2 RESTful Web Service_
    + Grupo 16: _V14.2 Dependency_

### 2. SAMM (_Software Assurance Maturity Model_)

Nesta secção é-lhe pedido para utilizar o ciclo de melhoria contínua do SAMM, aplicada ao projeto de desenvolvimento 2 (PD2) de software que o seu grupo está a desenvolver (no âmbito da avaliação prática 2).

Para isso deverá utilizar a Toolbox ([ficheiro excel](Aula9/SAMM/SAMM_Assessment_Toolbox_v1.5_FINAL.xlsx)) fornecida na diretoria [Aula9](Aula9/SAMM), onde também encontrará mais informação relativa ao SAMM (que pode ser relevante para a resposta às perguntas desta secção).

Note que:

+ Para a Fase _Assess_ deverá preencher a _sheet_ "_Interview_";
+ Para a Fase _Set the Target_, o grupo deverá discutir qual o  _score_ objetivo das práticas de segurança identificadas. Se necessitar de pressupostos, indique-os na justificação à decisão tomada;
+ Para a Fase _Define the Plan_ deverá preencher a _sheet_ "_Roadmap_", supondo que cada uma das fases tem 3 meses de duração. Tenha em conta o esforço necessário e a eventual dependência entre atividades em cada uma das fases.

Note que não há respostas certas nem erradas.

> A resposta às perguntas desta secção, devem ser adicionadas como anexo ao relatório do seu projeto de desenvolvimento 2 (PD2, no âmbito da avaliação prática 2), e respondidas e efetuadas nesse âmbito.

#### Pergunta P2.1

Identifique a maturidade de três práticas de segurança (à sua escolha) que utiliza no projeto de desenvolvimento 2 (PD2) da UC de Engenharia de Segurança (Fase _Assess_ do SAMM)

#### Pergunta P2.2

Para cada uma das práticas de segurança identificadas na pergunta anterior, estabeleça o objetivo para a mesma (Fase _Set the Target_ do SAMM), i.e., o nível de maturidade pretendido;

#### Pergunta P2.3

Desenvolva o plano para atingir o nível de maturidade pretendido identificado na pergunta anterior, em quatro fases (Fase _Define the Plan_ do SAMM).
