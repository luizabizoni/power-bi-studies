# Estudo de caso
## Dashboard de vendas, custo, margem de lucro e KPI

**Definição do Problema de Negócio**

Reproduzir o seguinte dashboard:
<center><img src="https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-04/exercicio.png" alt ="Dashboard a ser reproduzido" width="800"></center>

Sua fonte de dados é um [arquivo CSV](https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-04/Custos.csv).

Coluna   | Descrição
--- | ---
Data | Data de vendas
Produto | ID do produto
Serial number | Número serial
Valor de venda | Valor de venda do produto
Preço custo | Preço de custo do produto
Duração Venda Telefone (mins) | Duração da venda em minutos via telefone
Tempo Preparação (mins) | Tempo de preparação para venda em minutos

Os gráficos a serem apresentados serão:
- Média de vendas
- Valor de venda X preço de custo
- Margem de lucro por produto
- KPI - Meta de margem de lucro

Para construir o gráfico de média de vendas foi utilizado no eixo as informações de data e nos valores a média de valor de venda. Esta medida foi construída utilizando DAX (Média de venda = (AVERAGE(CustosGeral[Valor de Venda])).
Para o de valor de venda X preço de custo, no eixo X foi utilizada a soma do valor de vendas, o eixo y a soma do preço de custo e para detalhes o campo produto.
Para o gráfico de margem de lucro por produto o grupo selecionado foi o campo produto, e os valores a soma de margem de lucro. A construção da coluna de margem de lucro foi feita utilizando DAX (Margem de Lucro = 1 - (DIVIDE(CustosGeral[Preço Custo],CustosGeral[Valor de Venda],0))).
Finalmente, para o gráfico de KPI, como indicador foi utilizada a média da margem de lucro, para o eixo de tendência a coluna data e a meta de destino o valor máximo de margem de lucro.

## Dashboard construído
[Arquivo Power BI](https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-04/projeto3.pbix)

**Visão geral**
<center><img src="https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-04/exercicioResolucao.PNG" alt ="Dashboard de vendas, custo, margem de lucro e KPI" width="800"></center>
