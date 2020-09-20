# Desafio
## Dashboard Analítico de Gastos com Seguro de Saúde

**Definição do Problema de Negócio**

Você é o Analista de Dados de uma operadora de plano de saúde que atende em quatro regiões do Brasil.

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


## Dashboard construído
[Arquivo Power BI](https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-07/desafio_cap_07.pbix)

**Visão geral**
Para visualizar o dashboard interativo [clique aqui](https://app.powerbi.com/view?r=eyJrIjoiYWVjM2NlY2QtYTQ2YS00NDU4LTliZmMtOWI3YzNlZjU2ODRhIiwidCI6IjE0Y2JkNWE3LWVjOTQtNDZiYS1iMzE0LWNjMGZjOTcyYTE2MSIsImMiOjh9)
<center><img src="https://github.com/luizabizoni/power-bi-studies/blob/master/dsa-cap-07/desafio07_visual.png" alt ="Dashboard Analítico de Gastos com Seguro de Saúde" width="800"></center>

## Passo a passo do processo
1. Importar o dataset "seguro_saude" para o Power BI.
2. Transformar dados:
   - O dataset não possuí cabeçalho, porém há duas linhas com os títulos das colunas. A primeira linha foi utilizada como cabeçalho e a segunda foi excluída.
   - A coluna "sexo" possuí por padrão os valores "masculino" e "feminino". As linhas com valores diferentes destes foram excluídas.
   - O tipo de dado da coluna "imc" foi transformado para número decimal e os valores arredondados para duas casas decimais.
   - A coluna "crianca" por ser uma variável categórica teve seus valores transformados para "1" caso o valor fosse diferente de 0 e caso este fosse igual a 0, o valor foi mantido.
   - A coluna "fumante" não foi utilizada nas análises, portanto foi excluída.
   - A coluna "regiao" possuí por padrão os valores "nordeste", "norte", "sudeste" e "sul". As linhas com valores diferentes destes foram excluídas.
   - O tipo de dado da coluna "valor_seguro_saude" foi transformado para número decimal e os valores arredondados para duas casas decimais.
   - Foi criada a coluna "Faixa etária" com 4 divisões de idade: "Até 29", "30 a 39", "40 a 49" e "Acima de 50" utilizando a função lógica "IF" do DAX.
   - Para fins visuais as colunas tiveram seus nomes modificados e as variáveis categóricas tiveram seus valores alterados para que a primeira letra de cada palavra seja maiúscula.

3. Inserir filtros de "Região", "Gênero", "É criança?" e "Faixa Etária" para tornar mais simples a interação do usuário final.
4. Criar visualizações que respondem às questões dos diretores:
    - Textos com as informações de gasto total, média de idade e média de imc dos usuários da operadora.
    - Gráfico de barras empilhadas na horizontal com a média de gasto por região e faixa etária.
    - Treemap com a proporção de crianças por região.
    - Gráfico de barras com o total do gasto com crianças e adultos separado por gênero.
    - Gráfico de área com a média de IMC por idade e gênero.

