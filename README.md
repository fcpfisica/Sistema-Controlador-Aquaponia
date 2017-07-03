# Sistema-Controlador-Aquaponia
Montagem de um sistema baseado no controlador Arduino para automatizar um módulo de aquaponia simples.
Partes inicialmente inclusas: arduino UNO R3, fonte 12V 10A (ligada a rede elétrica), Fonte 12V 7Ah (ligada a painel solar/baterias), DS3231, Sheild SD, DS18B20, Módulo Relé 4 portas, chave interruptor alavanca (fim de curso), componentes (capacitores/resistores/fios/placas).

O sistema deverá ser capaz de controlar a circulação de água, aeração dos tanques, controlar temperatura, fornecimento de comida, além de realizar o gerenciamento da energia, garantindo a máxima duração em caso de falta de energia e realizar o registro de todo o fundionamento (datalogger dos sensores e portas/relés). O controle do nível de água geral é feito por um sistema mecânico convencional (boia de caixa d`água).

A montagem do datalogger prevê o uso de um cartão de 4Gb (capacidade de armazenamento de todas as informações por período muito superior a manutenção do sistema).

O gerenciamento da energia setrá feito utilizando um carregador de celular antigo (5V 500mA) passando por um divisor de tensão ligado a uma porta analógica. Se esta porta estiver com valor baixo (momento de falta de energia no carregador) aciona um rele que faz o chaveamento entre as portas NO NC mudando a fonte da fase 12V entre a fonte externa e bateria. Os neutros estão conectados levando o sistema para o mesmo zero (não temos aterramento nos circuitos!).

O módulo relé controlará uma bomba para circulação de 12V, um compressor de ar 12V, um motor de 12V (alto torque, 13RPM) e um aquecedor de 1000W 127V (~8A).

O DS3231 terá a funcionalidade de alarme ativada para acionar o fluxo de alimentação (interrupção hardware pela porta 3).

A chave interruptor terá a funcionalidade de suspender a bomba de circulação na falta de água (interrupção hardware pela porta 2).
