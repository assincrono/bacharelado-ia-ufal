# Introdução à Inteligência Artificial

O AIMA (Russell & Norvig) organiza as definições de IA a partir de duas perguntas: o interesse está no *processo* (pensar) ou no *comportamento* (agir)? E o padrão de comparação é o *ser humano* ou um *ideal de racionalidade*? O cruzamento gera quatro abordagens:

| | Padrão humano | Padrão racional |
|---|---|---|
| **Pensar** | Pensar como humanos | Pensar racionalmente |
| **Agir** | Agir como humanos | Agir racionalmente |

- **Agir como humanos:** baseada no Teste de Turing (1950), em que uma máquina é inteligente se um interrogador, conversando por texto, não a distingue de uma pessoa. Importam as capacidades exigidas: linguagem, memória, raciocínio e aprendizado.
- **Pensar como humanos:** busca programas cujos passos internos imitem o raciocínio humano, o que exige conhecimento de ciência cognitiva, neurociência e psicologia.
- **Pensar racionalmente:** segue a tradição da lógica, das "leis do pensamento" de Aristóteles, com regras que, a partir de premissas verdadeiras, geram apenas conclusões verdadeiras.
- **Agir racionalmente:** o agente racional age para obter o melhor resultado (ou o melhor resultado esperado, em caso de incerteza), dado o que percebe e sabe. É a abordagem central do AIMA, por ser mais geral (a lógica é só um caminho entre outros, e às vezes um reflexo basta) e mais fácil de avaliar.

Nenhuma das quatro é a definição "certa": cada uma ilumina um aspecto do problema.

Uma forma prática de usar a definição: pergunte se o sistema apenas executa regras fixas escritas por alguém, ou se ele percebe, raciocina, aprende e se adapta.

## História da IA em cinco marcos

A história da IA pode ser resumida em cinco marcos, e o que vale conhecer é o padrão por trás deles: cada avanço veio da combinação de dados, hardware e algoritmos, e cada inverno, da falta de pelo menos um deles.

1. **Fundações (1943–1956):** McCulloch e Pitts propõem o neurônio artificial (1943), Turing publica o artigo do teste que leva seu nome (1950) e a conferência de Dartmouth cunha o termo "inteligência artificial" (1956). O otimismo era enorme.
2. **Entusiasmo e primeiros invernos (1956–1980):** programas provam teoremas e jogam damas, mas esbarram na explosão combinatória e na falta de conhecimento do mundo real. O financiamento seca, no primeiro inverno da IA.
3. **Sistemas especialistas (1980–1990):** o conhecimento passa a ser codificado em regras escritas com especialistas humanos, com sucesso comercial em diagnóstico médico e outras áreas. Manter milhares de regras, porém, era caro e frágil, o que levou a um segundo inverno.
4. **Retorno dos dados e das redes neurais (1990–2011):** a IA se aproxima da estatística e passa a aprender com exemplos em vez de seguir regras. O Deep Blue vence o campeão mundial de xadrez (1997), enquanto a internet gera dados em escala inédita.
5. **Aprendizado profundo e grandes modelos (2012–hoje):** uma rede neural profunda vence com folga uma competição de reconhecimento de imagens (2012) e, com muitos dados, GPUs e novos algoritmos, redes com bilhões de parâmetros superam os métodos anteriores. Em 2022, os grandes modelos de linguagem levam a IA ao grande público.
