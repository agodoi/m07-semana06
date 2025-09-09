## O que é esse trem Grupo de Destino?

Imagine que você tem um restaurante delivery com vários cozinheiros:

* O telefone do delivery é o Load Balancer: ele recebe todos os pedidos dos clientes.
* O grupo de destino é a lista dos cozinheiros disponíveis naquele momento.
  - Se um cozinheiro estiver doente (instância com problema), ele sai da lista e não recebe pedidos.
  - Se tiver muita demanda, entram mais cozinheiros (Auto Scaling adiciona novas instâncias ao grupo).
* O Load Balancer consulta essa lista (grupo de destino) e distribui os pedidos apenas para os cozinheiros ativos.
* Assim, ninguém fica sobrecarregado e os pedidos são entregues no tempo certo.

## Conexão com esse Lab:

1) Você vai criar instâncias EC2 que rodam um servidor Apache.
2) Vai configurar um Application Load Balancer para receber as requisições.
3) Vai ciar um grupo de destino (LabGroup) que lista quais instâncias estão aptas a receber tráfego.
4) E então, o ELB distribuirá as requisições entre essas instâncias de forma equilibrada, garantindo escalabilidade e alta disponibilidade. Beleza?
