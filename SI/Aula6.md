## Certificados de chave pública
Um **certificado de chave pública** é uma estrutura que associa uma chave pública a uma entidade em particular (ou a uma representação da sua identidade). A associação chave / entidade é estabelecida por um terceiro, designado na literatura por **Autoridade de Certificação (AC)**, que assina digitalmente cada certificado.

No fundo, esta autoridade é quem assegura ao recetor do certificado que determinada chave pertence a determinada entidade. Assim, a **utilidade** de um certificado depende, apenas e só, da c**onfiança que as entidades têm relativamente à Autoridade de Certificação**.

## Certificados digitais
É um documento que liga dois conceitos, assinado por alguém, que certifica, e não dá para desfazer qualquer detalhe.

### Exemplo de certificado digital
  - **Nome para quem é passado**;
  - **Quem passou o certificado**;
  - **Data de início do certificado**;
  - **Data de fim do certificado**;
  - **Chave pública**;
  - **Algoritmo de assinatura**;
  - **Assinatura**;

Nota: Os sistemas operativos têm uma lista de certificados digitais de confiança e as respetivas chaves públicas.

## Infraestrutura de chave pública

Esta infraestrutura envolve os seguintes passos:
 - Um certificado de assinatura de chave pública é emitido por uma autoridade de certificação (CA) para um utilizador final.
 - Gera um par de chaves pública/privada.
 - Coloca a chave pública no certificado.
 - Instalo o certificado e a chave secreta no meu computador.

## Caminho de Certificação (Certification Path)

Conforme discutido antes, para usar um serviço que dependa do conhecimento de determinada chave pública,
o utilizador deve primeiro obter e validar um certificado dessa chave. A utilização da criptografia de chave pública é, portanto, mais complexa por si só. Contudo, há detalhes que ainda não foram discutidos.

Por exemplo, **a validação de um certificado de um utilizador envolve, por sua vez, o conhecimento da chave pública da AC1 que emitiu o certificado e, consequentemente, requer a obtenção do certificado que contém a chave pública do AC**.

### Raiz de confiança

Normalmente o sistema operativo tem uma lista de certificados de confiança e as respetivas chaves públicas. Sempre que é pedido a um determinado site o seu certificado, ele manda em conjunto os certificados as autoridades certificadores e as acima das mesmas que passaram o certificado (cadeia de certificados). Caso estas autoridades do topo não se encontrem no 'browser' ou no sistema operativo, o certificado não é válido. Estas autoridades do topo são denominadas de raiz de confiança.

OBS: Só depois de estabelecer toda a certificação, é que comunicações podem ser feitas.

## Lista de revogação de certificados

É um documento com a lista de certificados que foram revogados. É uma lista que é atualizada regularmente e que é assinada pela autoridade de certificação. É uma lista que é descarregada pelo sistema operativo e pelo 'browser' e que é usada para verificar se um determinado certificado foi revogado (ou seja, se o certificado foi comprometido).

##  LRCs Base e Delta
Uma LRC pode ser de um de dois tipos possíveis:

 - Uma **LRC completa (Base)** lista todos (dentro do seu domínio de atuação) os certificados que ainda não expiraram mas que foram revogados por uma das razões de revogação cobertas no âmbito da LRC.

 - Uma **LRC Delta** lista apenas aqueles **certificados que, dentro do seu domínio de atuação, mudaram o seu estado relativo à revogação (ou ficaram revogados, ou saíram da revogação)**, desde a emissão de uma LRC Base. O âmbito de uma LRC Delta deve ser o mesmo que o âmbito da LRC Base que referência.