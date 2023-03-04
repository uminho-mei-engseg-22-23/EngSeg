# Aula TP - 07/Mar/2022

Cada grupo deve colocar a resposta às **perguntas** (note que pode colocar as respostas às **experiências**, mas estas não irão contar para avaliação) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 21/Mar/22. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

## Exercícios

### Parte V: Funções de sentido único

##### Pergunta P.V.1.1

Relembre a pergunta P.IV.1.1 da semana passada, assim como a sua resposta. Deve-se ter apercebido que para utilizar o ChaCha20, a chave tinha de ter 32 bytes (i.e., 256 bits).

1. Altere o programa que fez, de modo a permitir que o utilizador forneça uma chave com o tamanho que considerar adequado, e utilize uma função KDF para amplificar a entropia da chave que o utilizador lhe forneceu.

   Justifique as opções tomadas.

##### Experiência E.V.1.1

1. Explique porque não deve utilizar uma função de hash normal para guardar a hash de uma password.

2. Foi publicado na internet um ficheiro de passwords de acesso a um serviço online, tendo sido referido que a aplicação de guarda de passwords desse serviço utiliza o SHA256 e guarda essa representação das passwords em hexadecimal. Ou seja, a password do utilizador é guardada do seguinte modo: hex(SHA256(password)).

   Sabendo que a passsword representada por `96cae35ce8a9b0244178bf28e4966c2ce1b8385723a96a6b838858cdd6ca0a1e` faz parte do top200 das passwords mais comuns (<https://nordpass.com/most-common-passwords-list/>), indique qual é essa password, e explique os passos que deu para a encontrar, assim como o código que desenvolveu.

##### Pergunta P.V.1.2

1. Utilizando o openssl indique qual é o comando linha que tem de utilizar para obter o HMAC-SHA256 de todos os ficheiros numa diretoria.

2. O que teria de fazer para saber se um determinado ficheiro foi alterado, desde a última vez que efetuou a operação indicada no ponto anterior?

### Parte VI: Acordo de chaves

##### Pergunta P.VI.1.1

Desenvolva, na linguagem que preferir e utilizando uma biblioteca criptográfica à sua escolha, um programa linha de comando que permita **visualizar** o acordo de chave entre a Alice e o Bob, utilizando o protocolo Diffie-Hellman, assim como a posterior comunicação de mensagens cifradas (pela chave acordada) entre esses mesmos dois intervenientes.

##### Experiência VI.1.1

No exemplo com openssl dado na aula teórica, existe um erro quando comento o slide 17. Qual é esse erro?
