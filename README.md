# Coleta de Passagens e Ocupação de Assentos – ClickBus
Este projeto apresenta um coletor automatizado desenvolvido em Python (Selenium + WebDriver) que extrai informações de viagens de ônibus no site da ClickBus, incluindo empresa, horário de saída, classe/serviço, preço e ocupação de assentos (livres/ocupados por deck quando disponível).
O objetivo principal é fornecer uma visão clara e estruturada dos resultados de busca por trecho e por data, permitindo análises de preço, oferta e capacidade de assentos.

## Descrição do projeto
O script navega até as páginas da ClickBus para os trechos configurados e percorre um ou mais dias a partir da data atual, coletando os cards de resultado. Para cada card, ele tenta abrir o seatmap dentro do próprio card, conta assentos por deck (quando houver abas de “1º/2º andar”) e retorna um DataFrame com as principais colunas de interesse: data da viagem, empresa, horario_saida, classe, preço, assentos livres, assentos ocupados, trecho.
As informações são organizadas para facilitar a exploração e a comparação entre datas e trechos, com scroll infinito, esperas explícitas e fallbacks de seletores para maior robustez.
