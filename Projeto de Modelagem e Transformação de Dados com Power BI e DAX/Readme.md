# Modelagem e Transformação de Dados com Power BI e DAX
---
Criando um modelo de dados utilizando o Power BI e a linguagem DAX.

## Passos:

### 1. Conectar-se aos Dados:

- Abra o Power BI Desktop.
- Na guia "Página Inicial", clique em "Obter Dados" e selecione o tipo de origem de dados adequado (por exemplo, Excel, CSV, Banco de Dados SQL, etc.).
- Selecione a tabela "Financial Sample" como fonte de dados.

### 2. Transformação de Dados:

- No Editor de Consultas, renomeie a tabela para "Financials_origem".
- Realize limpeza e formatação necessárias nos dados.
- Crie tabelas de dimensão e fato:
  - **D_Produtos:** Calcule métricas solicitadas (médias, mediana, máximo, mínimo) com base nas vendas de cada produto.
  - **D_Produtos_Detalhes:** Selecione colunas relevantes da tabela original para detalhes adicionais sobre os produtos.
  - **D_Descontos:** Calcule descontos aplicados a cada produto com base nos dados de vendas.
  - **D_Calendário:** Crie uma tabela de calendário utilizando a função `CALENDAR()` para abranger o período de tempo dos dados.
  - **F_Vendas:** Selecione colunas relevantes da tabela original para criar a tabela fato, garantindo relacionamentos corretos.

### 3. Relacionamentos:

- Na visualização de modelo, defina relacionamentos entre tabelas de dimensão e fato com base nas chaves primárias e estrangeiras.
- Verifique se os relacionamentos estão configurados corretamente e se não há ambiguidades.

### 4. Criação de Medidas e Colunas Calculadas:

- Utilize DAX para criar medidas e colunas calculadas para análises adicionais.
- Exemplo: Calcular lucro total, receita líquida, etc.

### 5. Desenvolvimento de Relatórios:

- Crie relatórios com visualizações relevantes para analisar dados de vendas, como gráficos de barras, tabelas dinâmicas, gráficos de dispersão, etc.
- Use filtros, slicers e segmentações para fornecer interatividade.

### 6. Validação e Otimização:

- Valide os resultados das análises em relação aos requisitos originais.
- Otimize consultas DAX conforme necessário para garantir eficiência do modelo de dados.

### 7. Publicação e Compartilhamento:

- Publique o arquivo do Power BI no serviço Power BI quando estiver satisfeito com o modelo e os relatórios.
- Compartilhe o relatório com usuários relevantes e forneça acesso conforme apropriado.

Este roteiro ajudará na criação de um modelo de dados eficaz e interativo no Power BI, atendendo aos requisitos específicos de uma análise baseada em star schema.