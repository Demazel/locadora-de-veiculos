# Análise de Dados de Locadora de Veículos no Google Colab

Projeto de **Análise de Dados** desenvolvido no Google Colab, focado em tratamento, enriquecimento e exploração de dados de uma locadora de veículos, incluindo clientes, locações, veículos e créditos de carbono. [file:1]

## Visão Geral

Este notebook apresenta um fluxo completo de preparação e exploração de dados:
- Carregamento de múltiplas bases (CSV e JSON).
- Análise inicial de estrutura e qualidade dos dados.
- Tratamento de valores ausentes, datas inválidas e valores inconsistentes.
- Criação de variáveis derivadas para suporte à decisão e sustentabilidade. [file:1]

## Conjunto de Dados

Foram utilizadas quatro bases principais: [file:1]

- **Carbon offsets**: informações de compensação de carbono por ano (toneladas e custo).
- **Customers**: perfil dos clientes (tipo, idade, cidade e score de lealdade).
- **Rentals**: registros de locações (datas, cidade, diária, distância percorrida).
- **Vehicles**: frota de veículos (modelo, tipo de combustível, categoria, emissão de CO₂ por km).

## Etapas da Análise

Principais etapas realizadas no notebook: [file:1]

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
  - Extração de ano e mês da data de início da locação para análises temporais. [file:1]

## Tecnologias Utilizadas

- **Python**
- **Pandas** para manipulação, limpeza e junção de dados. [file:1]
- **Google Colab** como ambiente de desenvolvimento e execução do notebook. [file:1]

## Como Executar o Projeto

1. Faça o download do notebook `.ipynb`.
2. Abra o arquivo no **Google Colab**.
3. Disponibilize os arquivos de dados (CSV/JSON) no ambiente (Google Drive ou upload direto). [file:1]
4. Atualize os caminhos de leitura dos arquivos, se necessário.
5. Execute as células em ordem para reproduzir todo o fluxo de análise. [file:1]

## Próximos Passos

- Criar visualizações para acompanhar:
  - Receita por período.
  - Uso da frota por categoria de veículo.
  - Emissão de CO₂ por cliente, cidade e tipo de veículo. [file:1]
- Explorar segmentações por tipo de cliente, cidade e categoria de veículo para gerar insights de negócio e sustentabilidade. [file:1]
```

[1](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/139582365/67be79a9-5833-44c9-8c3a-3a338d995799/34_4_DA_FM_TUC_AS6_PY_07_Avaliacao_Projeto_de_Conclusao_da_Unidade.ipynb)
