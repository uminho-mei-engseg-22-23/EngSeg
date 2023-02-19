# Aula TP - 21/Fev/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 06/Mar/23. Por cada dia de atraso será descontado 0,25 valores à nota desse trabalho.

## Exercícios

### Parte I: Criptografia – conceitos básicos

#### Experiência 1.1

Hoje é reconhecida a importância de eliminar o secretismo como factor na segurança dos sistemas criptográficos ("_no securith through obscurity_"). Existem autores que defendem que tal já está retratados nos Princípios de Kerckhoff de 1883. Comente (mas não exceda o equivalente a meia folha de papel A4).

Note que para além da versão francesa dos Princípios de Kerckhoff apresentada na aula teórica, pode encontrar a versão inglesa em <https://www.petitcolas.net/kerckhoffs/index.html>.

#### Pergunta P1.1

Na aula teórica ouviu falar de alguns nomes famosos da Criptografia moderna.

Explique a contribuição dos seguintes cientistas para a Criptografia moderna, e indique a importância dessa contribuição (não exceda o equivalente a uma folha de papel A4) -  responda a esta pergunta para o(s) cientista(s) indicado(s) para o seu grupo -:

+ Grupo 1 - Craig Gentry
+ Grupo 2 - Mihir Bellare
+ Grupo 3 - Bruce Schneier
+ Grupo 4 - Dan Boneh
+ Grupo 5 - John Kelsey
+ Grupo 6 - Martin Hellman
+ Grupo 7 - Joan Daemen e Vincent Rijmen
+ Grupo 8 - Don Coppersmith
+ Grupo 9 - Paul Kocher
+ Grupo 10 - Dan Bernstein
+ Grupo 11 - Shafi Goldwasser e Silvio Micali
+ Grupo 12 - Jean-Jacques Quisquater

### Parte II: Exemplos de Cifras Clássicas

#### II.1 Cifra de Cesar

##### Experiência 1.1

A cifra ROT13 é uma cifra de substituição, conhecida por ser uma cifra de Cesar com chave 13.

Para cifrar a sua mensagem com a cifra ROT13, pode utilizar o módulo pycipher do python. Instale-o com `pip3 install pycipher` (ou `pip install pycipher`).

Para o utilizar no Python3,

```python
from pycipher import Rot13
Rot13().encipher('Engenharia de seguranca')
Rot13().decipher('RATRAUNEVNQRFRTHENAPN')
```

Verifique o que significa a seguinte mensagem: `VFGBRENHZNRKCREVRAPVN`.

##### Pergunta P1.1

A cifra de César pode ser quebrada em milisegundos, utilizando ferramentas automáticas, através de ataques por força bruta.

Adicionalmente existem técnicas que permitem, por análise de frequência de letras (ou conjunto de letras), avaliar qual dos resultados obtidos por força bruta que tem mais probabilidade de ser correto.

Utilizando a técnica (e o código) descrita em <http://practicalcryptography.com/cryptanalysis/stochastic-searching/cryptanalysis-caesar-cipher/>, verifique qual a chave utilizada para cifrar o seguinte texto em espanhol, e qual o texto original a que corresponde.

O texto é o seguinte: `Itkt ltuxk vnte xl xe mxqmh hkbzbgte eh wxlvbyktfhl vhg vtwt ngt wx etl vetoxl ihlbuexl vtevnetgwh et bwhgxbwtw itkt vtwt iknxut wx wxlvbyktwh`

##### Experiência 1.2

Uma maneira de dificultar o ataque por força bruta a uma mensagem cifrada com cifra de Cesar, é encadear várias cifras de Cesar?

Utilizando a técnica do exercício anterior, desenvolva um programa em python3 que:

+ cifre _cleartext_ aplicando várias cifras de Cesar, sequencialmente.
+ decifre _ciphertext_ aplicando várias cifras de Cesar, sequencialmente.
+ faça um ataque de força bruta ao espaço de todas as chaves de cifras sequenciais aplicadas ao _ciphertext_ (por uma questão de simplificação, um dos parâmetros a passar a esta função é a quantidade de cifras sequenciais aplicadas ao _ciphertext_), indicando no final qual o _cleartext_ que tem mais probabilidade de ser o texto original.

No final faça a comparação dos tempos necessários para ataque de força bruta a um texto de 100 caracteres, para uma a 5 cifras sequenciais. Em cada um dos casos indique qual é o espaço total de chaves que estão a ser avaliadas.

#### II.2 Cifra por substituição mono-alfabética

##### Experiência 2.1

O _ciphertext_ seguinte foi cifrado por substituição mono-alfabética: `xykme rplryz opeimuzfz m rpvrm ifqzyom`.

Utilizando a ferramenta disponibilizada em <https://www.dcode.fr/monoalphabetic-substitution>, obtenha o _cleartext_, sabendo que uma das palavras originais é `texto`.

##### Pergunta 2.1

Se for utilizada uma cifra por substituição mono-alfabética (com chave desconhecida), e interceptar o _ciphertext_ `OXAO`, justifique se o _plaintext_ correspondente pode ser `ALTA`.

#### II.3 Cifra por substituição poli-alfabética

A cifra de Hill é um exemplo de cifra por substituição poli-alfabética (para além do exemplo clássico da cifra de Vigenère que foi visto na aula teórica), baseada na álgebra linear. Mais informação em <https://en.wikipedia.org/wiki/Hill_cipher>, <https://www.geeksforgeeks.org/hill-cipher/> e <https://www.dcode.fr/hill-cipher>.

##### Pergunta 3.1

Utilize código já desenvolvido (procure no github, por exemplo) para cifrar e decifrar utilizando a cifra de Hill.

Note que na resposta a esta pergunta tem que incluir a descrição de todos os passos que o código está a fazer para cifrar o _cleartext_ `cifra de Hill` e posteriormente decifrar o _ciphertext_ resultante, assim como identificar as componentes do código onde tal é feito.

#### II.4 Cifra one-time pad

##### Experiência 4.1

A cifra de Vernam (também chamada de _one time pad Vignère_) é um caso particular da cifra de Vignère, em que a chave é tão comprida como o texto a cifrar.

Veja esta cifra em ação em <https://www.dcode.fr/vernam-cipher>.

##### Pergunta 4.1

Explique porque é que, na cifra _one-time pad_, os problemas inerentes à geração e distribuição da chave, assim como a necessidade de utilizar um “verdadeiro” gerador de números aleatórios, tornam (na prática) a cifra inviável.

#### II.5 Cifra por transposição

A transposição simples (vista na aula teórica) pode ser atacada advinhando possíveis comprimentos de coluna, escrevendo o _ciphertext_ nessas colunas (mas provavelmente na ordem errada, pois a chave ainda não é conhecida) e, em seguida, procurando possíveis anagramas.

Para tornar a cifra por transposição mais forte, é frequentemente utilizada uma transposição dupla, i.e., uma tranposição simples aplicada duas vezes. A mesma chave pode ser usada para ambas as transposições, ou duas chaves diferentes podem ser usadas.

Note que a transposição dupla foi uma das cifras manuais mais seguras utilizadas na segunda guerra mundial, conforme descrito em  <https://www.pbs.org/wgbh/nova/decoding/doubtrans.html>.

##### Experiência 5.1

Experimente esta cifra em <https://www.dcode.fr/double-transposition-cipher>, e perceba como funciona.

##### Pergunta 5.1

Desenvolva o código para a cifra/decifra por transposição dupla, documentando adequadamente o código desenvolvido.

Na resposta a esta pergunta inclua um exemplo manual (i.e., exemplificando sem o uso do código desenvolvido) de como funciona a dupla transposição para o _cleartext_ `a transposicao dupla funciona`, com as chaves de transposição `MUITO`e `BOM`.
