# Análise Exploratória de Dados do Titanic (EDA)

## Visão Geral do Projeto
Com o objetivo principal de entender quais fatores (gênero, classe socioeconômica, idade, presença de familiares, porto de embarque, etc.) influenciaram diretamente as chances de sobrevivência dos passageiros do conhecido naufrágio do navio Titanic, este projeto realiza uma Análise Exploratória de Dados utilizando o conjunto de dados da plataforma Kaggle e seguindo as diretrizes e requisitos do roadmap de Análise de Dados do [roadmap.sh](https://roadmap.sh/projects/titanic-eda-python).


---
## O que foi utilizado:
* **Python**
* **Pandas** (manipulação e limpeza de dados)
* **Matplotlib** & **Seaborn** (visualização de dados)
* **JupyterLite**

---

## O que foi Analisado?
Foram criadas visualizações combinadas (**Gráficos de Barras** para contagem/sobrevivência e **Gráficos de Pizza** para proporções) para 10 cenários e variáveis cruciais:

1. **Status da Idade:** Comparação entre passageiros com idade informada vs. desconhecida.
2. **Irmãos/Cônjuges (`SibSp`):** Impacto de viajar com irmãos ou cônjuge.
3. **Pais/Filhos (`Parch`):** Impacto de viajar com pais ou filhos.
4. **Faixas Etárias:** Distribuição por faixas de idade (Crianças, Adolescentes, Jovens Adultos, Adultos, Idosos e Desconhecida).
5. **Classes Socioeconômicas (`Pclass`):** Comparação das taxas de sobrevivência entre 1ª, 2ª e 3ª classes.
6. **Sexo:** Análise do impacto do gênero na sobrevivência.
7. **Porto de Embarque (`Embarked`):** Análise por local de embarque (Cherbourg, Queenstown, Southampton).
8. **Tarifa Zero (`Fare == 0`):** Análise específica para passageiros que não pagaram pela tarifa.
9. **Tamanho do Grupo de Viagem:** Passageiros sozinhos vs. pequenos grupos vs. famílias grandes.
10. **Títulos Extraídos do Nome:** Análise das taxas por títulos (Mr, Miss, Mrs, Master, Outros).

---

## Principais Insights Descobertos
* **Gênero:** As mulheres apresentaram uma taxa de sobrevivência expressivamente superior à dos homens, refletindo a política de "mulheres e crianças primeiro".
* **Classe Socioeconômica:** Passageiros da 1ª classe tiveram a maior taxa de sobrevivência, enquanto a 3ª classe sofreu o maior número de vítimas.
* **Idade:** Crianças tiveram maior prioridade de resgate, enquanto passageiros idosos tiveram menor taxa de sobrevivência.
* **Tamanho do Grupo:** Viajar sozinho ou em famílias muito grandes (5+ pessoas) reduziu as chances de sobrevivência em comparação com pequenos grupos (2-4 pessoas).

---


## Conceitos Teóricos e Técnicas Aplicadas

Durante a fase de exploração e estruturação dos dados, foram aplicados conceitos fundamentais de Ciência de Dados e Machine Learning:

### 1. Frequência Absoluta vs. Frequência Relativa
* **Frequência Absoluta:** O número exato e contagem bruta de ocorrências em uma categoria (ex.: *549 passageiros não sobreviveram*). Utilizada nos **gráficos de barras** para visualizar a dimensão real do grupo.
* **Frequência Relativa:** A proporção ou porcentagem de cada categoria em relação ao total (ex.: *61.6% dos passageiros eram do sexo masculino*). Utilizada nos **gráficos de pizza** para permitir comparações justas e padronizadas, independentemente do tamanho da amostra.

### 2. One-Hot Encoding (Codificação One-Hot)
* Técnica de pré-processamento essencial para transformar variáveis categóricas (como `Sex`, `Embarked` ou `Title_Group`) em colunas binárias (`0` ou `1`).
* Permite converter categorias de texto em formatos numéricos adequados para alimentar modelos de aprendizado de máquina sem criar uma ordem de importância fictícia entre elas.

### 3. Agrupamento com K-Means (K-Means Clustering)
* Algoritmo de Aprendizado Não Supervisionado explorado para agrupar passageiros com base em características numéricas semelhantes (como `Age` e `Fare`).
* Ajuda a identificar perfis e padrões ocultos de passageiros (clusters) de forma automática, complementando a análise exploratória tradicional.
