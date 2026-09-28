# Introdução à Ciência de Dados

Ciência de dados é uma área interdisciplinar que combina matemática, estatística, programação, técnicas analíticas e conhecimento do domínio para investigar problemas, produzir conhecimento e apoiar decisões. Em geral, o trabalho segue um ciclo: coleta, leitura e integração, limpeza, análise e comunicação dos resultados.

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

## Coleta e leitura de dados

### Coleta de dados

A coleta é o ato de obter os dados que serão utilizados na análise. Ela pode ser:

- **Primária:** os dados são produzidos especificamente para o objetivo da análise. Por exemplo, distribuir questionários aos estudantes da UFAL e analisar as respostas.
- **Secundária:** utilizam-se dados que já existem, como os do IBGE ou do "UFAL em números".

### Leitura de dados

Após a coleta, é preciso que uma ferramenta consiga interpretar a estrutura e o conteúdo dos dados. Isso é a leitura: carregar os dados na ferramenta de análise, por exemplo, com `pd.read_csv` em Python (biblioteca pandas).

Como cada fonte costuma entregar os dados em um formato diferente, o passo seguinte é padronizá-los e integrá-los em uma única base, adequada à tarefa de ciência de dados que se pretende realizar.

Imagine uma coleta secundária em que parte dos dados veio de uma API e outra parte de um arquivo CSV. Para trabalhar com eles, é necessário reuni-los em um só lugar, criando uma base consolidada e coerente. Só então é possível acessá-la e conduzir a análise até a conclusão.
