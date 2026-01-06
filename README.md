# Análise de Dados de Locadora de Veículos no Google Colab

Projeto de **Análise de Dados** desenvolvido no Google Colab, focado em tratamento, enriquecimento e exploração de dados de uma locadora de veículos, incluindo clientes, locações, veículos e créditos de carbono.
## Visão Geral

Este notebook apresenta um fluxo completo de preparação e exploração de dados:
- Carregamento de múltiplas bases (CSV e JSON).
- Análise inicial de estrutura e qualidade dos dados.
- Tratamento de valores ausentes, datas inválidas e valores inconsistentes.
- Criação de variáveis derivadas para suporte à decisão e sustentabilidade.

## Conjunto de Dados

Foram utilizadas quatro bases principais:

- **Carbon offsets**: informações de compensação de carbono por ano (toneladas e custo).
- **Customers**: perfil dos clientes (tipo, idade, cidade e score de lealdade).
- **Rentals**: registros de locações (datas, cidade, diária, distância percorrida).
- **Vehicles**: frota de veículos (modelo, tipo de combustível, categoria, emissão de CO₂ por km).

## Etapas da Análise

Principais etapas realizadas no notebook:

- **Inspeção inicial**
  - Uso de `info()` e `head()` para entender colunas, tipos e problemas de qualidade.

- **Tratamento de dados**
  - Preenchimento de idade faltante de clientes com a média da coluna.
  - Ajuste de valores nulos em `co2gperkm` com um valor padrão (ex.: 120 g/km).
  - Correção de diárias com valor zero/negativo, marcando como `NaN` para tratamento.
  - Conversão de datas de locação para `datetime`, tratando datas inválidas com `errors="coerce"`.  

- **Engenharia de atributos**
  - Cálculo da duração da locação em dias.
  - Cálculo da receita total por locação (diária × duração).
  - Junção das bases de locações, veículos e clientes para criar um dataset unificado.
  - Cálculo da emissão estimada de CO₂ por locação com base em `co2gperkm` e `distancekm`.
  - Extração de ano e mês da data de início da locação para análises temporais.

## Tecnologias Utilizadas

- **Python**
- **Pandas** para manipulação, limpeza e junção de dados. [file:1]
- **Google Colab** como ambiente de desenvolvimento e execução do notebook. [file:1]

## Como Executar o Projeto

1. Faça o download do notebook `.ipynb`.
2. Abra o arquivo no **Google Colab**.
3. Suba os arquivos de dados (CSV/JSON) no ambiente (Google Drive ou upload direto).
4. Atualize os caminhos de leitura dos arquivos, se necessário.
5. Execute as células em ordem para reproduzir todo o fluxo de análise.

