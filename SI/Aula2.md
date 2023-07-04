# Aula 2

## Criptografia, Criptanálise, Definição de Cifra e Modelos de Ataque

### Criptografia
Conjunto de técnicas que procuram tornar possivel a comunicação secreta entre 2 agentes sobre um canal aberto. É constituído por cifras, mecanismos de integridade e de troca de chaves ou segredos criptográficos.

### Criptanálise
É o estudo de técnicas que visam gorar os objetivos da Criptografia, isto é, quebrar a segurança da comunicação.

### Criptologia
Conjuntamente, a Criptografia e a Criptanálise formam uma disciplina a que podemos chamar Criptologia. é uma área com profundas raízes na Matemática e nas Ciências da Computação.

## Cifras
A cifra constitui um dos mecanismos mais importantes da criptografia. É
possível definir cifras de chave-simétrica e cifras de chave-pública, bem como dividir as primeiras em cifras de chave-simétrica contínuas ou por blocos.

### Propriedades necessárias de cifras seguras
Estas são algumas das propriedades que uma cifra segura tem:
- **Difusão**: Se uma cifra for de qualidade, quaisquer propriedades estatísticas do texto limpo estão completamente **difusas** (sem qualquer tipo de correlação) por todo o criptograma.
- **Confusão**: Se uma cifra for de qualidade, não são perceptiveis quaisquer relações entre um bloco de texto-limpo, a chave de cifra e o bloco de criptograma.
- **Não maneável**: Se uma cifra for de qualidade, não é possível **manejar** (alterar) o texto cifrado sem que o texto limpo seja alterado. Esta propriedade é mantida por um código de **autenticação de mensagem**.
- **Semântica**: Se uma cifra for de qualidade, o adversário não deverá ser capaz de obter informações sobre o texto limpo a partir do texto cifrado.
- **Não determinística**: Esta propriedade permite que a cifra produza saídas diferentes para o mesmo texto limpo e chave de cifra.

Nota: Todas estas propriedades acima têm que ser balenceadas com a **usabilidade** da cifra.

### Cifras clássicas
São algoritmos que utilizam a mesma chave para cifrar e decifrar. Cifras clássicas têm **um** algoritmo (para cifrar e para decifrar).

Alguns Exemplos:
 - Cifra de César;
 - Cifra de Vigenère (mais difusa que a de César);
 - Cifra Enigma;
 - Cifra de Vernam (perfeita em termos de secretismo, contudo não é usável);

### Cifras de chave simétrica
Um par de algoritmos eficientes que usam a mesma chave para ambas as operações. O algoritmo (ou operação) de cifra é normalmente dotada de aleatoriedade, enquanto que a decifra é determinística.

#### Cifras de chave simétrica continuas
As cifras de chave simétrica continuas usam um algoritmo que a partir de uma chave com tamanho **fixo** e **comportável**, geral uma sequência tão grande quanto necessária para cifrar um ficheiro. Cifras de chave simétrica continua têm **três** algoritmos (para cifrar, para decifrar e para gerar chaves).

Nota: Este tipo de cifra tem como defeito a sua **maneabilidade** (facilidade da alteração do texto cifrado). Se cifrarmos um ficheiro já antes cifrado com a **mesma chave**, iremos obter o texto-limpo.

#### RC4 (Rivest Cipher 4)
É um algoritmo de cifra simétrica que utiliza uma chave de 40 a 2048 bits.

#### Cifras de chave simétrica por blocos
A diferença entre as cifras de chave simétrica de bloco e as cifras de chave simétrica continua é que as cifras de chave simétrica de bloco geram uma cifra de tamanho fixo (bloco) e não uma cifra de tamanho variável. Caso a cifra de chave simétrica de bloco seja alterada (maneada), o texto cifrado perderá toda a sua integridade.

### *Padding* (Preenchimento)
O **padding** é uma técnica de preenchimento de dados que consiste em adicionar um número de bytes ao final de um bloco de dados, de forma a que o tamanho do bloco de dados seja múltiplo do tamanho do bloco de dados da cifra.

Nota: O último bloco tem sempre *padding*, mesmo que o bloco da mensagem seja múltiplo do tamanho do bloco da cifra é acrescentado um bloco de *padding*.

Nota: Este tipo de cifra é mais segura, dependendo de como são usadas, quando o canal de comunicação permite a **alteração** da mensagem cifrada.

## Algoritmos conhecidos

### AES (Advanced Encryption Standard)
É um algoritmo de cifra simétrica por blocos que utiliza uma chave de 128, 256 OU 512 bits. Ele é bastante usado para criptografar dados em trânsito na internet.

### DES (Data Encryption Standard)
É (era!?) um das cifras de chave simétrica por blocos mais importantes. Estabeleceu o precedente em meados de 1970 como a primeira cifra de nível comercial com uma completa e aberta especificação dos detalhes de implementação.

### Definição de Cifra de Chave-Pública (Assimétrica)
Um cifra de chave pública é constituída por um conjunto de algoritmos eficientes (G, E, D) em que um conjunto de chaves (pK, sK) são usados para cifrar e decifrar e outro gera essas mesmas chaves.

## Algoritmos conhecidos

### RSA (Rivest, Shamir, Adleman)
É um algoritmo de cifra pública que utiliza uma chave de 512 a 4096 bits. Ele é bastante usado para criptografar dados em trânsito na internet.

Nota: RSA no modo livre de escola é **determinístico**.

## Tipos de ataques
Alguns exemplos dos tipos de ataques mais comuns:

### Ataque força bruta (Brute force)
É uma técnica de ataque que consiste em tentar todas as possíveis chaves de cifra até encontrar a chave correta.

### Ataque com conhecimento de texto-limpo original (Known plaintext attack)
É uma técnica de ataque que consiste em tentar descobrir a chave de cifra a partir de um texto-limpo original e do texto-cifrado correspondente.

### Ataque com conhecimento do criptograma original (Cyphertext Only Attack)
ataque que consiste em tentar descobrir a chave de cifra ou o texto-limpo, a partir de um texto-cifrado.

### Ataque com o texto-limpo original escolhido pelo atacante (Chosen plaintext attack)
É uma técnica de ataque que consiste em tentar descobrir a chave de cifra ou o texto-limpo a partir de um texto-limpo original escolhido pelo atacante.

### Ataque com o texto-limpo original escolhido pelo ataque adaptativo (Adaptative Chosen plaintext attack)
Semelhante ao anterior, porém o atacante obtém exemplos de texto cifrado antes e depois de começar o ataque.

### Ataques com criptogramas escolhidos pelo atacante (Chosen ciphertext attack)
É uma técnica de ataque que consiste em tentar descobrir a chave de cifra ou o texto-limpo a partir de um conjunto de textos-cifrados escolhidos pelo atacante, diferentes do texto que queremos cifrar.

Nota: Não é uma técnica de criptanálise.

### Ataque do homem no meio
Este tipo de ataque é feito quando a **Pessoa A (Alice)** e a **Pessoa B (Bob)** estão sujeitos a um ataque por uma **Pessoa C (Claire)** que se encontra no meio da comunicação entre as duas pessoas. Existem dois tipos de ataque do homem no meio:
- **Ataque do homem no meio passivo**: A **Pessoa C (Claire)** não consegue alterar (apenas vê) a mensagem cifrada (também chamada de **Pessoa E (Eve)**).
- **Ataque do homem no meio ativo**: A **Pessoa C (Claire)** consegue alterar e ver a mensagem cifrada.

