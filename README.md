# Tech Challenge - Análise de Dados de Câncer de Mama 🎯

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/WeslleyRibeiro-1999/Tech-Challenge/blob/main/tech_challenge.ipynb)

## 📋 Sobre o Projeto

Este projeto faz parte do **Tech Challenge da FIAP - Fase 1** e consiste em uma análise exploratória e modelagem preditiva para classificação de tumores de mama como benignos ou malignos, utilizando o dataset de câncer de mama do Wisconsin disponível no Kaggle.

### 🎯 Objetivos
- Realizar análise exploratória de dados (EDA)
- Implementar técnicas de pré-processamento
- Desenvolver modelos de machine learning para classificação
- Comparar performance de diferentes algoritmos
- Apresentar insights e conclusões

## 📊 Dataset

**Fonte:** [Breast Cancer Wisconsin Data - Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)

O dataset contém características computacionais de imagens de massas de mama, incluindo:
- **569 amostras** de tumores
- **30 características** numéricas
- **2 classes**: Maligno (M) e Benigno (B)

### Principais Features
- **Raio médio** (radius_mean)
- **Textura média** (texture_mean)
- **Perímetro médio** (perimeter_mean)
- **Área média** (area_mean)
- **Suavidade média** (smoothness_mean)
- **Compacidade média** (compactness_mean)
- **Concavidade média** (concavity_mean)
- E outras características estatísticas...

## 🧠 Modelos Implementados

### 1. PCA + Regressão Logística
- **Redução de dimensionalidade**: 30 → 5 componentes principais
- **Acurácia**: 98%
- **Vantagens**: Simplicidade e alta performance

### 2. Random Forest
- **Otimização de hiperparâmetros** via RandomizedSearchCV
- **Acurácia**: 97.37%
- **Análise de importância das features**

### 3. K-Nearest Neighbors (KNN)
- **Padronização** com StandardScaler
- **Otimização do parâmetro K**
- **Acurácia**: 94.73%

## 🚀 Como Executar o Projeto

### Pré-requisitos

- Python 3.11+
- UV (gerenciador de ambientes Python)

### 1. Instalação do UV

```bash
pip install uv
```

### 2. Clone do Repositório

```bash
git clone https://github.com/WeslleyRibeiro-1999/Tech-Challenge.git
```

### 3. Criação do Ambiente Virtual

``` bash
# Criar ambiente virtual com UV
uv venv

# Ativar ambiente virtual
# No macOS/Linux:
source .venv/bin/activate

# No Windows:
# .venv\Scripts\activate
```

### 4. Instalação das Dependências

```bash
uv pip install -r requirements.txt
```

### 5. Executar o Notebook

```bash
# Iniciar Jupyter Lab/Notebook
jupyter lab
# ou
jupyter notebook
```
Abra o arquivo tech_challenge.ipynb e execute as células sequencialmente.

### 📈 Principais Visualizações
O notebook inclui diversas visualizações:

- Distribuição de diagnósticos (Maligno vs Benigno)
- Histogramas das features
- Gráficos de dispersão para análise de correlações
- Swarm plots e box plots para comparação entre classes
- Matrizes de confusão para avaliação dos modelos
- Análise de importância das features

### 🔍 Principais Insights
- **Tamanho do tumor** (área, raio, perímetro) é um forte preditor de malignidade
- **Tumores malignos** tendem a ter maior concavidade e suavidade
- **PCA** preserva informação suficiente para alta acurácia com apenas 5 componentes
- **Random Forest** oferece boa interpretabilidade com análise de importância das features


### 📄 Licença
Este projeto é desenvolvido para fins educacionais como parte do Tech Challenge da FIAP.