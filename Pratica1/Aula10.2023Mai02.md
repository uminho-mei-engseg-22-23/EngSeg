# Aula TP - 02/Mai/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 16/Mai/23. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios

### 1\. RGPD (Regulamento Geral de Proteção de Dados)

Na diretoria Aula10 estão disponibilizados os seguintes documentos, entre outros:

+ Regulamento (UE) 2016/679 (RGPD), em [português](Aula10/UE_2016_679.RGPD.PT.pdf) e [inglês](Aula10/UE_2016_679.GDPR.ENG.pdf);
+ [Draft da ISO 27552](Aula10/Draft.PIM_PbD.pdf) (_Security techniques - Extension to ISO/IEC 27001 and to ISO/IEC 27002 for privacy management — Requirements and guidelines_);
+ [_Standard Data Protection Model_](Aula10/Germany.SDM-Methodology_V1.0.pdf) publicado pelo DPA (_Data Protection Atuhority_) alemão;
+ [_Handbook on European data protection law_](Aula10/EDPS-2018-handbook-data-protection_en.pdf), publicado pelo [_European Data Protection Supervisor_](https://edps.europa.eu/);
+ Vários documentos disponibilizados pela ENISA (_European Union Agency for Network and Information Security_) a partir da sua página de [Data Protecion](https://www.enisa.europa.eu/topics/data-protection)

#### Experiência 1.1

Nesta pergunta cada grupo vai efetuar uma pequena análise do Regulamento (UE) 2016/679 (RGPD) ou do ISO 27552 (_Security techniques - Extension to ISO/IEC 27001 and to ISO/IEC 27002 for privacy management — Requirements and guidelines_) ou do _Handbook on European data protection law_, de acordo com as regras seguintes:

+ Se o grupo escolher o RGPD, deverá analisar o seguinte artigo do regulamento e escrever um pequeno texto (entre 1/2 e 1 página A4) em que reflita sobre a forma como esse artigo do regulamento pode influir no desenvolvimento do software. Note que o documento tem 173 considerandos iniciais, podendo alguns serem relevantes para esta reflexão.
  + Artigo 5º
  + Artigo 25º
  + Artigo 32º
  + Secção 4 (Encarregado de Proteção de Dados)

+ Se o grupo escolher o draft do ISO 27552, deverá analisar o seguinte ponto e escrever um pequeno texto (entre 1/2 e 1 página A4) em que reflita sobre as implicações que esse ponto tem no desenvolvimento do software e/ou na operação do mesmo.
  + 6.4 (_Human resource security_) e 6.5 (_Asset management_)
  + 6.9 (_Operations Security_)
  + 6.13 (_Information security incident management_)
  + 6.15 (_Compliance_)

+ Se o grupo escolher o _Handbook on European data protection law_, deverá analisar as secções indicadas e e escrever um pequeno texto (entre 1/2 e 1 página A4) em que reflita sobre  as implicações que esse assunto tem no desenvolvimento do software:
  + _Lawfulness, fairness and transparency of processing principles_ - secção 3.1 ;
  + _Principle of purpose limitation_ - secção 3.2 ;
  + _Data minimisation principle_ - secção 3.3 ;
  + _Data accuracy principle_ - secção 3.4 ;
  + _Storage limitation principle_ - secção 3.5 ;
  + _Data security principle_ - secção 3.6 ;
  + _Accountability principle_ - secção 3.7 ;
  + _Right to be informed_ - secção 6.1.1 ;
  + _Right to rectification_  - secção 6.1.2 ;
  + _Right to erasure_ - secção 6.1.3 ;
  + _Right to restriction of processing_ - secção 6.1.4 ;
  + _Right to data portability_ - secção 6.1.5 ;

Note que a análise deverá apenas ser efectuada a um dos documentos, devendo o grupo escolher qual prefere, de acordo com as regras anteriores.

#### Experiência 1.2

A ENISA (_European Union Agency for Network and Information Security_) tem feito um trabalho relevante na produção de documentação relevante para a proteção de dados.

No documento [_Recommendations on shaping technology according to GDPR provisions - An overview on data pseudonymisation_](Aula10/ENISA.WP2018-O.2.2.5-Recomendations-on-shaping-technology-according-to-GDPR-provisions-Part1.pdf) analise as _Pseudonymisation techniques_ (secção 3), e faça um resumo das mesmas (entre 1/2 e 1 página A4) - Grupos 1, 4, 7, 10, 13.

No documento [_Recommendations on shaping technology according to GDPR provisions - Exploring the notion of data protection by default_](Aula10/ENISA.WP2018-O.2.2.5-Recommendations-on-shaping-technology-according-to-GDPR-provisions-Part2.pdf) analise o _Data protection by default in practice_ (secção 3), e faça um resumo das mesmas (entre 1/2 e 1 página A4) - Grupos 2, 5, 8, 11, 14.

No documento [_Privacy and Data Protection by Design – from policy to engineering_](Aula10/ENISA.Privacy-and-Data-Protection-by-Design.pdf) analise as oito estratégias de _privacy design_ (secção 3.2), e faça um resumo das mesmas (entre 1/2 e 1 página A4) - Grupos 3, 6, 9, 12.

#### Pergunta P1.1

O _ARTICLE 29 DATA PROTECTION WORKING PARTY_ publicou o [_Guidelines on Data Protection Impact Assessment (DPIA) and determining whether processing is “likely to result in a high risk” for the purposes of Regulation 2016/679_](Aula10/EU.20171013_wp248_rev01_enpdf.pdf) em que indica os nove critérios que devem ser considerados para avaliar se o processamento de dados pessoais irá resultar num risco elevado, devendo ser efetuado um DPIA sempre que o processamento satisfizer dois desses critérios.

1. Identifique os nove critérios
2. Verifique como é que o PD2 (projeto de desenvolvimento 2, no âmbito da avaliação prática 2) que está a efetuar para esta UC se enquadra nesses nove critérios.

> A resposta a esta pergunta, deve ser adicionada como anexo ao relatório do seu projeto de desenvolvimento 2 (PD2, no âmbito da avaliação prática 2), e respondida e efetuada nesse âmbito.

#### Pergunta P1.2

O CNIL (_Commission Nationale de l'Informatique et des Libertés_) disponibilizou uma ferramenta open-source para ajudar no _Data Protection Impact Assessment_ (DPIA) em <https://www.cnil.fr/en/open-source-pia-software-helps-carry-out-data-protection-impact-assesment>.

1. Instale a ferramenta (disponível para Linux, Windows e MacOS) que se encontra em <https://www.cnil.fr/en/open-source-pia-software-helps-carry-out-data-protection-impact-assesment>
2. Utilize a ferramenta para o DPIA do seu PD2 (projeto de desenvolvimento 2, no âmbito da avaliação prática 2), preenchendo sucintamente (pode preencher em português) todas as componentes pedidas, indicando como o seu projeto responde aos vários requisitos.
3. No final do preenchimento e validação, vá ao dashboard e escolha a apresentação em lista, selecione "_Display PIA_" e imprima para ficheiro PDF.

> A resposta a esta pergunta, deve ser adicionada como anexo ao relatório do seu projeto de desenvolvimento 2 (PD2, no âmbito da avaliação prática 2), e respondida e efetuada nesse âmbito.

#### Experiência 1.3

1. Responda à mesma pergunta do exercício anterior, mas em vez da ferramenta da CNIL, utilize o [template DPIA](Aula10/ICO.dpia-template.pdf) (obtido de <https://ico.org.uk/for-organisations/guide-to-data-protection/guide-to-the-general-data-protection-regulation-gdpr/accountability-and-governance/data-protection-impact-assessments/>).
2. Tendo utilizado o template DPIA e a ferramenta DPIA do CNIL (pergunta P1.2), conclua sobre qual a que melhor se adapta ao seu projeto, assim como as vantagens e desvantagens que percepcionou na utilização de ambas as "ferramentas".

#### Experiência 1.4

A ENISA (_European Union Agency for Network and Information Security_) tem feito um trabalho relevante na produção de documentação para a proteção de dados.

O documento [_Handbook on Security of Personal Data Processing_](Aula10/ENISA.WP2017.GDPRMeasuresHandbook.pdf) é relevante na medida em que apresenta uma metodologia para avaliar o risco de segurança no processamento de dados pessoais, assim como uma série de casos de uso que permitem calcular o nível de risco baseado na metodologia descrita.

O objetivo deste exercício é cada grupo analisar um caso de uso, discutir os vários passos metodológicos seguidos até à avaliação do risco, identificar o risco existente, e propor medidas apropriadas para diminuir (ou mitigar) o risco baseado nos anexos A.1, A.2 e A.3 do documento.

Caso de uso a avaliar:

+ Payroll management - Grupos 1, 7, 13
+ Recruitment - Grupos 2, 8, 14
+ Evaluation of employees - Grupos 3, 9
+ Order and delivery of goods - Grupos 4, 10
+ Marketing/advertising - Grupos 5, 11
+ Suppliers of services and goods - Grupos 6, 12

#### Pergunta P1.3

A ENISA (_European Union Agency for Network and Information Security_) tem feito um trabalho relevante na produção de documentação relevante para a proteção de dados.

O documento [Data Pseudonymisation: Advanced techniques & Use cases](Aula10/ENISA.Report-DataPseudonymisation-AdvancedTechniquesandUseCases.pdf) várias técnicas para pseudonimização dos dados, assim como alguns casos de uso.

O objetivo deste exercício é cada grupo analisar uma técnica de pseudonimização e um caso de uso, e discutir até que ponto é que a técnica de pseudonimização analisada podia ser utilizada no caso de uso.

Técnica de pseudonimização e caso de uso a avaliar:

+ _Asymmetric encryption_ e _Patient record comparison use-case_ - Grupos 1, 8
+ _Ring signature and Group pseudonyms_ e _Medical research institution use-case_ - Grupos 2, 9
+ _Chaining mode_ e _Distributed storage use-case_ - Grupos 3, 10
+ _Pseudonyms based on multiple identifiers or attributes_ e _File Reputation use case_ - Grupos 4, 11
+ _Pseudonyms with proof of ownership_ e  _URL Reputation use case_ - Grupos 5, 12
+ _Secure Multiparty Computation_ e  _Security Operations Centers use case_ - Grupos 6, 13
+ _Secret sharing schemes_ e _Consumer customer support use case_ - Grupos 7, 14

#### Experiência 1.5

Na tabela 1 do documento [_Online privacy tools for the general public - Towards a methodology for the evaluation of PETs for internet & mobile users_](Aula10/ENISA.Study-on-the-availability-of-trustworthy-online-privacy-tools-for-the-general-public.pdf) são apresentados os portais web mais relevantes na promoção da utilização de ferramentas que garantem a privacidade dos dados (e/ou do utilizador).

Baseado nos portais web identificados, efetue as seguintes experiências:

+ Utilize a ferramenta Panopticlick da _Electronic Frontier Foundation_ (EFF) para verificar se o seu browser é seguro contra _tracking_ - <https://panopticlick.eff.org/>
+ No _PRISM Break_ verifique que aplicações deve evitar e aquelas que deve preferir na sua plataforma - <https://prism-break.org/en/>
+ No _Security in-a-box_ verifique a tática para proteger ficheiros sensíveis no seu computador - <https://securityinabox.org/en/files/secure-file-storage/>
+ O privacytools.io disponibiliza informação sobre um conjunto alargado de ferramentas que preservam a privacidade - <https://www.privacytools.io/>
