
# Rover Project 🚀

Este repositório centraliza o software do projeto **Rover**, incluindo os pacotes e nós desenvolvidos em **ROS 2**, além do script utilitário `main.sh` para gerenciamento e configuração do sistema operacional embarcado.

---

## 🛠 Arquitetura & Tecnologias

### ROS 2

Adotamos o **ROS 2** devido à sua alta confiabilidade, modularidade e padronização na comunicação entre processos. Ele oferece uma camada de abstração robusta para troca de mensagens e tópicos, garantindo baixa latência e requisitos adequados para controle e navegação em tempo real.

### Computador de Bordo

O processamento embarcado é realizado por uma **Raspberry Pi 3 Model B** rodando **Ubuntu Server 24.04 LTS**. Ela atua na linha de frente para:

* **Percepção:** Leitura e filtragem dos dados provenientes dos sensores.
* **Atuação:** Controle de estado e acionamento dos motores.
* **Telemetria:** Monitoramento do status geral do veículo.

### Access Point (Rede Wi-Fi)

O sistema conta com um script em Python responsável por criar um Ponto de Acesso (AP) Wi-Fi dedicado. Essa rede permite que qualquer dispositivo externo se conecte ao Rover para receber dados de telemetria e monitoramento em tempo real.

### Controle Sem Fio (Wireless Controller)

Utiliza-se o pacote nativo `joy` do ROS 2 para interfacear um controle sem fio. O nó mapeia as entradas do joystick e envia os comandos de movimentação diretamente para a camada de controle dos motores, permitindo a operação manual do robô.
