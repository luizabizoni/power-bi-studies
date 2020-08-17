# Estudo de caso 2
## Estratégias de Vendas para empresa PontoMaximo

**Definição do Problema de Negócio**

Você  é  Analista  de  Dados  na  empresa PontoMaximo,  uma rede  de  varejo  que  vende produtos eletrônicos e eletrodomésticos com lojas espalhadas por diversas cidades do Brasil. A empresa começou sua operação no Brasil em 2012 e atua nos quatro estados da região sudeste mais os estados do Paraná e Bahia.

A empresa está montando a estratégia de vendas para o próximo ano e precisa saber *qual  dos  fabricantes  dos  produtos  vendidos  apresenta  melhor  desempenho  nas  vendas*.  O objetivo é descartar os fabricantes cujos produtos possuem poucas vendas e tentar negociar melhores condições com os principais fabricantes.

Em paralelo a isso, a empresa gostaria de ter diferentes visões das vendas realizadas nos últimos 4 anos (período de 2012 a 2015). Deve ser possível segmentar os relatórios de vendas por  diferentes  informações  e  por  diferentes  ângulos.  Estas  informações  irão  suportar  as estratégias da empresa para o próximo ano.

Sua fonte de dados é um [arquivo Excel](https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-03/Vendas.xlsx) com dados coletados do sistema de vendas, CRM e ERP da empresa. O conjunto de dados foi entregue pelo departamento de TI com as seguintes colunas:

Coluna   | Descrição
--- | ---
ID-Produto | Identificador único de cada produto
Produto | Nome do produto
Categoria | Categoria do produto
Segmento | Segmento do produto
Fabricante | Fabricante do produto
Loja | Loja onde foi efetuada a venda
Cidade | Cidade da loja onde foi efetuada a venda
Estado | Estado da loja onde foi efetuada a venda
Vendedor | Nome do vendedor
ID-Vendedor | ID-Vendedor
DataVenda | Data da venda
ValorVenda | Valor da venda

Haverá diversas reuniões para definição da estratégia de vendas e os relatórios poderão ser extraídos sob demanda, de acordo com a necessidade dos gestores. Por conta disso, você deve *criar um modelo de dados que permita a extração de relatórios a qualquer momento e que permita extrair dados por diferentes visões e ângulos*.

### Dashboard construído

[Arquivos Power BI](https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-03/estudo_02.pbix)

**Modelo Star Schema**

<center><img src="https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-03/dashboard_estudo_02.PNG" alt ="Modelo star schema das tabelas da empresa PontoMaximo" width="800"></center>

**Visão geral**

<center><img src="https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-03/dashboard_estudo_02_02.PNG" alt ="Dashboard para definir as estratégias de vendas para empresa PontoMaximo" width="800"></center>
