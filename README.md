# Análise Exploratória de Emissões e Remoções de GEE no Brasil

## 1. Visão Geral do Projeto

Este projeto tem como objetivo realizar uma **Análise Exploratória de Dados (EDA)** sobre as emissões e remoções de Gases de Efeito Estufa (GEE) no Brasil, utilizando a base de dados `Dados-nacionais-v12.xlsx`. A análise visa identificar tendências históricas, a distribuição das emissões por setor e gás, e os principais vetores de poluição climática no país.

Os resultados desta EDA são cruciais para:
* Informar políticas de mitigação.
* Monitorar o progresso em relação às metas climáticas nacionais (NDC).
* Educar sobre o perfil de emissões do Brasil.

## 2. Estrutura do Repositório

O repositório está estruturado da seguinte forma:
. ├── Programacao_WEB/ │ └── Dados-nacionais-v12.xlsx # Fonte de dados (Emissões e Remoções) ├── EDA_GEE_Brasil.ipynb # Notebook Jupyter/Colab com o código de análise └── README.md # Este arquivo

## 3. Dados

O conjunto de dados principal é o arquivo **`Dados-nacionais-v12.xlsx`**, que contém séries históricas de emissões e remoções de GEE, desagregadas por:

| Coluna Sugerida | Descrição |
| :--- | :--- |
| `Ano` | Ano da estimativa de emissão. |
| `Setor` | Setor da economia (e.g., Energia, Agropecuária, MUT). |
| `Gás` | Gás de Efeito Estufa (e.g., $\text{CO}_2$, $\text{CH}_4$, $\text{N}_2\text{O}$). |
| `Emissão_MtCO2e` | Valor da emissão em Megatoneladas de $\text{CO}_2$ Equivalente. |
| *Outras colunas* | (e.g., `Remoção_MtCO2e`, `Estado`, etc.) |

**Nota:** Os scripts de análise assumem que as colunas acima estão presentes. Ajuste as variáveis no bloco de código **"2. PADRONIZAÇÃO DAS COLUNAS"** conforme a estrutura exata do seu Excel.

## 4. Análises Realizadas (EDA)

O script principal (`EDA_GEE_Brasil.ipynb`) realiza as seguintes análises exploratórias:

### 4.1. Tendência Histórica
* **Visualização:** Gráfico de linha mostrando a evolução da **Emissão Total Anual** ($\text{Mt} \text{CO}_2e$).
* **Objetivo:** Identificar picos de emissão, anos de redução significativa e a tendência de longo prazo.

### 4.2. Composição Setorial
* **Visualização:** Gráfico de Pizza (Pie Chart) exibindo a proporção de cada setor nas emissões totais acumuladas.
* **Objetivo:** Determinar os setores mais contribuintes para as emissões nacionais (frequentemente **Uso da Terra/Desmatamento** e **Agropecuária** no contexto brasileiro).

### 4.3. Evolução Setorial ao Longo do Tempo
* **Visualização:** Gráfico de linha com múltiplos traços, mostrando a evolução das emissões de cada setor principal ao longo dos anos.
* **Objetivo:** Entender como a participação e o volume de emissão de cada setor mudaram, buscando *drivers* históricos (ex: aumento de desmatamento em certos períodos).

### 4.4. Ranking de Gases
* **Visualização:** Gráfico de Barras mostrando a contribuição de cada Gás ($\text{CO}_2$, $\text{CH}_4$, $\text{N}_2\text{O}$, etc.) em $\text{CO}_2$ Equivalente.
* **Objetivo:** Focar a atenção nos gases com maior Potencial de Aquecimento Global (GWP) e volume de emissão.

## 5. Como Executar o Código

### Pré-requisitos

Para rodar o notebook, você precisará ter o Python instalado com as seguintes bibliotecas:

```bash
pip install pandas openpyxl matplotlib seaborn
```
## Execução no Google ColabMontar o Google Drive:

* Execute a seguinte célula no Colab. Um pop-up pedirá sua autorização.Pythonfrom google.colab import drive drive.mount('/content/drive')

Desenvolvido por: Lucas Bretas Prata de Pinho Tavares
Data da Última Atualização: Outubro de 2025
