# Estudo de caso
## Dashboard Analítico de Geolocalização e Mapeamento de Clientes por Saldo Bancário

**Definição do Problema de Negócio**

Você é o Analista de  Dados  de  uma operadora  de  plano  de  saúde  que atende em quatro regiões do Brasil.

Os diretores perceberam que os gastos de seguro saúde aumentaram de forma considerável e precisam monitorar a evolução dos gastos. Eles fizeram diversas perguntas e gostariam de poder visualizar as respostas em uma única tela ou visualização.

Sua fonte de dados é um [arquivo CSV](https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-07/seguro_saude.csv) com as informações que correspondem ao ano anterior dos usuários da operadora.

Coluna   | Descrição
--- | ---
Idade | Idade do cliente
Sexo | Sexo do cliente
IMC | Índice de massa corpórea do cliente
Criança | Cliente é criança?
Fumante | Cliente é fumante?
Região | Região do Brasil na qual o cliente reside
Valor_seguro_saude | Valor do seguro saúde do cliente

Os diretores precisam saber:
1. Qual o gasto total da operadora?
2. Qual a idade média dos usuários da operadora?
3. Qual o gasto médio por região?
4. Qual faixa etária possui maior gasto com seguro saúde por região?
5. Crianças tem gasto maior que adultos?
6. Qual a proporção de crianças por região?
7. O aumento da idade influencia no imc?
8. Quem tem maior gasto, homens ou mulheres?
9. Se o usuário for mulher, o imc é acima ou abaixo da média?
10. Se for homem, com mais de 50 anos e da região Sudeste, o gasto é maior ou menor que a média de gastos da região?


*********Você  deve  construir  seu  projeto  no  Power  BI e  enviar para projeto@dsacademy.com.br. Você deve enviar o projeto criado no Power BI. Você deve enviar o projeto criado no Power BI.*************

***Para tal, os gráficos apresentados são:
- 
***

## Dashboard construído
[Arquivo Power BI](https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-06/projeto_cap_06.pbix)

**Visão geral**
<center><img src="https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-06/projeto06_visual.png" alt ="Dashboard Analítico de Geolocalização e Mapeamento de Clientes por Saldo Bancário" width="800"></center>

## Passo a passo do processo
1. Importar o dataset "seguro_saude" para o Power BI.
2. Transformar dados:
   - O dataset não possuí cabeçalho, porém há duas linhas com os títulos das colunas. A primeira linha foi utilizada como cabeçalho e a segunda foi excluída.
   - A coluna "sexo" possuí por padrão os valores "masculino" e "feminino". As linhas com valores diferentes destes foram excluídas.
   - O tipo de dado da coluna "imc" foi transformado para número decimal e os valores arredondados para duas casas decimais.
   - A coluna "crianca" por ser uma variável categórica teve seus valores transformados para "não" caso este fosse igual a 0 e para "sim" caso fosse diferente de 0.
   - A coluna "fumante" não foi utilizada nas análises, portanto foi excluída.
   - A coluna "regiao" possuí por padrão os valores "nordeste", "norte", "sudeste" e "sul". As linhas com valores diferentes destes foram excluídas.
   - O tipo de dado da coluna "valor_seguro_saude" foi transformado para número decimal e os valores arredondados para duas casas decimais.
   - Para fins visuais as colunas tiveram seus nomes modificados conforme a tabela abaixo e as variáveis categóricas tiveram seus valores alterados para que a primeira letra de cada palavra seja maiúscula: Nome real | Nome após alteração
--- | ---
idade | Idade
sexo | Gênero
imc | IMC
criança | É criança?
região | Região
valor_seguro_saude | Gasto com Seguro Saúde
3. Identificar os filtros a serem utilizados afim de tornar mais simples a interação do usuário final 
4. 

