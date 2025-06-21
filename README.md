Projeto de Regressão: Previsão de Aluguel de Bicicletas com Azure ML Studio
Este projeto demonstra a utilização do Azure Machine Learning Studio para construir e treinar um modelo de regressão capaz de prever o volume de aluguel de bicicletas com base em dados históricos. O foco foi explorar as funcionalidades de ML Automatizado (AutoML) para otimizar o processo de criação e seleção do modelo.

Descrição e Objetivo
O principal objetivo deste projeto foi desenvolver um modelo preditivo para estimar o número de bicicletas alugadas em determinado período. Ao utilizar dados históricos de aluguel, buscamos identificar padrões e fatores que influenciam a demanda por bicicletas, aproveitando o poder do Azure ML Studio para acelerar a experimentação e encontrar o melhor algoritmo para essa tarefa de regressão.

Metodologia e Fluxo de Trabalho no Azure ML Studio
O desenvolvimento e treinamento do modelo seguiram um fluxo de trabalho estruturado no Azure Machine Learning Studio, utilizando a funcionalidade de ML Automatizado (AutoML):

Início do Projeto:

Acesso e configuração inicial no Azure Machine Learning Studio.
Seleção da funcionalidade ML Automatizado (AutoML) para otimizar a escolha do modelo e os hiperparâmetros.
Definição do Tipo de Tarefa como Regressão, adequada para a previsão de um valor numérico contínuo (quantidade de aluguéis).
Preparação e Ingestão de Dados:

Os dados foram configurados como Tabulares, um formato ideal para conjuntos de dados estruturados.
A descrição do conjunto de dados foi definida como "dados históricos de aluguel de bicicletas".
A fonte de dados utilizada foi um arquivo Excel contendo registros históricos de aluguéis.
As configurações de importação do arquivo incluíram: formato delimitado por vírgulas (CSV), codificação UTF-8 e a indicação de que "somente o primeiro arquivo possui cabeçalhos".
Configuração da Tarefa AutoML:

A coluna-alvo para a previsão foi especificada como rentals (assumindo que rentals é a coluna que contém o número de aluguéis).
As métricas de avaliação foram cuidadosamente selecionadas para o problema de regressão (por exemplo, RMSE, MAE, R-squared – se você lembra qual métrica principal você configurou, pode mencioná-la aqui).
Limites de tempo para o treinamento e configurações de validação foram ajustados para garantir um processo eficiente e robusto.
Configurações de Computação e Execução:

O ambiente de computação (cluster ou instância) foi configurado para suportar o treinamento intensivo do modelo.
O trabalho de treinamento do AutoML foi revisado e enviado. O Azure ML então executou automaticamente múltiplas iterações, testando diferentes algoritmos e combinações de hiperparâmetros para identificar o modelo com melhor desempenho.
Análise e Validação do Modelo:

Após a conclusão do treinamento, as métricas de desempenho do modelo vencedor foram validadas.
Foi realizada uma análise aprofundada do projeto para entender os resultados, identificar os principais fatores preditivos e avaliar a qualidade geral da solução de Machine Learning.
Tecnologias Utilizadas
Microsoft Azure Machine Learning Studio: Plataforma principal para desenvolvimento e treinamento do modelo.
Azure Automated ML (AutoML): Recurso utilizado para automação da seleção de algoritmos e otimização de hiperparâmetros.
Microsoft Excel: Formato original da fonte de dados histórica.
Próximos Passos (Opcional, mas recomendado)
Para futuras iterações deste projeto, poderíamos explorar:

Deploy do Modelo: Realizar o deploy do modelo treinado como um endpoint para consumo em aplicações.
Monitoramento: Implementar monitoramento contínuo do desempenho do modelo em produção.
Engenharia de Features: Explorar a criação de novas features a partir dos dados existentes para melhorar a precisão do modelo.
Fontes de Dados Adicionais: Integrar dados externos (clima, eventos especiais) para enriquecer o modelo preditivo.
