 Conforme orientado no bootcamp segue o passo a passo realizado e a análise do estoque com o dataset fornecido.
 
  No domínio criado na plataforma AWS, foi usado a API Canvas SageMaker. Foi feita a seleção do arquivo de dataset "dataset-1000-com-preco-variavel-e-renovacao-estoque.csv" disponível no repositório da DIO disponibilizado na plataforma/aula. Após o envio do dataset no Canvas foi realizado a configuração do modelo, sendo escolhido o tipo de predição númerica pelo alvo da coluna de preço do dataset. O resultado do Quick build foi de um raiz do erro quadrático médio(RMSE) de 30.78, indicando que a diferença dos valores previstos e dos valores observados está fora dos valores recomendados para uma análise satisfatória(0,2~0,5). O resultado do risco quadrático(MSE) foi de 947.437, indicando um desvio padrão de até 947,437 pontos do dataset analisado. Sendo os valores fora dos padrões aceitaveis passou-se para o retreinamento do modelo. Concluido o retreinamento no modelo standart; o RMSE caiu para 29.696 e o MSE foi para 881.839. Demonstrando que o dataset não tem dados suficientes para uma predição de alta qualidade(valores próximos de 0) de predição de estoque. Os resultados obtidos com a predição da quantidade em estoque no período de três anos em três diferentes itens foram:
   item 1
 31/12/2023 -- 65.24
 31/12/2024 -- 48.813
 31/12/2025 -- 43.237
   item 10
 31/12/2023 -- 57.264
 31/12/2024 -- 53.036
 31/12/2025 -- 46.248
   item 100
 31/12/2023 -- 59.614
 31/12/2024 -- 53.632
 31/12/2025 -- 47.988

  Pela análise da predição, o item 1 é o item com maior redução de estoque durante o ano de 2024 (16,427). Pelo estoque de produtos, não seria necessário adquirir mais itens do que o disponível já em estoque para todos os itens do dataset. Seria de se avaliar uma possível reanálise de preços e um dataset mais robusto para melhor predição com o modelo. Não houve muita diferença nos resultados do quick build e do standart no SageMaker Canvas.
