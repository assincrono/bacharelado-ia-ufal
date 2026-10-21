# Resumo: Introdução à Inteligência Artificial

> Este resumo foi escrito por IA generativa a partir de uma apostila feita com base no planejamento das aulas (a própria apostila também foi gerada por IA generativa). É IA até o fim. Não reclame comigo, olhe o nome da matéria.


**Apostila do aluno · Bacharelado em Inteligência Artificial, 1º período · UFAL, Instituto de Computação · Semestre 2026.2**

A apostila acompanha os 13 encontros da disciplina, organizados em 6 módulos. Livros-texto de apoio: Brookshear & Brylow (Módulos 1 e 2) e Russell & Norvig, o "AIMA" (Módulos 3 a 6). Cada capítulo traz objetivos, texto, uma frase-resumo e indicações de leitura. Cada módulo termina com exercícios de fixação [F], prática [P] e discussão [D].

**Três conselhos do início:** leia antes do encontro; faça os exercícios no papel antes de ver as respostas; use IA generativa para *estudar*, nunca para responder por você.

---

## Visão geral

| Módulo | Capítulos | Tema central |
| --- | --- | --- |
| 1 | 1–2 | O que é IA; como estudar; o que é um computador |
| 2 | 3–5 | Bits, arquitetura do computador, algoritmos e linguagens |
| 3 | 6–7 | Agentes, busca e conhecimento (IA simbólica) |
| 4 | 8–9 | Aprendizado de máquina e como desenvolver soluções com ele |
| 5 | 10–11 | Linguagem natural, redes neurais e IA generativa |
| 6 | 12–13 | IA no mundo real (ética, carreiras) e Projeto Integrador |

---

## Módulo 1. O que é Inteligência Artificial

### Capítulo 1. O que é (e o que não é) IA

- **Definição de trabalho:** IA estuda como fazer máquinas realizarem tarefas que, nas pessoas, exigiriam inteligência. Há o **efeito IA**: o que a máquina passa a fazer de forma rotineira deixa de ser chamado de "inteligente".
- **Quatro maneiras de definir IA** (AIMA), cruzando *pensar/agir* com *padrão humano/racional*:
  - **Agir como humanos**: Teste de Turing (1950).
  - **Pensar como humanos**: ciência cognitiva e neurociência.
  - **Pensar racionalmente**: tradição da lógica.
  - **Agir racionalmente**: o *agente racional*, abordagem adotada pelo AIMA por ser mais geral e mais fácil de avaliar.
- **Automação rígida × IA:** automação executa regras fixas; IA percebe, aprende e se adapta. O veredito depende de *como o sistema é construído*, não do nome do produto (ex.: um corretor ortográfico pode ser lista fixa ou modelo que aprende).
- **Fundamentos da IA:** filosofia, matemática, economia, neurociência, psicologia, engenharia de computadores, teoria de controle e linguística. Cada um corresponde a disciplinas do curso.
- **História em cinco marcos:**
  1. Fundações (1943–1956): neurônio artificial, Teste de Turing, Dartmouth.
  2. Entusiasmo e primeiros invernos (1956–1980): explosão combinatória e falta de conhecimento do mundo.
  3. Sistemas especialistas (1980–1990): conhecimento em regras; caro e frágil, levando a um segundo inverno.
  4. Retorno dos dados e das redes neurais (1990–2011): aprender com exemplos; Deep Blue em 1997.
  5. Aprendizado profundo e grandes modelos (2012–hoje): LLMs chegam ao público em 2022.
- **Padrão por trás da história:** os **três combustíveis**, *dados, hardware e algoritmos*. Cada avanço combinou os três; cada inverno veio da falta de pelo menos um.
- **Hype × realidade:** a IA faz coisas impressionantes, mas inventa fatos, erra de formas inesperadas e amplifica vieses. A postura do curso: entender o que o sistema faz, como, onde falha e quem é afetado.
- **O curso em três trilhos:** Matemática (a linguagem), Computação (a oficina) e IA (o ofício). Há também iniciação científica, monitoria, extensão (320 h), atividades complementares (240 h) e TCC.

### Capítulo 2. Como se estuda e o que é um computador

- **Estudar para construir competência, não para reproduzir.** Técnicas com evidência científica:
  - recuperação ativa (testar-se);
  - espaçamento;
  - intercalação de assuntos;
  - pedir ajuda cedo;
  - tratar o erro como informação.
- **Ciência da computação = ciência dos algoritmos.** Algoritmo é um conjunto de instruções que define, passo a passo, como realizar uma tarefa. O computador executa o que foi dito, não a intenção.
- **Abstração:** camadas que escondem detalhes da camada de baixo. O bacharel aprende a *descer as camadas* quando preciso (entender por que falhou, criar o que não existe).
- **Máquina de Turing (1936):** fita, cabeçote e tabela de regras. Existe uma **máquina universal** que imita qualquer outra (*o programa é um dado*). A **tese de Church–Turing** afirma que tudo que é mecanicamente calculável é calculável por uma Máquina de Turing: o notebook e o supercomputador diferem em velocidade e memória, não em poder.
- **Arquitetura de von Neumann (1945):** memória guarda dados *e* programa; a CPU busca e executa instruções. Por isso o mesmo aparelho faz tudo.
- **O profissional de IA** é um resolvedor de problemas, que usa **pensamento computacional**: decompor, reconhecer padrões, abstrair e descrever a solução como algoritmo.

---

## Módulo 2. Computação, Matemática e o Computador: por baixo do capô

### Capítulo 3. Tudo é bit

- **Bit é um símbolo, não um número.** Um **código** (convenção) decide o que os bits significam.
- **Operações:** AND, OR, XOR e NOT. As **portas lógicas** são os tijolos do computador. Um somador de 1 bit usa XOR (soma) e AND (vai-um). Realimentação gera o **flip-flop** (guarda 1 bit); a memória é feita deles. **Máscaras** com AND/OR/XOR manipulam bits; XOR duas vezes com a mesma chave devolve o original (cifra mais simples).
- **Base 2:** cada posição vale o dobro da anterior. Converte-se binário→decimal somando posições com 1, e decimal→binário por divisões sucessivas por 2. Soma binária tem "vai um". Deslocar à esquerda multiplica por 2.
- **Hexadecimal:** atalho de leitura (4 bits por dígito, 0–9 e A–F). É só notação compacta para pessoas.
- **Memória:** células de 1 byte com **endereços**. RAM é volátil e rápida; armazenamento em massa (HD/SSD) é persistente, maior e mais lento. Unidades: KB = 2¹⁰, MB = 2²⁰, GB = 2³⁰, TB = 2⁴⁰.
- **Texto, imagem e som viram bits:**
  - **Texto:** ASCII (7 bits), Unicode e UTF-8 (símbolos com 1 a 4 bytes). Mal-entendidos de tabela geram "OlÃ¡".
  - **Imagem:** grade de pixels; RGB usa 3 bytes por pixel (uma foto de 12 MP crua tem ~34 MB; o JPEG, ~3 MB, por compressão).
  - **Som:** amostragem e quantização (CD: ~10 MB por minuto).
- **Lição:** o computador só guarda números; toda IA sobre texto, imagem ou som começa por essa conversão.

### Capítulo 4. Arquitetura e funcionamento do computador

- **Números têm tamanho fixo**, com duas consequências.
  - **Complemento de dois:** representa inteiros negativos (inverter bits e somar 1); subtrair vira somar. **Overflow** ocorre quando o resultado não cabe (ex.: 7 + 1 = −8 em 4 bits; caso do contador do YouTube).
  - **Ponto flutuante:** sinal, mantissa e expoente. Gera **erro de truncamento**; por isso 0.1 + 0.2 = 0.30000000000000004. Os parâmetros de um modelo de IA são floats: um modelo de 7 bilhões de parâmetros em 32 bits ocupa ~28 GB (14 GB em 16 bits), um *trade-off* entre precisão e memória.
- **Componentes:** CPU (ULA, unidade de controle, registradores), RAM, barramento e cache. A analogia do cozinheiro: registradores = mãos, cache = bancada, RAM = despensa, disco = mercado.
- **Linguagem de máquina:** conjunto de instruções (op-code + operando). A apostila usa a máquina didática **MIA-8** (LOAD, STORE, ADD, SUB, JUMPZ, JUMP, HALT). Instruções e dados convivem na mesma memória.
- **Ciclo de máquina:** **buscar → decodificar → executar**, repetido sem parar. Todo `if` e `while` vira saltos.
- **CPU × GPU:** a CPU tem poucos núcleos versáteis; a GPU tem milhares de núcleos simples executando a mesma operação em dados diferentes (SIMD). Redes neurais são, no fundo, **multiplicação de matrizes**, por isso a GPU tornou o aprendizado profundo viável (um dos três combustíveis). Limites: o **gargalo memória–processador** e o **consumo de energia**.

### Capítulo 5. Algoritmos e linguagens de programação

- **Algoritmo (definição formal):** conjunto *ordenado* de passos *executáveis* e *não ambíguos* que define um processo *finito*. Distingue-se a ideia da sua representação.
- **Representação:** primitivas, **fluxograma** e **pseudocódigo**. Sequência, seleção e repetição bastam para escrever qualquer algoritmo.
- **Quatro fases de Polya** para descobrir algoritmos: entender, planejar, executar, avaliar. Ajudam: resolver uma versão menor e trabalhar de trás para frente.
- **Três algoritmos:**
  - **Busca sequencial:** ~n comparações.
  - **Ordenação por inserção:** ~n²/2.
  - **Busca binária:** ~log₂ n (exige lista ordenada; exemplo de recursão; achar 1 nome em 1 milhão leva 20 perguntas).
- **Eficiência:** importa a *forma da curva* (linear, logarítmica, quadrática), não os segundos. Com 1 bilhão de elementos, 30 passos versus 1 bilhão é "instantâneo versus impossível". Testar mostra que funciona nos exemplos; só a **prova de correção** garante que funciona sempre.
- **Linguagens:** máquina → assembly (montador) → alto nível. A tradução é por **compilador** (tudo antes; ex.: C) ou **interpretador** (linha a linha; ex.: Python). Paradigmas: imperativo, orientado a objetos, funcional, declarativo.
- **Por que Python domina a IA** (legível, com bibliotecas como NumPy e PyTorch escritas em C/GPU) **e por que se aprende C primeiro** (mostra a máquina que Python esconde). Nesta disciplina o aluno lê e executa pequenos programas, sem escrever Python.

---

## Módulo 3. Agentes Inteligentes, Busca e Conhecimento

### Capítulo 6. Agentes inteligentes e busca

- **Agente:** percebe o ambiente por **sensores** e age por **atuadores**. A *função do agente* mapeia percepções em ações. Exemplo mínimo: o mundo do aspirador.
- **Agente racional:** escolhe a ação que maximiza a **medida de desempenho esperada**, dado o que percebeu e sabe. Racional não é onisciente. A medida deve refletir o *efeito desejado no ambiente*, não o comportamento imaginado.
- **PEAS:** Performance, Environment, Actuators, Sensors (ex.: táxi automatizado). Propriedades do ambiente:
  - observável (total/parcial);
  - determinístico ou não;
  - estático ou dinâmico;
  - discreto ou contínuo;
  - agente único ou multiagente.

  O mais difícil é parcialmente observável, não determinístico, dinâmico, contínuo e multiagente (como dirigir).
- **Cinco tipos de agente:** reativo simples → reativo baseado em modelo → baseado em objetivos → baseado em utilidade → **agente que aprende** (o de quase toda IA moderna).
- **Busca em espaço de estados:** o problema é formulado por estado inicial, ações, modelo de transição, teste de objetivo e custo de caminho (exemplos: jogo dos oito, mapa/GPS). A **explosão combinatória** impede a força bruta.
- **Estratégias:**

| Tipo | Estratégia | Característica |
| --- | --- | --- |
| Cega | Largura | Acha a solução com menos passos; gasta muita memória |
| Cega | Profundidade | Pouca memória; pode se perder; não garante o menor caminho |
| Cega | Custo uniforme | Garante a solução mais barata |
| Informada | Gulosa | Usa só a heurística h(n); rápida, mas enganável |
| Informada | **A\*** | f(n) = g(n) + h(n); ótima se a heurística for **admissível** (nunca superestima) |

  Uma heurística ruim engana o agente.

### Capítulo 7. Conhecimento, lógica e sistemas especialistas

- **IA simbólica:** raciocina a partir de conhecimento explícito, o que gera **explicações** "de graça" (importante para decisões que a lei exige explicar).
- **Agente baseado em conhecimento:** **base de conhecimento** + **motor de inferência**, interagindo por TELL e ASK. O mesmo motor serve a vários domínios.
- **Mundo de Wumpus:** ambiente parcialmente observável em que o agente deduz posições de poços e do monstro a partir de brisa/fedor.
- **Lógica:** sintaxe, semântica e consequência lógica (correção e completude). **Lógica proposicional** (¬, ∧, ∨, ⇒, ⇔), com atenção à implicação. Tabelas-verdade crescem como 2ⁿ.
- **Inferência:** **modus ponens** e regras SE…ENTÃO (cláusulas de Horn).
  - **Encadeamento para a frente:** parte dos fatos (dirigido por dados).
  - **Encadeamento para trás:** parte da pergunta (dirigido por objetivo).
  - A **árvore de justificativa** é a explicação. Exemplo: regras de aprovação da UFAL.
- **Além das proposições:** **lógica de primeira ordem** (objetos, relações, ∀ e ∃), **redes semânticas** (com herança) e **grafos de conhecimento** (Wikidata).
- **Virtudes:** explicabilidade e garantias. **Limites:** gargalo de aquisição de conhecimento e fragilidade diante de exceções, ruído e incerteza. Esses limites motivaram o aprendizado de máquina. O conhecimento explícito voltou via **IA neuro-simbólica**: os dois paradigmas são complementares, não rivais.

---

## Módulo 4. Aprendizagem de Máquina

### Capítulo 8. Aprender com exemplos

- **Programação clássica:** regras + dados → respostas. **ML:** dados + respostas → regras. Definição de Mitchell: um programa aprende com a experiência **E**, para a tarefa **T**, medida por **P**, se seu desempenho em T melhora com E. O que se aprende é uma função, escolhida no **espaço de hipóteses**.
- **Três formas de aprender:**
  - **Supervisionado:** exemplos rotulados. Dividido em *classificação* ("de que tipo é?") e *regressão* ("quanto?").
  - **Não supervisionado:** sem rótulos, busca estrutura (ex.: agrupamento).
  - **Por reforço:** aprende por tentativa e erro, guiado por recompensas.
- **Generalizar × decorar:** o objetivo é acertar exemplos *novos*. **Sobreajuste** (overfitting): decorou os exemplos, incluindo o acidental. **Subajuste** (underfitting): modelo simples demais. Busca-se o meio-termo (navalha de Occam). O erro de treino sempre cai com mais complexidade; o erro em dados separados cai e depois sobe.
- **Modelos simples:**
  - **Árvore de decisão:** perguntas encadeadas, interpretável; construída escolhendo o atributo que melhor separa os rótulos.
  - **k-NN (vizinhos mais próximos):** vota entre os k exemplos mais próximos; k = 1 sobreajusta, k grande demais subajusta.
  - **Regressão linear:** a reta que minimiza o erro total.
- **Descida do gradiente ("a montanha na neblina"):** sente-se a inclinação do erro (a **derivada/gradiente**) e dá-se um passo na direção que desce. É o motor do ML moderno e a razão de Cálculo e Álgebra Linear estarem no curso. Cuidados: tamanho do passo e a existência de vários vales.

### Capítulo 9. Desenvolvendo soluções com ML

- **Exemplo do banco:** um modelo com 99,9% de acurácia pode não detectar nenhuma fraude se elas são só 0,1% dos casos.
- **Ciclo de um projeto (5 etapas):**
  1. formular o problema;
  2. coletar, avaliar e gerenciar os dados (incluindo engenharia de atributos);
  3. escolher e treinar o modelo (começar pelo mais simples que funcione);
  4. confiança, interpretabilidade e explicabilidade;
  5. operar, monitorar e manter.

  Treinar é a parte menor.
- **Dados ("entra lixo, sai lixo"):**
  - valores faltantes;
  - valores errados;
  - duplicatas;
  - rótulos errados;
  - **viés de amostragem** (examine quem está e quem não está nos dados);
  - **vazamento** (*leakage*): atributo que contém a resposta sem querer; dá resultados espetaculares e falha na vida real.
- **Treino / validação / teste:** o teste é usado **uma única vez**, no fim. A validação cruzada reaproveita dados escassos. O número reportado deve vir de dados nunca vistos.
- **Matriz de confusão** (VP, FN, FP, VN) e métricas:
  - **Acurácia** = (VP+VN)/total (engana com dados desbalanceados);
  - **Precisão** = VP/(VP+FP) (confiabilidade dos alarmes);
  - **Revocação** = VP/(VP+FN) (quanto escapa).

  Os erros têm custos diferentes: não há "melhor modelo" sem dizer qual erro custa mais.
- **Depois do treino:** explicabilidade e verificação com casos extremos fazem parte do sistema. O modelo *envelhece*, então é preciso monitorar e retreinar: lançar é o começo, não o fim.

---

## Módulo 5. Linguagem Natural, Redes Neurais e IA Generativa

### Capítulo 10. Processamento de Linguagem Natural (PLN)

- **Por que é difícil:** ambiguidade, contexto, ironia, metáfora, elipse e variação regional ("Que massa!"). A variação linguística é um **problema de dados** (representatividade).
- **Modelo de linguagem:** distribuição de probabilidade sobre sequências de palavras (qual vem a seguir). Antes dele vem a **tokenização**, que parece trivial e não é; cada token vira um número.
- **Saco de palavras (bag of words):** conta palavras e ignora a ordem; funciona para spam, sentimento e assunto (base do naive Bayes), mas "gostei" e "não gostei" ficam quase iguais.
- **N-gramas (bigramas, trigramas):** a ordem começa a contar. Geram texto localmente plausível, mas globalmente sem sentido: *fluente, mas sem memória e sem entendimento*.
- **Embeddings:** palavras como vetores construídos a partir de seus contextos; proximidade no espaço = semelhança de significado (medida por distância ou similaridade de cosseno). Exemplo: rei − homem + mulher ≈ rainha. Aqui entra Álgebra Linear.

### Capítulo 11. Redes neurais, IA generativa e LLMs

- **Neurônio artificial:** soma ponderada das entradas com limiar. Com pesos 1 e 1, o limiar 1,5 dá AND e o limiar 0,5 dá OR. "Aprender" é ajustar números. Um neurônio não faz **XOR** (separa o plano só com uma reta); é preciso **camadas**, origem do "profundo" em aprendizado profundo.
- **Treinar uma rede:** minimizar o erro por **descida do gradiente**, com funções suaves no lugar do degrau. A **retropropagação** calcula as derivadas. Cada camada é uma multiplicação de matriz por vetor: *a GPU multiplica matrizes, o aprendizado desce gradientes, e a rede neural é onde os dois se encontram*.
- **Modelo de linguagem neural e atenção (Transformer, 2017):** pesos que dependem da própria frase dão memória de contexto longo ("ele" olha para "cachorro"). A fluência local vira coerência de parágrafos.
- **Pré-treinamento:** prever a próxima palavra em bilhões de páginas, sem rótulos (meses de milhares de GPUs). Depois, um ajuste mais barato para instruções e conversa. O chatbot é, no fundo, *um previsor de próxima palavra muito bom*.
- **Fluência não é verdade (alucinação):** o texto mais provável não é necessariamente o verdadeiro. Cuidados:
  - verificar fatos, números e referências;
  - desconfiar da confiança;
  - lembrar do viés;
  - perguntar com contexto;
  - não fornecer dados sensíveis.

  Resposta parcial da engenharia: dar ao modelo documentos confiáveis no contexto (busca + conhecimento + geração), sempre com supervisão humana.
- **Política de IA generativa da disciplina:** pode usar para **estudar**; **declare** o uso nas entregas; **nunca entregue como seu** o que não produziu. O Projeto Integrador tem linha obrigatória de declaração.

---

## Módulo 6. IA no Mundo Real e Projeto Integrador

### Capítulo 12. Ética, pessoas, processos, dados e carreiras

- **Três histórias reais:**
  - triagem de currículos que penalizava mulheres;
  - reconhecimento facial com erro >30% para mulheres de pele escura e <1% para homens de pele clara;
  - IA que detecta retinopatia diabética onde não há especialistas.

  A mesma tecnologia, com resultados opostos: depende de como foi construída, para quem e com que cuidado.
- **Limites e a pergunta filosófica:** a lista de "uma máquina nunca fará X" foi sempre desmentida, mas há limites reais (senso comum, aprender com um exemplo, saber o que não sabe). O **quarto chinês de Searle** questiona se a máquina *entende* ou só manipula símbolos. É preciso separar a pergunta de engenharia da pergunta filosófica.
- **Ética em quatro perguntas:**
  1. **De quem são os dados?** LGPD (Lei 13.709/2018): finalidade, necessidade/minimização, consentimento ou outra base legal, transparência e segurança; dados sensíveis têm proteção reforçada.
  2. **Quem pode ser prejudicado?** As definições de justiça (individual × de grupo) podem ser matematicamente incompatíveis; escolher uma é decisão de projeto.
  3. **Dá para explicar?** Direito a explicação de decisões automatizadas; regras e árvores explicam, redes neurais não.
  4. **Quem responde?** Manter uma pessoa no circuito (*human in the loop*).
- **Por que projetos de IA falham, os três pilares:**
  - **Dados:** que dados existem, de onde vêm e posso usá-los?
  - **Processos:** qual é a pergunta, como medir o sucesso e quem cuida depois?
  - **Pessoas:** quem usa, quem é afetado, quem mantém, e foram ouvidos?
- **Carreiras do bacharel (17 papéis em 5 famílias):** Dados; Engenharia de ML/IA; Pesquisa; Produto e negócios; Governança e ética. Conselhos: iniciação científica (a porta mais subestimada), extensão (320 h) e comunidade (SBC, ENIAC, hackathons).

### Capítulo 13. Projeto Integrador: o guia

- **O que é:** um **diagnóstico**, não uma implementação (sem código nem modelo treinado). Em grupos de 3 a 4, escolhe-se um problema real e responde-se: *que tipo de problema é esse e o que seria preciso para resolvê-lo com IA?* Produto: pôster (A3) ou 6 slides e pitch de 5 minutos na Feira de Diagnóstico.
- **Bom problema:** real, delimitado (cabe em uma pergunta), com dados ou conhecimento imagináveis e de um domínio que o grupo entende.
- **As seis perguntas do pôster:**
  1. Qual é a pergunta? (ficha de formulação: pergunta, sucesso, decisão apoiada, quem decide)
  2. É um problema de IA? De que tipo? (taxonomia abaixo) + especificação **PEAS** e tipo de agente
  3. Que dados ou conhecimento seriam necessários e de onde viriam?
  4. O que pode dar errado? (erros e custos, viés, LGPD, imprevistos, responsabilidade)
  5. Que disciplinas do curso ensinam a resolver?
  6. Declaração de uso de IA (obrigatória, mesmo que seja "não utilizada")

| Tipo de problema | Pergunta típica | Cap. |
| --- | --- | --- |
| Encontrar um caminho (busca/planejamento) | Que sequência de ações leva ao objetivo? | 6 |
| Aplicar regras e explicar | Dadas regras e fatos, qual a conclusão e por quê? | 7 |
| Aprender com exemplos | Dados exemplos resolvidos, como prever o próximo? | 8–9 |
| Entender ou gerar linguagem | Como transformar texto em algo computável, ou vice-versa? | 10–11 |

  Dizer que "isso não é problema de IA" é um diagnóstico válido e valioso.
- **Exemplo abreviado:** prever quais alunos do 1º período têm maior risco de evasão (classificação; agente que aprende; cuidados com vazamento, viés, LGPD e decisão humana).
- **Apresentação e avaliação:** pitch de 5 min (problema 1 → diagnóstico 2 → dados e riscos 1 → o que o curso ensina 1); "não sabemos ainda" é resposta válida. A rubrica tem 4 critérios de peso igual (clareza do problema; diagnóstico; dados, limites e riscos; comunicação e equipe), com avaliação por pares.
- **Calendário:** 01/out escolha do problema · 08/out ficha de formulação · 05/nov diagnóstico preliminar · 12/nov check-in · 19/nov oficina · 26/nov Feira.

---

## Ideias-chave que atravessam a apostila

1. **IA = agentes que agem racionalmente**, alimentados por dados, hardware e algoritmos.
2. **Abstração em camadas:** do bit à IA; o bacharel sabe descer as camadas.
3. **A escolha do algoritmo importa mais que a velocidade da máquina.**
4. **Dois grandes paradigmas, complementares:** simbólico (regras, explicável, frágil) e aprendizado (dados, flexível, opaco).
5. **Aprender = minimizar erro** (gradiente, derivada, GPU e matrizes) e **generalizar, não decorar.**
6. **Medir bem:** dados nunca vistos e métrica que reflita o custo real dos erros.
7. **Fluência ≠ verdade:** verifique, declare o uso de IA e mantenha a autoria.
8. **Dados, processos e pessoas** decidem se um projeto de IA funciona; as **quatro perguntas éticas** devem vir antes do lançamento.

---

## Conteúdo complementar da apostila

- **Mapa do curso:** tabela que liga cada disciplina dos períodos 1º a 9º aos capítulos em que o tema aparece.
- **Exercícios** ao fim de cada módulo, com **respostas dos de número ímpar** no final.
- **Apêndices:** A (tabela ASCII), B (potências de 2 e unidades), C (a máquina MIA-8) e D (glossário).
