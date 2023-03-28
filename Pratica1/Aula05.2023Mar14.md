# Aula TP - 14/Mar/2023

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 28/Mar/23. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios

### Parte VII: Criptografia de chave pública

#### Pergunta P.VII.1.1

No slide 23 da aula de hoje é indicado que, na prática, as cifras assimétricas e as cifras simétricas são utilizadas em conjunto, sendo dado como exemplo o **envelope digital** (utilizado para garantir confidencialidade na transmissão de uma mensagem).

1. Reutilizando o que for possível do programa elaborado como resposta à pergunta P.V.1.1 da semana passada, implemente a técnica de **envelope digital** para cifrar e decifrar um ficheiro. Lembre-se que:

   + A cifra simétrica a utilizar é o ChaCha20;
   + A chave de sessão é gerada aleatoriamente pelo seu programa e não necessita de passwd fornecida pela linha de comando;
   + O par de chaves é gerado pelo seu programa, e utilize RSA (grupos com número impar) ou curvas elípticas (grupos com número par);
   + Na operação de cifra, o seu programa deve ter a opção de gravar a chave privada e a chave pública em ficheiros, sendo que a chave privada deve estar protegida por password. Reutilize o que tinha feito na resposta à pergunta P.V.1.1 da semana passada, para que a entropia da password que lhe é fornecida possa ser amplificada;
   + Na operação de cifra, o seu programa deve ter a opção de lhe ser passada a chave pública pela linha de comando (guardada num ficheiro);
   + Na operação de decifra, o seu programa tem de ter a opção de lhe ser passada a chave privada pela linha de comando (guardada num ficheiro);
   + Como output da operação de cifra terá:
     + um ficheiro cifrado com criptografia simétrica (contém ficheiro de input cifrado com a chave de sessão) e
     + outro ficheiro cifrado com criptografia assimétrica (contém chave de sessão cifrada com chave pública);
   + Como input da operação de decifra terá a chave privada, um ficheiro cifrado com criptografia simétrica (ficheiro de input cifrado com a chave de sessão) e outro ficheiro cifrado com criptografia assimétrica (chave de sessão cifrada com chave pública);
   + Como output da operação de decifra terá o ficheiro decifrado (ficheiro que estava cifrado com criptografia simétrica).

2. Apresente comandos linha de exemplo para cifra/decifra de ficheiros, utilizando o seu programa.

#### Experiência VII.1.1

1. Desenvolva em java uma aplicação linha de comando que permita assinar e verificar a assinatura de um ficheiro. Para a cifra assimétrica e hash, utilize os seguintes algoritmos, consoante o número do seu grupo:

   + Grupo 1: RSA-PSS com chave de 2048 bits e SHA256, utilizando os _providers_ da Sun fornecidos por omissão;
   + Grupo 2: RSA-PSS com chave de 3072 bits e SHA512, utilizando os _providers_ da Sun fornecidos por omissão;
   + Grupo 3: RSA-PSS com chave de 4096 bits e SHA3-256, utilizando os _providers_ do BouncyCastle;
   + Grupo 4: ECC com curva NIST P-256 e SHA256, utilizando os _providers_ da Sun fornecidos por omissão;
   + Grupo 5: ECC com curva NIST P-384 e SHA384, utilizando os _providers_ do BouncyCastle;
   + Grupo 6: ECC com curva NIST P-521 e SHA512, utilizando os _providers_ da Sun fornecidos por omissão;
   + Grupo 7: RSA-PSS com chave de 4096 bits e SHA3-256, utilizando os _providers_ da Sun fornecidos por omissão;
   + Grupo 8: ECC com curva NIST P-384 e SHA384, utilizando os _providers_ da Sun fornecidos por omissão;
   + Grupo 9: ECC com curva NIST P-521 e SHA512, utilizando os _providers_ do BouncyCastle;
   + Grupo 10: ECC com curva brainpoolP256r1 e SHA256, utilizando os _providers_ do BouncyCastle;
   + Grupo 11: ECC com curva brainpoolP384r1 e SHA384, utilizando os _providers_ do BouncyCastle;
   + Grupo 12: ECC com curva brainpoolP512r1 e SHA512, utilizando os _providers_ do BouncyCastle;
   + Grupo 13: RSA-PSS com chave de 3072 bits e SHA512, utilizando os _providers_ do BouncyCastle.

2. Apresente comandos linha de exemplo para assinatura/verificação de ficheiros, utilizando o seu programa.

#### Pergunta P.VII.1.2

Adapte o exemplo com openssl dado na aula teórica, para utilizar ECC com uma curva brainpool à sua escolha.
Indique os comandos a efetuar.
