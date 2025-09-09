## Elastic Load Balancer

O que é esse trem?

* O termo Elastic Load Balancer (ELB) é o “guarda-chuva”.
* É o serviço da AWS que oferece balanceamento de carga elástico, ou seja, que cresce e se adapta automaticamente conforme o tráfego aumenta ou diminui.
* Dentro do ELB, você pode escolher tipos diferentes de balanceadores, dependendo da necessidade:
  - Application Load Balancer (ALB) → Camada 7 (HTTP/HTTPS), entende URLs, cabeçalhos, hosts.
  - Network Load Balancer (NLB) → Camada 4 (TCP/UDP), ultra rápido e de baixa latência.
  - Gateway Load Balancer (GLB) → Camada 3, usado para integrar appliances de rede (firewall, IDS/IPS).
