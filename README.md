# Data Visualization — Aulas Práticas (PUC Minas EAD)

Repositório de apoio para as **aulas práticas** da disciplina de **Visualização de Dados** (EAD — PUC Minas). O material está organizado principalmente em **notebooks Jupyter (`.ipynb`)** com exemplos e exercícios.

## Conteúdo (notebooks)

- `UNIDADE 2 - 2.1 - Categóricos com Barras Ordenação e Comparação.ipynb` — gráficos de barras, ordenação e comparação.
- `UNIDADE 2 - 2.2 - Categóricos por Meio de Dot Plot, Lollipop e Small Multiples.ipynb` — alternativas ao gráfico de barras (dot plot, lollipop, small multiples).
- `UNIDADE 2 - 2.3 - Séries Temporais.ipynb` — visualizações para séries temporais.
- `UNIDADE 2 - 2.5 - Distribuição a Partir de Histogramas.ipynb` — distribuição e histogramas.
- `UNIDADE 2 - 2.6 - Boxplot, Violino e Densidade.ipynb` — boxplot, violin plot e curvas de densidade.
- `UNIDADE 2 - 2.7 - Correlação e Relação.ipynb` — relação entre variáveis (ex.: dispersão) e correlação.
- `UNIDADE 2 - 2.8 - Matriz de Correlação com Heatmap.ipynb` — heatmap de correlação.
- `UNIDADE 2 - 2.9 - Gráficos de Mapa.ipynb` — mapas (geodados) com `geopandas`.
- `UNIDADE 2 - 2.10 - Praticando com Dados Reais.ipynb` — prática integrando técnicas com dados reais.

## Pré-requisitos

- Python 3.10+ (recomendado)
- Jupyter Lab ou Jupyter Notebook
- Bibliotecas usadas ao longo dos notebooks: `pandas`, `numpy`, `matplotlib`, `seaborn` e `geopandas` (para a parte de mapas).

## Como executar (local)

1) Entre na pasta do repositório (a que contém os notebooks):

```bash
cd data-visualization
```

2) Crie e ative um ambiente virtual:

```bash
python -m venv .venv
source .venv/bin/activate
```

3) Instale dependências (pip):

```bash
python -m pip install -U pip
python -m pip install jupyterlab pandas numpy matplotlib seaborn geopandas
```

4) Inicie o Jupyter:

```bash
jupyter lab
```

Abra o notebook desejado e execute as células **na ordem** (de cima para baixo).

### Dica: `geopandas` no macOS

Dependências geoespaciais podem variar por sistema. Se tiver erro ao instalar/rodar a unidade de mapas, a alternativa mais simples costuma ser usar **Conda/Mamba**:

```bash
conda create -n dataviz python=3.11 -y
conda activate dataviz
conda install -c conda-forge jupyterlab pandas numpy matplotlib seaborn geopandas -y
jupyter lab
```

## Como usar no Google Colab

Você pode rodar os notebooks no **Google Colab** sem instalar nada localmente.

### Opção A — Abrir do GitHub (recomendado)

1) Acesse `https://colab.research.google.com`
2) Vá em **File → Open notebook → GitHub**
3) Cole a URL do repositório (ou pesquise pelo nome) e selecione o notebook `.ipynb`

### Opção B — Upload do arquivo

1) Acesse `https://colab.research.google.com`
2) Vá em **File → Upload notebook**
3) Envie o arquivo `.ipynb` baixado deste repositório

### Instalando dependências no Colab

Em geral, `pandas`, `numpy`, `matplotlib` e `seaborn` já funcionam no Colab. Para garantir, rode uma célula no início do notebook:

```python
!pip -q install -U pandas numpy matplotlib seaborn
```

Para a parte de **mapas** (quando usar `geopandas`), instale também:

```python
!pip -q install -U geopandas
```

Depois de instalar, use **Runtime → Restart runtime** e execute as células novamente.