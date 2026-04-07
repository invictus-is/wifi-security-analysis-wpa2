# Análise de Segurança em Redes Wi-Fi WPA2

## Objetivo
Este projeto tem como objetivo analisar a segurança de redes Wi-Fi que utilizam o protocolo WPA2-PSK em um ambiente controlado e autorizado.

## Ambiente
- Laboratório controlado
- Rede própria / autorizada
- Ferramentas de análise de tráfego

## Identificação da Rede
Foi identificada uma rede com as seguintes características:
  ![Scan](monitoramento-WPA2.png)
- Protocolo: WPA2
- Cifra: CCMP
- Autenticação: PSK
- Canal: 6
- Tráfego ativo presente
- Clientes conectados


## Captura do Handshake
Durante a análise, foi possível observar pacotes EAPOL, indicando que o handshake WPA2 foi capturado com sucesso.

## Análise de Segurança
A captura do handshake permite a realização de ataques offline baseados em dicionário.  
Neste cenário, a rede demonstrou vulnerabilidade devido ao uso de uma senha fraca.

## Limitações
- Necessidade de clientes conectados
- Dependência da qualidade do sinal
- Ineficiente contra senhas fortes

## Mitigações
- Utilizar senhas fortes (mínimo 12 caracteres, com alta entropia)
- Implementar WPA3
- Desativar WPS
- Monitorar eventos de desautenticação

 ## 📊 Resultado da Análise
A captura do handshake permitiu validar a vulnerabilidade da rede a ataques de dicionário.

![Resultado](handshake.png)

## Ética
Este projeto foi realizado exclusivamente em ambiente controlado e autorizado, com fins educacionais.
