## Language

- English (default)
- Portuguese: [README.pt-BR.md](README.pt-BR.md)

# Wi-Fi Security Analysis (WPA2)

## Objective
This project aims to assess the security of Wi-Fi networks using the WPA2-PSK protocol in a controlled and authorized environment.

## Environment
- Controlled laboratory
- Authorized network
- Traffic analysis tools

## Network Identification
A network with the following characteristics was identified:

![Scan](monitoramento-WPA2.png)

- Protocol: WPA2
- Cipher: CCMP
- Authentication: PSK
- Channel: 6
- Active traffic observed
- Connected clients present

## Handshake Capture
During the analysis, EAPOL packets were observed, confirming that the WPA2 handshake was successfully captured.

## Security Analysis
Capturing the handshake enables offline dictionary-based attacks.  
In this scenario, the network was found to be vulnerable due to the use of a weak password.

## Limitations
- Requires connected clients
- Dependent on signal quality
- Ineffective against strong passwords

## Analysis Result
The captured handshake allowed validation of the network’s exposure to dictionary-based attacks.

![Result](handshake.png)

## Mitigations
- Use strong passwords (minimum 12 characters with high entropy)
- Adopt WPA3 where possible
- Disable WPS
- Monitor deauthentication events

## Key Insight
WPA2 security depends heavily on password strength rather than the protocol itself.

## Ethics
This project was conducted in a controlled and authorized environment for educational purposes only.
