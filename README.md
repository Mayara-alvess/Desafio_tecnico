# Desafio_tecnico

## Objetivo
Efetuar uma análise exploratória de dados com base em um conjunto de dados sobre o uso de um programa de compartilhamento de bicicletas.

## Obtenção dos dados
Nessa análise foi utilizado uma amostra de 50 mil dados.
O conjunto de dados completo contenddo as 58.937.715 viagens você pode acessar [clicando Aqui](https://console.cloud.google.com/marketplace/product/city-of-new-york/nyc-citi-bike?project=data-sandbox-319716) NYC Citi Bike Trips. 

## Processamento e análises
  SELECT 
    *,
    ROUND(tripduration / 60, 2) AS tripduration_in_minutes,
    FORMAT_DATE('%Y-%m-%d', stoptime) AS stop_date,
    EXTRACT(YEAR FROM CURRENT_DATE()) - birth_year AS idade
  FROM 
    `meu-primeiro-projeto01-408821.bike.bike`
    
### Explicando a consulta
ROUND(tripduration / 60, 2) AS tripduration_in_minutes,
Converta a duração da viagem de segundos para minutos e criei uma nova variável chamada tripduration_in_minutes.

FORMAT_DATE('%Y-%m-%d', stoptime) AS stop_date,
Converta o tempo de parada (stoptime) para uma data formatada e criei uma nova variável chamada stop_date.

EXTRACT(YEAR FROM CURRENT_DATE()) - birth_year AS idade
Calcula a idade a partir do ano de nascimento (birth_year) e criei uma nova variável chamada idade.

## Conclusões
O Citi Bike é o maior programa de compartilhamento de bicicletas dos Estados Unidos, com 25.000 bicicletas e mais de 1.500 estações distribuídas por Manhattan, Brooklyn, Queens, Bronx, Jersey City e Hoboken. O programa oferece duas modalidades para os usuários: clientes assinantes, com plano anual, e clientes avulsos, com passes de 24 horas ou 3 dias.

Os clientes assinantes realizam o maior número de viagens. Além disso, o gênero masculino é o que mais utiliza o serviço, seguido pelo feminino. Analisando os dados de 2015 a 2018, observamos um aumento no total de viagens até 2017, seguido por uma queda em 2018.

A média diária de viagens é de 53.

# Dashboard
[Clique Aqui](https://lookerstudio.google.com/u/0/reporting/e4d4b87b-c58e-480f-a584-fe3f3b8d5cf1/page/4qZ1D/edit)
![](https://github.com/Mayara-alvess/Desafio_tecnico/blob/main/citibikee.png)
