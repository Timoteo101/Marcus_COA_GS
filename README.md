# Marcus_COA_GS
Este projeto utiliza um Arduino para realizar o monitoramento em tempo real de três variáveis ambientais: vibração, temperatura e luminosidade. Os dados coletados são processados e exibidos em um display OLED SSD1306, enquanto um conjunto de LEDs indica o estado geral do sistema com base em condições pré-definidas.

Funcionamento do Sistema
O código realiza a leitura contínua dos sensores conectados às portas analógicas e digitais. A temperatura é calculada através de um termistor utilizando a constante Beta para maior precisão. O display atualiza as informações exibindo o status de cada sensor.

A lógica de indicação visual através dos LEDs funciona da seguinte forma:

LED Verde: Acende quando o sistema está em condições ideais (vibração normal, temperatura estável e luminosidade adequada).
LED Vermelho: Acende quando o sistema detecta uma falha ou condição crítica (vibração ativa, temperatura fora da faixa ideal e iluminação inadequada).
LED Amarelo: Acende em qualquer outra situação, servindo como um indicador de alerta ou estado intermediário.

Hardware Necessário
Arduino (Uno, Nano ou compatível).
Display OLED 128x64 (Interface I2C).
Sensor de Vibração.
Termistor (para leitura de temperatura).
Sensor de Luz (LDR).
3 LEDs (Verde, Amarelo e Vermelho) com resistores limitadores de corrente.

Bibliotecas Utilizadas
Para que o código funcione corretamente, certifique-se de ter instalado na sua IDE do Arduino as bibliotecas Adafruit GFX Library e Adafruit SSD1306, disponíveis no Gerenciador de Bibliotecas.

Conexões
O código está configurado para utilizar os pinos digitais 2 (vibração), 4, 7 e 8 (LEDs) e os pinos analógicos A0 (temperatura) e A1 (luz). O display utiliza o protocolo I2C (pinos SDA e SCL). Certifique-se de ajustar as conexões físicas de acordo com as definições presentes no cabeçalho do arquivo
