# Carrinho Autônomo com ESP32

Projeto final do 1º semestre do curso Técnico em Redes de Computadores (SENAI São Caetano do Sul, Cyber e IA).

Robô móvel autônomo que **segue uma linha no solo** e **desvia de obstáculos** em tempo real.

## Como funciona

- **Navegação:** 8 sensores infravermelhos (lidos por um expansor MCP23017) acompanham a linha e corrigem a direção.
- **Obstáculos:** um sensor de distância a laser **VL53L0X (Time of Flight)** detecta objetos à frente. A detecção de obstáculo tem prioridade sobre o seguimento de linha: o robô para, faz uma manobra de desvio e volta para a rota.
- **Movimento:** quatro motores DC.
- **Sinalização:** LEDs indicam o estado do robô.
- Se a linha não for detectada, o robô entra em estado de parada por segurança.

## Hardware e bibliotecas

ESP32 · MCP23017 · VL53L0X · sensores IR · 4 motores DC · LEDs

Bibliotecas: `Wire`, `Adafruit_MCP23017`, `VL53L0X`

## Código

O código está em [`ESP32.sh`](ESP32.sh). Apesar da extensão, é um sketch em **C++ para Arduino/ESP32**: para usar, copie o conteúdo para um arquivo `.ino` e abra na Arduino IDE.

---

Autor: [Matheus Ziravello](https://www.linkedin.com/in/matheusziravello) · [Portfólio](https://mathziraa.github.io)
