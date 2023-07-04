## PGP

O acrónimo PGP abrevia a expressão inglesa **Pretty Good Privacy** e é utilizado para designar o software que combina diversos mecanismos da **criptografia de chave simétrica e de chave pública** reconhecidamente fortes para fornecer serviços de segurança a comunicações eletrónicas, nomeadamente e-mail, e  armazenamento de dados.

## Serviços Disponibilizados pelo PGP

 - **Autenticação**

 - **Confidencialidade**

 - **Compressão**

 - **Serviço de compatibilidade** (Codificação Base64)
 
 - **Serviço de Segmentação** (Quando um ficheiro é grande)


## Gestão de Chaves no PGP

Quando um utilizador **instala e inicializa** uma aplicação que implemente o PGP, tem de necessariamente **gerar pares de chaves públicas e privadas ou importar pares de chaves que já possua**. Como ficará claro adiante estas chaves são centrais ao funcionamento deste software. Como normalmente são usadas com dois objetivos diferentes (confidencialidade e autenticação ou assinatura digital), **o utilizador começa quase sempre por criar (ou importar) 2 pares de chaves públicas ou privadas**: um par só para **assinaturas digitais** e outro par só para **confidencialidade**. A utilização destas chaves pode ser resumida da seguinte forma:

 1. O utilizador usa a **sua chave privada**, do par definido para autenticação, **para fazer a sua assinatura digital** nas mensagens que envia;

 2. O utilizador **usa a chave pública do recipiente, do par** definido para autenticação, **para fazer a verificação de assinaturas recebidas deste**;

 3. O utilizador **usa a chave pública do recipiente**,
do par definido para confidencialidade, **para cifrar
chaves de sessão**;

 4. O utilizador **usa a sua chave privada**, do par definido para confidencialidade, **para decifrar chaves de sessão**.

Numa implementação PGP, as chaves assimétricas são
guardadas em **dois chaveiros diferentes**:

 1. Um **chaveiro privado**, que contem **uma ou mais chaves privadas do utilizador**. Este chaveiro está **protegido por uma palavra ou frase-passe**.

 2. Um **chaveiro público**, que o utilizador vai manualmente ou semi-automaticamente **povoando com chaves públicas de outros utilizadores**.

## Rede de Confiança (Web of Trust)

No PGP, a **confiança em chaves é construída através da Web of Trust**, um sistema descentralizado baseado na assinatura digital das chaves. Não é necessário confiar em entidades terceiras. Podemos estabelecer confiança pessoalmente, importando e assinando as chaves de outros utilizadores. Existem **três níveis de confiança**: absoluta, marginal e sem confiança. Confiamos nas chaves assinadas por **nós** e por **utilizadores de confiança absoluta**. Para confiar numa chave com **confiança marginal**, é necessário que **várias chaves com confiança marginal a tenham assinado**. A Web of Trust permite estabelecer confiança com base nessas assinaturas.

## Revogação de Chaves

Para **revogar chaves públicas** no PGP, existem duas formas:

 - **O utilizador emite um certificado de revogação assinado com a sua chave privada para invalidar a sua própria chave pública**. No entanto, esse método não é adequado se o utilizador revoga a chave devido à perda da mesma.

 - **Um utilizador pode designar outro utilizador em quem confia absolutamente para revogar as suas chaves caso as perca**. Nesse caso, o utilizador emite um documento assinado, indicando essa nomeação enquanto ainda possui as chaves. Se precisar revogar as chaves (por exemplo, devido à perda), solicita ao outro utilizador que emita um certificado de revogação, que é adicionado ao documento mencionado anteriormente.


## Cartão de Cidadão

O cartão do cidadão tem dois certificados digitais X.509. Um certificado de autenticação e um certificado de assinatura. O cartão de cidadão tem uma chave privada e uma chave pública. A chave privada está protegida por um **PIN**. A chave pública está no certificado de autenticação e no certificado de assinatura.

OBS: O cartão de cidadão não permite cifrar mensagens.

 - Pode ser visto como um documento físico para identificação segura.
 
 - Também é considerado um documento tecnológico para autenticação em serviços informatizados e para autenticar documentos eletrónicos.
 
 - O Cartão de Cidadão possui um formato de smartcard.
 
 - Na frente do cartão, exibe a fotografia e os elementos de identificação civil, enquanto o verso contém os números de identificação de diferentes organismos, uma zona de leitura ótica e o chip.
 
 - Ele possui um chip de contacto com certificados digitais, permitindo autenticação e assinatura eletrónica.
 
 - Além disso, o cartão pode armazenar notas pessoais do cidadão, como informações de contato de emergência.
 
 - Uma funcionalidade adicional é a verificação presencial da impressão digital do titular do cartão, garantindo privacidade, pois os dados de impressão digital não são transmitidos para fora do chip.
 
 - O Cartão de Cidadão é utilizado para autenticação em serviços da Internet, assinatura eletrónica qualificada reconhecida legalmente e verificação de impressão digital.
 
 - Os serviços de identificação da Administração Pública têm acesso inicial a essa funcionalidade de verificação da impressão digital.

### Autenticação
O cartão de cidadão é conhecido por usar autenticação de dois fatores usando o Cartão do Cidadão, através do *smartcard* e a inserção do PIN do titular do cartão. Existe no cartão de cidadão **9 PINs** diferentes ao todo:
 - Ativação do *smartcard*: 8 dígitos
 - Assinatura digital: 4 dígitos
 - Cancelamento do *smartcard*: 8 dígitos
 - PIN da morada: 4 dígitos
 - PIN de autenticação: 4 dígitos
 - PIN de assinatura: 4 dígitos
 - Desbloqueio do PIN de morada: 4 dígitos
 - Desbloqueio do PIN de autenticação: 4 dígitos
 - Desbloqueio do PIN de assinatura: 4 dígitos

Nota: A **cada operação** feita com o cartão de cidadão, é pedido o PIN de autenticação.

### Assinatura Digital
O cartão do cidadão **possui um par de chaves assimétricas RSA para assinatura digital**. Possui igualmente o certificado X.509v3 relativo à chave pública usada para assinaturas, para que possa ser disponibilizado à entidade que quer validar a assinatura digital. O PIN da assinatura digital do titular tem de ser enviado para o smartcard **cada vez que for necessário usar a chave privada dedica à cifragem**.

Note que, por omissão, a funcionalidade de validação da
assinatura digital **não vem ativada por defeito para o cartão do cidadão**: é possível produzir assinaturas desde o primeiro dia, mas as mesmas não podem ser validadas enquanto não se ativar a funcionalidade. A ativação desta funcionalidade tem de ser requerida presencialmente numa instituição autorizada para esse efeito. A respetiva chave é então retirada de uma Lista de Revogação de Certificados.

#### PIN
Em termos de autorização de operações, há 3 PINs diferentes para o cartão de cidadão:
 - Um para autorizar a indicação da morada;
 - Outro para autenticação do titular;
 - Outro para produzir assinaturas digitais.

