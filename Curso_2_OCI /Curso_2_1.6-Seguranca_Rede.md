## 🔹 Pergunta

Você é a pessoa responsável pela segurança de uma infraestrutura de rede em uma empresa de tecnologia. Recentemente, foi detectado um aumento significativo de tentativas de intrusão à aplicação web, o que levou à necessidade de revisar e fortalecer o modelo de segurança da rede. Seu desafio é avaliar as camadas do modelo TCP/IP e identificar onde novas políticas de segurança poderiam ser mais eficazes.

Qual seria a camada do modelo TCP/IP que você definiria como prioritária para reforçar as políticas de segurança?


## 🔹Resposta

Para reforçar a segurança de uma aplicação web em uma infraestrutura de rede, a camada do modelo TCP/IP prioritária é geralmente a Camada de Aplicação.

Justificativa
Camada de Aplicação
É onde o HTTP/HTTPS opera.
É o ponto de entrada das requisições de usuários e potenciais atacantes.
Políticas de segurança aqui podem incluir:
WAF (Web Application Firewall) para filtrar ataques como SQL Injection e XSS
Validação de entradas e autenticação
Criptografia HTTPS/TLS
Atacar vulnerabilidades nesta camada previne que o ataque avance para camadas inferiores.
Outras camadas
Transporte (TCP/UDP): pode implementar firewalls, IDS/IPS, limitação de taxa, mas não protege contra ataques específicos de aplicação.
Rede (IP): políticas de filtragem de IP, VPNs, segmentação de rede; importante, mas complementar.
Enlace/Física: segurança física e controle de dispositivos; fundamental, mas não previne ataques web diretamente.

✅ Reforço

A Camada de Aplicação é realmente a prioritária para reforçar a segurança de aplicações web, pois é nela que ocorrem as interações diretas com os usuários e onde os protocolos HTTP/HTTPS operam.
Implementar políticas de segurança como WAF, validação de entradas e criptografia HTTPS/TLS nessa camada é crucial para prevenir ataques. 

## ✅ Resumo

Camada prioritária: Aplicação
Motivo: concentra-se nos protocolos que interagem diretamente com usuários e potenciais atacantes (HTTP/HTTPS), onde os ataques à aplicação ocorrem.
Estratégias: WAF, TLS/HTTPS, validação de entradas, autenticação forte.
