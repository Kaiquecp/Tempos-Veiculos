Este código SQL combina dados de várias tabelas para determinar o estado atual de veículos em trânsito com base no histórico de cercas e documentos de transporte. Ele realiza os seguintes passos:

Ultima_Cerca: Seleciona o histórico de cercas de veículos, considerando apenas cercas relacionadas a clientes e grupos específicos.
Ultimo_KM_Vazio: Obtém informações sobre a quilometragem de saída e chegada dos veículos.
CTE (Conhecimento de Transporte): Coleta dados de documentos de transporte, como remetente, destinatário e terminais.
OST (Ordem de Serviço): Coleta dados de ordens de serviço relacionadas aos veículos.
Combined: Junta as informações das CTE e OST em uma tabela unificada, considerando os registros mais recentes para cada veículo.
Estados_Veiculo: Determina o estado atual de cada veículo (como "Carregando", "Deslocando para Descarregar", etc.), com base no histórico das cercas e documentos.
A consulta retorna o estado atual de cada veículo, considerando o relacionamento entre cercas, ordens de serviço e documentos de transporte.
