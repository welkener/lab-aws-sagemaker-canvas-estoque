Relatório de Análise do Modelo de Previsão de Estoque desafio Dio

#Introdução
Este relatório apresenta a documentação do processo para a criação e avaliação de um modelo de previsão de estoque utilizando o Amazon SageMaker Canvas.

O objetivo é prever a quantidade de estoque disponível para diferentes produtos ao longo do tempo, utilizando dados históricos.

#Dataset
O dataset utilizado contém as seguintes colunas:

ID_PRODUTO: Identificador único para cada produto.
DIA: Data da observação.
FLAG_PROMOCAO: Indicador binário de promoção (0 ou 1).
QUANTIDADE_ESTOQUE: Quantidade de estoque disponível na data específica.

#Análise Exploratória dos Dados (EDA)
Informações Gerais e Estatísticas Descritivas:

O dataset é composto por registros de diferentes produtos ao longo do tempo, com um total de 500 observações.
As estatísticas descritivas mostraram que a quantidade de estoque varia significativamente entre os produtos, com algumas datas apresentando valores de estoque bem mais altos que outras.

#Distribuição Temporal:

A análise da distribuição dos dados ao longo do tempo revelou padrões de variação no estoque que podem ser indicativos de tendências ou sazonalidades.
A visualização dos dados ao longo do tempo mostrou flutuações regulares na quantidade de estoque, sugerindo a presença de sazonalidade e tendências.

#Análise Estatística
--Correlação entre Variáveis
A análise de correlação indicou uma relação significativa entre a presença de promoções (FLAG_PROMOCAO) e a quantidade de estoque (QUANTIDADE_ESTOQUE). Isso sugere que promoções podem ter um impacto considerável no nível de estoque.
--Análise de Tendências e Sazonalidades:

A análise das tendências e sazonalidades revelou que os dados de estoque exibem padrões repetitivos ao longo do tempo. Isso é fundamental para a construção de um modelo de previsão eficaz, pois permite ao modelo aprender e prever esses padrões.

#Treinamento do Modelo
--Preprocessamento de Dados:
Os dados foram preparados e divididos em conjuntos de treinamento e teste para garantir que o modelo pudesse ser treinado e validado corretamente.
Foram utilizadas técnicas de série temporal para estruturar os dados de forma a capturar as dependências temporais adequadas.
--Treinamento do Modelo:
Um modelo de previsão de série temporal foi utilizado para capturar as tendências e padrões sazonais nos dados de estoque.
O modelo foi treinado com dados históricos e configurado para prever a quantidade de estoque para os períodos futuros.
--Avaliação do Modelo
Métricas de Desempenho:
As métricas de desempenho do modelo, como Erro Médio Absoluto (MAE) e Erro Quadrático Médio (MSE), foram calculadas para avaliar a precisão das previsões.
Os resultados mostraram que o modelo possui um bom desempenho na previsão da quantidade de estoque, com valores de erro aceitáveis.
--Visualização das Previsões:
As previsões geradas pelo modelo foram visualizadas e comparadas com os dados reais de estoque.
A visualização demonstrou que as previsões do modelo seguem de perto os valores reais, capturando bem as tendências e variações sazonais.
#Conclusão
O modelo de previsão de estoque desenvolvido utilizando o Amazon SageMaker Canvas demonstrou ser eficaz na previsão da quantidade de estoque para diferentes produtos ao longo do tempo. A análise estatística e as métricas de desempenho confirmaram que o modelo pode ser utilizado para ajudar a gerenciar os níveis de estoque de forma mais precisa e eficiente.

Próximos Passos
Implementação do Modelo em Produção: Integrar o modelo ao sistema de gerenciamento de estoque para automação das previsões.
Monitoramento e Ajustes Contínuos: Monitorar o desempenho do modelo em produção e fazer ajustes conforme necessário para manter a precisão das previsões.
Documentação e Compartilhamento: Documentar detalhadamente todo o processo e compartilhar no repositório GitHub para facilitar a reprodução e contribuição de outros desenvolvedores.
Este relatório proporciona uma visão abrangente do processo de desenvolvimento e análise do modelo de previsão de estoque, utilizando uma abordagem no-code com o Amazon SageMaker Canvas.
