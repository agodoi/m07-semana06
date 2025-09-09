## O que é Application Load Balancer?

* O Application Load Balancer (ALB) é um balanceador de carga que trabalha na Camada 7 (Aplicação) do modelo OSI, ou seja, ele entende o conteúdo da requisição HTTP/HTTPS.
* Isso significa que ele não só distribui as requisições, mas também pode tomar decisões inteligentes baseadas no conteúdo da requisição:
  - Qual URL foi chamada (ex: /login, /produtos, /checkout)
  - Qual cabeçalho HTTP está presente
  - Qual host/domínio o usuário acessou
* Com isso, você pode configurar regras de roteamento muito mais avançadas, direcionando cada requisição para um grupo de destino específico.
* O Application Load Balancer é um tipo específico de ELB. Ou seja:
  - Todo ALB é um ELB.
  - Mas nem todo ELB é um ALB (ele pode ser NLB ou GLB também).
  - Exemplo simples. Pensa em transportes:
    - “Transporte público” = ELB (conceito geral).
    - Dentro dele, você pode escolher: ônibus (ALB), metrô (NLB) ou trem de carga (GLB).
    - Cada um tem sua função, mas todos fazem parte do mesmo sistema de transporte.

## Exemplo simples sobre ALB

* Imagine que você tem um shopping center com várias lojas:
  - O Application Load Balancer é o porteiro do shopping.
  - Quando uma pessoa chega e diz: “Quero ir à praça de alimentação” → ele manda para o corredor das lanchonetes.
  - “Quero comprar roupas” → ele manda para as lojas de moda.
  - “Preciso ir ao cinema” → ele direciona para a entrada das salas de cinema.
* Ou seja, o ALB entende o pedido do cliente e o manda para o grupo de destino certo (EC2s responsáveis por cada parte da aplicação).

## Ligação com o esse lab

* No exercício, você tá usando um Application Load Balancer (LabELB) para:
  - Receber todas as requisições HTTP dos usuários (porta 80).
  - Consultar o grupo de destino (LabGroup).
  - Distribuir o tráfego de forma inteligente, podendo no futuro:
    - Mandar /api/* para servidores de API.
    - Mandar /app/* para servidores da aplicação web.
    - Mandar /img/* para servidores otimizados para imagens.
O Application Load Balancer é um balanceador inteligente da AWS, que entende o tráfego HTTP/HTTPS e pode rotear com base em regras, não apenas dividir aleatoriamente. Isso o torna ideal para aplicações modernas, com microsserviços e múltiplos endpoints.
