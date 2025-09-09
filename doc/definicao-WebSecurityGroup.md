## O que é um Web Security Group?

* É uma **parede de proteção (firewall virtual)** que controla **quem pode entrar e sair** de uma instância (EC2, Load Balancer, RDS, etc.).
* O **Web Security Group** é apenas um **Security Group configurado especialmente para aplicações web**, geralmente liberando portas como:
  - **80 (HTTP)** → tráfego web comum
  - **443 (HTTPS)** → tráfego web seguro (com SSL/TLS)

## Exemplo simples

Pensa em um **prédio com portaria**:

* O **prédio** é sua instância EC2.
* A **portaria** é o **Security Group**.
* Você pode dizer para o porteiro:
  - “Só entra quem está com convite para o **apartamento 80**” (porta 80 → HTTP).
  - “Só entra quem tem crachá para o **apartamento 443**” (porta 443 → HTTPS).
* Se alguém tenta entrar por uma porta que não foi liberada (ex: 22/SSH ou 3306/MySQL), o porteiro simplesmente **bloqueia**.

Ou seja, o Security Group funciona como um **porteiro que filtra os acessos** de acordo com as regras que você definiu.

## Relação com esse lab

Na sua prática, você:

1. Criou ou está criando o **Application Load Balancer (LabELB)**.
2. Precisou escolher um **Security Group** para ele.
3. Usou o **Web Security Group**, que já estava configurado para permitir apenas o tráfego web (HTTP/HTTPS).
4. Isso garantiu que só conexões **legítimas da web** chegassem ao seu balanceador de carga.
Quer que eu faça também um **quadro rápido com exemplos de regras de entrada e saída** típicas de um Web Security Group, para usar direto em slide?

