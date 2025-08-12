# Cortina Automática com Arduino

<img src="assets/images/banner.jpg">

## Visão Geral

Automação de cortina usando Arduino, sensor de luz (LDR) e motor DC. Abre/fecha automaticamente conforme a luz ou por botão manual.

---

## Materiais

- Arduino Uno/Nano (ou ESP8266/ESP32 para Wi-Fi)
- LDR + resistor (10 kΩ)
- Motor DC + ponte H (L298N ou TB6612FNG)
- Botão(s) para controle manual
- Fonte 12V (motor) + 5V (Arduino)
- Fins de curso

---

## Esquema Simplificado

- LDR ligado a um pino analógico (A0)
- Motor DC controlado pela ponte H (2 pinos digitais para direção, 1 PWM para velocidade)
- Botão em pino digital (com pull-down)
- Fins de curso em pinos digitais

---

## Lógica Básica

1. Ler valor do LDR (0–1023)
2. Se luz > limiar, abrir cortina; se luz < limiar, fechar
3. Botão manual alterna entre abrir/fechar
4. Parar motor ao atingir fim de curso (ou por tempo)