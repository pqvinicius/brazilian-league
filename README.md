# Análise de Performance do Campeonato Brasileiro (2009-2018)

## 1. Descrição & Objetivo

Este projeto realiza uma análise exploratória de dados (EDA) sobre 10 anos de história do Campeonato Brasileiro de futebol (de 2009 a 2018). O objetivo principal é identificar padrões de desempenho, destacar as equipes mais consistentes e vitoriosas do período, e entender os fatores que mais se correlacionam com o sucesso na competição.

* **Termo Técnico:** **Análise Exploratória de Dados (EDA - Exploratory Data Analysis)**: Pense na EDA como o trabalho de um detetive de dados. Antes de tirar conclusões finais, nós mergulhamos nos dados para "interrogá-los". Usamos estatísticas e gráficos para resumir suas principais características, encontrar padrões, identificar anomalias (como dados faltantes ou estranhos) e testar hipóteses iniciais. É a primeira etapa para entender a história que os dados têm para contar.

## 2. Contexto de Negócio

Embora o tema seja esportivo, a análise demonstra habilidades transferíveis para qualquer contexto de negócio. A lógica aplicada aqui pode ser usada para:
* Analisar o desempenho de produtos ou concorrentes ao longo do tempo.
* Identificar KPIs (Key Performance Indicators) que levam ao sucesso.
* Criar rankings de eficiência (ofensiva vs. defensiva) para otimizar recursos.
* Entender tendências de mercado (como a média de gols por ano, que pode indicar mudanças táticas).

## 3. Fonte dos Dados

Os dados foram obtidos a partir de um dataset público disponível no Kaggle, contendo as classificações finais do campeonato, pontos, vitórias, gols e outras estatísticas de cada time participante entre 2009 e 2018.

## 4. Ferramentas e Bibliotecas Utilizadas

* **Linguagem:** Python
* **Bibliotecas:** Pandas (para manipulação de dados), Matplotlib e Seaborn (para visualização de dados).
* **Ambiente:** Jupyter Notebook.

## 5. Metodologia Aplicada

A análise foi estruturada em várias etapas para extrair o máximo de valor dos dados:

1.  **Análise Descritiva e de Ranking:**
    * Identificação dos campeões de cada ano e o ranking dos maiores vencedores no período.
    * Criação de um **filtro de relevância**, analisando apenas os times que participaram de um número de temporadas acima da média. Isso garante que as comparações de desempenho (gols, aproveitamento) sejam feitas entre equipes com um histórico mais consolidado na Série A.
    * Criação de rankings de desempenho médio (ataque, defesa e aproveitamento) para esses times filtrados.

2.  **Análise Temporal:**
    * Investigação da evolução da média de gols marcados por ano no campeonato, identificando tendências ofensivas ao longo da década.
    * **Estudo de Caso (Corinthians):** Análise aprofundada do desempenho do Corinthians ano a ano, cruzando sua performance de gols (pró e contra) com a sua classificação final.

3.  **Análise de Consistência e Eficiência:**
    * Análise dos times que mais frequentaram o G4 (zona de classificação para a Libertadores).
    * Comparação entre a **consistência** (vezes no G4) e a **eficiência** (títulos conquistados), revelando equipes que se mantiveram no topo, mas sem o mesmo sucesso em títulos.

4.  **Análise Geográfica e de Correlação:**
    * Agrupamento por estados para avaliar o desempenho médio regional.
    * Criação de uma matriz de correlação para entender numericamente quais variáveis (pontos, vitórias, saldo de gols) têm maior impacto na posição final.

## 6. Principais Insights e Resultados

* **Eficiência vs. Consistência:** O Grêmio foi o time mais consistente no G4 (6 vezes), mas não conquistou títulos no período. Em contrapartida, o Corinthians, com 5 presenças no G4, foi o maior campeão (3 títulos), demonstrando maior eficiência.
* **Correlação com Sucesso:** A análise de correlação confirmou que **Pontos** (`0.99` de aproveitamento) e **Vitórias** (`0.98`) são os fatores mais fortes para uma boa classificação, com uma correlação quase perfeita. O número de derrotas (`-0.91`) é o indicador mais forte de uma campanha ruim.
* **Desempenho Regional:** O estado do Rio Grande do Sul (RS) apresentou a melhor média de pontos e a melhor classificação média, superando eixos tradicionalmente dominantes como SP e RJ na década analisada.
* **Tendência Ofensiva:** A média de gols por equipe no campeonato atingiu seu pico em 2009 e, após uma queda, mostrou uma tendência de recuperação a partir de 2013.