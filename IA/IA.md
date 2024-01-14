# Inteligência Artificial

A definição de Inteligência Artificial (IA) pode ser integrada em quatro grupos:
* **1 -** _Sistemas que agem como os humanos_:
    * Teste de Turing (1950) - uma máquina passa no teste se, após responder a questões colocadas por escrito, não é possível definir se as respostas foram dados por um humano ou não. A máquina necessita de:
        * **Processamento da linguagem natural** - capacidade de comunicar na linguagem humana;
        * **Representação do conhecimento** - armazenamento da informação;
        * **Raciocínio automático** - uso de informação armazenada para responder a perguntas e atingir conclusões;
        * **Aprendizagem automática** - adaptação a novas circunstâncias, deteção e extrapolação de padrões;
    * Teste de Turing total - usa também sinal de vídeo, permitindo ao interrogador testar as capacidades percetuais do candidato e a passagem de objetos. A máquina necessita, além do supracitado, de:
        * **Visão computacional** - reconhecimento de objetos;
        * **Robótica** - manipulação de objetos e deslocação;
    * No entanto, não é preciso agir como um humano para ser inteligente - como é caso da aerodinâmica;
* **2 -** _Sistemas que pensam como os humanos_:
    * A perceção de como os humanos pensam é feita por **introspeção** (tentativa de análise dos próprios pensamentos) ou **experiências psicológicas** (ciências cognitivas). No entanto, a interligação para a IA enfrenta dois grandes obstáculos:
        * Difícil passagem de conhecimento informal para notação lógica;
        * Diferença entre capacidade de resolver problemas na teoria e na prática;
* **3 -** _Sistemas que agem racionalmente_:
    * Um **agente** é algo que age de forma autónoma, com captação de dados do ambiente (sensores), durante longos períodos de tempo, com adaptação a mudanças e capaz de atingir determinados objetivos. Um **agente racional** age de forma a alcançar o melhor resultado ou, no caso de existir incerteza, o melhor resultado esperado;
    * Este estudo é mais vantajoso porque é mais geral que a abordagem do pensamento racional e é mais adaptado ao desenvolvimento científico (usa uma definição de racionalidade clara e geral);
* **4 -** _Sistemas que pensam racionalmente_.

Um **agente** é algo que tem perceção do ambiente através de sensores e que pode agir sobre esse ambiente através de atuadores. Um **agente racional** é o que toma a decisão correta, ou seja, o seu desempenho melhora na tarefa que realiza. Uma **medida de desempenho** contém o critério de sucesso relativo ao comportamento de um agente, devendo ser desenhada de acordo com o que se pretende que aconteça no ambiente ao invés do que se pensa ser o melhor comportamento do agente.

Num dado instante, uma **decisão racional** depende da medida de desempenho, do conhecimento que o agente tem do ambiente, das ações que o agente pode executar e da sequência de observações realizadas pelos sensores do agente até ao instante atual. Para cada sequência de observações possível, um **agente racional** deve escolher a ação que se espera que maximize a sua medida de desempenho, dadas as observações realizadas e o conhecimento adquirido pelo agente.

Os ambientes de tarefa devem ter: a medida de desempenho, o ambiente da tarefa, os atuadores e os sensores do agente. Quanto mais restrito for o ambiente de atuação, mais fácil é o problema. Um ambiente é:
* **Totalmente observável** (se os sensores do agente tiverem acesso a todo o estado do ambiente em cada instante) ou **parcialmente observável** (existência de ruído, mau funcionamento ou inexistência de sensores);
* **Determinístico** (se o estado do ambiente no instante seguinte for determinado pelo estado atual e pela ação do agente) ou **estocástico** (caso contrário);
* **Episódico** (se as ações num episódio não influenciam as de outro) ou **sequencial** (se todas as ações influenciam o estado);
* **Dinâmico** (se o ambiente mudar enquanto há decisão) ou **estático** (caso contrário);
* **Discreto** (se o problema tem estados discretos) ou **contínuo** (caso contrário);
* **Agente único** ou **multi-agente**.

| Problema | Totalmente Observável | Determinístico | Episódico | Estático | Discreto | Agente Único |
| --- | --- | --- | --- | --- | --- | --- |
| Palavras Cruzadas | Sim | Sim | Não | Sim | Sim | Sim |
| Robô de Peças     | Não | Não | Sim | Não | Não | Sim |
| Táxi Automático   | Não | Não | Não | Não | Não | Não |
| Xadrez            | Sim | Sim | Não | Sim | Sim | Não |
| Monopólio         | Sim | Não | Não | Sim | Sim | Não |

Um **agente reflexivo** escolhe a ação a executar com base na observação atual, sem contar com as observações feitas anteriormente (segue uma regra _condição-ação_). Um **agente reflexivo baseado em modelo** deve manter um estado interno onde armazene informação dependente das observações passadas, que é atualizada com base no funcionamento do mundo independentemente das observações e na influência das ações do agente no mundo - **modelo**.

![](https://i.imgur.com/cX2s8It.png)

![](https://i.imgur.com/8wRNB2m.png)


Um **agente com objetivo** combina a informação acerca das suas possíveis ações com o seu objetivo para decidir a ação a tomar, precisando por vezes de executar uma longa sequência de ações para o atingir.

![](https://i.imgur.com/kL9Czpe.png)


Um **agente com utilidade** escolhe o **estado** (representação de um instante no mundo em que o agente se encontra) mais favorável. Uma **função de utilidade** faz corresponder a um estado um número real que indica o respetivo grau de utilidade, utilizado quando existem objetivos contraditórios para encontrar um equilíbrio e quando existem objetivos múltiplos e não se sabe se é possível atingi-los.

![](https://i.imgur.com/WP27SLi.png)


Um **agente que aprende** aprende sozinho as melhores ações a tomar em cada situação, permitindo a sua atuação em ambientes inicialmente desconhecidos onde se torna gradualmente mais competente. Tem **elementos de aprendizagem** (melhoram comportamentos do agente), **elementos de desempenho** (selecionam as ações a tomar), **críticos** (indicam como o agente se está a comportar e como deve ser alterado o elemento de desempenho) e **geradores de problemas** (sugerem ações e permitem que o agente se comporte de forma sub-ótima de forma a poder, a médio prazo, atingir melhores resultados).

![](https://i.imgur.com/xVHJtG0.png)

Os agentes devem tentar maximizar a sua medida de desempenho, examinando diferentes possíveis sequências de ações que levam a estados de valor conhecido para decidir a melhor sequência: **pesquisa**. Para tal, é necessário:
1. _Definir o problema_:
    * Um problema pode ser **real** ou **artificial** e é definido por:
        * Estado inicial;
        * Descrição das ações possíveis - função sucessor (`suc(x)`), que recebe estados e devolve pares do tipo `(ação, estado)`, que mostram o estado atingido partindo do estado inicial seguindo determinada ação;
        * Teste de objetivo - avaliação de um determinado estado para confirmar se é o estado objetivo;
        * Função de custo do caminho - atribuição de valores numéricos a cada caminho;
    * Através do estado inicial e a função sucessor define-se implicitamente o **espaço de estados** do problema (conjunto de todos os estados que se podem alcançar a partir do estado inicial, usando qualquer sequência de ações), que forma um **grafo** em que os nodos são estados e as arestas são ações. Um **caminho** é uma sequência de estados ligados por uma sequência de ações, e o **custo** é o custo de ir entre dois estados com uma determinada ação;
    * A **solução** de um problema é um caminho do estado inicial ao estado objetivo, cuja qualidade é definida pelo custo do caminho, e diz-se **ótima** se for a que tem menor custo;
2. _Formular o objetivo_;
3. _Pesquisar a solução_:
    * Uma **árvore de pesquisa** é uma estrutura de dados em que o estado inicial é a raiz, à qual se acrescentam os nodos correspondentes aos estados obtidos a partir de cada ação possível (**expansão**), cujo caminho ótimo é calculado através de uma **estratégia de pesquisa**:
        * **Não informada** - quando a única informação disponível é a presente na definição do problema:
            * _Pesquisa primeiro em largura_ (**PPL**) - expansão de todos os nodos num dado nível antes de prosseguir a expansão aos nodos do nível seguinte. É completa se o fator de ramificação é finito e ótima quando o custo do caminho é uma função não decrescente da profundidade do nodo;
            * _Pesquisa primeiro em profundidade_ (**PPP**) - expansão de cada nodo até que se atinja a maior profundidade;
            * _Pesquisa primeiro em profundidade com profundidade limitada_ (**PPP-PL**) - a pesquisa só atinge uma dada profundidade pré-definida. É útil para árvores de pesquisa não equilibradas, mas corre-se o risco de explorar profundidades muito grandes;
            * _Pesquisa primeiro em profundidade com profundidade iterativa_ (**PPP-PI**) - a profundidade da pesquisa é variável com graduação. Tem requisitos de memória reduzidos, é completa quando o fator de ramificação é finito e ótima quando o custo do caminho é uma função não decrescente da profundidade do nodo;
            * _Pesquisa bidirecional_ (**PB**) - são feitas duas pesquisas, uma com início no estado inicial e outra com início no estado objetivo através uma função predecessor (`pred(x)`) que devolve o estado anterior ao estado `x`. É completa se o fator de ramificação for finito e ótimo se as ações tiverem o mesmo custo (ambas as pesquisas devem ser em largura);
        * **Informada** - utilizam conhecimento específico do problema para permitir a descoberta de solução de forma mais eficiente, definindo se um estado é melhor que outro:
            * _Pesquisa melhor primeiro_ (**PMP**) - o nodo a expandir é escolhido em função do valor dado por uma **função de avaliação** que dá uma estimativa do custo associado, expandindo-se o de menor custo. Há vários algoritmos dependendo da **função heurística** (componente da função de avaliação que estima o custo do caminho mais barato do nodo inicial até ao objetivo);
            * _Pesquisa melhor primeiro gulosa_ (**PMPG**) - o nodo a expandir é o que estiver mais próximo do nodo objetivo. Não é completa nem ótima;
            * _Pesquisa A estrela_ (**PA***) - a função de avaliação usa também o custo do caminho para chegar ao nodo objetivo vindo do ponto inicial. É ótima se a função heurística for **admissível** (nunca sobrestima o custo de atingir o objetivo);
    * A **qualidade dos métodos de pesquisa** podem ser medidos por:
        * _Completude_: se o algoritmo for sempre capaz de encontrar a solução;
        * _Otimização_: se o algoritmo for sempre capaz de encontrar a solução ótima;
        * _Complexidade espacial_: espaço necessário em memória RAM para a execução do algoritmo;
        * _Complexidade temporal_: tempo necessário para a execução do algoritmo;
4. _Executar a solução_.

Na teoria dos jogos, **ambientes multi-agente** (cooperativo ou competitivo) são considerados um jogo desde que o impacto de cada agente sobre os outros seja significativo. Os jogos passam-se num ambiente determinístico e totalmente observável, com dois agentes de ações executadas de forma alternada e com os valores da função de utilidade no final de valores iguais e de sinal oposto (soma final nula). Um jogo pode ser definido como um **problema de pesquisa** com:
* _Estado inicial_ - posições no tabuleiro e jogador que irá começar;
* `jogador (s)` - jogador que joga no estado `s`;
* `acoes (s)` - conjunto de jogadas possíveis no estado `s`;
* `resultado (s, a)` - estado resultado de fazer a ação `a` no estado `s`);
* `estado_terminal (s)` - verdadeiro quando `s` é um estado terminal e falso quando contrário;
* `utilidade (s, j)` - função objetivo; atribui um valor numérico ao estado terminal `s` para o jogador `j`.

Uma estratégia é **ótima** se levar a um resultado de MAX pelo menos tão bom quanto o alcançável se MIN fosse infalível. Pode ser obtida ao examinar o **valor minimax** de cada nodo (`MINIMAX (s)`), que corresponde à utilidade para MAX desse nodo assumindo que ambos os jogadores jogam de forma ótima. MAX prefere um movimento para um nodo de valor minimax máximo, ao passo que MIN prefere um nodo com valor minimax mínimo. O algoritmo `minimax` gera todo o espaço de pesquisa para encontrar a decisão minimax a partir do nodo atual de modo recursivo. Usa PPP e se a maior profundidade da árvore for `p` e existirem `b` jogadas legais, a complexidade temporal é `O(b^p)`.

O algoritmo `poda alfa-beta` permite eliminar parte do espaço de pesquisa, removendo ramos da árvore que não podem influenciar a decisão. Vai atualizando os valores `α` e `β` enquanto percorre a árvore e remove os restantes ramos num nodo assim que o seu valor for pior que o valor atual de `α` ou `β`, consoante o jogador (MAX ou MIN).

Em 1950, Shannon sugeriu que os programas deviam terminar a pesquisa antes de chegarem aos nodos folha e usarem uma função de avaliação heurística para estimar a utilidade do nodo. Os algoritmos `minimax` e `poda alfa-beta` são então alterados:
* Substituição da função de utilidade por uma função de avaliação heurística, `EVAL`, que estima a utilidade do nodo. Devolve uma estimativa para a utilidade do jogo a partir de uma dada posição e deve ordenar os estados terminais como a função de utilidade verdadeira, ser rápida e fortemente correlacionada com a probabilidade de vitória para estados não terminais;
* Susbtituição da função de terminação por um **teste de corte** que decide quando se deve usar `EVAL`.

A pesquisa é interrompida, ou definindo uma profundidade máxima `p`, escolhida de forma a que nunca se exceda a quantidade de tempo disponível no jogo, ou aplicando a profundidade iterativa.

Em jogos com nodos aleatórios, devem incluir-se nodos aleatórios na árvore de pesquisa. Calcular o **valor esperado** pela função `expectiminimax`, que generaliza o valor minimax para jogos com nodos aleatórios.

Uma dada representação de conhecimento tem associado um equilíbrio que é preciso gerir: _mais expressividade implica normalmente maior complexidade_.

Na lógica proposicional, as conclusões são obtidas usando uma **regra de inferência**. A lógica de primeira ordem amplia as capacidades da lógica proposicional (factos) com a inclusão de objetos e relações para comparar gramáticas. O conceito de **categoria** permite agrupar vários objetos dentro de uma só entidade e é fundamental para a representação de conhecimento. Categorias podem ser **predicados** e **objetos**.

Uma outra forma de representar conhecimento é a partir de **regras** do tipo _se-então_, usadas tipicamente nos **sistemas periciais** (domínios muito específicos onde existem peritos humanos, divididos em dois subsistemas: base de conhecimento (BC, guarda factos e regras) e motor de inferência). `Se X então Y`, sendo `X` a _condição_ e `Y` o _consequente_. Nos sistemas periciais, uma regra dispara se a condição for verdadeira e pode ser feita **dedução** (cada consequente é um novo facto) ou **reação** (cada consequente é uma ação). Permite: regras de formato intuitivo cujas conclusões podem ser explicadas; facilidade de manutenção (não é necessário escrever código para alterar as regras); facilidade e rapidez na criação de protótipos. No entanto, é necessária a obtenção de conhecimento (o tempo de peritos é valioso). Os sistemas periciais devem ser usados quando faça sentido economicamente, peritos humanos não estejam sempre disponíveis, o problema requeira raciocínio simbólico.

Uma **rede semântica** é um grafo que representa relações semânticas binárias entre conceitos, objetos e categorias, num processo de inferência simples e transparente. São pesadas computacionalmente (exigem travessia das redes), têm falta de capacidade de expressão (quantificadores, negação, ...). Uma **ontologia** é uma representação de entidades e das suas relações em linguagens próprias que pode ser representada num grafo, composta por:
* **Indivíduos** - instâncias ou objetos;
* **Classes** - conjuntos, coleções de conceitos, propriedades ou parâmetros de objetos ou classes;
* **Atributos** - aspetos, características, propriedades ou parâmetros de objetos ou classes;
* **Relações** - formas segundo as quais indivíduos e classes se relacionam;
* **Restrições** - descrições formais que devem ser verdadeiras para que uma dada afirmação seja aceite;
* **Regras** - afirmações _se-então_ que descrevem uma inferência lógica;
* **Axiomas** - afirmações (incluindo regras) que contêm toda a teoria descrita pela ontologia;
* **Eventos** - alterações de atributos ou relações.

Uma rede semântica é uma _notação gráfica_ usada para representar conhecimento com os nodos e as arestas de um grafo; uma ontologia é a representação de conceitos dentro de um domínio e das suas relações de forma explícita e formal, que pode ser visualizada como um grafo.

Uma **_semantic web_** é uma extensão da _web_ que possibilita a partilha de dados entre aplicações, empresas e comunidades, adicionando meta-dados às páginas _web_ em formatos legíveis por máquinas. A **_Resource Description Framework_** (RDF) é uma família de especificações que permite representar conhecimento sob a forma de expressões sujeito-predicado-objeto (_triplo_), em que o sujeito representa um recurso e o predicado representa a relação entre o sujeito e o objeto. A **_Web Ontology Language_** (OWL) é uma linguagem que permite escrever ontologias, adicionando semântica e sistemas de raciocínio automático (classificadores).

Uma base de dados é ótima para guardar informação quando as características (atributos) a guardar relativas aos dados são conhecidas e estáveis; em IA, o conhecimento vai sendo guardado à medida que é adquirido.

**Inferência** é o processo de derivação de novo conhecimento a partir de conhecimento já existente (na IA, _motor de inferência_). No **raciocínio dedutivo**, nova informação é deduzida a partir de informação com relação lógica. No **raciocínio indutivo**, generaliza-se a partir de um conjunto de observações. O **raciocínio abdutivo** permite inferência plausível. A **analogia** permite comparações entre duas situações. **Senso-comum** é um raciocínio informal que usa regras aprendidas pela experiência (heurísticas). **Raciocínio não-monótono** é usado quando os factos podem mudar.

**Lógica** pode não ser _prática_ (impossível listar todas as possíveis causas e consequências de uma regra), tem _ignorância_ (desconhecimento de algumas causas e consequências), _incerteza_ (regras não aplicáveis a todos os casos). O agente só consegue ter um dado grau de certeza, e não a certeza absoluta do que se está a passar - pelo que se recorre às **probabilidades**. As afirmações probabilísticas dizem respeito ao estado de conhecimento, e não ao que se passa na realidade.

Tem de se ter em conta a utilidade do estado que resulta de uma ação. A **teoria da utilidade** diz que cada estado tem um dado grau de utilidade e que o agente deve preferir estados com maior grau de utilidade, sendo que a utilidade depende do agente. Para que o agente possa tomar a sua decisão, deve ter em conta a probabilidade de uma dada ação o levar a um estado desejado e a utilidade do estado que resulta dessa ação. Um agente é **racional** se e só se escolher a ação que tem maior utilidade esperada.

O conjunto de todos os resultados possíveis chama-se **espaço amostral** `S`, de onde qualquer subconjunto é chamado **acontecimento**. Para cada acontecimento `A` define-se um número chamado a probabilidade do acontecimento `A`, `P(A)`, que obedece às condições `0 <= P(A) <= 1`, `P(S) = 1`, para qualquer sequência de eventos mutuamente exclusivos, a probabilidade da união dos acontecimentos é igual à soma das probabilidades de cada elemento.

A **base de conhecimento** é a distribuição conjunta dos acontecimentos que estão envolvidos no mundo em consideração. A probabilidade relativa a uma única variável, **probabilidade marginal**, é obtida somando os valores de todos os eventos em que ela está envolvida.

A **regra de Bayes** permite descobrir a probabilidade de uma dada causa estar por trás de um efeito: `P(causa|efeito) = (P(efeito|causa) * P(causa)) / P(efeito)`. A probabilidade `P(efeito|causa)` é na **direção da causa** (a partir de uma causa, procurar o efeito); a probabilidade `P(causa|efeito)` é na **direção do diagnóstico** (a partir de um efeito, saber a causa).

A **independência condicional** de duas variáveis `X` e `Y` dada a variável `Z` é `P(X, Y|Z) = P(X|Z) * P(Y|Z)`, permitindo que sistemas de inferência que lidam com `n` variáveis booleanas escalem com `O(n)` em vez de `O(2^n)`, já que é mais fácil ter a informação relativa a independência condicional que a independência absoluta.

**Video Explicativo:** ` https://www.youtube.com/watch?v=PGaxIKVP4ao `

Uma **rede bayesiana** é um grafo dirigido que contém informação probabilística em cada nodo:
* Cada nodo corresponde a uma variável aleatória (discreta ou contínua);
* Uma aresta do nodo `X` para o `Y` significa que `X` é o pai de `Y` (`X` influencia `Y`);
* O grafo não tem ciclos;
* Cada nodo `X_i` guarda a distribuição probabilística condicional `P(X_i | Pais (X_i))` que quantifica os efeitos dos pais no nodo em causa.

Após se ter as causas e respetivos efeitos, que constroem a topologia da rede bayesiana, basta determinar as probabilidades condicionais a colocar em cada nodo, descobrindo a distribuição conjunta para todas as variáveis. Se um nodo tem `m` nodos pai que são variáveis booleanas, então a sua probabilidade condicional pode ser representada numa tabela com `2^m` entradas. Nodos que não estão ligados na rede bayesiana são **nodos condicionalmente independentes**.

A probabilidade conjunta é obtida por `P (x_1, ..., x_n) = i=1_Π^n P (x_i | Pais (X_i))`.

Na construção de uma rede bayesiana, os **nodos** são o conjunto de variáveis necessárias para modelar o domínio, `{X_1, ..., X_n}`, ordenados de modo a que as causas apareçam antes dos efeitos. As **arestas**, para cada `i`, escolhe-se em `{X_1, ..., X_(i - 1)}` os pais que tornem a equação `P (X_i | X_1, ... X_(i - 1) = P(X_i | Pais(X_i))` válida, e cria-se uma ligação entre eles.

Uma rede bayesiana **não tem valores redundantes**, logo, não tem inconsistências.

**Algoritmos de Monte Carlo** são métodos de amostragem aleatória que fornecem aproximações baseadas na geração de muitas amostras aleatórias. Os métodos MCMC (_Markov Chain Monte Carlo_) geram cada nova amostra fazendo uma alteração aleatória na amostra anterior.

O **lençol de Markov** (LM) de uma variável aleatória inclui os seus pais, filhos, e os outros pais dos seus filhos.

Para obter uma amostra para `X_i`, apenas se tem em conta os valores das variáveis que pertencem ao seu lençol de Markov. A **amostragem de Gibbs** parte de um estado em que as variáveis observadas têm os seus valores fixos e gera um novo estado, mudando de forma aleatória o valor das restantes variáveis. Em cada iteração, escolhe-se uma variável `X`, calcula-se `P (X = verdade | LM(X))` e atribui-se a `X` verdadeiro a probabilidade calculada.

---

`final de matéria para frequência 1`

---

O Agente pode aprender através de aprendizagem:

 * **Não supervisionada**
    * o agente aprende padrões das entradas, sem receber informação do _feedback_: _clustering_ ou agrupamento de dados.

 * **Supervisionada**
    * o agente recebe pares de entrada-saída e *aprende a relação existente entre eles*, podendo depois usar a relação aprendida para estimar os valores de saída de novos dados quando recebe apenas as entradas.
    
    * **Recebe** um **conjunto de treino** com `N` pares entrada-saída -> **estima** a relação `y = f(x)` -> **formula** uma **hipótese** `h` tal que `h` aproxima a verdadeira relação `f`, passando então a ser uma pesquisa no **espaço de hipóteses**

    * Quando os valores de `y` pertencem a um conjunto finito, diz-se que o problema é de **classificação**;

        * **Máquinas de vetores de suporte**
            * As **máquinas de vetores de suporte** (MVS, 1995) têm algumas propriedades interessantes:
                * Constroem uma fronteira de decisão que tem a margem máxima em relação aos pontos do conjunto de treino;
                * Conseguem obter fronteiras de decisão complexas construindo um separador linear num espaço de maior dimensão que o de entrada;
                * São resistentes ao sobre-ajuste.

            * Em vez de minimizar o *erro empírico*, as MVS tentam minimizar o *erro de generalização* ao escolher o plano separador que esteja mais afastado dos pontos vistos até ao momento: **separador de margem máxima**. A **margem** é o dobro da distância entre o separado e o ponto mais próximo.

            * A solução para achar os pesos que permitem construir o plano separador pode ser obtida resolvendo: `arg max α ∑j (αj - 0.5 ∑j,k (α αj k yjyk (xj · xk)))` onde αj ≥ 0 e Pj αjyj = 0.

            Há 3 características importantes na equação:
            * É uma **expressão convexa**: tem apenas uma máximo global que pode ser encontrado de forma eficiente;
            * Os dados só aparecem em produtos de pares de pontos;
            * Os pesos aj associados aos pontos são zero menos nos **Vetores de Suporte**: Os pontos mais perto do separador

        * **aprendizagem bayesiana (Máximo à posteriori)** - Calcula a probabilidade de cada uma das hipóteses, face aos dados disponíveis, e efetua a previsão de acordo com essas probabilidades. Seja `d` uma sequência de dados `{d_1, d_2, ..., d_n}` e `m` o número de hipóteses, a probabilidade de cada hipótese `h_i` face aos dados recebidos é dada pela regra de Bayes (probabilidade *a posteriori*): `P(h_i|d) = P(d, h_i) / P(d) = P(d|h_i)P(h_i) / m^Σ_j=1 P(d|h_j)P(h_j)` (1). As previsões são feitas usando as previsões de cada uma das hipóteses pesadas pelas suas probabilidades: `P(d_n+1|d) = m^Σ_i=1 P(d_n+1|h_i)P(h_i|d)` (2). 
        
        * A **verosimilhança** dos dados em face de cada hipótese é `P(d|h_i)= n^Π_j=1 P(d_j|h_i)` (3). A previsão bayesiana é ótima no sentido em que, dado o mesmo vetor de dados *a priori*, qualquer outro método de previsão vai acertar menos vezes.

        A aproximação mais frequente é fazer a previsão com base apenas na hipótese mais provável em vez de fazer a soma pesada de (2). Acham-se as probabilidades `P(h_i|d)` por (1), podendo ignorar-se o denominador, escolhe-se a hipótese `h_i` que tenha maior valor de `P(h_i|d)`, `h_i^*`, e faz-se a previsão com  `P(d_n+1|d) = P(d_n+1|h_i^*`: **máximo *a posteriori*** (MAP).

        A **máxima verosimilhança** (MV) permite simplificar ainda mais a previsão ao assumir que todas as hipóteses são igualmente prováveis *a priori*. Acham-se as probabilidades `P(d|h_i)` por (3), escolhe-se a hipótese `h_i` que tenha maior valor de `P(h_i|d)`, `h_i^*`, e faz-se a previsão com  `P(d_n+1|d) = P(d_n+1|h_i^*`.

        * **Naive Bayes** - Usa muito do que se viu atrás para construir um classificador partindo do princípio que os atributos são condicionalmente independentes uns dos outros. A probabilidade *a priori* de cada classe, `P(C)`, é facilmente achada contando o número de pontos que pertencem a cada classe e dividindo pelo total de pontos no conjunto de treino. Permite lidar com problemas com muitos atributos (número de parâmetros cresce linearmente com o número de atributos do problema), é computacionalmente eficiente e lida bem com o ruído.

            **Vantagens do Naive Bayes**
                * Consegue lidar bem com problemas de muitos atributos: o número de parâmetros que usa **cresce linearmente** com o número de atributos do problema;
                * Computacionalmente eficiente;
                * Lida bem com o ruído

        * O classificador **k-NN** (*k-nearest neighbour*) acha a distância de A a todos os pontos do conjunto de treino (aos quais se conhece a verdadeira classe) e classifica na classe mais comum entre os `k` pontos do conjunto de treino mais próximos de A.

            * Dependendo do valor K o ponto pode ser classificado de diversas formas. No caso de existir um empate, sorteia-se a classe a atribuir de entre as que empataram. No caso de um problema de 2 classes e para evitar empates, usa-se um valor de k impar.

    * Quando os valores de `y` pertencem a um conjunto infinito, diz-se que o problema é de **regressão**.

        * **Regressão linear**
        * **regressão logística**

    Para estimar quão bom será o desempenho da hipótese criada pelo nosso agente, usa-se um novo conjunto de dados, **conjunto de teste**, que não terá valores em comum com o conjunto de treino.

    * É escolhida a hipótese `h* = arg max (h ∈ H) P (h | dados)`, onde `H` é o espaço de hipóteses.

    * Uma hipótese diz-se **consistente** se estiver de acordo com todos os dados do conjunto de treino.

    * **Navalha de Ockham** - Quando temos várias hipóteses, qual escolher? A mais simples!!!

    Para escolher o espaço de hipóteses, deve-se usar conhecimento _a priori_ para tentar descobrir um espaço que contenha uma hipótese consistente ou que seja o mais vasto possível (para se ter a certeza de encontrar hipóteses consistentes). Deve alcançar-se um equilíbrio entre a **expressividade** do espaço de hipóteses e a **complexidade** de encontrar nesse espaço uma hipótese consistente.
    
    * Uma **árvore de decisão** recebe como entrada um vetor de atributos `x` e devolve uma decisão `y`, o valor previsto para a entrada que recebeu. Chega à decisão através de uma **sequência de testes**: cada nodo não terminal da árvore corresponde a um teste do valor de um dos atributos e as arestas que saem do nodo são etiquetadas com os valores possíveis do teste; cada folha da árvore especifica a decisão a devolver se se atingir essa folha. A ideia básica do algoritmo para induzir árvores de decisão é começar por testar primeiro os atributos mais importantes (aqueles que fazem maior diferença na classificação de um ponto, ou seja, apresentam maior ganho de informação).

        * Um algoritmo de aprendizagem é bom se produzir hipóteses que conseguem prever a classe de pontos nunca vistos, através de um conjunto de teste numa **validação cruzada**, em que são utilizados todos os pontos tanto no treino como no teste, mas nunca em simultâneo:
        1. Recolher conjunto de dados com número de pontos `n`;
        2. Escolher o número de vezes, `k`, que se irá dividir os dados;
        3. Dividir os dados em conjuntos disjuntos: de treino com `n - n/k` pontos e de teste com os restantes `n/k` pontos;
        4. Aplicar
        5. Aplicar h ao conjunto de teste e calcular a proporção de acertos.
        6. Repetir os passos 3 a 5, k vezes, nunca usando para teste pontos já usados em repetições anteriores.

        Neste processo, são usados todos os pontos tanto no treino como no teste, mas **nunca simultaneamente**

        Se usarmos `k = n` temos a forma de avaliação chamada _leave-one-out_, em que se treinam todos os pontos exceto um (usado para teste) e repete-se o processo `n` vezes: é a forma ideal de avaliação mas normalmente é muito demorada.

        Como referido anteriormente, se aumentarmos o conjunto de treino, os modelos têm melhores resultados.

        **Sobre-ajuste** (_overfitting_) - o algoritmo de aprendizagem está a tirar partido dos atributos que são todos irrelevantes para este problema e a criar hipóteses que são consistentes mas que não irão generalizar bem. Quando o espaço de hipóteses é muito grande, corre-se o risco de **memorização** dos dados de treino sem que se consiga obter uma boa hipótese _h_ (generalização). Para saber se um atributo é ou não relevante, pode usar-se o ganho de informação pela **entropia**.

        Uma forma de **evitar o sobre-ajuste** consiste em usar a **Poda**. A ideia é não permitir que, os atributos que não são relevantes gerem sub-árvores.

        Para medirmos informação, usamos a **entropia**: se existirem n possíveis respostas a uma questão, cada uma com probabilidade P(ai) de ocorrer, a quantidade de informação que uma resposta fornece é dada por `E(P(a1), P(a2), ..., P(an)) = -∑(i=1 até n) P(ai) log2 P(ai) bits`. Nesse sentido a entropia decresce quando adquirimos mais informação, pois ela é uma medida da incerteza de uma variável aleatória.

        Imaginemos o **lançar duma moeda ao ar**: o resultado de cada lançamento irá dar-nos um bit de informação no caso em que a moeda não está viciada. Vai permitir responder à questão: irá sair cara? (com um sim ou não).

        O **ganho de informação** obtido com o teste do atributo A é igual à *diferença* entre a informação necessária inicialmente e aquela que passa a ser necessária após o teste: `Ganho(A) = E( p/(p + n), n/(p + n) ) - R(A)` onde `R(A) = ∑(i=1 até v) (pi + ni)/(p + n) * E(pi/(pi + ni), ni/(pi + ni))`. Onde n é o número de pontos cuja classe é Não, p o número de pontos cuja classe é Sim, ni e pi são equivalentes mas agora para os v sub-conjuntos que se criam com as possíveis respostas ao teste do atributo A.

        Em suma, a **noção de ganho de informação** é usada também na *escolha dos atributos mais informativos* durante a construção da árvore: devem ser escolhidos primeiro os testes que envolvem os atributos mais informativos.

        O uso da **poda** permite que as árvores de decisão consigam também lidar adequadamente com eventual ruído que exista nos dados: *quanto mais simples for o modelo, menos se pode ajustar ao ruído*.

        As árvores podadas são mais curtas em média que as não podadas e por isso permitem uma melhor compreensão do processo de decisão (existem menos nodos com testes).

 * **Semi-supervisionada**
    * o conjunto de dados que o agente recebe tem apenas um pequeno subconjunto com os valores de saída e o restante tem apenas valores de entrada.

 * **Por reforço**
    * o agente aprende ao receber recompensas, positivas ou negativas, após realizar ações.

    * **Política** - define o comportamento do agente. Pode ser *estocástica* (num dado estado, a ação a executar depende de uma distribuição probabilística);

    * **Função recompensa** - *define o objetivo do Problema de Aprendizado por Reforço* indicando a recompensa associada a um estado. Define o objetivo do problema, sendo o objetivo do agente maximizar a recompensa total obtida a longo prazo, e pode alterar a política;

    * **Função valor** - indica qual o valor total de recompensa esperado se se partir de um determinado estado: toma em conta os estados seguintes prováveis e as recompensas associadas;

        * Ao contrário da função recompensa, que nos indica o que é bom em termos imediatos, a **função valor** indica o que será *benéfico no longo prazo*.

    * **Modelo do ambiente** - conhecimento anterior interno ao agente sobre o ambiente para tentar prever o estado resultante de uma ação e a respetiva recompensa. 

        * **planeamento**: decidir o conjunto de acções a tomar tendo em vista estados futuros, antes de eles serem efetivamente vivenciados. As abordagens mais avançadas podem usar ambos: aprender por tentativa e erro, criar um modelo e passar a usá-lo para ações futuras.

    * Recebe Feedback: 
        * **Avaliativo** - indica se a ação executada foi boa ou não, não dizendo se é a melhor ou pior possível
        * **Instrutivo (Aprendizagem supervisionada)** - indica qual a ação correta a executar

## Estruturas

Numa **rede neuronal**, os valores das entradas `x_i` num neurónio são multiplicadas por um peso `w_i` e somadas para produzirem uma média pesada `s = n^Σ_i=0 x_i * w_i`, que depois é passada pela **função de ativação**. A saída ou ativação do neurónio obtém-se por **y = f(s)**. 

Existem muitas propostas para f (s), mas uma muito usada é a logística que vimos atrás (também chamada de sigmóide). Neste caso a saída do neurónio obtém-se com: `h_w(x) = logistica(w * x) = 1 / (1 + e^(-w * x))`

Uma rede neuronal com apenas uma camada de neurónios chama-se **percetrão**. As redes neuronais são muito versáteis e podem ser usadas para todos os tipos de aprendizagem (não supervisionada, supervisionada, semi-supervisionada e por reforço).

## Problemas
  * **Bandido de N-Braços**
    * No problema do bandido com n-braços, o agente escolhe entre n ações e recebe recompensas numéricas seguindo uma distribuição de probabilidade. O objetivo é maximizar as recompensas. Cada ação tem um valor médio associado. O agente estima esses valores e escolhe a ação com a estimativa mais alta (**ação gulosa**), balanceando entre (***exploration***) (procurar ações melhores) e ***exploitation*** (usar o conhecimento atual).

    ### Abordagens
      * **ε-gulosa**
        * Indica que, ocasionalmente (em uma pequena proporção de jogadas, ε), em vez de escolher a opção gulosa, seleciona-se uma ação aleatória. Isso ajuda a obter excelentes estimativas dos verdadeiros valores de `Q*(a)` para todas as ações `a`.

      * **não estacionário**
        * No caso **não estacionário** deve alterar-se a forma como se faz a estimativa das recompensas, pensando mais as recompensas mais recentes que as antigas: `Q_t = Q_t-1 + α(r_t - Q_t-1)`, onde `a ∈ [0,1]` é uma constante chamada **passo**. 
            
            * No não estacionário **com política**, a probabilidade de, no instante `t`, estar no estado `s` e escolher a ação `a`, é a política `π_t (s, a)`, que vai sendo ajustada de acordo com a experiência do agente.

## Processamento de Linguagem Natural

É importante que um agente consiga lidar com a **linguagem natural** de modo a poder interagir facilmente com humanos e a poder adquirir conhecimento a partir de textos escritos. Para tal, um **modelo da linguagem** permite a previsão da distribuição de probabilidade das expressões da linguagem.

Uma linguagem pode definir-se como um conjunto de *strings*, para o qual a **gramática** define regras de construção de afirmações válidas. As linguagens naturais são ambíguas, com afirmações a poderem ter mais que um significado, ou seja, o **significado** de uma frase é dado por uma distribuição de probabilidade dos possíveis significados. Além disso, as linguagens formais são muito grandes e estão em constante mudança, o que implica que todos os modelos acabam por ser aproximações.

Chama-se a uma sequência de comprimento `n` um **`n`-grama**, sendo um unigrama um símbolo, um bigrama dois e um trigrama três.

 * **modelo `n`-grama de símbolos** - Cadeia de Markov de ordem `n - 1`. Este modelo permite identificar uma dada linguagem (dado um texto, dizer em que língua está escrito), corrigir erros em editores de texto, classificar o tipo de texto (romance, poesia, jornalístico, ...), reconhecer nomes-entidades.

 * **Modelo `n`-grama de palavras** - Similares aos modelos `n`-grama de símbolos, com a diferença de que o número de palavras é muito maior que o de símbolos: o vocabulário é maior, logo os modelos têm de resolver o problema das palavras fora do vocabulário. São usados para classificação de texto (deteção de *spam*, análise de sentimento).

## Perceção 

A **perceção** interpreta os dados recolhidos pelos sensores do agente para lhe fornecer informação sobre o ambiente. Nalguns casos faz-se *active sensing*: enviar um sinal para o ambiente e recolher os resultados (radar, ultrassons). Uma imagem pode ser representada como uma matriz (ou uma matriz de matrizes) e tem arestas como descontinuidades; a textura é o padrão espacial repetido apresentado numa região da imagem.

(Inserir imagem slide 32)

As operações a realizar sobre imagens digitais podem ser categorizadas em 3 tipos:
 * **nível baixo**: as primeiras normalmente a serem executadas. 
  * **Remoção de ruído** 
  * **Deteção de arestas**
    * *d(i) = I(linha, i + 1) − I(linha, i)*
  * **Análise de texturas** - *Local Binary Patterns*
  * **Cálculo do fluxo ótico.**

 * **nível médio**: segmentação, extração de profundidade, deteção e
remoção de sombras, etc.

 * **nível alto**: aspetos da visão que refletem o uso da memória, contexto
ou intenções. 
  * **Reconhecimento de objetos, locais ou faces**

## Robótica

Os **robôs** são máquinas que se podem caracterizar por possuírem *dois tipos de componentes*:
 * **Sensores** que recolhem informação do ambiente;
 * **Atuadores** que alteram de alguma forma o ambiente (ou a posição do robô no ambiente)
 
Podemos dizer que existem **3 tipos de robôs**:
 * **Manipuladores** tipicamente são braços robotizados, fixos num determinado local;
 * **Robôs móveis** possuem pernas ou rodas;
 * **Manipuladores móveis** combinam as caracteristicas dos 2 tipos anteriores.

A **Localização** é o problema de saber onde se encontram objetos, incluindo o próprio robô.

A forma mais comum de determinar a localização de um robô é por meio de **filtros de partículas**. Cada partícula representa uma possível localização do robô e se movimenta para áreas que são consistentes com as observações dos sensores do robô. Inicialmente, as partículas estão dispersas uniformemente pelo mapa, já que não há informações sobre a posição do robô devido à ausência de observações.

Com o tempo, as *partículas refletem o conhecimento adquirido pelos sensores*, ajustando suas posições para os locais com maior probabilidade de serem a verdadeira posição do robô. Após um período de navegação, poucas posições no mapa estão de acordo com as informações dos sensores, e é nessas posições que as partículas se agrupam.

Frequentemente, os robôs precisam se mover em áreas desconhecidas e criar um mapa do local à medida que se deslocam por ele. A tarefa de criar um mapa do ambiente e ao mesmo tempo se localizar nesse mapa é chamada de **localização e mapeamento simultâneos** (SLAM, em inglês), sendo uma das tarefas mais importantes para os robôs móveis. Existem várias abordagens para realizar o SLAM, e entre as mais bem-sucedidas estão aquelas baseadas em filtros de partículas.

**IA fraca** Propõe a construção de máquinas capazes de agir como humanos, enquanto a IA forte afirma que essas máquinas podem pensar como os humanos. A definição da IA é crucial - considerar um agente capaz de tomar a melhor decisão com recursos disponíveis é viável. No entanto, se limitarmos o agente a um programa em um computador com k bits de espaço, há apenas 2^k programas possíveis, tornando a busca pela melhor solução exaustiva.

**Objeções à IA fraca** Uma objeção importante é o teorema de Gödel, que sugere que a IA, como sistema formal contendo aritmética, estaria limitada por ele. No entanto, isso não diminui o mérito de um sistema, uma vez que os humanos demonstraram inteligência antes da invenção da matemática. Outra objeção, o problema da qualificação, aponta que a complexidade do comportamento humano não pode ser totalmente representada por um conjunto de regras, mas abordagens probabilísticas podem ajudar a modelar comportamentos complexos.

**IA forte** Questiona se as máquinas podem de fato pensar. O teste de Turing é debatido, com algumas objeções levantadas sobre a simulação do pensamento. Turing respondeu a isso, argumentando que é estranho exigir das máquinas o que não exigimos das pessoas, sugerindo que poderíamos presumir a inteligência das máquinas se as víssemos agindo de forma inteligente, da mesma forma que presumimos a inteligência em outras pessoas.

# Ética e o Risco da IA

A construção de inteligência artificial (IA) suscita questões éticas, ponderando-se se o seu desenvolvimento é aconselhável. Os impactos negativos da IA, como perda de empregos, abuso ou falta de responsabilidade, levantam preocupações. Contudo, a IA também pode trazer benefícios, criando empregos mais interessantes e oferecendo mais tempo de lazer.

No entanto, a implementação da IA suscita dilemas éticos, como a responsabilização por erros, questões legais e o uso potencial para fins maléficos, seja na guerra, na perda de privacidade ou no desenvolvimento de sistemas de IA hostis.

Controlar a evolução da IA é crucial para evitar consequências desastrosas. Propostas, como as 3 Leis da Robótica de Isaac Asimov ou a definição de valores que promovam o bem comum, foram apresentadas para garantir que a IA evolua de forma ética e responsável.
