# K-Means
Aplicação de K-Means para Análise de Dados Biológicos

---

Exploramos o algoritmo de clustering K-Means aplicado a um contexto diferente do usual: dados biológicos. Em vez de segmentar perfis de viajantes ou clientes de e-commerce, utilizamos características físicas de pinguins para segmentar diferentes espécies. Esta abordagem destaca a versatilidade do K-Means para diversas áreas além de vendas e marketing.

A base de dados utilizada é a penguins do pacote seaborn, que contém informações sobre três espécies de pinguins: Adelie, Chinstrap e Gentoo. As variáveis disponíveis incluem medições físicas dos pinguins coletadas na Antártica. O objetivo é usar o K-Means para identificar esses grupos de pinguins de forma não supervisionada.

Dicionário de Dados:

species: Espécie do pinguim (Adelie, Chinstrap, Gentoo)
island: Ilha onde o pinguim foi observado (Biscoe, Dream, Torgersen)
bill_length_mm: Comprimento do bico em milímetros
bill_depth_mm: Profundidade do bico em milímetros
flipper_length_mm: Comprimento da barbatana em milímetros
body_mass_g: Massa corporal em gramas
sex: Sexo do pinguim (Male, Female)
year: Ano em que a observação foi feita

## 1 - Pré-processamento dos Dados: Tratamento de Valores Ausentes e Seleção de Variáveis
Nesta etapa, realizamos o pré-processamento inicial do dataset de pinguins. O objetivo é garantir a qualidade dos dados para a aplicação do algoritmo K-Means. Isso envolve a identificação e remoção de valores ausentes (NaNs), bem como a exclusão de colunas que contêm dados categóricos, pois o K-Means opera com variáveis numéricas.

## 2 - Análise Descritiva e Visualização de Agrupamentos Iniciais (Pairplot)
Nesta seção, utilizamos a função pairplot do Seaborn para realizar uma análise descritiva visual dos dados limpos. O pairplot gera uma matriz de gráficos de dispersão para cada par de variáveis numéricas, além de histogramas para cada variável individual. O objetivo é observar a distribuição das variáveis e, principalmente, identificar visualmente a presença de possíveis agrupamentos naturais nos dados antes da aplicação do K-Means.

Já podemos analisar que, visualmente, os gráficos de dispersão sugerem a presença de 3 grupos distintos na nossa base de dados. Esta observação prévia é consistente com o número de espécies de pinguins que esperamos encontrar.

## 3 - Padronização dos Dados
Para garantir que todas as variáveis contribuam igualmente para o processo de clustering e para evitar que variáveis com maiores escalas dominem as distâncias calculadas pelo K-Means, realizamos a padronização dos dados. Utilizamos o StandardScaler, que transforma os dados para que tenham média zero e desvio padrão um. Após a padronização, visualizamos as primeiras linhas do DataFrame transformado.

## 4 - Aplicação do Algoritmo K-Means
Nesta fase, aplicamos o algoritmo K-Means aos dados padronizados. Escolhemos o número de clusters (n_clusters) como 3, pois sabemos que a base de dados contém três espécies distintas de pinguins (Adelie, Chinstrap e Gentoo). O random_state é definido para garantir a reprodutibilidade dos resultados, e n_init=10 especifica o número de vezes que o algoritmo K-Means será executado com diferentes sementes de centróides, escolhendo a melhor entre elas para evitar mínimos locais.

Após o treinamento, os rótulos de cluster são adicionados ao DataFrame original (penguins_limpo), e a contagem de membros em cada cluster é exibida para verificar a distribuição.

## 5 - Visualização dos Clusters e Centroides
Para uma melhor compreensão dos agrupamentos formados pelo K-Means, construímos duas matrizes de dispersão utilizando a biblioteca plotly.express. Esses gráficos permitem visualizar os pontos de dados coloridos de acordo com o cluster atribuído, e os centroides de cada cluster são marcados para indicar seus respectivos centros.

Começamos analisando o comprimento do bico versus a profundidade do bico e, em seguida, exploramos a relação entre o comprimento da barbatana e a massa corporal.

## 6 - Outras Aplicações de Algoritmos de Clusterização
Além da segmentação de dados biológicos, os algoritmos de clusterização possuem uma vasta gama de aplicações em diversas áreas. Abaixo, são apresentadas três utilidades adicionais:

---

## Conclusão
Neste notebook, demonstramos a aplicação do algoritmo de clustering K-Means para segmentar dados biológicos, especificamente características físicas de pinguins. Através de um processo de pré-processamento de dados, padronização e visualização, fomos capazes de identificar três clusters distintos que correspondem às espécies de pinguins presentes no dataset.

Este exercício não só reforça a compreensão do funcionamento do K-Means, mas também destaca sua versatilidade em diferentes domínios, desde a segmentação de clientes até a análise de dados científicos. A capacidade de descobrir padrões e agrupamentos em dados não rotulados é uma ferramenta poderosa na análise exploratória de dados e em diversas aplicações de machine learning.

---

**Gostou da Análise?** Conecte-se para trocarmos experiências e ideias sobre projetos de dados!

🔗 **Meu LinkedIn:** [https://www.linkedin.com/in/diego-kaique-9ba3697b]

📧 **Contato:** [kaique_0208@hotmail.com]
