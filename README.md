# Coleta de Passagens e Ocupação de Assentos – ClickBus
Este projeto apresenta um coletor automatizado desenvolvido em Python que extrai informações de viagens de ônibus no site da ClickBus, incluindo empresa, horário de saída, classe/serviço, preço e ocupação de assentos.
O objetivo principal é fornecer uma visão clara e estruturada dos resultados de busca por trecho e data, permitindo análises de preço, oferta e ocupação.

## Descrição do projeto
O script navega até as páginas da ClickBus para os trechos configurados e percorre um ou mais dias a partir da data atual, coletando os cards de resultado. Para cada card, ele tenta abrir o seatmap dentro do próprio card, conta assentos por deck e retorna um DataFrame com as principais colunas de interesse: data da viagem, empresa, horario_saida, classe, preço, assentos livres, assentos ocupados, trecho.
