# Análise de Teste A/B — Sistema de Recomendação

## 📌 Sobre o Projeto

Este projeto analisa um teste A/B realizado por uma loja online para avaliar o impacto da introdução de um novo sistema de recomendação sobre a conversão dos usuários.

A análise verifica a qualidade e consistência dos dados, explora o comportamento dos usuários no funil de conversão e utiliza testes estatísticos para avaliar se o grupo experimental apresentou melhora significativa em relação ao grupo de controle.

## 🎯 Objetivos
- Avaliar a qualidade e consistência dos dados do experimento;
- Analisar o comportamento dos usuários nos grupos A e B;
- Avaliar as taxas de conversão nas etapas do funil;
- Verificar possíveis problemas na composição das amostras;
- Comparar estatisticamente as taxas de conversão dos grupos;
- Avaliar se o novo sistema de recomendação atingiu o aumento esperado de 10%.

## 🛠️ Ferramentas e Tecnologias
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook

## 🔎 Análises Realizadas
- Tratamento e validação dos dados;
- Análise dos participantes e grupos do experimento;
- Análise da distribuição de eventos por usuário e ao longo do tempo;
- Construção do funil de conversão;
- Análise das conversões entre as etapas do funil;
- Teste Z para comparação de proporções;
- Correção de Bonferroni para múltiplas comparações.
  
## 📈 Principais Resultados
- Foram identificados 441 usuários presentes simultaneamente nos grupos A e B, que foram removidos para evitar interferência entre as amostras.
- Os grupos apresentaram distribuição diferente no número de eventos por usuário: média de 4,13 eventos no grupo A e 3,03 no grupo B.
- A mediana foi de 3 eventos no grupo A e 0 eventos no grupo B, indicando diferença relevante de engajamento entre as amostras.
- Foram identificados usuários que realizaram product_cart antes de product_page, tornando necessário considerar a ordem temporal dos eventos no cálculo das conversões.
- O período de análise apresentou uma queda acentuada no volume de eventos em 30/12, indicando possível coleta incompleta dos dados nesse dia.
- Na etapa product_page → product_cart, o grupo B apresentou aumento de aproximadamente 3,66%, abaixo da meta de 10%.
- Na etapa product_cart → purchase, o aumento do grupo B foi de aproximadamente 2,78%, também abaixo da meta de 10%.
- Os testes Z não identificaram diferenças estatisticamente significativas entre os grupos: p-valor = 0,5999 para product_page → product_cart e p-valor = 0,9638 para product_cart → purchase.
- Mesmo após a aplicação da correção de Bonferroni, os resultados permaneceram sem significância estatística.
- Portanto, o novo sistema de recomendação não apresentou evidências de melhoria significativa na conversão e não atingiu o aumento mínimo de 10% esperado pelo experimento.

## 💡 Conclusão

Os resultados não fornecem evidências suficientes para recomendar a implementação do novo sistema de recomendação. Além de não apresentar diferenças estatisticamente significativas, o grupo experimental não atingiu a melhoria mínima de 10% esperada.

Também foram identificadas limitações na execução do experimento, como usuários presentes nos dois grupos, diferenças na distribuição de eventos e possível incompletude dos dados no último dia. Recomenda-se revisar o desenho experimental e realizar um novo teste com grupos adequadamente controlados e uma janela de observação comparável.

📓 Notebook

A análise completa pode ser consultada no notebook:

[👉 Acessar o notebook do projeto](notebook.ipynb)
