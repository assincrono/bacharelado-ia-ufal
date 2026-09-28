# Introdução à Ciência de Dados

Ciência de dados é uma área interdisciplinar que combina matemática, estatística, programação, técnicas analíticas, e conhecimento do domínio para investigar problemas, produzir conhecimento e apoiar decisões.

## Dado, informação, conhecimento

- Dado: Representação bruta de um fato, sem contexto ou significado próprio
- Informação: Dados organizados, possuem significado próprio
- Conhecimento: Interpretação da informação

Por exemplo:

Dado: 8
Informação: O aluno tirou 8 na prova
Conhecimento: O aluno apresenta bom desempenho acadêmico, portanto é bem provável que ele passe de ano

## Fontes, tipos, formatos e estruturas de dados

### Fontes de dados
O nome é auto-explicativo, é a origem de onde os dados são obtidos para responder a uma pergunta ou apoiar uma análise. Uma fonte pode ser:
- Primária: Dados coletados especificamente para aquela investigação
- Secundária: Dados que já existiam e foram produzidos para outra finalidade

### Tipos de Dados

Dados são classificados em dois tipos:

- Quantitativos: Representam quantidades mensuráveis, dados quantitativos são classificados em:
    - Discretos: Valores inteiros, como números de aprovações, disciplinas cursadas, idade etc
    - Contínuos: Inclui valores não inteiros, como peso, altura, temperatura etc
- Qualitativos/Categóricos: Representam categorias ou características, eles podem ser:
    - Nominais: Representam uma característica sem uma ordem específica, por exemplo, cidade onde nasceu, curso, modalidade de ingresso etc
    - Ordinais: Representam uma característica com uma ordem específica, por exemplo, nível de satisfação (baixo, médio, alto) 

### Estruturas de dados

Os dados podem estar organizados em 3 níveis:

- Dados estruturados: Possuem uma organização claramente definida, normalmente em linhas e colunas
- Dados semi-estruturados: Possuem uma certa organização, mas não necessariamente uma estrutura tabular rígida (como um JSON)
- Dados não estruturados: Não apresentam uma estrutura tabular previamente definida (textos, PDFs, imagens, vídeos etc)

## Coleta e leitura de dados

### Coleta de dados

Outro nome auto-explicativo, coleta corresponde a coletar os dados que serão utilizados na sua análise. Essa coleta pode ser:

- Primária: Os dados serão produzidos especificamente para o objetivo da sua análise, por exemplo, você mesmo irá distribuir questionários para os estudantes da UFAL para fazer uma análise com base nas respostas
- Secundária: Você irá utilizar dados que já existem, como o IBGE ou o UFAL em números

### Leitura de dados

Após coletar os dados, precisamos fazer com que uma ferramenta consiga interpretar sua estrutura e conteúdo. 

Como cada fonte costuma entregar os dados em um formato diferente, o próximo passo é padronizá-los e integrá-los em uma única base, adequada à tarefa de ciência de dados que você quer realizar.

Imagine, por exemplo, que você fez uma coleta secundária: parte dos dados veio de uma API e outra parte de um arquivo CSV. Para trabalhar com eles, você precisará reuni-los em um só lugar, criando uma base consolidada e coerente. Só então será possível acessá-la e conduzir a análise até a conclusão.
