# Época Especial

Na época especial poderá melhorar a sua nota de PD2. Para tal terá que se inscrever na época especial através do portal académico ou serviços académicos da Universidade do Minho.

---
De seguida são apresentados os vários projetos para a época especial. O relatório final e o código fonte deverá ser colocado na área do Grupo no github até ao dia 26/07/2023, na subdiretoria "EpocaEspecial" (**Note que no relatório tem de indicar os passos necessários para se poder testar o código fonte, incluindo o ambiente**).

## Data e horário de apresentação do trabalho

Para além da apresentação oral do trabalho, também se vai querer ver o trabalho a funcionar, assim como aceder ao código fonte para que possam explicar algumas das alterações efetuadas.

Data e hora: Sexta-feira, dia 28 de Julho, pelas 14h00 em <https://us02web.zoom.us/j/86061994997?pwd=c2RnWDhXZlZKRDd4Znd1Y1FrMU1aZz09>.

## Avaliação

A avaliação do trabalho será efetuada entre 0 e 20 valores.

**Note** que o projeto de desenvolvimento, para além do desenvolvimento em si, deverá incluir as componentes de:

+ Identificação do “_Software Assurance Maturity Model_ (SAMM)” da equipa,
+ RGPD PIA, e
+ _Compliance_ com boas práticas de desenvolvimento.

Estas são as componentes identificadas para o PD2, mas que agora devem ser efetuadas no contexto deste trabalho de PD2.

## Objectivos

O objetivo destes projetos de desenvolvimento não é aprender a programar (esse poderia ser o objetivo se fosse um projeto no âmbito da licenciatura), mas

+ Integrar/utilizar/alterar frameworks, APIs, código de terceiros, ..., que sejam relevantes para o seu projeto, de modo a simplificarem o desenvolvimento e/ou aumentarem a segurança;
+ Utilizar metodologia de desenvolvimento de software seguro, realçando-se a [_Fundamental Practices for Secure Software Development_](https://safecode.org/resource-secure-development-practices/fundamental-practices-secure-software-development-2/), o [_Mitigating the Risk of Software Vulnerabilities by Adopting a Secure Software Development Framework_ (SSDF)](https://csrc.nist.gov/publications/detail/sp/800-218/final), e o [Microsoft _Security Development Lifecycle_ (SDL)](https://www.microsoft.com/en-us/securityengineering/sdl);
+ Identificar e melhorar as capacidades do grupo de trabalho no desenvolvimento de software seguro, através do modelo de maturidade [OWASP _Software Assurance Maturity Model_ (SAMM)](https://owasp.org/www-project-samm/);
+ Seguir o standard de verificação de segurança de aplicações ([OWASP _Application Security Verification Standard_](https://github.com/OWASP/ASVS)), no desenvolvimento do projeto;
+ Utilizar [ferramentas de análise de impacto da proteção de dados](https://www.cnil.fr/en/privacy-impact-assessment-pia) (PIA - _Privacy Impact Assessment_), de modo a demonstrar compliance com o RGPD (Regulamento Geral de Proteção de Dados).

----

## Utilização/integração de ferramentas disponibilizadas no âmbito do Digital Signature Services (DSS)

A União Europeia disponibiliza uma biblioteca de software _open-source_ ([_Digital Signature Services_ - DSS](https://ec.europa.eu/digital-building-blocks/wikis/display/DIGITAL/Digital+Signature+Service+-++DSS)) para a criação e validação de assinaturas eletrónicas, em linha com o Regulamento eIDAS e standards relacionados.

O código fonte do DSS encontra-se disponível no [repositório Bitbucket do DSS](https://ec.europa.eu/digital-building-blocks/code/projects/ESIG/repos/dss/browse) e, no github em <https://github.com/esig/dss>.

Também são disponibilizadas várias aplicações de demonstração da utilização do DSS, que pode encontrar no [repositório Bitbucket do DSS](https://ec.europa.eu/digital-building-blocks/code/projects/ESIG/repos/dss-demos/browse) e, no github em <https://github.com/esig/dss-demonstrations>.

### DSS Standalone Application

Como aplicação de demonstração, o DSS disponibiliza a [DSS Standalone Application](https://ec.europa.eu/digital-building-blocks/DSS/webapp-demo/signature-standalone) que pode fazer download e instalar a partir do [GitHub](https://github.com/esig/dss-demonstrations).

Os seus colegas do ano letivo 2020/21 alteraram a _DSS Demo WebApp_ - versão 5.8.2 - (pode ver no [projeto dos seus colegas](https://github.com/uminho-miei-engseg-20-21/Grupo3/tree/main/AP2-PD)), de modo a poder ser utilizada com:

+ Cartão de Cidadão,
+ Chave Móvel Digital, e
+ a fonte de _timestmap_ do Cartão de Cidadão, de modo a não se utilizar a _dummy timestamp source_ que é utilizada nas várias opções da Demo WebApp que utilizam _timestamp_.

Neste seu PD2, Pretende-se que instale e coloque a funcionar a _DSS Standalone Application_, e que adicionalmente adicione pelo menos duas das 3 seguintes funcionalidades:

+ assinatura com o Cartão de Cidadão,
+ assinatura com a Chave Móvel Digital,
+ utilização da fonte de _timestmap_ do Cartão de Cidadão.

Para tal poderá, se assim o entender, reutilizar código desenvolvido para a _DSS Demo WebApp_ pelos seus colegas referidos acima.

Nota: Para testar a Chave Móvel Digital necessita de a ativar (componente de autenticação e assinatura) em <https://www.autenticacao.gov.pt/>.
