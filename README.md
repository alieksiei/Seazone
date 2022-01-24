# Seazone
Referente à etapa de code challenge do processo seletivo.

O arquivo Rmarkdown, quando executado na mesma pasta que os dois arquivos de dados disponibilizados, gera o pdf com as análises pedidas.

Para isso é necessário o Rstudio(e o próprio R) junto das bibliotecas Tidyverse, Lubridate e Cowplot, e uma instalação de LaTeX para exportar como pdf.

Foram encontrados alguns problemas no dataset, acredito que suas resoluções são parte do desafio. Seguem os problemas e suas soluções:


Problema 1: Multiplicidade nos anúncios

Solução: Selecionar apenas linhas únicas


Problema 2: Valores nulos para quartos e/ou banheiros

Solução: Substitui-se os valores nulos pela mediana


Problema 3: Valores nulos para o número de reviews e valor nulo ou 0 para o rating(que deve ir de 1 a 5)

Solução Substituir os valores nulos de reviews por 0 e de ratings pela média. Observou-se que tanto reviews nulos quanto 0 geralmente estão juntos a um rating nulo, por isso a escolha de valor para a imputação.


Problema 4: Dois anúncios onde a data de reserva é 01/01/2000. 

Solução: Remover as observações da análise, foram apenas duas de mais de 100 mil observações.


Por fim, para realizar a análise de correlação com o bairro foi necessário aplicar o one-hot encoding, por tratar-se de uma variável qualitativa não ordenada. 
