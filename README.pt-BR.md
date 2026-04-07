# Análise de Segurança em Redes Wi-Fi (WPA2)

## Objetivo
Este projeto tem como objetivo avaliar a segurança de redes Wi-Fi que utilizam o protocolo WPA2-PSK em um ambiente controlado e autorizado.

## Ambiente
- Laboratório controlado
- Rede autorizada para testes
- Ferramentas de análise de tráfego

## Identificação da Rede
Foi identificada uma rede com as seguintes características.

A imagem abaixo apresenta o processo de identificação e monitoramento da rede:

![Scan](monitoramento-WPA2.png)

- Protocolo: WPA2
- Cifra: CCMP
- Autenticação: PSK
- Canal: 6
- Tráfego ativo observado
- Presença de clientes conectados

## Captura do Handshake
A análise revelou a presença de pacotes EAPOL, confirmando que o handshake WPA2 foi capturado com sucesso.

## Análise de Segurança
O WPA2-PSK utiliza um mecanismo de autenticação compartilhado, no qual a mesma senha é utilizada por todos os clientes.  
Esse modelo aumenta o risco de exposição quando são utilizadas senhas de baixa complexidade.

A captura do handshake possibilita a realização de ataques offline baseados em dicionário.  
Neste cenário, a rede demonstrou vulnerabilidade devido à baixa complexidade da senha utilizada.

## Limitações
- Necessidade de clientes conectados
- Dependência da qualidade do sinal
- Ineficiente contra senhas fortes

## Resultado da Análise
A imagem abaixo demonstra a captura do handshake e a validação da exposição da rede:

![Resultado](handshake.png)

Os resultados indicam que a rede é suscetível a ataques de dicionário quando são utilizadas senhas de baixa complexidade.

## Mitigações
- Utilizar senhas fortes (mínimo 12 caracteres com alta entropia)
- Adotar WPA3 sempre que possível
- Desativar WPS
- Monitorar eventos de desautenticação

## Insight
A segurança do WPA2 depende principalmente da complexidade da senha, e não apenas do protocolo em si.

## Ética
Este projeto foi realizado exclusivamente em ambiente controlado e autorizado, com fins educacionais.

## Autor
João Carlos Velho de Oliveira
