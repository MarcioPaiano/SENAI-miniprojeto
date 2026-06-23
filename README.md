📊 MiniProjeto DataView
📌 Sobre o projeto
O DataView é um projeto de Análise Exploratória de Dados (Exploratory Data Analysis - EDA) desenvolvido em Python, utilizando as bibliotecas Pandas, NumPy, Matplotlib e Seaborn.

O projeto simula o processo de tratamento e análise de um dataset de vendas, desde a geração de dados sintéticos até a produção de métricas, gráficos e relatórios. Durante o desenvolvimento são aplicadas técnicas de limpeza de dados, tratamento de valores ausentes, detecção de outliers, criação de variáveis derivadas e segmentação de clientes.

O objetivo é demonstrar um fluxo completo de preparação de dados semelhante ao utilizado em projetos de Ciência de Dados e Business Intelligence.

🎯 Objetivos
O projeto foi desenvolvido para praticar conceitos fundamentais de programação e análise de dados em Python, incluindo:

Estruturas de dados
Funções reutilizáveis
Programação modular
Manipulação de arquivos CSV e JSON
Limpeza e tratamento de dados
Transformação de dados
Análise estatística
Visualização de dados
Exportação de resultados
Organização de projetos em Data Science
📂 Dataset
O dataset utilizado foi gerado sinteticamente em Python e contém aproximadamente 1500 registros de vendas.

Cada registro possui as seguintes informações:

Coluna	Descrição
id	Identificador da venda
data	Data da venda
cliente	Nome do cliente
produto	Produto vendido
categoria	Categoria do produto
regiao	Região da venda
quantidade	Quantidade vendida
preco	Preço unitário
Para fins de estudo foram inseridos propositalmente diversos problemas de qualidade dos dados, como:

valores nulos (None)
datas inválidas
espaços extras em textos
registros duplicados
outliers
valores inconsistentes
Esses problemas foram tratados nas etapas de limpeza do projeto.

📈 Etapas do projeto
O fluxo de análise foi dividido em onze requisitos funcionais.

RF01 – Criação do Dataset
Geração de um dataset sintético de vendas.
Inserção de dados propositalmente inconsistentes.

RF02 – Inspeção dos Dados
Visualização das primeiras linhas.
Informações do DataFrame.
Estatísticas descritivas.
Identificação de valores ausentes.

RF03 – Limpeza dos Dados
Remoção de datas inválidas.
Conversão da coluna de datas.
Remoção de espaços extras.
Tratamento de valores nulos.
Remoção de registros duplicados.

RF04 – Tratamento de Outliers
Foram geradas duas versões do dataset:

v1: dados limpos mantendo os outliers;
v2: dados limpos com tratamento dos outliers utilizando o método IQR.
A versão escolhida para utilização em data/final/ foi a v2, pois apresenta dados mais consistentes para análises posteriores.
A versão v2 foi escolhida porque, além da limpeza de valores nulos, datas inválidas e espaços extras, os outliers das colunas quantidade e receita_total foram detectados pelo método do Intervalo Interquartil (IQR) e removidos antes da etapa final de análise. Isso reduz a influência de valores extremos nas análises estatísticas e em futuros modelos de aprendizado de máquina.

RF05 – Criação de Colunas Derivadas
Foram criadas as colunas:

receita_total
mes
trimestre
ano
faixa_receita_item

RF06 – Métricas Agregadas
Foram calculadas métricas por:

mês
produto
categoria
região

RF07 – Segmentação de Clientes
Os clientes foram classificados em:

Bronze
Prata
Ouro
de acordo com o total gasto.

RF08 – Estatísticas com NumPy
Foram utilizadas operações vetorizadas do NumPy para calcular:

média
mediana
desvio padrão
percentis
soma
participação percentual
vendas acima da média
RF09 – Visualizações
Foram gerados gráficos em PNG utilizando Matplotlib e Seaborn.

Receita por mês
Top 5 produtos
Distribuição da receita por região

RF10 – Organização do Código
Todo o projeto foi estruturado em funções reutilizáveis, contendo:

parâmetros
retorno
docstrings
funções lambda

RF11 – Exportação dos Resultados
Os resultados foram exportados para:

CSV
JSON
📁 Estrutura do projeto
projeto/
│
├── data/
│   ├── raw/
│   ├── processed/
│   │   ├── v1_com_outliers/
│   │   └── v2_outliers_tratado/
│   └── final/
│
├── notebooks/
│   └── dataview.ipynb
│
├── outputs/
│   ├── metricas_por_mes.csv
│   ├── segmentacao_clientes.csv
│   ├── estatisticas_gerais.json
│   └── graficos/
│       ├── receita_por_mes.png
│       ├── top_produtos.png
│       └── distribuicao_regiao.png
│
└── README.md
🛠 Tecnologias utilizadas
Python 3.10+
Pandas
NumPy
Matplotlib
Seaborn
JSON
OS
Random
Datetime
Google Colab
Visual Studio Code
Git e GitHub
▶ Como executar
Google Colab
Faça upload do notebook dataview.ipynb.
Execute todas as células na ordem.
VS Code
Instale as bibliotecas necessárias:

pip install pandas numpy matplotlib seaborn
Em seguida, execute o notebook ou o script principal.

📤 Arquivos gerados
Ao final da execução são criados:

Dataset final tratado;
Métricas mensais em CSV;
Segmentação de clientes em CSV;
Estatísticas gerais em JSON;
Três gráficos em formato PNG.
👨‍💻 Autor
Marcio Paiano de Souza

Projeto desenvolvido para a disciplina de Análise Exploratória de Dados com Python.

🎥 Vídeo de demonstração
Inserir aqui o link do vídeo hospedado no Google Drive ou YouTube.