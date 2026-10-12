# BI_Chuvas_Brasil_2025
Dashboard de Análise Climática e Pluviométrica (INMET) com dados sobre o Brasil em 2025
# 🌧️ Dashboard de Análise Climática e Pluviométrica (INMET)


## 📋 Sobre o Projeto
Este projeto consiste em uma solução ponta a ponta (End-to-End) de engenharia e análise de dados para monitoramento do histórico pluviométrico brasileiro utilizando os dados oficiais do **INMET (Instituto Nacional de Meteorologia)**. 

O objetivo principal é transformar dados brutos de estações meteorológicas em um painel executivo interativo no Power BI, permitindo identificar padrões climáticos, recordes históricos de precipitação, sazonalidade e distribuição geográfica das chuvas.

---

## ⚙️ Arquitetura e Pipeline de Dados (ETL)

O fluxo da solução foi estruturado em quatro etapas principais:

1. **Extração (Extract):** Baixados os arquivos com o histórico de dados meteorológicos disponibilizados publicamente pelo INMET.
2. **Transformação (Transform - Python):** Utilização de scripts em **Python** (`Pandas` e bibliotecas de manipulação de dados) para realizar a limpeza da base, tratamento de nulos, padronização de datas, mapeamento de regiões/UFs e estruturação das colunas de apoio (como estações do ano e meses).
3. **Carga (Load - SQL Server):** Os dados tratados foram inseridos e modelados em um banco de dados relacional no **SQL Server**, garantindo integridade e performance nas consultas.
4. **Visualização (Power BI & DAX):** Conexão direta com o SQL Server, criação de relacionamentos, colunas calculadas e medidas **DAX avançadas** (`TOPN`, `SUMMARIZE`, `ALLEXCEPT`, formatações dinâmicas) para alimentar o painel visual.

---

## 🎛️ Funcionalidades e Estrutura do Dashboard

O painel foi desenvolvido com foco em experiência do usuário (UX) e design executivo, dispondo de recursos interativos e visuais de alto impacto:

### 🔍 Filtros Interativos (Slicers)
* **Região e Estado (UF):** Filtragem geográfica dinâmica.
* **Estação do Ano:** Sazonalidade mapeada (Verão, Outono, Inverno e Primavera).
* **Mês:** Seleção cronológica dos meses do ano.

### 📊 Cartões Executivos (KPI Cards)
* **Recorde de Precipitação Diária:** Exibe o dia, a cidade/UF e o maior volume de chuva registrado em um único evento no escopo filtrado.
* **Total Acumulado:** Soma geral da precipitação de acordo com os filtros aplicados.
* **Cidade Mais Chuvosa:** Identifica o município com o maior acumulado total no período.
* **Média de Chuva Diária:** Indicador de tendência central da precipitação.

### 📈 Gráficos e Análises Visuais
* **Top 10 Estados (Gráfico de Barras):** Ranking dos estados brasileiros com maior volume acumulado de precipitação.
* **Top 10 Cidades (Gráfico de Área):** Visualização de tendência e volume das dez cidades mais chuvosas da base filtrada.
* **Acumulado por Mês (Gráfico de Barras):** Distribuição sazonal do volume de chuvas mês a mês (ordenados cronologicamente de Janeiro a Dezembro).

  
<img width="1432" height="802" alt="image" src="https://github.com/user-attachments/assets/b4e5bbb1-bc0a-48be-945e-1ca005161528" />


---

## 🛠️ Tecnologias Utilizadas

* **Python:** Limpeza, tratamento e automação do pipeline de ETL.
* **SQL Server:** Armazenamento, modelagem e consultas relacionais.
* **Power BI:** Construção do modelo de dados e design do dashboard interativo.
* **DAX (Data Analysis Expressions):** Criação de medidas complexas de agregação, filtros de contexto dinâmicos e formatação de textos condicionais.

---

## 🚀 Como Executar o Projeto

1. **Banco de Dados:** Restaure ou crie a estrutura de tabelas no seu **SQL Server** utilizando a base de dados tratada.
2. **Power BI:** Abra o arquivo `.pbix` incluído neste repositório.
3. **Fonte de Dados:** Atualize as credenciais do servidor SQL Server nas configurações de fonte de dados do Power BI para apontar para a sua instância local ou em nuvem.
4. **Explorar:** Navegue pelos filtros e interaja com os visuais!

---
