Mottu Tracker – Sistema IoT de Monitoramento de Motos
FIAP – Challenge 2025 – Sprint 4: Disruptive Architectures (IoT, IoB & Generative AI)

Grupo: 2TDSR
Curso: Análise e Desenvolvimento de Sistemas

1. Objetivo do Projeto

O Mottu Tracker é uma solução IoT integrada para o monitoramento em tempo real da frota de motos da Mottu.
O sistema coleta dados de telemetria (velocidade, bateria, localização e status), processa e persiste essas informações em banco de dados, atualizando dashboards dinâmicos para acompanhamento e controle das operações.

A proposta une IoT + Backend + Banco de Dados + Mobile + DevOps, garantindo um fluxo ponta a ponta totalmente funcional.

2. Arquitetura da Solução

Fluxo geral da aplicação:

Wokwi (ESP32 Simulado)
      ↓  MQTT
Node-RED (processamento e persistência)
      ↓  HTTP Requests
Backend (API Java/.NET)
      ↓
Banco de Dados (SQLite / Oracle)
      ↓
Dashboard (Node-RED UI)


Principais componentes:

Sensores simulados (Wokwi): capturam dados de velocidade, nível de bateria e status da moto.

MQTT Broker: canal de comunicação entre os dispositivos e o servidor Node-RED.

Node-RED: processa, armazena e exibe as informações no dashboard, além de integrar-se ao backend via HTTP.

Backend (Java/.NET): recebe dados e fornece endpoints REST para o app mobile.

Banco de Dados: armazena registros de telemetria e status.

Dashboard: exibe indicadores em tempo real (velocidade, bateria, alertas e status das motos).

3. Tecnologias Utilizadas
Camada	Tecnologias
Simulação	Wokwi (ESP32)
Protocolo de Comunicação	MQTT – broker.hivemq.com
Processamento e Visualização	Node-RED + node-red-dashboard
Backend	Java Spring Boot / .NET
Banco de Dados	SQLite / Oracle
Persistência	HTTP + JDBC / Entity Framework
IDEs	VS Code, IntelliJ, Node-RED Editor
Versionamento	GitHub
4. Funcionalidades Principais

Leitura de sensores simulados: 3 motos publicando dados a cada 2 segundos.

Processamento MQTT: parse e persistência automática no banco.

Dashboard: indicadores de bateria e velocidade em tempo real.

Comandos remotos: acionamento de LED/trava via MQTT (retorno imediato no Node-RED).

Integração com backend: envio de dados para API REST (/api/telemetria).

Logs e persistência: inserções SQL exibidas no painel de depuração.
