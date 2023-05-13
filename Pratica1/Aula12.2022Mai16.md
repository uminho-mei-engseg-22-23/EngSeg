
# Aula TP - 16/Mai/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 31/Mai/23. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios

### 1. Vulnerabilidade de codificação

#### Experiência 1.1 - _Common Weakness Enumeration_ (CWE)

A _Common Weakness Enumeration_ (CWE) classifica classes de vulnerabilidade, atribuindo a cada classe de vulnerabilidades um identificador.

Aceda a <https://cwe.mitre.org/> e veja quais as vulnerabilidades que são identificadas como:

- vulnerabilidades de projeto, introduzidas durante a fase de projeto do software (obtenção de requisitos e desenho) - <https://cwe.mitre.org/data/definitions/701.html>. Explore um dos membros dessa classe de vulnerabilidades e veja (e perceba) um dos exemplos demonstrativos.
- vulnerabilidades de codificação, introduzidas durante a programação do software - <https://cwe.mitre.org/data/definitions/702.html>. Explore um dos membros dessa classe de vulnerabilidades e veja (e perceba) um dos exemplos demonstrativos.
- vulnerabilidade operacional, causadas pelo ambiente no qual o software é executado ou pela sua configuração - <https://cwe.mitre.org/data/definitions/2.html>. Explore um dos membros dessa classe de vulnerabilidades e veja (e perceba) um dos exemplos demonstrativos..

Veja ainda quais as vulnerabilidades identificadas como:

- _CWE/SANS Top 25 Most Dangerous Software Errors_ (2021) - <https://cwe.mitre.org/top25/>
- _OWASP Top Ten_ (2021) - <https://cwe.mitre.org/data/definitions/1344.html>

#### Pergunta 1.1 - _Common Weakness Enumeration_ (CWE)

Tendo por base o **The CWE Top 25** de 2022 <https://cwe.mitre.org/top25/>,

1. Explique as características da _Weakness_ no ranking correspondente ao número do seu grupo, em que linguagens (e tecnologias, se aplicável) são mais prevalentes, e quais são as suas consequências mais comuns. Dê exemplo (e explique) de código e de CVE que inclua essa _Weakness_.

#### Experiência 1.2 - _Common Vulnerabilities and Exposures_ (CVE)

A _Common Vulnerabilities and Exposures_ (CVE) identifica vulnerabilidades (de projeto e codificação) existentes em software comercial ou aberto, com identificador com formato CVE-AAAA-NNNN, sendo AAAA o ano em que a vulnerabilidade foi catalogada e NNN o seu número.

Aceda a <https://cve.mitre.org/> e verifique:

- o detalhe da vulnerabilidade mais recente;
- as vulnerabilidades identificadas no WhatsApp;
- as vulnerabilidades identificadas no Firefox.

#### Experiência 1.3 - _Common Vulnerability Scoring System_ (CVSS)

O _Common Vulnerability Scoring System_ (CVSS) disponibiliza um modelo quantitativo para definir as características e impacto das vulnerabilidades, garantindo
uma medição precisa e repetível para gerar pontuações de impacto de vulnerabilidade.

Dois usos comuns do CVSS são a priorização das atividades de correção de vulnerabilidades e, o cálculo da gravidade das vulnerabilidades descobertas.

Explore o calculador de vulnerabilidades em <https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator>.

#### Experiência 1.4 - _National Vulnerability Database_ (NVD)

A _National Vulnerability Database_ (NVD) é o repositório de vulnerabilidades gerido pelo NIST. Baseia-se no CVE, mas inclui a gravidade da vulnerabilidade, de acordo com o CVSS (_Common Vulnerability Scoring System_)

Aceda a <https://nvd.nist.gov/> e verifique:

- qual é a vulnerabilidade mais recente identificada?
- essa vulnerabilidade é a mesma vulnerabilidade mais recente encontrada na experiência 1.2 (CVE)? Qual poderá ser o motivo?
- as vulnerabilidades identificadas no WhatsApp;
- as vulnerabilidades identificadas no Firefox.

#### Experiência 1.5 - _SLOC - Source Lines Of Code_

 Em <https://informationisbeautiful.net/visualizations/million-lines-of-code/> encontra (algumas são estimativas) o número de linha de código
 (_SLOC - Source Lines Of Code_) de alguns pacotes/plataformas de software.

1. Estime o número de bugs do Debian 5.0, Google Chrome e Windows Vista.
2. Quantos desses bugs são vulnerabilidades?

#### Pergunta P1.2

Considere os três tipos de vulnerabilidades: de projeto, de codificação e operacional. Apresente para cada um deles dois exemplos e discuta a dificuldade de correção.

#### Pergunta P1.3

O que é que distingue uma vulnerabilidade dia-zero de outra vulnerabilidade de codificação que não seja de dia-zero?

#### Experiência 1.6 - _Exploit Database_

O _Exploit Database_ contém um arquivo de _exploits_ públicos, identificando o CVE da vulnerabilidade e/ou software que explora, para utilização por investigadores de vulnerabilidades e _penetration testers_.

Aceda a <https://www.exploit-db.com/> e verifique:

- qual é o _exploit_ mais recente identificado?
- o que é que o _exploit_ relativo ao  CVE-2022-24112 lhe permite fazer?

#### Experiência 1.7 - _Google Hacking Database_

O _Google Hacking Database_ é um arquivo de Google _dorks_ (_query_ de pesquisa que retorna a informação sensível) que embora sendo uma forma de _exploits_, são também utilizados para criar novos _exploits_.

Aceda a <https://www.exploit-db.com/google-hacking-database/> e verifique:

- qual é o _dork_ mais recente identificado?
- explore alguns _dorks_.

#### Experiência 1.8 - Linguagem C

Tal como visto na aula teórica, a linguagem C é uma linguagem compilada em que cada instrução C é traduzida para instruções em linguagem máquina.

Compile um programa C com o `gcc` com a opção `-S`, de forma a produzir o código assembly correspondente ao código binário/executável (o código assembly fica no ficheiro com extensão .s).
Verifique o ficheiro .s e compare-o com o ficheiro .c original.

Como exemplo utilize o seguinte código C:

    #include <stdio.h>

    void main()
    {
      printf("Hello World\n");
    }
