# Aula TP - 21/Mar/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 04/Abr/22. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios

### Parte VIII: Infraestrutura de chave pública

#### Experiência P.VIII.1.1

No slide 85 da aula de hoje, é apresentada a cadeia de confiança da EC do Cartão de Cidadão.

Utilizando o openssl, gere essa cadeia de confiança. Emita também um certificado de utilizador, pela EC de Autenticação e pela  EC de Chave Móvel Digital.

#### Pergunta P.VIII.1.1

No âmbito desta pergunta necessita de ter acesso ao seu certificado de assinatura do Cartão de Cidadão ou ao seu certificado de assinatura da Chave Móvel Digital. Caso não tenha acesso a nenhum deles, pode obter um certificado de assinatura da Chave Móvel Digital numa Loja do Cidadão ou num Espaço Cidadão (ou então, online em <https://www.autenticacao.gov.pt>, para o que precisa de aceder ao seu certificado de autenticação do Cartão de Cidadão).

1. Utilize o openssl para ver o conteúdo do seu certificado CC/CMD.
   + Identifique as várias componentes do mesmo, e o seu significado e/ou objetivo.
  
Note que para obter o certificado CMD, o mais simples é assinar um PDF, e de seguida exportar o certificado do PDF.

2. Utilizando a(s) biblioteca(s) que achar mais adequada, desenvolva um program linha de comando em node.js que tem como input um certificado (neste caso, o exemplo que terá que testar é com o seu certificado CC/CMD, mas deve funcionar para o caso geral de certificados CC/CMD), e vai indicar se o mesmo está ou não revogado através da consulta da CRL.
   + Indique o motivo da escolha da(s) biblioteca(s).
   + Note que o seu programa terá que "ir" à estrutura do certificado para obter o URL da CRL, após o que terá de ir buscar a CRL e verificar se o seu certificado faz parte da mesma ou não.
   + Como output, o seu programa deverá indicar o URL da CRL, a data da CRL atual e da próxima CRL, assim como o estado do seu certificado - se estiver revogado deve indicar a data em que foi revogado.

3. Utilizando a(s) biblioteca(s) que achar mais adequada, desenvolva um program linha de comando em node.js que tem como input um certificado (neste caso, o exemplo que terá que testar é com o seu certificado CC/CMD, mas deve funcionar para o caso geral de certificados CC/CMD), e vai indicar se o mesmo está ou não revogado através da consulta do OCSP.
   + Indique o motivo da escolha da(s) biblioteca(s).
   + Note que o seu programa terá que "ir" à estrutura do certificado para obter o URL do serviço de OCSP, após o que terá de comunicar com o servidor OCSP para obter o estado do certificado.
   + Como output, o seu programa deverá indicar o URL do OCSP, a data de resposta do servidor OCSP, assim como o estado do seu certificado - se estiver revogado deve indicar a data em que foi revogado.

#### Experiência P.VIII.1.2

1. Teste o exemplo de timestamp, apresentado no slide 132 e 133 da aula de hoje.

2. Faça uma script em bash/shell/zshell que automatize os quatro passos identificados.
