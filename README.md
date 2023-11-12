# TempESP8266
Aplicação do ESP8266 NodeMCU para Mensuração da Temperatura Corporal

1. Software e Hardware

   O presente projeto tem o objetivo de criar um medidor de temperatura corporal utlizando o módulo NodeMCU ESP8266 e a aplicação do Display LCD (Liquid Crystal Display) usado para representar um medidor de temperatura que será dado pelo sensor LM35. Materiais utilizados:
   •	Módulo WiFi ESP8266 NodeMcu
   •	Cabo Micro USB para Arduino Leonardo, Micro, DUE e Raspberry Pi - Azul 30cm
   •	Sensor de temperatura LM35
   •	Display LCD
   •	Módulo Serial I2C para Display LCD
   •	Jumpers - Macho/Macho
   •	Jumpers - Fêmea/Fêmea
   •	Protoboard
   
2. Funcionamento
 
    Para seu correto funcionamento o circuito, os três jumpers posicionados no protoboard na linha G conectam-se no módulo ESP8266 na corrente 5V, na entrada analógica 0 (A0) e na entrada de referência GND, respectivamente. Paralelamente, na linha F do protoboard, o LM35 tem o pino +Vs em paralelo ao jumper de corrente 3,3V, o pino Vout em paralelo ao jumper de entrada analógica 0, e o pino GND que é o negativo (terra) paralelo ao jumper de entrada de referência GND. Para promover a extensão do LM35, levando em consideração a necessidade de aferição axilar da temperatura, os jumpers fêmea/ fêmea são utilizados.
	  Para utlização do display LCD, os pinos do módulo IC2 são acoplados ao display e os pinos de fornecimento de energia (VCC e GND) e de interface (SDA e SCL) são conectados ao módulo ESP8266 por um jumper fêmea/ fêmea e um jumper macho/ macho em cada pino respectivamente. As conexões são: pino GND do módulo IC2 conectado à entrada GND do módulo ESP8266, pino VCC do módulo IC2 conectado à VIN do módulo ESP8266, pino SDA conectado à entrada digital 2 (D2) do módulo ESP8266, e pino SCL do módulo IC2 conectado à entrada digital 1 (D1) do módulo ESP8266.
O cabo micro UBS conecta o módulo ESP8266 ao computador pela entrada USB do mesmo.

3. Codificação 

  Para programação e obtenção dos dados, é utilizada a linguagem C++ no software Arduino IDE para facilitar o desenvolvimento e a gravação de códigos diretamente no microcontrolador. O protocolo MQTT (Message Queuing Telemetry Transport) foi conectado com o MQTT Explorer que fornece uma visão geral estruturada dos tópicos MQTT (GARLAND, 2021). O código está descrito no arquivo code desse mesmo reposítório.
