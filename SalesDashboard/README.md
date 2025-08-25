# 📊 Análise de Vendas e Lucro — Dashboard Interativo em Power BI  

## 📝 Sobre o Projeto  
Este projeto faz parte do meu portfólio e tem como objetivo **monitorar os principais KPIs** de uma empresa fictícia internacional de plantas, utilizando um **dashboard interativo** no **Power BI**.  

Os dados brutos estão armazenados em **Excel** e foram tratados no **Power Query** antes da modelagem. Todas as medidas foram criadas em **DAX** para o **desenvolvimento de habilidades** e para poder criar um painel intuitivo, dinâmico e interativo.  

O dashboard permite acompanhar **faturamento bruto, quantidade vendida e lucro bruto** em diferentes níveis de detalhamento, oferecendo filtros por **ano** e **tipo de indicador**. Todos os títulos, valores e visuais são atualizados dinamicamente com base na seleção do usuário.  

---

## **Visão Geral do Dashboard**

O painel foi desenvolvido para oferecer uma visão gerencial clara e objetiva. Os principais elementos incluem:

- **Treemap – Arrecadação por País**  
  Identifica os países com maior e menor contribuição para o faturamento total.
- **Gráfico Waterfall – Variação Mês a Mês**  
  Exibe a evolução mensal do KPI selecionado (**Vendas, Quantidade ou Lucro Bruto**), destacando aumentos e reduções.
- **Gráfico de Colunas + Linha – Comparativo Ano a Ano**  
  Mostra a evolução acumulada do KPI escolhido, comparando ano atual e anterior.
- **Scatterplot – Lucratividade por Conta**  
  Apresenta a relação entre **margem de lucro (%)** e **acúmulo no ano** para cada cliente.
- **Cards de KPIs**  
  Destacam valores do ano atual, ano anterior, variação absoluta e percentual de lucro.
- **Slicer Dinâmico**  
  Permite alternar entre diferentes KPIs de forma simples e intuitiva.

![Dashboard Geral](Dashboard1.jpg)

---

## **Drill Down no Gráfico Waterfall**

O gráfico waterfall é totalmente interativo e suporta **drill down** para aprofundar a análise.  
A hierarquia de detalhamento segue a seguinte ordem:

**Mês → Tipo de Produto → Produto**

No exemplo abaixo, foi realizado o drill down em um **mês específico**, detalhando os resultados por **tipo de produto**. Isso possibilita entender quais categorias tiveram maior impacto no desempenho do período.

![Drill Down no Waterfall](Dashboard2.jpg)

---

## **Segmentação de Contas no Scatterplot**

O **scatterplot** exibe a **lucratividade (%)** das contas em relação ao **valor acumulado no ano**.  
É possível selecionar **uma conta específica** diretamente no gráfico, e todos os demais visuais do dashboard são filtrados para apresentar os indicadores relacionados apenas a esse cliente.  

No exemplo abaixo, uma conta foi selecionada para acompanhar sua performance individual.

![Segmentação de Contas](Dashboard3.jpg)

---

## 🛠️ Ferramentas e Tecnologias  

| Ferramenta      | Finalidade                                          |
|-----------------|-----------------------------------------------------|
| **Power BI**    | Criação do dashboard, construção de visuais e KPIs |
| **DAX**         | Criação de todas as medidas calculadas             |
| **Power Query** | Transformação e limpeza dos dados                  |
| **Excel / CSV** | Base de dados para análise                         |
| **GitHub**      | Versionamento e publicação do projeto              |

---

## 📊 Principais Métricas (KPIs)

- **Faturamento Bruto:** evolução mensal, comparativo entre anos e total acumulado.  
- **Quantidade Vendida:** variação por mês, produto e tipo de produto.  
- **Lucro Bruto:** impacto financeiro agregado e individual por cliente.  
- **Diferença entre Anos:** análise percentual e absoluta da evolução.  
- **Distribuição por País:** ranking de performance global.  

---

## 🗂️ Modelagem de Dados  

O modelo foi construído com base no conceito **Star Schema** para otimizar o desempenho e a usabilidade do dashboard.

### **Plant_FACT** *(2.440 linhas × 7 colunas)*  
Tabela de **fatos de vendas**, representando cada transação.  

| Coluna       | Descrição                                      |
|-------------|-----------------------------------------------|
| Product_id  | Identificador único do produto vendido         |
| Sales_USD   | Valor da venda em dólares                      |
| Quantity    | Quantidade vendida                             |
| Price_USD   | Preço unitário do produto em dólares           |
| COGS_USD    | Custo do produto vendido                       |
| Date_Time   | Data e hora da transação                       |
| Account_id  | Identificador da conta do cliente              |

---

### **Accounts** *(1.744 linhas × 10 colunas)*  
Tabela de **clientes** (*dimensão*), com dados detalhados sobre cada conta.  

| Coluna        | Descrição                          |
|--------------|----------------------------------|
| Account_id   | Identificador único do cliente   |
| Account      | Nome da conta ou cliente        |
| Country_code | Código do país (ISO)            |
| Country2     | Nome do país                    |
| Latitude2    | Latitude da localização         |
| Longitude    | Longitude da localização        |
| Postal_code  | Código postal                   |
| Street_name  | Nome da rua                     |
| Street_number| Número do endereço              |

---

### **Plant_Hierarchy** *(1.000 linhas × 8 colunas)*  
Tabela de **produtos** (*dimensão*), com detalhes sobre categorias, tipos e tamanhos.  

| Coluna         | Descrição                      |
|---------------|-------------------------------|
| Product_Family | Família principal do produto  |
| Product_Group  | Subcategoria do produto       |
| Product_Name   | Nome do produto              |
| Product_Size   | Tamanho do produto           |
| Product_Type   | Tipo do produto             |

---

## 🚀 Principais Destaques do Projeto  

- **Uso de DAX** para cálculo dinâmico de KPIs.  
- **Drill down interativo** no gráfico waterfall para análise detalhada.  
- **Segmentação de contas** para acompanhamento individual da performance.  
- **Modelagem otimizada** com esquema estrela, melhorando tempo de resposta.  
- **Design responsivo e intuitivo**, pensado para gestores e tomadores de decisão.  



