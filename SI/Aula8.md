## Quantificiação de risco
É possível definitr uma forma simples para o cálculo do risco (R) associado a uma determinada vulnerabilidade:

**R = P x V**, sendo o P a probabilidade de ocorrência de um ataque e o V o valor do ativo.

Apesar de ser uma forma simples de calcular o risco, esta fórmula não é muito precisa, pois implica:
 - Identificação e caracterização de vulnerabilidades;
 - Dedução da probabilidade de ocorrência de um ataque;

## Vulnearbilidades e os seus tipos

As vulnerabilidades são problemas de segurança que afetam os sistemas informáticos, tanto os terminais (como computadores pessoais) quanto os de rede (como routers ou switches). Essas vulnerabilidades ocorrem principalmente devido a três razões: 

 - problemas de desenho;
 - Erros de realização;
 - Erros de administração de sistemas operativos e serviços.

Por vezes, as vulnerabilidades surgem de situações imprevistas, que o programador ou o arquiteto do sistema não conseguem prever, simplesmente porque são humanos. Estas vulnerabilidades podem ser exploradas por atacantes maliciosos para comprometer a segurança dos sistemas e obter acesso não autorizado a informações sensíveis ou para executar ações prejudiciais. Por isso, é essencial que os sistemas sejam regularmente atualizados e devidamente configurados para minimizar o risco de exploração de vulnerabilidades.

## Detetores de vulnerabilidades
Um dos primeiros passos para prevenir um possivel ataque será a **identificação do Sistema Operativo** (SO) e das **vulnerabilidades** da máquina alvo.

Estas são algumas das formulas de identificar vulnerabilidades:
 - **Flâmulas (*Banners*)**: Consiste em observar o *banner* publicitado por servidores aquando o seu acesso, não é muito usado em máquinas cliente pois normalmente não têm serviços de rede ativos.
 - **Impressão digital da Pilha IP**: Consiste em identificar e coletar informações específicas sobre um dispositivo ou rede com base no seu endereço IP. Esta técnica é usada para identificar o SO e a versão do mesmo.
 - **RING (Responder Identification Next Generation)**: Consiste em enviar um pacote ICMP para o alvo e analisar a resposta.
 - **NMAP**: Consiste em enviar pacotes TCP SYN para as portas mais comuns e analisar as respostas.
 - **Inventariação de Serviços (Service Scanning)**: Consiste em enviar pacotes TCP SYN (ou UDP) para as portas mais comuns e analisar as respostas com o objetivo de identificar os serviços que estão a correr na máquina alvo.
 - **Rastreio de Portas (Port Scanning)**: Consiste em enviar pacotes TCP SYN (ou UDP) para as portas mais comuns e analisar as respostas com o objetivo de identificar as portas que estão abertas na máquina alvo.
 - **Inventariação de Deficiências de Administração**: Consiste na exploração de vulnerabilidades conhecidas em serviços e aplicações comuns.
 - **Ataques LAND**: Consiste em enviar pacotes TCP SYN com o endereço IP de origem igual ao endereço IP de destino.
 - **Ataques Teardrop**: Consiste em enviar pacotes IP com fragmentos sobrepostos.
 - **Ataques Echo-Chargen**: enviar um pacote UDP com o mesmo endereço IP fonte e destino para a máquina vítima, e com os portos UDP de um e de outro serviço na fonte e no destino. O *echo* (porta 7) reenvia para o *chargen* (porta 19), e o *chargen* reenvia para o *echo*.
 - **Ataque de Inundação de inicialização (SYN Flood)**: Consiste em enviar um grande número de pacotes TCP SYN para a máquina vítima, sem nunca enviar o pacote ACK para completar a ligação.
 - **Ataque Ping-of-Death**: O ataque consiste em enviar um pacote ICMP demasiado grande mas muito fragmentado, esperar que o fragmentador o montasse antes de verificar que já tinha escrito em zonas da memória em que não devia.

## Erros de Realização
Por norma são mencionados **dois tipos** de ataques ou vulnerabilidades:
 - Vulnerabilidade de transbordamento de memória (*Buffer Overflow*): Consiste em escrever dados para além do limite de um *buffer* de memória, podendo assim corromper dados de outros programas ou do próprio sistema operativo.
 - Vulnerabilidades associadas a cadeias de formato (*Format String*): Consiste em usar dados de entrada com códigos de controlo de formatação de *strings*.