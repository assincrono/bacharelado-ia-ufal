# Introdução à Ciência de Dados

Ciência de dados é uma área interdisciplinar que combina matemática, estatística, programação, técnicas analíticas e conhecimento do domínio para investigar problemas, produzir conhecimento e apoiar decisões.

## Índice

- [Dado, informação, conhecimento](#dado-informação-conhecimento)
- [Fontes, tipos, formatos e estruturas de dados](#fontes-tipos-formatos-e-estruturas-de-dados)
    - [Fontes de dados](#fontes-de-dados)
    - [Tipos de dados](#tipos-de-dados)
    - [Formatos de dados](#formatos-de-dados)
    - [Estruturas de dados](#estruturas-de-dados)
- [Coleta, leitura e acesso a dados](#coleta-leitura-e-acesso-a-dados)
    - [Coleta de dados](#coleta-de-dados)
    - [Leitura de dados](#leitura-de-dados)
    - [Acesso a dados](#acesso-a-dados)
- [Qualidade e compreensão de dados](#qualidade-e-compreensão-de-dados)
- [Principais problemas no pré-processamento de dados](#principais-problemas-no-pré-processamento-de-dados)
    - [Valores ausentes (*missing values*)](#valores-ausentes-missing-values)
    - [Dados duplicados](#dados-duplicados)
    - [Ruídos e erros](#ruídos-e-erros)
    - [Padronização de formatos](#padronização-de-formatos)
    - [Variáveis categóricas (*encoding*)](#variáveis-categóricas-encoding)
    - [Normalização de escalas](#normalização-de-escalas)
- [Seleção de atributos](#seleção-de-atributos)

## Dado, informação, conhecimento

- **Dado:** representação bruta de um fato, sem contexto ou significado próprio.
- **Informação:** dados processados e contextualizados, que passam a ter significado.
- **Conhecimento:** interpretação da informação, que permite compreender uma situação e tomar decisões.

Por exemplo:

| Nível | Exemplo |
|---|---|
| Dado | 8 |
| Informação | O aluno tirou 8 em uma prova com nota máxima 10 |
| Conhecimento | A média da turma foi 6, então o aluno está acima da média, o que indica bom desempenho |

## Fontes, tipos, formatos e estruturas de dados

### Fontes de dados

A fonte é a origem de onde os dados são obtidos para responder a uma pergunta ou apoiar uma análise. Ela pode ser:

- **Primária:** dados coletados especificamente para aquela investigação.
- **Secundária:** dados que já existiam e foram produzidos para outra finalidade.

### Tipos de dados

Os dados são classificados em dois tipos:

- **Quantitativos:** representam quantidades mensuráveis e se dividem em:
    - **Discretos:** valores inteiros, como número de aprovações, de disciplinas cursadas ou de filhos.
    - **Contínuos:** valores que podem ser não inteiros, como peso, altura, temperatura e idade (quando medida com precisão, e não em anos completos).
- **Qualitativos (categóricos):** representam categorias ou características e se dividem em:
    - **Nominais:** categorias sem ordem específica, como cidade de nascimento, curso e modalidade de ingresso.
    - **Ordinais:** categorias com ordem específica, como nível de satisfação (baixo, médio, alto).

### Formatos de dados

O formato é a forma como os dados são armazenados ou entregues. Os mais comuns são:

- **CSV:** texto simples, com valores separados por vírgula ou ponto e vírgula.
- **Excel (XLSX):** planilhas com várias abas.
- **JSON e XML:** formatos hierárquicos, muito usados na troca de dados entre sistemas.
- **Parquet:** formato colunar, eficiente para grandes volumes.
- **Bancos de dados SQL:** dados armazenados em tabelas relacionais, acessados por consultas.
- **APIs:** interfaces que fornecem dados sob demanda, geralmente em JSON.

### Estruturas de dados

Os dados podem ser organizados de 3 formas:

- **Estruturados:** possuem organização claramente definida, em tabelas (linhas e colunas), como planilhas e bancos relacionais.
- **Semiestruturados:** possuem alguma organização, mas sem estrutura tabular rígida, como arquivos JSON e XML.
- **Não estruturados:** não apresentam estrutura previamente definida, como textos, PDFs, imagens e vídeos.

## Coleta, leitura e acesso a dados

### Coleta de dados

A coleta é o ato de obter os dados que serão utilizados na análise. Ela pode ser:

- **Primária:** os dados são produzidos especificamente para o objetivo da análise. Por exemplo, distribuir questionários aos estudantes da UFAL e analisar as respostas.
- **Secundária:** utilizam-se dados que já existem, como os do IBGE ou do "UFAL em números".

### Leitura de dados

Após a coleta, é preciso que uma ferramenta consiga interpretar a estrutura e o conteúdo dos dados. Isso é a leitura: carregar os dados na ferramenta de análise, por exemplo, com `pd.read_csv` em Python (biblioteca pandas).

Como cada fonte costuma entregar os dados em um formato diferente, o passo seguinte é padronizá-los e integrá-los em uma única base, adequada à tarefa de ciência de dados que se pretende realizar.

Imagine uma coleta secundária em que parte dos dados veio de uma API e outra parte de um arquivo CSV. Para trabalhar com eles, é necessário reuni-los em um só lugar, criando uma base consolidada e coerente. Só então é possível acessá-la e conduzir a análise até a conclusão.

### Acesso a dados

O acesso é o meio pelo qual se chega aos dados de uma fonte. Os mais comuns são:

- **Download de arquivos:** a fonte disponibiliza arquivos (CSV, XLSX, JSON etc.) que são baixados e armazenados localmente.
- **APIs:** interfaces que fornecem dados sob demanda, por meio de requisições, geralmente em JSON.
- **Consultas a bancos de dados:** os dados são obtidos com linguagens de consulta, como SQL.
- **Web scraping:** extração automatizada de dados de páginas da web, usada quando a fonte não oferece outra forma de acesso (é preciso verificar os termos de uso do site).

O meio de acesso influencia o formato em que os dados chegam e, portanto, a forma como serão lidos.

## Qualidade e compreensão de dados

A qualidade de dados é o grau em que os dados são adequados ao uso que se pretende fazer deles. Dados de qualidade são suficientemente completos, válidos, únicos, consistentes, acurados e atuais para apoiar uma análise ou decisão.

Ela é avaliada por meio de algumas dimensões:

- **Validade:** verifica se os valores respeitam as regras e os domínios esperados. Por exemplo, uma idade negativa ou uma data com dia 35 são inválidas.
- **Completude:** verifica se os dados estão preenchidos. Um conjunto de dados pode conter valores nulos ou ausentes.
- **Unicidade:** verifica se há registros duplicados. Cada entidade deve aparecer apenas uma vez.
- **Consistência:** verifica se os dados seguem o mesmo padrão e não se contradizem. Por exemplo, em uma coluna de idade, todos os valores devem estar como números inteiros, e não alguns por extenso ("vinte e dois"). O mesmo vale para formatos de data, unidades de medida e valores entre bases diferentes.
- **Acurácia:** verifica se o dado corresponde à realidade. Por exemplo, um aluno cadastrado com 30 anos quando na verdade tem 20 (o valor é válido, mas incorreto).
- **Atualidade:** verifica se o dado ainda reflete a situação atual. Por exemplo, um endereço que estava correto na época do cadastro, mas que já mudou.

Uma dimensão pode falhar sem que as outras falhem. Um dado pode ser válido e consistente, mas inacurado, e por isso a qualidade deve ser avaliada em conjunto.

## Principais problemas no pré-processamento de dados

Os problemas abaixo são os mais comuns no pré-processamento de dados.

| Problema | Descrição |
|---|---|
| **Valores ausentes (*missing values*)** | Campos sem valor em algumas linhas. |
| **Dados duplicados** | Registros repetidos, que dão à informação mais peso do que ela realmente tem e enviesam a análise e o modelo. |
| **Ruídos e erros** | Valores absurdos ou incorretos, como uma idade de 999 anos ou um preço negativo. |
| **Inconsistência de formatos** | A mesma informação escrita de formas diferentes, como "São Paulo ", " sao paulo " e "SP". |
| **Escalas diferentes** | Variáveis com magnitudes muito distintas (como salário e nota de 0 a 10) fazem com que as maiores dominem o resultado em algoritmos sensíveis à escala. |
| **Variáveis categóricas (*encoding*)** | Muitos algoritmos só aceitam entradas numéricas, então categorias como "feminino" e "masculino" precisam ser convertidas. |

Cada problema é detalhado a seguir, junto com as formas usuais de tratá-lo.

#### Valores ausentes (*missing values*)

Há duas famílias de estratégias: eliminar os dados ausentes ou imputar (preencher) valores no lugar deles.

##### Eliminação

- **Remover a coluna:** indicada quando a maior parte dos valores está ausente (como regra prática, mais de 50% a 60%), pois a coluna traz pouca informação.
- **Remover as linhas:** indicada quando poucas linhas são afetadas (como regra prática, menos de 5%), pois a perda de dados é pequena.

Esses limites são referências, não regras fixas, e dependem do tamanho da base e da importância da variável. Entre os dois extremos, costuma-se preferir a imputação. Vale lembrar também que remover linhas pode enviesar a análise quando a ausência tem causa sistemática (por exemplo, um grupo que deixa de responder a certa pergunta).

##### Imputação estatística

Consiste em substituir os valores ausentes por uma medida resumo da própria coluna. A escolha depende do tipo de dado.

**Dados numéricos: média ou mediana**

A escolha depende da distribuição dos dados. A distribuição gaussiana, também chamada de normal, é um modelo de probabilidade contínua em forma de sino, simétrico em torno de uma média central.

<img width="1128" height="363" alt="Distribuição normal (curva em forma de sino)" src="https://github.com/user-attachments/assets/8bbd04f9-dadc-4122-ae62-30539215898d" />

- **Média:** indicada quando a distribuição é aproximadamente simétrica, como a normal.
- **Mediana:** indicada quando a distribuição é assimétrica ou há muitos valores extremos (*outliers*), que distorceriam a média.

**Dados categóricos: moda e alternativas**

Quando existe uma única categoria mais frequente (distribuição unimodal), basta usá-la como moda. Quando não existe (amodal, ou seja, todas as categorias têm a mesma frequência) ou existe mais de uma (bimodal), a moda deixa de ser uma escolha clara. Nesses casos, há as seguintes alternativas:

- **Nova categoria (por exemplo, "Desconhecido"):** é a abordagem mais segura e recomendada, e vale para qualquer variável categórica, especialmente quando não há uma moda clara. Ela evita introduzir vieses artificiais, preserva a incerteza dos dados originais e permite que algoritmos de *machine learning* identifiquem a ausência da informação como um possível padrão.
- **Imputação aleatória proporcional (caso amodal):** quando não é possível criar uma nova categoria, sorteia-se o valor entre as categorias existentes. Como todas têm a mesma frequência, todas recebem a mesma probabilidade. Assim, a distribuição original se mantém, sem inflar nenhuma categoria.
- **Imputação aleatória entre as modas (caso bimodal):** sorteia-se o valor apenas entre as duas modas, preservando o equilíbrio entre elas. É a mesma lógica da estratégia anterior, mas restrita às categorias mais frequentes.

##### Imputação condicional (segmentação)

Em alguns casos, a bimodalidade surge porque há dois subgrupos diferentes misturados na mesma base. A solução é segmentar a base por outra variável (gênero, região, faixa etária etc.) e recalcular a moda dentro de cada subgrupo. O valor ausente é então preenchido com a moda do grupo a que o indivíduo pertence.

Por exemplo, se a moda da coluna "tipo de calçado" está dividida entre salto e tênis, ao segmentar por gênero a moda do subgrupo feminino pode ser salto e a do masculino, tênis.

##### Imputação preditiva

Em vez de olhar apenas para a coluna com valores ausentes, essa abordagem utiliza as demais variáveis da base para estimar o valor que falta. Podem ser usados modelos como o **K-NN** (*K-Nearest Neighbors*), que se baseia nos registros vizinhos, árvores de decisão ou o **MICE** (*Multiple Imputation by Chained Equations*). É a estratégia mais avançada e também a mais custosa, sendo mais indicada quando a variável ausente se relaciona bem com as outras.

#### Dados duplicados

O tratamento de dados duplicados é mais simples que o de valores ausentes e segue três passos:

1. **Identificar** as linhas repetidas, comparando todas as colunas ou apenas um subconjunto delas.
2. **Validar** se são duplicatas reais e não meras coincidências. Duas pessoas podem ter o mesmo nome e a mesma idade sem serem o mesmo registro, por isso a validação deve usar um identificador único, como a chave primária, o ID ou o CPF.
3. **Remover** as cópias, mantendo apenas uma ocorrência de cada registro.

#### Ruídos e erros

O tratamento começa pela detecção e depende da natureza do valor encontrado: um valor impossível é um erro, enquanto um valor apenas extremo pode ser um fenômeno real.

##### Detecção

- **Regras de negócio:** filtros lógicos que definem o intervalo de valores possíveis para cada variável. Por exemplo, em um cadastro de pessoas, `Idade >= 0 e Idade <= 110`. Tudo o que estiver fora do intervalo é marcado como erro. Os limites dependem do contexto: em uma base de estudantes universitários, o intervalo poderia ser bem mais estreito.
- **Métodos estatísticos:** apontam valores atípicos (*outliers*), que ainda precisam ser investigados. Você pode utilizar:
    - **Boxplot**
    - **IQR (intervalo interquartil)**
    - **Z-score**

As regras de negócio identificam valores **impossíveis**, e os métodos estatísticos identificam valores **incomuns**. Um salário de R$ 1.000.000 pode ser os dois ou apenas o segundo, e é isso que a etapa seguinte precisa esclarecer.

##### Tratamento

- **Se for um erro:** Tratar o valor como ausente e aplicar as estratégias vistas em valores ausentes, como a imputação pela mediana do grupo correspondente, ou remover a linha.
- **Se for um fenômeno real:** manter o dado, pois ele representa algo que de fato aconteceu (por exemplo, uma compra muito acima do normal na Black Friday). Nesse caso, é possível usar modelos menos sensíveis a valores extremos.

#### Padronização de formatos

O objetivo é que a mesma informação seja escrita sempre da mesma forma.

1. **Limpeza básica de textos:** remover espaços extras no início e no fim e converter todo o texto para minúsculas (ou maiúsculas), evitando variações como "São Paulo " e "são paulo".
2. **Remoção de acentos e caracteres especiais:** transformar "São Paulo" em "Sao Paulo". Essa etapa deve ser avaliada caso a caso, pois em alguns contextos os acentos distinguem palavras diferentes (como "sábia" e "sabia").
3. **Mapeamento de sinônimos:** criar um dicionário que consolide as variações em um único termo. Por exemplo, "sp", "s.p." e "sao paulo" passam a ser "Sao Paulo". Como o mapeamento depende dos textos já limpos, ele vem depois das etapas anteriores, o que reduz o número de variações a listar.
4. **Datas e números:** unificar as datas em um único padrão, como o ISO 8601 (AAAA-MM-DD), formatos mometários/ponto flutuante devem seguir uma única representação.

#### Variáveis categóricas (*encoding*)

Muitos algoritmos só aceitam entradas numéricas, então as categorias precisam ser convertidas em números. A técnica correta depende do tipo da variável, que já foi visto em "Tipos de dados".

##### 1. Identificar o tipo de categoria

- **Ordinais:** possuem uma ordem natural. Por exemplo, escolaridade: Fundamental, Médio, Superior.
- **Nominais:** não possuem ordem. Por exemplo, cor: Azul, Vermelho, Verde.

##### 2. Aplicar a técnica adequada

- ***Ordinal encoding* (para variáveis ordinais):** atribui números sequenciais respeitando a ordem das categorias. Por exemplo, Fundamental = 1, Médio = 2, Superior = 3. O algoritmo passa a interpretar que Superior é "maior" que Médio, o que é coerente com a natureza da variável.
- ***One-hot encoding* (para variáveis nominais):** cria uma coluna binária (0 ou 1) para cada categoria, também chamada de variável *dummy*. Por exemplo, se a variável cidade tem as categorias Maceió, Recife e Salvador, uma pessoa que mora em Maceió recebe 1 na coluna `Cidade_Maceio` e 0 nas colunas `Cidade_Recife` e `Cidade_Salvador`. Como não impõe ordem entre as categorias, é a escolha adequada para variáveis nominais. Seu custo é o número de colunas, que cresce com a quantidade de categorias.
- ***Target encoding* (avançado):** substitui cada categoria pela média da variável que se quer prever (a variável-alvo) naquela categoria.

#### Normalização de escalas

Variáveis em escalas muito diferentes precisam ser colocadas em uma faixa comparável. Isso é feito em três passos.

##### 1. Analisar a distribuição dos dados

Verificar se a variável segue aproximadamente uma distribuição normal (o "sino" visto em valores ausentes) ou se é assimétrica e tem valores extremos (*outliers*). Essa análise orienta a escolha do método.

##### 2. Escolher o método adequado

- ***Min-max scaling* (normalização):** redimensiona os valores para a faixa de 0 a 1. É indicado para algoritmos baseados em distância (como K-NN) e para redes neurais.
- ***Z-score* (padronização):** transforma os valores para que a média seja 0 e o desvio padrão seja 1. É indicado para algoritmos que assumem dados aproximadamente normais, como regressão linear.

##### 3. Aplicar separadamente em treino e teste

Os parâmetros da transformação (mínimo e máximo, ou média e desvio padrão) devem ser calculados apenas com os dados de treino. Em seguida, esses mesmos parâmetros são aplicados aos dados de teste. Assim, evita-se vazamento de dados (data leakage).

## Seleção de atributos

Selecionar atributos é escolher quais variáveis serão mantidas na análise ou na modelagem, com base na relevância que têm para o problema.

| Técnica | Descrição | Exemplo |
|---|---|---|
| **Conhecimento do domínio** | Remover atributos claramente irrelevantes para o problema, com base no entendimento do contexto. | Ao prever a aprovação de estudantes, remover o ID do registro e o nome do aluno. |
| **Baixa variabilidade** | Excluir variáveis que quase não mudam, pois pouco ajudam a distinguir os registros. | Uma coluna "País" com o valor "Brasil" em 99,9% dos registros. |
| **Excesso de valores ausentes** | Descartar atributos com pouca informação disponível. | Uma coluna "Segundo telefone" com 90% dos valores nulos. |
| **Correlação entre atributos** | Quando dois atributos são muito correlacionados, carregam informação redundante e um deles pode ser removido. | "Altura em cm" e "Altura em m" têm correlação 1, então basta manter uma. |
| **Correlação com o alvo** | Atributos com correlação muito baixa com a variável-alvo tendem a ser menos úteis. | "Número de faltas" tem forte correlação negativa com a nota final, enquanto "número do calçado" tem correlação próxima de zero. |
| **Teste estatístico univariado** | Avaliar individualmente a relação entre cada atributo e o alvo, com testes como ANOVA (atributo numérico e alvo categórico) e qui-quadrado (ambos categóricos). | ANOVA entre "horas de estudo" (numérico) e "aprovado" (sim/não); qui-quadrado entre "turno" (categórico) e "aprovado". |
| **Informação mútua** | Medir o quanto conhecer um atributo reduz a incerteza sobre o alvo. | O risco de certa doença é maior em crianças e idosos do que em adultos. A correlação com a idade fica próxima de zero, mas a informação mútua é alta, pois a idade informa bastante sobre o risco. |
| **Importância de atributos** | Treinar um modelo (como árvore de decisão ou *random forest*) e estimar quais variáveis mais contribuem para as previsões. | Um *random forest* indica que "nota da 1ª prova" e "frequência" são as variáveis mais importantes, e "cidade" contribui quase nada. |
| **Eliminação recursiva (*RFE*)** | Treinar o modelo, retirar o atributo menos útil e repetir o processo até restar o número desejado de atributos. | Partir de 20 atributos e repetir o ciclo (treinar, retirar o menos útil) até restarem 5. |
