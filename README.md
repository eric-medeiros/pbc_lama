# 📊 PBC - LAMA
Este repositório contém o código e dados para o projeto LAMA, focado na análise espacial e estimativa de densidade kernel para dados biológicos em um programa de monitoramento costeiro.

## 🎯 Objetivo
O projeto realiza análises espaciais para modelar e visualizar padrões em dados de avistagem, produzindo mapas interativos com várias camadas de informação para análise.

## 📁 Estrutura do Projeto
```
pbc_lama/
├── 00_data/
│   ├── 00_dados_brutos/
│   │   └── Dados Botos com Lama.ods
│   ├── 01_tratados_excel/
│   │   └── Dados_Lama.xlsx
│   └── 02_georefs/
│       └── amostragem_area.gpkg
├── 01_scripts/
│   └── kernel_lama.R
├── 02_outputs/
│   ├── kernel.tif
│   ├── p50.gpkg
│   ├── p95.gpkg
│   └── pontos.gpkg
├── 03_markdown/
│   └── leaflet_lama.Rmd
└── pbc_lama.Rproj
```

## 🗂️ Dados

### Fontes
- **dados_lama.xlsx:** Conjunto de dados primário contendo os dados brutos de avistagem.
- **amostragem_area.gpkg:** Arquivo GeoPackage definindo o polígono da área de estudo.

### Saídas
A análise gera quatro principais arquivos espaciais:
- pontos.gpkg: Dados de pontos para visualizações.
- kernel.tif: Arquivo raster representando a estimativa de densidade kernel.
- p50.gpkg: Arquivo vetorial de polígono para a área do percentil 50 (área central de uso).
- p95.gpkg: Arquivo vetorial de polígono para a área do percentil 95 (área total de uso).

## 🔧 Processamento

### Pré-requisitos
Certifique-se de ter as seguintes bibliotecas do R instaladas:
```r
library(here)
library(xlsx)
library(dplyr)
library(sf)
library(spatstat)
library(terra)
```

## 📊 Dashboard
Um FlexDashboard interativo está disponível para visualizar os resultados.

### Funcionalidades
- ✅ Mapa interativo construído com Leaflet
- ✅ Alternância entre mapas base Satélite e Light
- ✅ Controle de visibilidade das quatro camadas de dados independentemente
- ✅ Popups informativos para os pontos de dados

### Como Gerar
Para construir o dashboard, execute o arquivo R Markdown localizado no diretório 03_markdown/. Isso renderizará a análise em um dashboard HTML interativo.

## 🚀 Como Usar Este Repositório
- Explore os Dados: Os dados brutos estão localizados em 00_data/.
- Execute a Análise: Execute o script de análise principal 01_scripts/kernel_lama.R para gerar as saídas em 02_outputs/.
- Visualize os Resultados: Execute 03_markdown/dashboard_lama.Rmd para recriar o dashboard interativo.

## 👤 Autor
Eric Medeiros

---

*Projeto desenvolvido como auxílio no TCC de  (pegar nome)*
