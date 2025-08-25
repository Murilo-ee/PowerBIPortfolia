# 📊 Análise de Vendas e Lucro — Dashboard Interativo Power BI

## 📝 Sobre o Projeto
Este é um projeto de portfolio feito para monitorar os KPI de uma empresa fictícia internacional de plantas e criar um dashboard interativo no Power BI para acompanhar métricas de vendas, quantidades, lucros e desempenho global. Os dados estão no arquivo excel.

Todas as medidas foram feitas em DAX no objetivo de desenvolver as minhas habilidades com a ferramenta.



O painel oferece uma visão gerencial dos KPI's e contem dois filtros que afetam todo o dashboard, é possivel filtrar por Ano e por tipo de indicador ( Lucro, Faturamento bruto  e Quantidade), todos os titulos são atualizados de acordo com o que esta sendo visualizado e os visuais são interativos


## 🛠️ Ferramentas e Tecnologias
| Ferramenta | Finalidade |
|-----------|------------|
| **Power BI** | Criação do dashboard, visualizações e KPIs |
| **DAX** | Todas as medidas na tabela 'measures' foram criadas utilizando DAX |
| **Power Query** | Foi utilizado para tratar os dados antes de montas os visuais |
| **Excel / CSV** | Base de dados para análise |
| **GitHub** | Versionamento e publicação do projeto |

---

## 📊 Principais Métricas (KPIs)
- **Vendas Totais**: valores acumulados e comparativos.
- **Quantidade Vendida**: evolução mensal e por produto.
- **Lucro Bruto**: análise do impacto financeiro.
- **Diferença entre anos (%)**: crescimento ou queda ano a ano.
- **Distribuição por País**: mapa e ranking de performance.

---

## 🖼️ Visualizações do Dashboard



### Plant_FACT *(2.440 linhas × 7 colunas)*  
Tabela de **fatos de vendas**, representando cada transação.

| Coluna         | Descrição                                      |
|---------------|-----------------------------------------------|
| Product_id    | Identificador único do produto vendido         |
| Sales_USD     | Valor da venda em dólares                      |
| quantity      | Quantidade vendida                             |
| Price_USD     | Preço unitário do produto em dólares           |
| COGS_USD      | Custo do produto vendido (Cost of Goods Sold)  |
| Date_Time     | Data e hora da transação                       |
| Account_id    | Chave para identificar o cliente na tabela **Accounts** |

Essa é a tabela fato


### Accounts *(1.744 linhas × 10 colunas)*  
Tabela de **clientes** ( tabela dimensão), contendo informações globais sobre localização e identificação.

| Coluna         | Descrição                               |
|---------------|----------------------------------------|
| Account_id    | Identificador único do cliente          |
| Account       | Nome da conta ou cliente                |
| country_code  | Código do país (ISO)                    |
| country2      | Nome do país                            |
| latitude2     | Latitude da localização                 |
| longitude     | Longitude da localização                |
| Postal_code   | Código postal                           |
| street_name   | Nome da rua                             |
| Street_number | Número do endereço                      |


### Plant_Hierarchy *(1.000 linhas × 8 colunas)*  
Tabela de **dimensão de produtos** (tabela dimensão), com detalhes sobre famílias, grupos e características.

| Coluna          | Descrição                            |
|-----------------|-------------------------------------|
| Product_Family  | Família principal do produto         |
| Product_Group   | Subcategoria dentro da família       |
| Product_Name    | Nome do produto                      |
| Product_Size    | Tamanho do produto                   |
| Produt_Type     | Tipo do produto                      |







---

Exemplo de como colocar imagens:

```markdown
### 📌 Visão Geral
![Dashboard — Visão Geral](./images/visao_geral.png)

### 📌 Evolução YTD vs PYTD
![Dashboard — YTD vs PYTD](./images/ytd_vs_pytd.png)

### 📌 Análise por Produto
![Dashboard — Produto](./images/analise_produto.png)
