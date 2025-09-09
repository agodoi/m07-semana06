## O que é Mapeamento de Rede?

É a etapa em que você diz ao Load Balancer em quais redes ele deve existir. Na prática, você informa:
* Em qual VPC o Load Balancer será criado.
* Quais sub-redes ele deve usar (públicas ou privadas).
* Em quais Zonas de Disponibilidade (AZs) ele precisa estar presente.
* Esse mapeamento garante que o Load Balancer seja acessível de forma redundante, espalhando-se por várias AZs para dar alta disponibilidade.

## Exemplo simples

Pensa em um restaurante com várias filiais em bairros diferentes:

* O nome do restaurante é o Load Balancer.
* O mapa da cidade com bairros é a VPC.
* Cada filial em um bairro diferente é uma sub-rede dentro de uma Zona de Disponibilidade.
* O mapeamento de rede é quando você escolhe em quais bairros (sub-redes) o restaurante vai funcionar.
* Assim, se um bairro ficar sem energia (uma AZ falhar), o restaurante ainda funciona nos outros bairros (as outras AZs).

## Relação com o esse lab

Ao criar o Application Load Balancer (LabELB), você:

* Escolheu a Lab VPC (ou a VPC da arquitetura corporativa).
* Selecionou duas sub-redes públicas em Zonas de Disponibilidade diferentes.

Isso permitiu que o Load Balancer ficasse acessível pela Internet e garantisse alta disponibilidade (se uma AZ cair, a outra continua atendendo).
