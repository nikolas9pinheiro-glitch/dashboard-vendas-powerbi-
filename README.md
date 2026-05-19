# 📊 Dashboard de Análise de Vendas Comercial

Análise visual e interativa de dados de vendas desenvolvida no Power BI para suporte à tomada de decisão estratégica. Este projeto engloba desde a modelagem dos dados até a criação de indicadores-chave de performance (KPIs).

---

## 📌 Contexto e Objetivo do Projeto

O objetivo deste painel é fornecer aos gestores uma visão clara do desempenho de vendas, permitindo identificar gargalos, produtos mais rentáveis, comportamento dos clientes e a evolução do faturamento ao longo do tempo.

Com este dashboard, a liderança consegue responder a perguntas como:
- Qual é o faturamento total acumulado e a margem de lucro atual?
- Quais regiões ou vendedores estão atingindo as metas?
- Existe alguma tendência ou sazonalidade visível no histórico de vendas?

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

- **Power BI Desktop:** Modelagem de dados, criação de medidas DAX e design dos relatórios.
- **Power Query:** Limpeza, transformação e tratamento dos dados (ETL).
- **Linguagem DAX:** Criação de métricas calculadas e KPIs de performance.
- **GitHub:** Versionamento e apresentação do portfólio.

---

## 🏗️ Estrutura e Modelagem de Dados

O projeto foi construído seguindo as melhores práticas de modelagem multidimensional. Os dados estão estruturados no formato **Star Schema** (Esquema Estrela), garantindo performance e integridade aos filtros.

- **Tabela Fato:** `Fato_Vendas` (contém o histórico das transações, valores e quantidades).
- **Tabelas Dimensão:** - `Dim_Clientes` (informações cadastrais e demográficas)
  - `Dim_Produtos` (categorias, custos e preços)
  - `Dim_Calendario` (criada em DAX para inteligência de tempo)
  - `Dim_Vendedores` (equipe comercial e metas)

---

## 📉 Visualização do Dashboard

*Substitua os caminhos abaixo pelas fotos que você salvou na pasta `imagens/`*

### 1. Visão Geral (Faturamento e Principais KPIs)
![Visão Geral](./imagens/1.jpg)
*Breve descrição desta tela (ex: Insights sobre faturamento total, margem e evolução mensal).*

### 2. Análise por Categoria e Produtos
![Análise de Produtos](./imagens/2.jpg)
*Breve descrição desta tela (ex: Ranking dos produtos mais vendidos e comportamento do ticket médio).*

*(Dica: Adicione as outras fotos que considerar mais relevantes para o usuário entender o fluxo do dashboard, como telas de filtros, detalhes de clientes, etc.)*

---

## 🧠 Métricas e Principais Fórmulas DAX

Aqui estão algumas das principais métricas desenvolvidas para este projeto:

**Faturamento Total:**
```dax
Faturamento Total = SUM(Fato_Vendas[Valor_Venda])