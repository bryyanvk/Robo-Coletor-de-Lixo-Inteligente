🤖 Robô Coletor de Lixo Inteligente
📖 Descrição

Este projeto consiste em um robô autônomo e controlável via Arduino capaz de detectar e coletar garrafas PET usando sensores de cor e ultrassônicos.
Ele possui braço robótico articulado para manipulação de objetos e pode ser controlado via Bluetooth ou operar de forma semi-autônoma.

🖼 Imagens do Robô

Substitua os caminhos abaixo pelas suas imagens reais

Robô completo

Braço robótico e servos

Sensores e motores

⚙ Tecnologias e Hardware

IDE: Arduino

Linguagem: C++

Componentes:

4 motores DC com ponte H

4 servos (base, ombro, cotovelo e pulso)

Sensor ultrassônico HC-SR04

Sensor de cor TCS230

Bluetooth (controle remoto via app)

📌 Diagrama dos Pinos
Servos:
- Base: 9
- Ombro: 10
- Cotovelo: 11
- Pulso: 12

Motores DC (Ponte H):
- Motor1: 22,23
- Motor2: 24,25
- Motor3: 26,27
- Motor4: 28,29

Sensor Ultrassônico:
- Trig: A0
- Echo: A1

Sensor de Cor TCS230:
- S0: 34
- S1: 35
- S2: 36
- S3: A2
- Out: A3

🔄 Fluxograma do Código
flowchart TD
    Start --> Setup
    Setup --> Loop
    Loop -->|Lê Ultrassônico| CheckObstacle
    CheckObstacle -->|Obstáculo?| StopMotors
    Loop -->|Lê Sensor de Cor| CheckColor
    CheckColor -->|Garrafa PET?| StopMotors
    Loop -->|Recebe Comando Bluetooth| ControlMotors
    ControlMotors --> Loop

🏗 Funcionalidades
1️⃣ Autonomia Parcial

Detecta obstáculos e para os motores automaticamente.

Identifica garrafas PET e interrompe o movimento.

2️⃣ Controle Remoto

Via Bluetooth: movimenta o robô e manipula o braço robótico.

Comando	Função
F	Mover motores para frente
R	Mover motores para trás
S	Parar motores
B/b	Rotacionar base do braço
S/s	Movimentar ombro do braço
E/e	Movimentar cotovelo do braço
W/w	Rotacionar pulso do braço
3️⃣ Braço Robótico

4 servos articulados controlando base, ombro, cotovelo e pulso.

Permite pegar e manipular garrafas detectadas.

🛠 Como Usar

Abra o arquivo .ino na Arduino IDE.

Conecte a placa Arduino e configure os pinos conforme o diagrama.

Instale a biblioteca Servo na IDE.

Faça o upload do código para o Arduino.

Utilize o Bluetooth ou deixe o robô operar de forma semi-autônoma.

💡 Possíveis Melhorias

Compartimento para armazenar garrafas coletadas.

Navegação totalmente autônoma usando mapeamento.

Sensores laterais para melhor detecção de obstáculos.

👨‍💻 Autores

Bryan Leandro e Jian Eduardo – Desenvolvedores do robô coletor de lixo inteligente.
