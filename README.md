"Traduz sempre para o Inglês, isso evita que as Escritas não apareçam fora do contexto"



Esse case, segue o processo completo de análise de dados:


1. Definição Do Negócio


1.1 PROBLEMA DE NEGÓCIO
   

Como aumentar a receita e a rentabilidade das vendas identificando os produtos, regiões e períodos que têm melhor desempenho?


1.2 PROBLEMA DE NEGÓCIO


	Descobrir quais produtos mais vendem.
	Identificar os clientes que mais compram.
	Avaliar sazonalidade (melhores meses).
	Medir lucratividade por produto, vendedor e região.
	Encontrar oportunidades para reduzir custos ou aumentar ticket médio.


1.3 PERGUNTAS DE NEGÓCIO


	Quais produtos geram mais receita?
	Quem São Os Top Vendedores Em Faturamento, Margem De Lucro E Ticket Médio?
	Qual região vende mais e qual tem menor lucro?
	Em que meses as vendas aumentam ou diminuem?
	Qual vendedor tem melhor conversão ou maior lucro?
	Quais produtos têm melhor margem de lucro?





Análise de dados não se começa no Power BI, mais sim no nosso Banco.
SQL é a habilidade que dá autonomia para o analista gerar N Insights, onde Planilha é cálculo e Banco de dados é informação.
Para a Estrutura da nossa Query, usamos os seguintes Comandos: 

	Comando de agregações
	CTE com a clausula With
	Funções de Janelas 
	Joins
	Etc...



<img width="1145" height="828" alt="image" src="https://github.com/user-attachments/assets/d5974af5-28d4-4d95-8692-c24c8d77a611" />


<img width="1168" height="1540" alt="image" src="https://github.com/user-attachments/assets/f0463423-01ec-4233-826e-6d08f08dc3c9" />


<img width="1150" height="1498" alt="image" src="https://github.com/user-attachments/assets/79a51fd5-ec38-4311-9103-f2c5ae576cdc" />








		O Nosso Power BI, Será A Consequência Da Nossa Análise Mais Visual 


			2. Coleta Dos Dados

			
	Fonte dos Dados:
	Os dados foram obtidos do Banco comercio 3 onde Compõem:
	A Tabela Base Venda:
 	Data Venda, Produto, Região, Vendedor, Quantidade, Preço Unitário, Custo Unitário, Receita e Lucro 




<img width="886" height="434" alt="image" src="https://github.com/user-attachments/assets/8a653f3b-9927-4b1c-a9f4-4036f42a28f0" />





	3. Ferramentas Utilizadas 

	
Usei Power Query para:

3.1 Importação, Limpeza e Tratamento (ETL com Power Query)

Tarefas realizadas:

Remoção de linhas em branco e duplicadas

Padronização de datas e nomes

Criação de colunas calculadas:

Custo = Quantidade × Custo Unitário

Criação de colunas de Mês e Ano




	
 	4. Modelagem de Dados: Relacionamentos e estrutura Star Schema.

Explicação Clara:

Usei Modelagem Dimensional, Criando a tabela Fato e Dimensão para facilitar o nosso relacionamento entre as tabelas. 
A normalização para dividir   a nossa tabela, evitando assim a redundância nas nossas informações. 

Modelo em estrela (Star Schema):

             Dim_Vendedor
                  |
				  
 Dim_Produto — Fato_Venda — Dim_Região
                  |
				  
             Dim_d_Calemdario 





<img width="1152" height="638" alt="image" src="https://github.com/user-attachments/assets/b36c97bb-e1bd-4e2d-b7dc-ee7d97320df5" />



		 5. DAX: Medidas, indicadores e KPIs.
    
		5.1 Métricas 

•	Total vendido (Medir tamanho do negócio)

•	Total de custo

•	Total de lucro (Medir eficiência)

•	Quantidade vendida

		5.2  Indicadores 


•	Ticket Médio = Receita ÷ Nº pedidos (Monitorar valor de vendas por transação)

•	Margem de Lucro (%) = Lucro ÷ Receita × 100 (Objetivo Avaliar saúde financeira)

•	Crescimento Anual (%) :Objetivo é avaliar o crescimento ano a ano (YOY) 


		5.3  KPIs Estruturados com os Seguintes Gráficos e Tabelas 

•	Receita por mês e ano 

•	Receita por produto 

•	Custo por produto

•	Lucro por produto

•	Tabela que ilustra o comparativo anual como: ano, faturamento, crescimento ano, lucro, margem de lucro e ticket médio

•	Lucro por região

•	Faturamento por região 

•	Crescimento anual por região 

•	Tabela que apresenta as seguintes analises dos produtos: Faturamento, lucro, margem de lucro e ticket médio

•	Tabela que ilustra a performance por vendedores: Faturamento, lucro, margem de lucro e ticket médio

•	Tabela que monstra a margem de lucro por produto em cada região: Nome produtos, regiões e margem de lucro 





<img width="1129" height="1104" alt="image" src="https://github.com/user-attachments/assets/a66d2a57-9833-4cda-ac62-f0de7b09fc15" />





	6. Visualização: Gráficos, tabelas dinâmicas e layout.
   
Elementos do Dashboard:

Card: para mostrar um único valor criando assim impacto rápido.

Gráfico de Linha:  Ideal para mostrar tendências ao longo do tempo 

Gráfico de Barra: Usamos para comparar categorias 

Gráfico de Coluna: Usamos para comparar categorias 

Tabela dinâmica: Usamos porque resumo grande volume de dados que permite agrupar com mais eficiência. 



<img width="1125" height="802" alt="image" src="https://github.com/user-attachments/assets/589b5c5c-2deb-48c2-91ed-a08a4c6e7fce" />




<img width="1035" height="645" alt="image" src="https://github.com/user-attachments/assets/b4643e6f-9d08-4c15-8fd5-bb4aff2e3f10" />



<img width="1060" height="688" alt="image" src="https://github.com/user-attachments/assets/22d9323b-2c9a-4fb4-99f5-e8c988c0acfa" />



<img width="1121" height="697" alt="image" src="https://github.com/user-attachments/assets/5a3ac58e-9dc6-4f78-ae03-0a7f99070daa" />




<img width="1108" height="678" alt="image" src="https://github.com/user-attachments/assets/bdb5715b-830b-42e9-82a9-28c39bc2ae70" />




			7. Interatividade: Segmentadores, Filtros, Drill Down e Bookmarks


		Segmentações (Slicers)


•	Análise Ano 

•	Análise Vendedor

•	Análise Produto

•	Análise Região





		 Informações Extras:
 
•	Botões de Paginação 

•	Botões para limpara a segmentação de dados

•	Tooltip no Card de Faturamento Total 

•	Drill Down, usei no gráfico de Linha 




			8. Insights 

		8.1. Quais Produtos Geram Mais Receita?


1.	Notebook pro — R$ 248,5 mil
   
2.	Smartphone  x— R$ 61,5 mil
   
3.	Smartwatch Z— R$ 46,4 mil
   
Esses três estão no topo da lista, com os notebooks liderando disparado.



		8.2. Quem São Os Top Vendedores Em Faturamento, Margem De Lucro E Ticket Médio?
		
Os top vendedores em faturamento são:

1.	Fernanda — R$ 194.700,00
   
2.	Pedro — R$ 187.100,00
   
3.	Ana — R$ 161.700,00
   
Esses três lideram em receita gerada, com Fernanda no topo. Ela faturou quase R$ 8 mil a mais que Pedro, o segundo colocado.


Top 3 em Margem de Lucro

1.	Carlos — 24,79%
   
2.	João — 24,64%
   
3.	Ana — 24,09%
   
Carlos lidera com a maior eficiência na geração de lucro sobre o faturamento.


Top 3 em Ticket Médio

1.	Fernanda — R$ 9.735,00
   
2.	João — R$ 9.056,25
   
3.	Pedro — R$ 8.909,52
   
Fernanda também se destaca aqui, indicando que suas vendas têm maior valor por transação.






		8.3. Qual região vende mais e qual tem menor lucro?

A região que vende mais é a Oeste, com um faturamento de R$ 305,4 mil.

Aqui está o ranking completo:

1.	Oeste — R$ 305,4 mil
   
2.	Leste — R$ 251 mil
	
3.	Sul — R$ 236,9 mil
	
4.	Norte — R$ 209,6 mil
	
A região Oeste lidera com folga, representando a maior contribuição para o faturamento total
A região com menor lucro é a Norte, com um total de R$ 54,6 mil.


Aqui está o ranking completo do lucro por região:

1.	Oeste — R$ 72,05 mil
   
2.	Sul — R$ 57,15 mil
	
3.	Leste — R$ 56,9 mil
   
4.	Norte — R$ 54,6 mil
   
Apesar de não estar muito distante das demais, a região Norte apresenta o menor desempenho em termos de lucro total.



		8.4. Em que meses as vendas aumentam ou diminuem?


Meses com aumento de vendas

•	Fevereiro → Março: salto de R$ 17,60 mil para R$ 126,20 mil (maior crescimento do período)

•	Abril → Maio: recuperação de R$ 7,60 mil para R$ 78,70 mil

•	Junho → Agosto: crescimento gradual de R$ 59,60 mil → R$ 41,30 mil (com leve queda em julho)

Meses com queda de vendas

•	Janeiro → Fevereiro: queda de R$ 47,40 mil para R$ 17,60 mil

•	Março → Abril: queda brusca de R$ 126,20 mil para R$ 7,60 mil (maior queda do período)

•	Maio → Junho → Julho: queda contínua de R$ 78,70 mil → R$ 59,60 mil → R$ 37,40 mil

Destaque: Março foi o pico de faturamento, enquanto Abril foi o fundo do poço. Isso pode indicar sazonalidade, problemas operacionais ou falta de campanhas nesse mês.


		8.5. Qual vendedor tem melhor conversão ou maior lucro?

Melhor Conversão (Maior Margem de Lucro)

A margem de lucro indica a eficiência na conversão de faturamento em lucro. Os líderes são:

1.	Carlos — 24,79%
	
2.	João — 24,64%
	
3.	Ana — 24,09%

   
Carlos é o mais eficiente em transformar vendas em lucro.

Maior Lucro Total

Aqui vemos quem gerou mais dinheiro líquido:

1.	Fernanda — R$ 45.750
   
2.	Pedro — R$ 43.850
	
3.	Ana — R$ 38.950
	
Fernanda lidera em lucro absoluto, mesmo com uma margem um pouco menor que Carlos.



		8.6. Quais produtos têm melhor margem de lucro?


Os produtos com melhor margem de lucro são:


1.	Fone Bluetooth — 50,00%

   
3.	Smartwatch Z — 37,50%

   
5.	Tablet Mini — 25,00%


   
Esses três se destacam por gerar mais lucro proporcionalmente ao faturamento. O Fone Bluetooth, apesar de ter o menor faturamento, é o mais lucrativo em termos percentuais.







		9. Recomendação (o que fazer agora?)

	9.1. Foco nos Produtos com Alta Margem de Lucro
	
•	Fone Bluetooth (50%) e Smartwatch Z (37,5%) têm margens muito superiores à média.

•	Apesar do faturamento menor, eles são extremamente rentáveis.

Recomendação: Invista em campanhas de marketing e volume para esses produtos. Aumentar vendas pode escalar o lucro rapidamente.


 	9.2. Potencial de Escala com Produtos de Alto Faturamento
 
•	Notebook Pro lidera em faturamento (R$ 497 mil) e lucro absoluto (R$ 99.400), mesmo com margem de 20%. 

Recomendação: Mantenha esse produto como carro-chefe, mas avalie formas de reduzir custos ou agregar valor para melhorar a margem.

	9.3. Vendedores com Maior Eficiência
	
•	Carlos tem a melhor margem de lucro (24,79%), enquanto Fernanda lidera em faturamento e lucro total. 

 Recomendação: Use Carlos como referência em treinamento para conversão eficiente e Fernanda como modelo de volume de vendas.
 
	9.4. Regiões com Maior Potencial
	
•	Oeste lidera tanto em faturamento (R$ 305,4 mil) quanto em lucro (R$ 72,05 mil). 

 Recomendação: Priorize investimentos logísticos, estoque e ações comerciais nessa região para maximizar retorno.
 
	9.5. Equilíbrio Estratégico

•	Produtos como Tablet Mini têm boa margem (25%) e faturamento intermediário — são ideais para manter equilíbrio entre volume e rentabilidade. 







 10. Publicação e Compartilhamento




Link  do meu Dashboard




https://app.powerbi.com/view?r=eyJrIjoiMDU2MDA5NzAtNjY2Ny00OGUzLTk5ODgtNDEwYmU2NjZhYzY0IiwidCI6IjJmMDIyNDJjLTgzZWUtNGU1NC1hNTUxLTc3YjI5OWFhMDMwNyJ9


